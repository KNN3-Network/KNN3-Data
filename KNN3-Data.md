# KNN3-Data
## Contents
  - [1.Asset Holding](#1-asset-holding) (Only Available through API/SDK)
    - [1.1 polygon_nft_hold](#11-polygon_nft_hold)
    - [1.2 polygon_token_hold](#12-polygon_token_hold)
    - [1.3 eth_nft_hold](#13-eth_nft_hold)
    - [1.4 eth_token_hold](#14-eth_token_hold)
  - [2.DID](#2-did) (Only Available through API/SDK)
    - [2.1 addr_bit](#21-addr_bit)
    - [2.2 avatar](#22-avatar)
    - [2.3 eth_ens_realtime](#23-eth_ens_realtime)
    - [2.4 bsc_spaceid](#24-bsc_spaceid)
    - [2.5 bsc_bab](#25-bsc_bab)
  - [3.Event](#3-event)
    - [3.1 poap](#31-poap) (Only Available through API/SDK)
    - [3.2 snapshot vote](#32-snapshot-vote)
  - [4.Lens](#)
    - [4.1 lens_profile_view](#41-lens_profile_view)
    - [4.2 lens_follow_view](#42-lens_follow_view)
    - [4.3 lens_publication_view](#43-lens_publication_view)
    - [4.4 lens_publication_summary_view](#44-lens_publication_summary_view)
    - [4.5 lens_publication_comment_view](#45-lens_publication_comment_view)
    - [4.6 lens_publication_mirror_view](#46-lens_publication_mirror_view)
    - [4.7 lens_publication_post_view](#47-lens_publication_post_view)
    - [4.8 lens_overall_score_view](#48-lens_overall_score_view)
    - [4.9 lens_overall_level_view](#49-lens_overall_level_view)

## 1. Asset Holding
### 1.1 polygon_nft_hold
|    | table_name       | column_name   | data_type         | Desc   |
|---:|:-----------------|:--------------|:------------------|:-------|
|  0 | polygon_nft_hold | address       | character varying |        |
|  1 | polygon_nft_hold | contract      | character varying |        |
|  2 | polygon_nft_hold | count         | numeric           |        |
### 1.2 polygon_token_hold
|    | table_name         | column_name   | data_type         | Desc   |
|---:|:-------------------|:--------------|:------------------|:-------|
|  0 | polygon_token_hold | contract      | character varying |        |
|  1 | polygon_token_hold | address       | character varying |        |
|  2 | polygon_token_hold | count         | numeric           |        |
### 1.3 eth_nft_hold
|    | table_name   | column_name   | data_type         | Desc   |
|---:|:-------------|:--------------|:------------------|:-------|
|  0 | nft_hold     | address       | character varying |        |
|  1 | nft_hold     | contract      | character varying |        |
|  2 | nft_hold     | count         | numeric           |        |
### 1.4 eth_token_hold
|    | table_name   | column_name   | data_type         | Desc   |
|---:|:-------------|:--------------|:------------------|:-------|
|  0 | token_hold   | contract      | character varying |        |
|  1 | token_hold   | address       | character varying |        |
|  2 | token_hold   | count         | numeric           |        |
## 2. DID
### 2.1 addr_bit
|    | table_name   | column_name   | data_type         | Desc   |
|---:|:-------------|:--------------|:------------------|:-------|
|  0 | addr_bit     | addr          | character varying |        |
|  1 | addr_bit     | account       | character varying |        |
|  2 | addr_bit     | algorithmId   | integer           |        |
|  3 | addr_bit     | chain         | character varying |        |
|  4 | addr_bit     | outpoint      | character varying |        |
### 2.2 avatar
|    | table_name   | column_name   | data_type                   | Desc   |
|---:|:-------------|:--------------|:----------------------------|:-------|
|  0 | avatar       | id            | integer                     |        |
|  1 | avatar       | avatar        | character varying           |        |
|  2 | avatar       | platform      | character varying           |        |
|  3 | avatar       | identity      | character varying           |        |
|  4 | avatar       | created_at    | timestamp without time zone |        |
|  5 | avatar       | updated_at    | timestamp without time zone |        |
### 2.3 eth_ens_realtime
|    | table_name       | column_name      | data_type                   | Desc   |
|---:|:-----------------|:-----------------|:----------------------------|:-------|
|  0 | eth_ens_realtime | id               | integer                     |        |
|  1 | eth_ens_realtime | owner            | character varying           |        |
|  2 | eth_ens_realtime | resolved_address | character varying           |        |
|  3 | eth_ens_realtime | name             | character varying           |        |
|  4 | eth_ens_realtime | node             | character varying           |        |
|  5 | eth_ens_realtime | namehash         | character varying           |        |
|  6 | eth_ens_realtime | label            | character varying           |        |
|  7 | eth_ens_realtime | labelhash        | character varying           |        |
|  8 | eth_ens_realtime | transaction_hash | character varying           |        |
|  9 | eth_ens_realtime | block_number     | integer                     |        |
| 10 | eth_ens_realtime | is_migrated      | boolean                     |        |
| 11 | eth_ens_realtime | expiry_date      | bigint                      |        |
| 12 | eth_ens_realtime | updated_at       | timestamp without time zone |        |
| 13 | eth_ens_realtime | created_at       | timestamp without time zone |        |
### 2.4 bsc_spaceid
|    | table_name   | column_name      | data_type                   | Desc   |
|---:|:-------------|:-----------------|:----------------------------|:-------|
|  0 | bsc_spaceid  | id               | integer                     |        |
|  1 | bsc_spaceid  | registrant       | character varying           |        |
|  2 | bsc_spaceid  | owner            | character varying           |        |
|  3 | bsc_spaceid  | resolver         | character varying           |        |
|  4 | bsc_spaceid  | resolved_address | character varying           |        |
|  5 | bsc_spaceid  | name             | character varying           |        |
|  6 | bsc_spaceid  | node             | character varying           |        |
|  7 | bsc_spaceid  | namehash         | character varying           |        |
|  8 | bsc_spaceid  | label            | character varying           |        |
|  9 | bsc_spaceid  | labelhash        | character varying           |        |
| 10 | bsc_spaceid  | expiry_date      | bigint                      |        |
| 11 | bsc_spaceid  | transaction_hash | character varying           |        |
| 12 | bsc_spaceid  | block_number     | integer                     |        |
| 13 | bsc_spaceid  | created_at       | timestamp without time zone |        |
| 14 | bsc_spaceid  | updated_at       | timestamp without time zone |        |
### 2.5 bsc_bab
|    | table_name   | column_name       | data_type         | Desc   |
|---:|:-------------|:------------------|:------------------|:-------|
|  0 | bsc_bab      | id                | integer           |        |
|  1 | bsc_bab      | address           | character varying |        |
|  2 | bsc_bab      | token_id          | character varying |        |
|  3 | bsc_bab      | block_number      | integer           |        |
|  4 | bsc_bab      | transaction_hash  | character varying |        |
|  5 | bsc_bab      | transaction_index | character varying |        |
|  6 | bsc_bab      | log_index         | character varying |        |
## 3. Event
### 3.1 poap
|    | table_name   | column_name   | data_type         | Desc   |
|---:|:-------------|:--------------|:------------------|:-------|
|  0 | poap         | id            | bigint            |        |
|  1 | poap         | addr          | character varying |        |
|  2 | poap         | eventId       | character varying |        |
### 3.2 Snapshot vote
|    | Field           | Type         | Null   | Key   | Default   | Extra   | Desc   |
|---:|:----------------|:-------------|:-------|:------|:----------|:--------|:-------|
|  0 | id              | varchar(255) | NO     |       |           |         |        |
|  1 | voter           | varchar(255) | YES    | MUL   |           |         |        |
|  2 | choice          | int(11)      | YES    |       |           |         |        |
|  3 | spaceId         | varchar(255) | YES    | MUL   |           |         |        |
|  4 | spaceName       | varchar(255) | YES    | MUL   |           |         |        |
|  5 | spaceAvatar     | varchar(255) | YES    |       |           |         |        |
|  6 | spaceAdmins     | json         | YES    |       |           |         |        |
|  7 | spaceModerators | json         | YES    |       |           |         |        |
|  8 | spaceMembers    | json         | YES    |       |           |         |        |
|  9 | proposalId      | varchar(255) | YES    | MUL   |           |         |        |
| 10 | proposalAuthor  | varchar(255) | YES    |       |           |         |        |
| 11 | proposalTitle   | varchar(255) | YES    |       |           |         |        |
| 12 | created         | timestamp    | YES    | MUL   |           |         |        |
## 4. Lens
### 4.1 lens_profile_view
|    | Field       | Type         | Null   | Key   | Default   | Extra   | Desc   |
|---:|:------------|:-------------|:-------|:------|:----------|:--------|:-------|
|  0 | profileId   | bigint(20)   | NO     | PRI   |           |         |        |
|  1 | metadata    | text         | YES    |       |           |         |        |
|  2 | handle      | varchar(255) | YES    | MUL   |           |         |        |
|  3 | address     | varchar(255) | YES    | MUL   |           |         |        |
|  4 | imageURI    | text         | YES    |       |           |         |        |
|  5 | create_date | date         | YES    |       |           |         |        |
### 4.2 lens_follow_view
|    | Field            | Type         | Null   | Key   | Default   | Extra   | Desc   |
|---:|:-----------------|:-------------|:-------|:------|:----------|:--------|:-------|
|  0 | follower_id      | bigint(20)   | YES    | PRI   |           |         |        |
|  1 | follower_address | varchar(255) | NO     | PRI   |           |         |        |
|  2 | follower         | varchar(255) | YES    | MUL   |           |         |        |
|  3 | followee_id      | bigint(20)   | YES    | PRI   |           |         |        |
|  4 | followee_address | varchar(255) | YES    | MUL   |           |         |        |
|  5 | followee         | varchar(255) | YES    | MUL   |           |         |        |
|  6 | create_date      | date         | YES    |       |           |         |        |
### 4.3 lens_publication_view
|    | Field         | Type         | Null   | Key   | Default   | Extra   | Desc   |
|---:|:--------------|:-------------|:-------|:------|:----------|:--------|:-------|
|  0 | profileId     | bigint(20)   | NO     | PRI   |           |         |        |
|  1 | address       | varchar(255) | YES    | MUL   |           |         |        |
|  2 | handle        | varchar(255) | YES    | MUL   |           |         |        |
|  3 | rootProfileId | bigint(20)   | YES    | MUL   |           |         |        |
|  4 | rootPubId     | int(11)      | YES    | MUL   |           |         |        |
|  5 | pubId         | int(11)      | NO     | PRI   |           |         |        |
|  6 | contentURI    | text         | YES    |       |           |         |        |
|  7 | rootAddress   | varchar(255) | YES    | MUL   |           |         |        |
|  8 | rootHandle    | varchar(255) | YES    | MUL   |           |         |        |
|  9 | type          | varchar(255) | YES    |       |           |         |        |
| 10 | create_date   | date         | YES    |       |           |         |        |
### 4.4 lens_publication_summary_view
|    | Field                  | Type         | Null   | Key   | Default   | Extra   | Desc   |
|---:|:-----------------------|:-------------|:-------|:------|:----------|:--------|:-------|
|  0 | profile_id             | bigint(20)   | NO     | PRI   |           |         |        |
|  1 | address                | varchar(255) | YES    | MUL   |           |         |        |
|  2 | handle                 | varchar(255) | YES    | MUL   |           |         |        |
|  3 | in_reply_to_profile_id | bigint(20)   | YES    | MUL   |           |         |        |
|  4 | in_reply_to_pub_id     | int(11)      | YES    | MUL   |           |         |        |
|  5 | pub_id                 | int(11)      | NO     | PRI   |           |         |        |
|  6 | content_URI            | text         | YES    |       |           |         |        |
|  7 | in_reply_to_address    | varchar(255) | YES    | MUL   |           |         |        |
|  8 | in_reply_to_handle     | varchar(255) | YES    | MUL   |           |         |        |
|  9 | create_date            | date         | YES    |       |           |         |        |
| 10 | type                   | varchar(255) | YES    |       |           |         |        |
| 11 | comment_count          | bigint(21)   | YES    |       |           |         |        |
| 12 | mirror_count           | bigint(21)   | YES    |       |           |         |        |
| 13 | image                  | varchar(255) | YES    |       |           |         |        |
| 14 | imageMimeType          | varchar(255) | YES    |       |           |         |        |
### 4.5 lens_publication_comment_view
|    | Field         | Type         | Null   | Key   | Default   | Extra   | Desc   |
|---:|:--------------|:-------------|:-------|:------|:----------|:--------|:-------|
|  0 | profileId     | bigint(20)   | NO     | PRI   |           |         |        |
|  1 | address       | varchar(255) | YES    | MUL   |           |         |        |
|  2 | handle        | varchar(255) | YES    | MUL   |           |         |        |
|  3 | pubId         | int(11)      | NO     | PRI   |           |         |        |
|  4 | rootProfileId | bigint(20)   | YES    | MUL   |           |         |        |
|  5 | rootPubId     | int(11)      | YES    | MUL   |           |         |        |
|  6 | contentURI    | text         | YES    |       |           |         |        |
|  7 | rootAddress   | varchar(255) | YES    | MUL   |           |         |        |
|  8 | rootHandle    | varchar(255) | YES    | MUL   |           |         |        |
|  9 | type          | varchar(255) | YES    |       |           |         |        |
| 10 | create_date   | date         | YES    |       |           |         |        |
### 4.6 lens_publication_mirror_view
|    | Field         | Type         | Null   | Key   | Default   | Extra   | Desc   |
|---:|:--------------|:-------------|:-------|:------|:----------|:--------|:-------|
|  0 | profileId     | bigint(20)   | NO     | PRI   |           |         |        |
|  1 | address       | varchar(255) | YES    | MUL   |           |         |        |
|  2 | handle        | varchar(255) | YES    | MUL   |           |         |        |
|  3 | pubId         | int(11)      | NO     | PRI   |           |         |        |
|  4 | rootProfileId | bigint(20)   | YES    | MUL   |           |         |        |
|  5 | rootPubId     | int(11)      | YES    | MUL   |           |         |        |
|  6 | contentURI    | text         | YES    |       |           |         |        |
|  7 | rootAddress   | varchar(255) | YES    | MUL   |           |         |        |
|  8 | rootHandle    | varchar(255) | YES    | MUL   |           |         |        |
|  9 | type          | varchar(255) | YES    |       |           |         |        |
| 10 | create_date   | date         | YES    |       |           |         |        |
### 4.7 lens_publication_post_view
|    | Field         | Type         | Null   | Key   | Default   | Extra   | Desc   |
|---:|:--------------|:-------------|:-------|:------|:----------|:--------|:-------|
|  0 | profileId     | bigint(20)   | NO     | PRI   |           |         |        |
|  1 | address       | varchar(255) | YES    | MUL   |           |         |        |
|  2 | handle        | varchar(255) | YES    | MUL   |           |         |        |
|  3 | pubId         | int(11)      | NO     | PRI   |           |         |        |
|  4 | rootProfileId | bigint(20)   | YES    | MUL   |           |         |        |
|  5 | rootPubId     | int(11)      | YES    | MUL   |           |         |        |
|  6 | contentURI    | text         | YES    |       |           |         |        |
|  7 | rootAddress   | varchar(255) | YES    | MUL   |           |         |        |
|  8 | rootHandle    | varchar(255) | YES    | MUL   |           |         |        |
|  9 | type          | varchar(255) | YES    |       |           |         |        |
| 10 | create_date   | date         | YES    |       |           |         |        |
### 4.8 lens_overall_score_view
|    | Field                     | Type         | Null   | Key   | Default   | Extra   | Desc   |
|---:|:--------------------------|:-------------|:-------|:------|:----------|:--------|:-------|
|  0 | profileId                 | varchar(200) | NO     | PRI   |           |         |        |
|  1 | handle                    | varchar(255) | YES    | MUL   |           |         |        |
|  2 | address                   | varchar(200) | YES    | MUL   |           |         |        |
|  3 | pr_value_influ            | double       | YES    |       |           |         |        |
|  4 | pr_score_influ            | double       | YES    |       |           |         |        |
|  5 | pr_rank_influ             | bigint(20)   | YES    | MUL   |           |         |        |
|  6 | pr_value_comment_compaign | double       | YES    |       |           |         |        |
|  7 | pr_score_comment_compaign | double       | YES    |       |           |         |        |
|  8 | pr_rank_comment_compaign  | bigint(20)   | YES    |       |           |         |        |
|  9 | pr_value_mirror_compaign  | double       | YES    |       |           |         |        |
| 10 | pr_score_mirror_compaign  | double       | YES    |       |           |         |        |
| 11 | pr_rank_mirror_compaign   | bigint(20)   | YES    |       |           |         |        |
| 12 | pr_score_compaign         | double       | YES    |       |           |         |        |
| 13 | pr_rank_compaign          | bigint(20)   | YES    | MUL   |           |         |        |
| 14 | pr_value_comment_engager  | double       | YES    |       |           |         |        |
| 15 | pr_score_comment_engager  | double       | YES    |       |           |         |        |
| 16 | pr_rank_comment_engager   | bigint(20)   | YES    |       |           |         |        |
| 17 | pr_value_mirror_engager   | double       | YES    |       |           |         |        |
| 18 | pr_score_mirror_engager   | double       | YES    |       |           |         |        |
| 19 | pr_rank_mirror_engager    | bigint(20)   | YES    |       |           |         |        |
| 20 | pr_score_engager          | double       | YES    |       |           |         |        |
| 21 | pr_rank_engager           | bigint(20)   | YES    | MUL   |           |         |        |
| 22 | pr_value_creator          | double       | YES    |       |           |         |        |
| 23 | pr_score_creator          | double       | YES    |       |           |         |        |
| 24 | pr_rank_creator           | bigint(20)   | YES    | MUL   |           |         |        |
| 25 | pr_value_collector        | double       | YES    |       |           |         |        |
| 26 | pr_score_collector        | double       | YES    |       |           |         |        |
| 27 | pr_rank_collector         | bigint(20)   | YES    | MUL   |           |         |        |
| 28 | curator_score             | bigint(20)   | YES    |       |           |         |        |
| 29 | curator_rank              | bigint(20)   | YES    | MUL   |           |         |        |
| 30 | overall_score             | double       | YES    |       |           |         |        |
| 31 | overall_rank              | bigint(20)   | YES    | MUL   |           |         |        |
| 32 | create_date               | varchar(10)  | NO     | PRI   |           |         |        |
### 4.9 lens_overall_level_view
|    | Field               | Type         | Null   | Key   | Default   | Extra   | Desc   |
|---:|:--------------------|:-------------|:-------|:------|:----------|:--------|:-------|
|  0 | profileId           | varchar(200) | NO     | PRI   |           |         |        |
|  1 | handle              | varchar(255) | YES    | MUL   |           |         |        |
|  2 | create_date         | varchar(10)  | NO     | PRI   |           |         |        |
|  3 | overall_level_str   | varchar(10)  | YES    |       |           |         |        |
|  4 | overall_level       | bigint(20)   | YES    |       |           |         |        |
|  5 | overall_level_rank  | bigint(20)   | YES    |       |           |         |        |
|  6 | overall_level_score | double       | YES    |       |           |         |        |
|  7 | address             | varchar(200) | YES    |       |           |         |        |
|  8 | influ_level         | bigint(20)   | YES    |       |           |         |        |
|  9 | influ_level_str     | varchar(10)  | YES    |       |           |         |        |
| 10 | compaign_level      | bigint(20)   | YES    |       |           |         |        |
| 11 | engager_level       | bigint(20)   | YES    |       |           |         |        |
| 12 | compaign_level_str  | varchar(10)  | YES    |       |           |         |        |
| 13 | engager_level_str   | varchar(10)  | YES    |       |           |         |        |
| 14 | creator_level       | bigint(20)   | YES    |       |           |         |        |
| 15 | creator_level_str   | varchar(10)  | YES    |       |           |         |        |
| 16 | collector_level     | bigint(20)   | YES    |       |           |         |        |
| 17 | collector_level_str | varchar(10)  | YES    |       |           |         |        |
| 18 | curator_level       | bigint(20)   | YES    |       |           |         |        |
| 19 | curator_level_str   | varchar(10)  | YES    |       |           |         |        |
