# KNN3 SQL Templates
SQL templates provided by K.Transformer are pre-built examples that can be used directly or modified to fit your specific query needs. They serve as a starting point for creating SQL queries using the K.Transformer SQL editor. By using pre-existing templates, you can save time and reduce errors when constructing complex SQL queries. Additionally, our AI-assisted SQL construction feature can help users generate SQL queries more efficiently.
## Contents
  - [1.Snapshot](#1-snapshot)
    - [1.1 Number of spaces address proposed in](#11-number-of-spaces-address-proposed-in)
    - [1.2 Number of spaces address voted in](#12-number-of-spaces-address-voted-in)
    - [1.3 Number of proposals of an address in space](#13-number-of-proposals-of-an-address-in-space)
    - [1.4 Get spaces where an address is admin](#14-get-spaces-where-an-address-is-admin)
    - [1.5 Get space stats over time](#15-get-space-stats-over-time)
  - [2.Lens Protocol](#2-lens-protocol)
    - [2.1 Top 10 commented publications on Lens](#21-top-10-commented-publications-on-lens)
    - [2.2 Top 10 mirrored publications on Lens](#22-top-10-mirrored-publications-on-lens)
    - [2.3 Number of publications over time](#23-number-of-publications-over-time)
    - [2.4 Lens handle ranks over time](#24-lens-handle-ranks-over-time)
    - [2.5 Follower quality on Lens](#25-follower-quality-on-lens)

## 1. Snapshot
### 1.1 Number of spaces address proposed in
``` sql
select
  proposalAuthor,
  count(distinct spaceId) as space_count
from
  vote
where
  proposalAuthor = '0xb01474b50382fae1a847e3a916ecdf07ba57bcc7'
group by
  proposalAuthor 
```
### 1.2 Number of spaces address voted in
``` sql
select
  voter,
  count(distinct spaceId) as space_count
from
  vote
where
  voter = '0xb01474b50382fae1a847e3a916ecdf07ba57bcc7'
group by
  voter
```
### 1.3 Number of proposals of an address in space
``` sql
select
  proposalAuthor,
  count(distinct proposalId) as proposal_cnt
from
  vote
where
  spaceId = 'aave.eth'
group by
  proposalAuthor
having
  count(distinct proposalId) > 1
```
### 1.4 Get spaces where an address is admin
``` sql
select
  spaceId
from
  vote
where
  spaceAdmins like '%0x6cd19880a74fd7b23084221ad8eeb8f24e476ca2%'
group by
  spaceId
``` 
### 1.5 Get space stats over time
``` sql
select
  spaceId,
  date(created) as stats_date,
  count(distinct proposalId) as proposal_count,
  count(distinct voter) as voter_count
from
  vote
where
  spaceId = 'aave.eth'
  and date(created) >= current_date() - INTERVAL 30 DAY
group by
  spaceId,
  date(created)
```

## 2. Lens Protocol
### 2.1 Top 10 commented publications on Lens
``` sql
select
  pub_id,
  COALESCE(comment_count, 0) AS comment_count,
  type
from
  lens_publication_summary_view
where
  handle = 'knn3_network.lens'
order by
  comment_count desc
limit
  10
```

### 2.2 Top 10 mirrored publications on Lens
``` sql
select
  pub_id,
  COALESCE(mirror_count, 0) AS mirror_count,
  type
from
  lens_publication_summary_view
where
  handle = 'knn3_network.lens'
order by
  mirror_count desc
limit
  10
```

### 2.3 Number of publications over time
``` sql
SELECT
  create_date,
  SUM(
    CASE
      WHEN type = 'Post' THEN 1
      ELSE 0
    END
  ) as posts,
  SUM(
    CASE
      WHEN type = 'Mirror' THEN 1
      ELSE 0
    END
  ) as mirrors,
  SUM(
    CASE
      WHEN type = 'Comment' THEN 1
      ELSE 0
    END
  ) as comments
FROM
  lens_publication_summary_view
WHERE
  handle = 'stani.lens'
  AND create_date > NOW() - INTERVAL '1' MONTH
GROUP BY
  create_date
ORDER BY
  create_date
```
### 2.4 Lens handle ranks over time
``` sql
select
  handle,
  overall_rank,
  pr_rank_influ as influence_rank,
  pr_rank_collector as collector_rank,
  pr_rank_compaign as campaign_rank,
  pr_rank_creator as creator_rank,
  pr_rank_engager as engager_rank,
  curator_rank,
  create_date
from
  lens_overall_score_view
where
  create_date >= current_date() - INTERVAL 7 DAY
  and handle = 'knn3_network.lens'
```

### 2.5 Follower quality on Lens
``` sql
select
  t1.*,
  t2.influence_level,
  collector_level,
  engager_level,
  campaign_level,
  creator_level,
  curator_level,
  overall_level
from
  (
    select
      followee,
      follower,
      follower_id,
      follower_address
    from
      lens_follow_view
    where
      followee = 'knn3_network.lens'
  ) t1
  left join (
    select
      handle,
      influ_level_str as influence_level,
      collector_level_str as collector_level,
      engager_level_str as engager_level,
      compaign_level_str as campaign_level,
      creator_level_str as creator_level,
      curator_level_str as curator_level,
      overall_level_str as overall_level
    from
      lens_overall_level_view
    where
      create_date = current_date()
  ) t2 on t1.follower = t2.handle
```
