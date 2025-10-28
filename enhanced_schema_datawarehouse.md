# Enhanced Database Schema: datawarehouse

*Generated on: 2025-10-28 12:40:22*
*Original Schema Date: 2025-10-24 15:54:28*
*Database Engine: ClickHouse*

**Total Tables:** 190

---

## About This Schema

This enhanced schema documentation includes:
- ✅ Table descriptions and business context
- ✅ Primary keys, foreign keys, and unique constraints
- ✅ Column-level descriptions and validation rules
- ✅ Owner/maintainer information
- ✅ Categorization tags
- ✅ All original metadata (types, ranges, statistics)

**Note:** Foreign key relationships, validation rules, and constraints are inferred based on naming patterns and data characteristics. Please review and validate with your database team.

---

<details>
<summary><h2>1. api_users</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** API authentication and access token management.

**Owner/Maintainer:** Platform/API Team

**Tags:** `api`, `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred based on naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `api_users`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | Category | 24.0 chars | - | 14 | Unique identifier for api_users record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **email** | Text | No | Email | 23.285714285714285 chars | - | 14 | Email address | Valid email format; Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 14 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hdaccountid** | Float | No | - | 189.0 to 28,052.0 | 20,419.428571428572 | 12 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **scopes** | Text | No | SerializedJSON | 17.928571428571427 chars | - | 2 | Scopes | Required | Not Null | Categorical (2 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **token** | Text | No | Category | 28.5 chars | - | 8 | Authentication or access token | Required | Not Null, Unique (likely) | Variable |

</details>

---

<details>
<summary><h2>2. api_users_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for api_users. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform/API Team

**Tags:** `staging`, `raw-data`, `api`, `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred based on naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `api_users_raw`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | Category | 24.0 chars | - | 14 | Unique identifier for api_users_raw record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **email** | Text | No | Email | 23.285714285714285 chars | - | 14 | Email address | Valid email format; Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 14 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hdaccountid** | Float | No | - | 189.0 to 28,052.0 | 20,419.428571428572 | 12 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **scopes** | Text | No | SerializedJSON | 17.928571428571427 chars | - | 2 | Scopes | Required | Not Null | Categorical (2 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **token** | Text | No | Category | 28.5 chars | - | 8 | Authentication or access token | Required | Not Null, Unique (likely) | Variable |

</details>

---

<details>
<summary><h2>3. broadcast_activity_aggregations</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages broadcast messaging campaigns and delivery tracking.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `marketing`, `campaigns`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred based on naming)
- `eventn_ctx_event_id` → Related table (inferred based on naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcast_activity_aggregations`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 9,999 | Unique identifier for broadcast_activity_aggregations record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **broadcast** | Text | No | - | 24.0 chars | - | 10,001 | Broadcast | Required | Not Null | Variable |
| **deliveredcount** | Float | No | - | 0.0 to 157,952.0 | 3,681.858 | 4,573 | Count of delivered | Numeric; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,998 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **failedbybspcount** | Float | No | - | 0.0 to 71,827.0 | 1,927.6225 | 3,482 | Count of failedbybsp | Numeric; Required | Not Null | Variable |
| **failedbyumscount** | Float | No | - | 0.0 to 96,703.0 | 294.3715 | 728 | Count of failedbyums | Numeric; Required | Not Null | Variable |
| **filteredoutbyums** | Float | Yes | - | 0.0 to 3,278.0 (Null: 82.9%) | 46.117852975495914 | 226 | Filteredoutbyums | Numeric | None | Variable |
| **optedoutbyums** | Float | Yes | - | 0.0 to 2,785.0 (Null: 22.7%) | 44.8115623383342 | 490 | Optedoutbyums | Numeric | None | Variable |
| **overallprogress** | Float | No | - | 0.0 to 207,752.0 | 6,469.946 | 4,315 | Overallprogress | Numeric; Required | Not Null | Variable |
| **readcount** | Float | No | - | 0.0 to 70,090.0 | 1,685.8446 | 3,510 | Count of read | Numeric; Required | Not Null | Variable |
| **sentbyumscount** | Float | No | - | 0.0 to 194,175.0 | 4,205.7452 | 4,767 | Count of sentbyums | Numeric; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>4. broadcast_activity_aggregations_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for broadcast_activity_aggregations. Contains unprocessed data before transformation.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `marketing`, `staging`, `raw-data`, `campaigns`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred based on naming)
- `eventn_ctx_event_id` → Related table (inferred based on naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcast_activity_aggregations_raw`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 10,000 | Unique identifier for broadcast_activity_aggregations_raw record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **broadcast** | Text | No | - | 24.0 chars | - | 10,000 | Broadcast | Required | Not Null | Variable |
| **deliveredcount** | Float | No | - | 0.0 to 157,952.0 | 3,743.1335 | 4,587 | Count of delivered | Numeric; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,998 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **failedbybspcount** | Float | No | - | 0.0 to 71,827.0 | 1,761.9301 | 3,352 | Count of failedbybsp | Numeric; Required | Not Null | Variable |
| **failedbyumscount** | Float | No | - | 0.0 to 96,703.0 | 264.8207 | 725 | Count of failedbyums | Numeric; Required | Not Null | Variable |
| **filteredoutbyums** | Float | Yes | - | 0.0 to 3,278.0 (Null: 77.5%) | 48.54331408262994 | 265 | Filteredoutbyums | Numeric | None | Variable |
| **optedoutbyums** | Float | Yes | - | 0.0 to 2,785.0 (Null: 29.9%) | 47.12255671279783 | 464 | Optedoutbyums | Numeric | None | Variable |
| **overallprogress** | Float | No | - | 0.0 to 207,752.0 | 6,386.1942 | 4,302 | Overallprogress | Numeric; Required | Not Null | Variable |
| **readcount** | Float | No | - | 0.0 to 102,969.0 | 1,697.952 | 3,546 | Count of read | Numeric; Required | Not Null | Variable |
| **sentbyumscount** | Float | No | - | 0.0 to 194,175.0 | 4,315.883099999999 | 4,796 | Count of sentbyums | Numeric; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>5. broadcast_reports</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Analytics and metrics table for reporting purposes.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `reporting`, `campaigns`, `marketing`, `analytics`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- None identified (or table uses non-standard FK naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcast_reports`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 10,000 | Unique identifier for broadcast_reports record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 2 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **broadcast** | Text | No | - | 24.0 chars | - | 9,999 | Broadcast | Required | Not Null | Variable |
| **createdat** | Text | No | - | 31.3656 chars | - | 9,539 | Timestamp when record was created | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **reportkey** | Text | No | - | 50.0 chars | - | 9,999 | Reportkey | Required | Not Null | Variable |
| **retryreportkeys** | Text | No | - | 7.0281 chars | - | 460 | Retryreportkeys | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updatedat** | Text | No | - | 31.4576 chars | - | 9,564 | Timestamp when record was last updated | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>6. broadcast_reports_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for broadcast_reports. Contains unprocessed data before transformation.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `raw-data`, `marketing`, `campaigns`, `reporting`, `staging`, `analytics`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- None identified (or table uses non-standard FK naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcast_reports_raw`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 9,998 | Unique identifier for broadcast_reports_raw record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 2 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **broadcast** | Text | No | - | 24.0 chars | - | 9,999 | Broadcast | Required | Not Null | Variable |
| **createdat** | Text | No | - | 30.9158 chars | - | 9,399 | Timestamp when record was created | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **reportkey** | Text | No | - | 50.0 chars | - | 9,998 | Reportkey | Required | Not Null | Variable |
| **retryreportkeys** | Text | No | - | 4.6386 chars | - | 304 | Retryreportkeys | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updatedat** | Text | No | - | 31.031 chars | - | 9,435 | Timestamp when record was last updated | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>7. broadcasts</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages broadcast messaging campaigns and delivery tracking.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `marketing`, `campaigns`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred based on naming)
- `hdaccountid` → `postgres_accounts.id` (inferred)
- `inboxid` → `postgres_inboxes.id` (inferred)
- `name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 20.11 chars
- **Distinct Values:** 8,168

### optedmessagecount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 169,215.0
- **Average:** 6,676.5685631386405
- **Distinct Values:** 3,879
- **Null %:** 20.7%

### requestbody_accountname

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.2879 chars
- **Distinct Values:** 180

### requestbody_automatedretrysettings_all_retries

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0316 chars
- **Distinct Values:** 7

### requestbody_automatedretrysettings_paused

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0006
- **Distinct Values:** 2

### requestbody_automatedretrysettings_retry_till

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 492
- **Null %:** 95.1%

### requestbody_cohortid` → `postgres_accounts.id` (inferred)
- `requestbody_metadata_buttonpayloads

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 76.4068 chars
- **Distinct Values:** 2,770

### requestbody_metadata_complextemplatepayload_cards

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.6039 chars
- **Distinct Values:** 106

### requestbody_metadata_dynamicctautmparameters_utm_campaign

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.4962 chars
- **Distinct Values:** 147

### requestbody_metadata_dynamicctautmparameters_utm_content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0481 chars
- **Distinct Values:** 40

### requestbody_metadata_dynamicctautmparameters_utm_medium

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.3777 chars
- **Distinct Values:** 57

### requestbody_metadata_dynamicctautmparameters_utm_source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.2471 chars
- **Distinct Values:** 11

### requestbody_metadata_dynamicctautmparameters_utm_term

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0885 chars
- **Distinct Values:** 77

### requestbody_metadata_fbbroadcastid` → `broadcasts._id` (inferred)
- `requestbody_metadata_fbbroadcastname

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.8209 chars
- **Distinct Values:** 373

### requestbody_metadata_media_url_add_utm_parameters

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### requestbody_metadata_media_url_default

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2433 chars
- **Distinct Values:** 20

### requestbody_metadata_media_url_shorten_link

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### requestbody_metadata_media_url_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.7707 chars
- **Distinct Values:** 4

### requestbody_metadata_media_url_value

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 97.0862 chars
- **Distinct Values:** 6,849

### requestbody_metadata_nodename

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### requestbody_metadata_shortenctabuttonurl

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.3581
- **Distinct Values:** 2

### requestbody_metadata_substitutionindexestoshorten

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.6115 chars
- **Distinct Values:** 10

### requestbody_metadata_substitutions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 55.3345 chars
- **Distinct Values:** 921

### requestbody_metadata_utmparameters_utm_campaign

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0407 chars
- **Distinct Values:** 20

### requestbody_metadata_utmparameters_utm_content

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0044 chars
- **Distinct Values:** 4

### requestbody_metadata_utmparameters_utm_medium

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0289 chars
- **Distinct Values:** 9

### requestbody_metadata_utmparameters_utm_source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.022 chars
- **Distinct Values:** 3

### requestbody_metadata_utmparameters_utm_term

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.004 chars
- **Distinct Values:** 4

### requestbody_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.863 chars
- **Distinct Values:** 8,061

### requestbody_ratelimit

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.9604 chars
- **Distinct Values:** 2

### requestbody_templateid` → `broadcasts._id` (inferred)
- `requestbody_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.2859 chars
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### state

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 9.0
- **Average:** 1.9761784723972775
- **Distinct Values:** 7
- **Null %:** 20.7%

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.9917 chars
- **Distinct Values:** 3

### templateid` → Related table (inferred based on naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcasts`
- **Total Columns:** 54

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 10,000 | Unique identifier for broadcasts record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 4 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **cohortid** | Text | No | - | 0.3552 chars | - | 138 | Reference to cohort | Required | Not Null, Foreign Key (likely) | Variable |
| **createdat** | Text | No | - | 32.8874 chars | - | 9,994 | Timestamp when record was created | Required | Not Null | Variable |
| **csvurl** | Text | No | URL | 138.901 chars | - | 9,892 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **events** | Text | No | SerializedJSON | 397.3511 chars | - | 9,909 | Events | Required | Not Null | Variable |
| **filteredmessagecount** | Float | Yes | - | 0.0 to 131,029.0 (Null: 80.8%) | 5,837.133402813965 | 1,242 | Count of filteredmessage | Numeric | None | Variable |
| **hdaccountid** | Float | No | - | 1.0 to 28,036.0 | 15,152.7041 | 180 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inboxid** | Float | No | - | 2.0 to 35,153.0 | 27,948.071400000004 | 252 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 20.11 chars | - | 8,168 | Human-readable name or title | Required | Not Null | Variable |
| **optedmessagecount** | Float | Yes | - | 0.0 to 169,215.0 (Null: 20.7%) | 6,676.5685631386405 | 3,879 | Count of optedmessage | Numeric | None | Variable |
| **requestbody_accountname** | Text | No | - | 10.2879 chars | - | 180 | Count of requestbody_acname | Required | Not Null | Variable |
| **requestbody_automatedretrysettings_all_retries** | Text | No | Category | 0.0316 chars | - | 7 | Requestbody Automatedretrysettings All Retries | Required | Not Null | Categorical (7 categories) |
| **requestbody_automatedretrysettings_paused** | Integer | Yes | Category | 0.0 to 1.0 | 0.0006 | 2 | Requestbody Automatedretrysettings Paused | Numeric | None | Enum-like (2 values) |
| **requestbody_automatedretrysettings_retry_till** | DateTime | Yes | - | - (Null: 95.1%) | - | 492 | Requestbody Automatedretrysettings Retry Till | Valid ISO 8601 datetime | None | Variable |
| **requestbody_cohortid** | Text | No | - | 0.3528 chars | - | 137 | Reference to requestbody cohort | Required | Not Null, Foreign Key (likely) | Variable |
| **requestbody_csvurl** | Text | No | URL | 131.1699 chars | - | 9,618 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **requestbody_inboxid** | Float | Yes | - | 2.0 to 35,153.0 (Null: 1.3%) | 28,126.349310903934 | 247 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **requestbody_metadata_buttonpayloads** | Text | No | SerializedJSON | 76.4068 chars | - | 2,770 | Requestbody Metadata Buttonpayloads | Required | Not Null | Variable |
| **requestbody_metadata_complextemplatepayload_cards** | Text | No | - | 11.6039 chars | - | 106 | Requestbody Metadata Complextemplatepayload Cards | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_campaign** | Text | No | - | 0.4962 chars | - | 147 | Requestbody Metadata Dynamicctautmparameters Utm Campaign | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_content** | Text | No | - | 0.0481 chars | - | 40 | Requestbody Metadata Dynamicctautmparameters Utm Content | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_medium** | Text | No | - | 0.3777 chars | - | 57 | Requestbody Metadata Dynamicctautmparameters Utm Medium | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_source** | Text | No | Source | 0.2471 chars | - | 11 | Requestbody Metadata Dynamicctautmparameters Utm Source | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_term** | Text | No | - | 0.0885 chars | - | 77 | Requestbody Metadata Dynamicctautmparameters Utm Term | Required | Not Null | Variable |
| **requestbody_metadata_fbbroadcastid** | Float | Yes | - | 19,026.0 to 20,318.0 (Null: 96.2%) | 19,988.36170212766 | 377 | Reference to requestbody metadata fbbroadcast | Numeric | Foreign Key (likely) | Variable |
| **requestbody_metadata_fbbroadcastname** | Text | No | - | 0.8209 chars | - | 373 | Requestbody Metadata Fbbroadcastname | Required | Not Null | Variable |
| **requestbody_metadata_media_url_add_utm_parameters** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | URL or web address | Numeric | None | Enum-like (1 values) |
| **requestbody_metadata_media_url_default** | Text | No | Category | 0.2433 chars | - | 20 | URL or web address | Required | Not Null | Variable |
| **requestbody_metadata_media_url_shorten_link** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | URL or web address | Numeric | None | Enum-like (1 values) |
| **requestbody_metadata_media_url_type** | Text | No | Category | 3.7707 chars | - | 4 | Type or category classification | Required | Not Null | Categorical (4 categories) |
| **requestbody_metadata_media_url_value** | Text | No | - | 97.0862 chars | - | 6,849 | URL or web address | Required | Not Null | Variable |
| **requestbody_metadata_nodename** | Text | No | Category | 0.0 chars | - | 1 | Requestbody Metadata Nodename | Required | Not Null | Variable |
| **requestbody_metadata_shortenctabuttonurl** | Integer | Yes | Category | 0.0 to 1.0 | 0.3581 | 2 | URL or web address | Numeric | None | Enum-like (2 values) |
| **requestbody_metadata_substitutionindexestoshorten** | Text | No | Category | 1.6115 chars | - | 10 | Requestbody Metadata Substitutionindexestoshorten | Required | Not Null | Categorical (10 categories) |
| **requestbody_metadata_substitutions** | Text | No | SerializedJSON | 55.3345 chars | - | 921 | Requestbody Metadata Substitutions | Required | Not Null | Variable |
| **requestbody_metadata_utmparameters_utm_campaign** | Text | No | Category | 0.0407 chars | - | 20 | Requestbody Metadata Utmparameters Utm Campaign | Required | Not Null | Variable |
| **requestbody_metadata_utmparameters_utm_content** | Text | No | Category | 0.0044 chars | - | 4 | Requestbody Metadata Utmparameters Utm Content | Required | Not Null | Categorical (4 categories) |
| **requestbody_metadata_utmparameters_utm_medium** | Text | No | Category | 0.0289 chars | - | 9 | Requestbody Metadata Utmparameters Utm Medium | Required | Not Null | Categorical (9 categories) |
| **requestbody_metadata_utmparameters_utm_source** | Text | No | Source | 0.022 chars | - | 3 | Requestbody Metadata Utmparameters Utm Source | Required | Not Null | Categorical (3 categories) |
| **requestbody_metadata_utmparameters_utm_term** | Text | No | Category | 0.004 chars | - | 4 | Requestbody Metadata Utmparameters Utm Term | Required | Not Null | Categorical (4 categories) |
| **requestbody_name** | Text | No | - | 19.863 chars | - | 8,061 | Requestbody Name | Required | Not Null | Variable |
| **requestbody_ratelimit** | Text | No | Category | 2.9604 chars | - | 2 | Requestbody Ratelimit | Required | Not Null | Categorical (2 categories) |
| **requestbody_templateid** | Float | Yes | - | 1.0 to 7,669.0 (Null: 1.3%) | 1,360.8628901499796 | 2,893 | Reference to requestbody template | Numeric | Foreign Key (likely) | Variable |
| **requestbody_type** | Text | No | Category | 8.2859 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **state** | Float | Yes | - | 0.0 to 9.0 (Null: 20.7%) | 1.9761784723972775 | 7 | State | Numeric | None | Variable |
| **status** | Text | No | Category | 6.9917 chars | - | 3 | Status or state of record | Required | Not Null | Categorical (3 categories) |
| **templateid** | Float | No | - | 1.0 to 7,669.0 | 1,358.3726 | 2,921 | Reference to template | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **throughput** | Float | No | - | 1.0 to 980.0 | 143.4905 | 7 | Throughput | Numeric; Required | Not Null | Variable |
| **totalmessagecount** | Float | No | - | 0.0 to 171,562.0 | 6,457.386099999999 | 4,172 | Count of totalmessage | Numeric; Required | Not Null | Variable |
| **updatedat** | Text | No | - | 32.8906 chars | - | 9,626 | Timestamp when record was last updated | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>8. broadcasts_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for broadcasts. Contains unprocessed data before transformation.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `marketing`, `staging`, `raw-data`, `campaigns`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred based on naming)
- `hdaccountid` → `postgres_accounts.id` (inferred)
- `inboxid` → `postgres_inboxes.id` (inferred)
- `name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 20.4716 chars
- **Distinct Values:** 8,416

### optedmessagecount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 169,215.0
- **Average:** 6,808.323686428772
- **Distinct Values:** 3,640
- **Null %:** 28.8%

### requestbody_accountname

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 9.7549 chars
- **Distinct Values:** 180

### requestbody_automatedretrysettings_all_retries

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0106 chars
- **Distinct Values:** 4

### requestbody_automatedretrysettings_paused

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0004
- **Distinct Values:** 2

### requestbody_automatedretrysettings_retry_till

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 370
- **Null %:** 96.3%

### requestbody_cohortid` → `postgres_accounts.id` (inferred)
- `requestbody_metadata_buttonpayloads

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 69.9875 chars
- **Distinct Values:** 2,626

### requestbody_metadata_complextemplatepayload_cards

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 9.6681 chars
- **Distinct Values:** 90

### requestbody_metadata_dynamicctautmparameters_utm_campaign

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.3927 chars
- **Distinct Values:** 127

### requestbody_metadata_dynamicctautmparameters_utm_content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0328 chars
- **Distinct Values:** 33

### requestbody_metadata_dynamicctautmparameters_utm_medium

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.3044 chars
- **Distinct Values:** 45

### requestbody_metadata_dynamicctautmparameters_utm_source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.1991 chars
- **Distinct Values:** 10

### requestbody_metadata_dynamicctautmparameters_utm_term

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0637 chars
- **Distinct Values:** 64

### requestbody_metadata_fbbroadcastid` → `broadcasts._id` (inferred)
- `requestbody_metadata_fbbroadcastname

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.6052 chars
- **Distinct Values:** 277

### requestbody_metadata_media_url_add_utm_parameters

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### requestbody_metadata_media_url_default

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2361 chars
- **Distinct Values:** 19

### requestbody_metadata_media_url_shorten_link

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### requestbody_metadata_media_url_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.7869 chars
- **Distinct Values:** 4

### requestbody_metadata_media_url_value

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 93.6962 chars
- **Distinct Values:** 6,884

### requestbody_metadata_nodename

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### requestbody_metadata_shortenctabuttonurl

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.3054
- **Distinct Values:** 2

### requestbody_metadata_substitutionindexestoshorten

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.4511 chars
- **Distinct Values:** 10

### requestbody_metadata_substitutions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 51.3469 chars
- **Distinct Values:** 903

### requestbody_metadata_utmparameters_utm_campaign

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0487 chars
- **Distinct Values:** 23

### requestbody_metadata_utmparameters_utm_content

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0063 chars
- **Distinct Values:** 5

### requestbody_metadata_utmparameters_utm_medium

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0316 chars
- **Distinct Values:** 9

### requestbody_metadata_utmparameters_utm_source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.0244 chars
- **Distinct Values:** 4

### requestbody_metadata_utmparameters_utm_term

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0059 chars
- **Distinct Values:** 5

### requestbody_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 20.1173 chars
- **Distinct Values:** 8,263

### requestbody_ratelimit

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.9424 chars
- **Distinct Values:** 2

### requestbody_templateid` → `broadcasts._id` (inferred)
- `requestbody_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.2784 chars
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### state

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 9.0
- **Average:** 1.695298245614035
- **Distinct Values:** 7
- **Null %:** 28.7%

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.9896 chars
- **Distinct Values:** 3

### templateid` → Related table (inferred based on naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcasts_raw`
- **Total Columns:** 54

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 10,001 | Unique identifier for broadcasts_raw record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 4 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **cohortid** | Text | No | - | 0.4752 chars | - | 175 | Reference to cohort | Required | Not Null, Foreign Key (likely) | Variable |
| **createdat** | Text | No | - | 32.887 chars | - | 9,992 | Timestamp when record was created | Required | Not Null | Variable |
| **csvurl** | Text | No | URL | 136.5421 chars | - | 9,846 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **events** | Text | No | SerializedJSON | 378.735 chars | - | 9,857 | Events | Required | Not Null | Variable |
| **filteredmessagecount** | Float | Yes | - | 0.0 to 131,029.0 (Null: 73.4%) | 6,005.730003755163 | 1,602 | Count of filteredmessage | Numeric | None | Variable |
| **hdaccountid** | Float | No | - | 1.0 to 28,036.0 | 14,417.352200000003 | 181 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inboxid** | Float | No | - | 2.0 to 35,153.0 | 27,082.49250000001 | 254 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 20.4716 chars | - | 8,416 | Human-readable name or title | Required | Not Null | Variable |
| **optedmessagecount** | Float | Yes | - | 0.0 to 169,215.0 (Null: 28.8%) | 6,808.323686428772 | 3,640 | Count of optedmessage | Numeric | None | Variable |
| **requestbody_accountname** | Text | No | - | 9.7549 chars | - | 180 | Count of requestbody_acname | Required | Not Null | Variable |
| **requestbody_automatedretrysettings_all_retries** | Text | No | Category | 0.0106 chars | - | 4 | Requestbody Automatedretrysettings All Retries | Required | Not Null | Categorical (4 categories) |
| **requestbody_automatedretrysettings_paused** | Integer | Yes | Category | 0.0 to 1.0 | 0.0004 | 2 | Requestbody Automatedretrysettings Paused | Numeric | None | Enum-like (2 values) |
| **requestbody_automatedretrysettings_retry_till** | DateTime | Yes | - | - (Null: 96.3%) | - | 370 | Requestbody Automatedretrysettings Retry Till | Valid ISO 8601 datetime | None | Variable |
| **requestbody_cohortid** | Text | No | - | 0.4728 chars | - | 174 | Reference to requestbody cohort | Required | Not Null, Foreign Key (likely) | Variable |
| **requestbody_csvurl** | Text | No | URL | 126.0694 chars | - | 9,466 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **requestbody_inboxid** | Float | Yes | - | 2.0 to 35,153.0 (Null: 1.9%) | 27,322.53639885806 | 245 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **requestbody_metadata_buttonpayloads** | Text | No | SerializedJSON | 69.9875 chars | - | 2,626 | Requestbody Metadata Buttonpayloads | Required | Not Null | Variable |
| **requestbody_metadata_complextemplatepayload_cards** | Text | No | - | 9.6681 chars | - | 90 | Requestbody Metadata Complextemplatepayload Cards | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_campaign** | Text | No | - | 0.3927 chars | - | 127 | Requestbody Metadata Dynamicctautmparameters Utm Campaign | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_content** | Text | No | - | 0.0328 chars | - | 33 | Requestbody Metadata Dynamicctautmparameters Utm Content | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_medium** | Text | No | - | 0.3044 chars | - | 45 | Requestbody Metadata Dynamicctautmparameters Utm Medium | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_source** | Text | No | Source | 0.1991 chars | - | 10 | Requestbody Metadata Dynamicctautmparameters Utm Source | Required | Not Null | Categorical (10 categories) |
| **requestbody_metadata_dynamicctautmparameters_utm_term** | Text | No | - | 0.0637 chars | - | 64 | Requestbody Metadata Dynamicctautmparameters Utm Term | Required | Not Null | Variable |
| **requestbody_metadata_fbbroadcastid** | Float | Yes | - | 19,026.0 to 20,318.0 (Null: 97.2%) | 19,996.540925266905 | 282 | Reference to requestbody metadata fbbroadcast | Numeric | Foreign Key (likely) | Variable |
| **requestbody_metadata_fbbroadcastname** | Text | No | - | 0.6052 chars | - | 277 | Requestbody Metadata Fbbroadcastname | Required | Not Null | Variable |
| **requestbody_metadata_media_url_add_utm_parameters** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | URL or web address | Numeric | None | Enum-like (1 values) |
| **requestbody_metadata_media_url_default** | Text | No | Category | 0.2361 chars | - | 19 | URL or web address | Required | Not Null | Variable |
| **requestbody_metadata_media_url_shorten_link** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | URL or web address | Numeric | None | Enum-like (1 values) |
| **requestbody_metadata_media_url_type** | Text | No | Category | 3.7869 chars | - | 4 | Type or category classification | Required | Not Null | Categorical (4 categories) |
| **requestbody_metadata_media_url_value** | Text | No | - | 93.6962 chars | - | 6,884 | URL or web address | Required | Not Null | Variable |
| **requestbody_metadata_nodename** | Text | No | Category | 0.0 chars | - | 1 | Requestbody Metadata Nodename | Required | Not Null | Variable |
| **requestbody_metadata_shortenctabuttonurl** | Integer | Yes | Category | 0.0 to 1.0 | 0.3054 | 2 | URL or web address | Numeric | None | Enum-like (2 values) |
| **requestbody_metadata_substitutionindexestoshorten** | Text | No | Category | 1.4511 chars | - | 10 | Requestbody Metadata Substitutionindexestoshorten | Required | Not Null | Categorical (10 categories) |
| **requestbody_metadata_substitutions** | Text | No | SerializedJSON | 51.3469 chars | - | 903 | Requestbody Metadata Substitutions | Required | Not Null | Variable |
| **requestbody_metadata_utmparameters_utm_campaign** | Text | No | Category | 0.0487 chars | - | 23 | Requestbody Metadata Utmparameters Utm Campaign | Required | Not Null | Variable |
| **requestbody_metadata_utmparameters_utm_content** | Text | No | Category | 0.0063 chars | - | 5 | Requestbody Metadata Utmparameters Utm Content | Required | Not Null | Categorical (5 categories) |
| **requestbody_metadata_utmparameters_utm_medium** | Text | No | Category | 0.0316 chars | - | 9 | Requestbody Metadata Utmparameters Utm Medium | Required | Not Null | Categorical (9 categories) |
| **requestbody_metadata_utmparameters_utm_source** | Text | No | Source | 0.0244 chars | - | 4 | Requestbody Metadata Utmparameters Utm Source | Required | Not Null | Categorical (4 categories) |
| **requestbody_metadata_utmparameters_utm_term** | Text | No | Category | 0.0059 chars | - | 5 | Requestbody Metadata Utmparameters Utm Term | Required | Not Null | Categorical (5 categories) |
| **requestbody_name** | Text | No | - | 20.1173 chars | - | 8,263 | Requestbody Name | Required | Not Null | Variable |
| **requestbody_ratelimit** | Text | No | Category | 2.9424 chars | - | 2 | Requestbody Ratelimit | Required | Not Null | Categorical (2 categories) |
| **requestbody_templateid** | Float | Yes | - | 1.0 to 7,669.0 (Null: 1.9%) | 1,367.417720228385 | 2,916 | Reference to requestbody template | Numeric | Foreign Key (likely) | Variable |
| **requestbody_type** | Text | No | Category | 8.2784 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **state** | Float | Yes | - | 0.0 to 9.0 (Null: 28.7%) | 1.695298245614035 | 7 | State | Numeric | None | Variable |
| **status** | Text | No | Category | 6.9896 chars | - | 3 | Status or state of record | Required | Not Null | Categorical (3 categories) |
| **templateid** | Float | No | - | 1.0 to 7,669.0 | 1,364.3954 | 2,948 | Reference to template | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **throughput** | Float | No | - | 1.0 to 980.0 | 160.1254 | 7 | Throughput | Numeric; Required | Not Null | Variable |
| **totalmessagecount** | Float | No | - | 0.0 to 171,562.0 | 6,495.0651 | 4,197 | Count of totalmessage | Numeric; Required | Not Null | Variable |
| **updatedat** | Text | No | - | 32.8911 chars | - | 9,723 | Timestamp when record was last updated | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>9. latest_broadcast_interactions</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages broadcast messaging campaigns and delivery tracking.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `marketing`, `campaigns`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred based on naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `latest_broadcast_interactions`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 9,999 | Unique identifier for latest_broadcast_interactions record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1,034 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **broadcastid** | Text | No | - | 24.0 chars | - | 1,794 | Reference to broadcast | Required | Not Null, Foreign Key (likely) | Variable |
| **createdat** | Text | No | - | 32.8899 chars | - | 9,992 | Timestamp when record was created | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hdaccountid** | Float | No | - | 1.0 to 28,003.0 | 14,104.0922 | 155 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updatedat** | Text | No | - | 32.8912 chars | - | 9,991 | Timestamp when record was last updated | Required | Not Null | Variable |
| **useridentifier** | Text | No | - | 11.9969 chars | - | 9,998 | Reference to userentifier | Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>10. latest_broadcast_interactions_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for latest_broadcast_interactions. Contains unprocessed data before transformation.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `marketing`, `staging`, `raw-data`, `campaigns`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred based on naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `latest_broadcast_interactions_raw`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 10,000 | Unique identifier for latest_broadcast_interactions_raw record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1,034 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **broadcastid** | Text | No | - | 24.0 chars | - | 1,792 | Reference to broadcast | Required | Not Null, Foreign Key (likely) | Variable |
| **createdat** | Text | No | - | 32.8852 chars | - | 9,989 | Timestamp when record was created | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hdaccountid** | Float | No | - | 1.0 to 27,991.0 | 14,162.0831 | 157 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updatedat** | Text | No | - | 32.881 chars | - | 9,995 | Timestamp when record was last updated | Required | Not Null | Variable |
| **useridentifier** | Text | No | - | 11.9971 chars | - | 9,998 | Reference to userentifier | Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>11. messages</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores message data and delivery information.

**Owner/Maintainer:** Conversations Team

**Tags:** `messaging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred based on naming)
- `error_data_error_user_msg

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0492 chars
- **Distinct Values:** 2

### error_data_error_user_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 0.0108 chars
- **Distinct Values:** 2

### error_data_erroredsyscall

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_errors

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_fbtrace_id` → `postgres_users.id` (inferred)
- `error_data_message

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.6648 chars
- **Distinct Values:** 23

### error_data_meta_api_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_meta_version

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_statuscode

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### error_data_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 5.8893 chars
- **Distinct Values:** 9

### error_data_to

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.4468 chars
- **Distinct Values:** 3

### eventn_ctx_event_id` → Related table (inferred based on naming)
- `inboxid` → `postgres_inboxes.id` (inferred)
- `message_account_id` → `postgres_accounts.id` (inferred)
- `message_channel

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_contacts

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_content

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_context

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_context_forwarded

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### message_context_frequently_forwarded

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### message_context_from

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_context_id` → Related table (inferred based on naming)
- `message_ctwasourceid` → Related table (inferred based on naming)
- `message_from

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0095 chars
- **Distinct Values:** 9

### message_id` → Related table (inferred based on naming)
- `message_interaction_buttonreply___ums_bidx

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 2.0
- **Average:** 0.49473684210526314
- **Distinct Values:** 4
- **Null %:** 98.1%

### message_interaction_buttonreply_payload

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.7569 chars
- **Distinct Values:** 86

### message_interaction_buttonreply_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 0.366 chars
- **Distinct Values:** 127

### message_interaction_istemplate

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0106
- **Distinct Values:** 2

### message_interaction_listreply___ums_ridx

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 8.0
- **Average:** 1.8786127167630058
- **Distinct Values:** 10
- **Null %:** 98.3%

### message_interaction_listreply___ums_sidx

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 2
- **Null %:** 98.3%

### message_interaction_listreply_description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.127 chars
- **Distinct Values:** 20

### message_interaction_listreply_payload

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0367 chars
- **Distinct Values:** 12

### message_interaction_listreply_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 0.2767 chars
- **Distinct Values:** 101

### message_interaction_nfmreply_body

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_interaction_nfmreply_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_interaction_nfmreply_response_json

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_interaction_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.4824 chars
- **Distinct Values:** 3

### message_interaction_undefined_payload

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_interaction_undefined_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_location

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_location_address

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_location_latitude

- **Type:** `Float`
- **Semantic Type:** `Latitude`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_location_longitude

- **Type:** `Float`
- **Semantic Type:** `Longitude`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_location_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_location_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_messageid` → Related table (inferred based on naming)
- `message_payload_content_parameters_order_discount_value

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_items

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_parameters_order_shipping_offset

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_shipping_value

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_parameters_order_subtotal_offset

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_subtotal_value

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_tax_offset

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_tax_value

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_payment_settings

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_parameters_reference_id` → Related table (inferred based on naming)
- `message_payload_content_parameters_total_amount_value

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_sections

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 8.4834 chars
- **Distinct Values:** 116

### message_payload_extra_body

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.3582 chars
- **Distinct Values:** 349

### message_payload_extra_buttons

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 15.0505 chars
- **Distinct Values:** 1,550

### message_payload_extra_caption

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2431 chars
- **Distinct Values:** 28

### message_payload_extra_cards

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.2549 chars
- **Distinct Values:** 44

### message_payload_extra_document_filename

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0022 chars
- **Distinct Values:** 2

### message_payload_extra_filename

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_extra_footer

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.6437 chars
- **Distinct Values:** 7

### message_payload_extra_header

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.2563 chars
- **Distinct Values:** 106

### message_payload_extra_header_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0564 chars
- **Distinct Values:** 3

### message_payload_extra_media_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 50.9801 chars
- **Distinct Values:** 1,655

### message_payload_extra_metadata_messageid` → Related table (inferred based on naming)
- `message_payload_extras_buttons

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_metadata_cvf_form_input

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0001
- **Distinct Values:** 2

### message_payload_substitutions

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.6704 chars
- **Distinct Values:** 2,085

### message_payload_template_id` → Related table (inferred based on naming)
- `message_payload_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.0737 chars
- **Distinct Values:** 8

### message_reaction

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0198 chars
- **Distinct Values:** 4

### message_reaction_emoji

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0008 chars
- **Distinct Values:** 4

### message_reaction_message_id` → Related table (inferred based on naming)
- `message_sticker_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 0.0303 chars
- **Distinct Values:** 2

### message_system

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_system_body

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_system_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_system_wa_id` → Related table (inferred based on naming)
- `message_template_allow_category_change

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0008
- **Distinct Values:** 2

### message_template_body

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 57.7796 chars
- **Distinct Values:** 613

### message_template_category

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.57 chars
- **Distinct Values:** 5

### message_template_complex_template_config_cards

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_template_complex_template_config_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_template_created_at

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.386 chars
- **Distinct Values:** 650

### message_template_created_from_limechat

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1514
- **Distinct Values:** 2

### message_template_display_id` → Related table (inferred based on naming)
- `message_template_footer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.4145 chars
- **Distinct Values:** 65

### message_template_header

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2958 chars
- **Distinct Values:** 30

### message_template_id` → Related table (inferred based on naming)
- `message_template_inbox_id` → `postgres_inboxes.id` (inferred)
- `message_template_language

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.6752 chars
- **Distinct Values:** 8

### message_template_media_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 0.217 chars
- **Distinct Values:** 2

### message_template_namespace

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 4.7484 chars
- **Distinct Values:** 96

### message_template_short_code

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.452 chars
- **Distinct Values:** 594

### message_template_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.5526 chars
- **Distinct Values:** 5

### message_template_template_buttons

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 25.4151 chars
- **Distinct Values:** 420

### message_template_template_code

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 5.0985 chars
- **Distinct Values:** 320

### message_template_template_type

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 3.0
- **Average:** 0.6562017498713331
- **Distinct Values:** 5
- **Null %:** 80.6%

### message_template_updated_at

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.3901 chars
- **Distinct Values:** 1,045

### message_templateid` → Related table (inferred based on naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `messages`
- **Total Columns:** 225

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 10,001 | Unique identifier for messages record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 7,123 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **batchid** | Text | No | - | 6.9573 chars | - | 3,302 | Reference to batch | Required | Not Null, Foreign Key (likely) | Variable |
| **broadcastid** | Text | No | - | 7.9872 chars | - | 1,521 | Reference to broadcast | Required | Not Null, Foreign Key (likely) | Variable |
| **bspsourceid** | Text | No | Source | 42.3313 chars | - | 9,457 | Reference to bspsource | Required | Not Null, Foreign Key (likely) | Variable |
| **channel** | Text | No | Source | 8.0 chars | - | 1 | Channel | Required | Not Null | Categorical (1 categories) |
| **channeltype** | Text | No | Source | 17.8559 chars | - | 6 | Type or category classification | Required | Not Null | Categorical (6 categories) |
| **createdat** | Text | No | - | 32.8883 chars | - | 9,999 | Timestamp when record was created | Required | Not Null | Variable |
| **dispatchtype** | Text | No | Category | 8.0 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **error** | Text | No | Category | 0.156 chars | - | 2 | Error | Required | Not Null | Categorical (2 categories) |
| **error_data** | Text | No | - | 1.5446 chars | - | 46 | Error Data | Required | Not Null | Variable |
| **error_data_code** | Text | No | Category | 1.8177 chars | - | 26 | Error Data Code | Required | Not Null | Variable |
| **error_data_data** | Text | No | Category | 0.1114 chars | - | 5 | Error Data Data | Required | Not Null | Categorical (5 categories) |
| **error_data_errno** | Text | No | Category | 0.0 chars | - | 1 | Error Data Errno | Required | Not Null | Variable |
| **error_data_error** | Text | No | Category | 0.0 chars | - | 1 | Error Data Error | Required | Not Null | Variable |
| **error_data_error_data_details** | Text | No | - | 9.1338 chars | - | 84 | Error Data Error Data Details | Required | Not Null | Variable |
| **error_data_error_data_messaging_product** | Text | No | Category | 0.2248 chars | - | 2 | Error Data Error Data Messaging Product | Required | Not Null | Categorical (2 categories) |
| **error_data_error_subcode** | Float | Yes | - | 33.0 to 2,593,006.0 (Null: 99.8%) | 864,357.3333333334 | 3 | Error Data Error Subcode | Numeric | None | Enum-like (3 values) |
| **error_data_error_user_msg** | Text | No | Category | 0.0492 chars | - | 2 | Error Data Error User Msg | Required | Not Null | Categorical (2 categories) |
| **error_data_error_user_title** | Text | No | Title | 0.0108 chars | - | 2 | Error Data Error User Title | Required | Not Null | Categorical (2 categories) |
| **error_data_erroredsyscall** | Text | No | Category | 0.0 chars | - | 1 | Error Data Erroredsyscall | Required | Not Null | Variable |
| **error_data_errors** | Text | No | Category | 0.0 chars | - | 1 | Error Data Errors | Required | Not Null | Variable |
| **error_data_fbtrace_id** | Text | No | - | 0.7222 chars | - | 315 | Reference to error data fbtrace | Required | Not Null, Foreign Key (likely) | Variable |
| **error_data_href** | Text | No | Category | 6.2168 chars | - | 2 | Error Data Href | Required | Not Null | Categorical (2 categories) |
| **error_data_is_transient** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Error Data Is Transient | Numeric | None | Enum-like (1 values) |
| **error_data_message** | Text | No | Category | 8.6648 chars | - | 23 | Error Data Message | Required | Not Null | Variable |
| **error_data_meta_api_status** | Text | No | Category | 0.0 chars | - | 1 | Status or state of record | Required | Not Null | Variable |
| **error_data_meta_version** | Text | No | Category | 0.0 chars | - | 1 | Error Data Meta Version | Required | Not Null | Variable |
| **error_data_statuscode** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Status or state of record | Numeric | None | Enum-like (1 values) |
| **error_data_title** | Text | No | Title | 5.8893 chars | - | 9 | Error Data Title | Required | Not Null | Categorical (9 categories) |
| **error_data_to** | Text | No | Category | 0.0 chars | - | 1 | Error Data To | Required | Not Null | Variable |
| **error_data_type** | Text | No | Category | 0.4468 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hdaccountid** | Float | No | - | 1.0 to 28,057.0 | 13,079.5251 | 201 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inboxid** | Float | No | - | 467.0 to 35,153.0 | 27,581.01019999999 | 279 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **message_account_id** | Text | No | Category | 0.1064 chars | - | 8 | Reference to account | Required | Not Null, Foreign Key (likely) | Categorical (8 categories) |
| **message_audio_format** | Text | No | Category | 0.0028 chars | - | 2 | Message Audio Format | Required | Not Null | Categorical (2 categories) |
| **message_audio_id** | Text | No | Category | 0.0031 chars | - | 3 | Reference to message audio | Required | Not Null, Foreign Key (likely) | Categorical (3 categories) |
| **message_audio_mimetype** | Text | No | Category | 0.0044 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **message_audio_sha256** | Text | No | Category | 0.0088 chars | - | 3 | Message Audio Sha256 | Required | Not Null | Categorical (3 categories) |
| **message_audio_signature** | Text | No | Category | 0.0 chars | - | 1 | Message Audio Signature | Required | Not Null | Variable |
| **message_audio_url** | Text | No | URL | 0.0 chars | - | 1 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **message_broadcast_id** | Float | Yes | - | 19,712.0 to 20,264.0 (Null: 100.0%) | 20,070.333333333332 | 4 | Reference to message broadcast | Numeric | Foreign Key (likely) | Enum-like (4 values) |
| **message_channel** | Text | No | Source | 0.0 chars | - | 1 | Message Channel | Required | Not Null | Variable |
| **message_contacts** | Text | No | Category | 0.0 chars | - | 1 | Message Contacts | Required | Not Null | Variable |
| **message_content** | Text | No | Category | 0.0 chars | - | 1 | Message Content | Required | Not Null | Variable |
| **message_context** | Text | No | Category | 0.0 chars | - | 1 | Message Context | Required | Not Null | Variable |
| **message_context_forwarded** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Message Context Forwarded | Numeric | None | Enum-like (1 values) |
| **message_context_frequently_forwarded** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Message Context Frequently Forwarded | Numeric | None | Enum-like (1 values) |
| **message_context_from** | Text | No | Category | 0.0 chars | - | 1 | Message Context From | Required | Not Null | Variable |
| **message_context_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to message context | Required | Not Null, Foreign Key (likely) | Variable |
| **message_conversational_flow_id** | Float | Yes | - | 8,451.0 to 26,398.0 (Null: 99.2%) | 19,434.0987654321 | 52 | Reference to message conversational flow | Numeric | Foreign Key (likely) | Variable |
| **message_ctwasourceid** | Text | No | Source | 0.0144 chars | - | 9 | Reference to message ctwasource | Required | Not Null, Foreign Key (likely) | Categorical (9 categories) |
| **message_ctwasourcetype** | Text | No | Source | 0.0016 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **message_destination** | Text | No | - | 10.4362 chars | - | 8,659 | Message Destination | Required | Not Null | Variable |
| **message_document_caption** | Text | No | Category | 0.0 chars | - | 1 | Message Document Caption | Required | Not Null | Variable |
| **message_document_filename** | Text | No | Category | 0.0028 chars | - | 2 | Message Document Filename | Required | Not Null | Categorical (2 categories) |
| **message_document_format** | Text | No | Category | 0.005 chars | - | 3 | Message Document Format | Required | Not Null | Categorical (3 categories) |
| **message_document_id** | Text | No | Category | 0.0016 chars | - | 2 | Reference to message document | Required | Not Null, Foreign Key (likely) | Categorical (2 categories) |
| **message_document_mimetype** | Text | No | Category | 0.0101 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **message_document_sha256** | Text | No | Category | 0.0044 chars | - | 2 | Message Document Sha256 | Required | Not Null | Categorical (2 categories) |
| **message_document_signature** | Text | No | Category | 0.0128 chars | - | 3 | Message Document Signature | Required | Not Null | Categorical (3 categories) |
| **message_document_url** | Text | No | URL | 0.0605 chars | - | 3 | URL or web address | Valid URL format; Required | Not Null | Categorical (3 categories) |
| **message_errors** | Text | No | Category | 0.0745 chars | - | 2 | Message Errors | Required | Not Null | Categorical (2 categories) |
| **message_event** | Text | No | Category | 0.0 chars | - | 1 | Message Event | Required | Not Null | Variable |
| **message_forwarded** | Text | No | Category | 0.0 chars | - | 1 | Message Forwarded | Required | Not Null | Variable |
| **message_frequently_forwarded** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Message Frequently Forwarded | Numeric | None | Enum-like (1 values) |
| **message_from** | Text | No | Category | 0.0095 chars | - | 9 | Message From | Required | Not Null | Categorical (9 categories) |
| **message_id** | Text | No | - | 5.7184 chars | - | 777 | Reference to message | Required | Not Null, Foreign Key (likely) | Variable |
| **message_image_caption** | Text | No | Category | 0.0428 chars | - | 7 | Message Image Caption | Required | Not Null | Categorical (7 categories) |
| **message_image_format** | Text | No | Category | 0.0869 chars | - | 4 | Message Image Format | Required | Not Null | Categorical (4 categories) |
| **message_image_id** | Text | No | - | 0.0493 chars | - | 33 | Reference to message image | Required | Not Null, Foreign Key (likely) | Variable |
| **message_image_mimetype** | Text | No | Category | 0.055 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **message_image_sha256** | Text | No | - | 0.1408 chars | - | 33 | Message Image Sha256 | Required | Not Null | Variable |
| **message_image_signature** | Text | No | Category | 0.1472 chars | - | 24 | Message Image Signature | Required | Not Null | Variable |
| **message_image_url** | Text | No | URL | 0.7034 chars | - | 25 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **message_inbox_id** | Float | Yes | - | 467.0 to 35,153.0 (Null: 13.3%) | 27,553.089923910524 | 260 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **message_interaction_buttonreply___ums_bidx** | Float | Yes | - | 0.0 to 2.0 (Null: 98.1%) | 0.49473684210526314 | 4 | Reference to message interaction buttonreply   ums bx | Numeric | Foreign Key (likely) | Enum-like (4 values) |
| **message_interaction_buttonreply_payload** | Text | No | - | 0.7569 chars | - | 86 | Message Interaction Buttonreply Payload | Required | Not Null | Variable |
| **message_interaction_buttonreply_title** | Text | No | Title | 0.366 chars | - | 127 | Message Interaction Buttonreply Title | Required | Not Null | Variable |
| **message_interaction_istemplate** | Integer | Yes | Category | 0.0 to 1.0 | 0.0106 | 2 | Message Interaction Istemplate | Numeric | None | Enum-like (2 values) |
| **message_interaction_listreply___ums_ridx** | Float | Yes | - | 0.0 to 8.0 (Null: 98.3%) | 1.8786127167630058 | 10 | Reference to message interaction listreply   ums rx | Numeric | Foreign Key (likely) | Variable |
| **message_interaction_listreply___ums_sidx** | Float | Yes | - | 0.0 to 0.0 (Null: 98.3%) | 0.0 | 2 | Reference to message interaction listreply   ums sx | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **message_interaction_listreply_description** | Text | No | Description | 0.127 chars | - | 20 | Message Interaction Listreply Description | Required | Not Null | Variable |
| **message_interaction_listreply_payload** | Text | No | Category | 0.0367 chars | - | 12 | Message Interaction Listreply Payload | Required | Not Null | Variable |
| **message_interaction_listreply_title** | Text | No | Title | 0.2767 chars | - | 101 | Message Interaction Listreply Title | Required | Not Null | Variable |
| **message_interaction_nfmreply_body** | Text | No | Category | 0.0 chars | - | 1 | Message Interaction Nfmreply Body | Required | Not Null | Variable |
| **message_interaction_nfmreply_name** | Text | No | Category | 0.0 chars | - | 1 | Message Interaction Nfmreply Name | Required | Not Null | Variable |
| **message_interaction_nfmreply_response_json** | Text | No | Category | 0.0 chars | - | 1 | Message Interaction Nfmreply Response Json | Required | Not Null | Variable |
| **message_interaction_type** | Text | No | Category | 0.4824 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **message_interaction_undefined_payload** | Text | No | Category | 0.0 chars | - | 1 | Message Interaction Undefined Payload | Required | Not Null | Variable |
| **message_interaction_undefined_title** | Text | No | Title | 0.0 chars | - | 1 | Message Interaction Undefined Title | Required | Not Null | Variable |
| **message_location** | Text | No | Category | 0.0 chars | - | 1 | Message Location | Required | Not Null | Variable |
| **message_location_address** | Text | No | Category | 0.0 chars | - | 1 | Message Location Address | Required | Not Null | Variable |
| **message_location_latitude** | Float | Yes | Latitude | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Location Latitude | Numeric | None | Enum-like (1 values) |
| **message_location_longitude** | Float | Yes | Longitude | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Location Longitude | Numeric | None | Enum-like (1 values) |
| **message_location_name** | Text | No | Category | 0.0 chars | - | 1 | Message Location Name | Required | Not Null | Variable |
| **message_location_url** | Text | No | URL | 0.0 chars | - | 1 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **message_messageid** | Text | No | Category | 0.0 chars | - | 1 | Reference to message message | Required | Not Null, Foreign Key (likely) | Variable |
| **message_mobile** | Text | No | Category | 0.0036 chars | - | 4 | Message Mobile | Required | Not Null | Categorical (4 categories) |
| **message_name** | Text | No | - | 0.1633 chars | - | 53 | Message Name | Required | Not Null | Variable |
| **message_node_name** | Text | No | Category | 0.0009 chars | - | 2 | Message Node Name | Required | Not Null | Categorical (2 categories) |
| **message_order_catalogid** | Text | No | Category | 0.0015 chars | - | 2 | Reference to message order catalog | Required | Not Null, Foreign Key (likely) | Categorical (2 categories) |
| **message_order_productitems** | Text | No | Category | 0.0087 chars | - | 2 | Message Order Productitems | Required | Not Null | Categorical (2 categories) |
| **message_order_text** | Text | No | Category | 0.0 chars | - | 1 | Message Order Text | Required | Not Null | Variable |
| **message_payload_buttons** | Text | No | - | 3.4107 chars | - | 135 | Message Payload Buttons | Required | Not Null | Variable |
| **message_payload_content** | Text | No | - | 15.3338 chars | - | 827 | Message Payload Content | Required | Not Null | Variable |
| **message_payload_content_button_text** | Text | No | Category | 0.2012 chars | - | 7 | Message Payload Content Button Text | Required | Not Null | Categorical (7 categories) |
| **message_payload_content_name** | Text | No | Category | 0.0 chars | - | 1 | Message Payload Content Name | Required | Not Null | Variable |
| **message_payload_content_parameters_currency** | Text | No | Category | 0.0 chars | - | 1 | Message Payload Content Parameters Currency | Required | Not Null | Variable |
| **message_payload_content_parameters_order_catalog_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to message payload content parameters order catalog | Required | Not Null, Foreign Key (likely) | Variable |
| **message_payload_content_parameters_order_discount_offset** | Float | Yes | Discount | NULL to NULL (Null: 100.0%) | NULL | 1 | Count of message_payload_content_parameters_order_dis_offset | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_discount_value** | Float | Yes | Discount | NULL to NULL (Null: 100.0%) | NULL | 1 | Count of message_payload_content_parameters_order_dis_value | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_items** | Text | No | Category | 0.0 chars | - | 1 | Message Payload Content Parameters Order Items | Required | Not Null | Variable |
| **message_payload_content_parameters_order_shipping_offset** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Order Shipping Offset | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_shipping_value** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Order Shipping Value | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_status** | Text | No | Category | 0.0 chars | - | 1 | Status or state of record | Required | Not Null | Variable |
| **message_payload_content_parameters_order_subtotal_offset** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Order Subtotal Offset | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_subtotal_value** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Order Subtotal Value | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_tax_offset** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Order Tax Offset | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_tax_value** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Order Tax Value | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_payment_settings** | Text | No | Category | 0.0 chars | - | 1 | Message Payload Content Parameters Payment Settings | Required | Not Null | Variable |
| **message_payload_content_parameters_reference_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to message payload content parameters reference | Required | Not Null, Foreign Key (likely) | Variable |
| **message_payload_content_parameters_total_amount_offset** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Total Amount Offset | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_total_amount_value** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Total Amount Value | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_type** | Text | No | Category | 0.0 chars | - | 1 | Type or category classification | Required | Not Null | Variable |
| **message_payload_content_sections** | Text | No | - | 8.4834 chars | - | 116 | Message Payload Content Sections | Required | Not Null | Variable |
| **message_payload_extra_body** | Text | No | - | 6.3582 chars | - | 349 | Message Payload Extra Body | Required | Not Null | Variable |
| **message_payload_extra_buttons** | Text | No | - | 15.0505 chars | - | 1,550 | Message Payload Extra Buttons | Required | Not Null | Variable |
| **message_payload_extra_caption** | Text | No | Category | 0.2431 chars | - | 28 | Message Payload Extra Caption | Required | Not Null | Variable |
| **message_payload_extra_cards** | Text | No | - | 7.2549 chars | - | 44 | Message Payload Extra Cards | Required | Not Null | Variable |
| **message_payload_extra_document_filename** | Text | No | Category | 0.0022 chars | - | 2 | Message Payload Extra Document Filename | Required | Not Null | Categorical (2 categories) |
| **message_payload_extra_filename** | Text | No | Category | 0.0 chars | - | 1 | Message Payload Extra Filename | Required | Not Null | Variable |
| **message_payload_extra_footer** | Text | No | Category | 0.6437 chars | - | 7 | Message Payload Extra Footer | Required | Not Null | Categorical (7 categories) |
| **message_payload_extra_header** | Text | No | - | 1.2563 chars | - | 106 | Message Payload Extra Header | Required | Not Null | Variable |
| **message_payload_extra_header_type** | Text | No | Category | 0.0564 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **message_payload_extra_media_url** | Text | No | URL | 50.9801 chars | - | 1,655 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **message_payload_extra_metadata_messageid** | Text | No | - | 0.7812 chars | - | 218 | Reference to message payload extra metadata message | Required | Not Null, Foreign Key (likely) | Variable |
| **message_payload_extra_metadata_phone** | Text | No | - | 0.26 chars | - | 218 | Message Payload Extra Metadata Phone | Required | Not Null | Variable |
| **message_payload_extra_metadata_region** | Text | No | Category | 0.0434 chars | - | 3 | Message Payload Extra Metadata Region | Required | Not Null | Categorical (3 categories) |
| **message_payload_extra_preview_url** | Integer | Yes | Category | 0.0 to 1.0 | 0.1069 | 2 | URL or web address | Numeric | None | Enum-like (2 values) |
| **message_payload_extras_buttons** | Text | No | Category | 0.0 chars | - | 1 | Message Payload Extras Buttons | Required | Not Null | Variable |
| **message_payload_metadata_cvf_form_input** | Integer | Yes | Category | 0.0 to 1.0 | 0.0001 | 2 | Message Payload Metadata Cvf Form Input | Numeric | None | Enum-like (2 values) |
| **message_payload_substitutions** | Text | No | - | 12.6704 chars | - | 2,085 | Message Payload Substitutions | Required | Not Null | Variable |
| **message_payload_template_id** | Float | Yes | - | 1.0 to 7,677.0 (Null: 47.3%) | 1,536.0652627584898 | 1,373 | Reference to message payload template | Numeric | Foreign Key (likely) | Variable |
| **message_payload_type** | Text | No | Category | 5.0737 chars | - | 8 | Type or category classification | Required | Not Null | Categorical (8 categories) |
| **message_reaction** | Text | No | Category | 0.0198 chars | - | 4 | Message Reaction | Required | Not Null | Categorical (4 categories) |
| **message_reaction_emoji** | Text | No | Category | 0.0008 chars | - | 4 | Message Reaction Emoji | Required | Not Null | Categorical (4 categories) |
| **message_reaction_message_id** | Text | No | Category | 0.0186 chars | - | 4 | Reference to message reaction message | Required | Not Null, Foreign Key (likely) | Categorical (4 categories) |
| **message_receivedat** | DateTime | Yes | - | - (Null: 100.0%) | - | 1 | Message Receivedat | Valid ISO 8601 datetime | None | Variable |
| **message_receiver** | Text | No | - | 1.5911 chars | - | 184 | Message Receiver | Required | Not Null | Variable |
| **message_referral_catalog_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to message referral catalog | Required | Not Null, Foreign Key (likely) | Variable |
| **message_referral_product_retailer_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to message referral product retailer | Required | Not Null, Foreign Key (likely) | Variable |
| **message_reply_to** | Text | No | Category | 0.0 chars | - | 1 | Message Reply To | Required | Not Null | Variable |
| **message_replyid** | Text | No | - | 2.3037 chars | - | 505 | Reference to message reply | Required | Not Null, Foreign Key (likely) | Variable |
| **message_sender** | Text | No | Category | 0.0 chars | - | 1 | Message Sender | Required | Not Null | Variable |
| **message_sender_name** | Text | No | - | 1.4343 chars | - | 1,262 | Message Sender Name | Required | Not Null | Variable |
| **message_sender_phone** | Text | No | - | 1.5882 chars | - | 1,326 | Message Sender Phone | Required | Not Null | Variable |
| **message_senderid** | Text | No | - | 1.5882 chars | - | 1,326 | Reference to message sender | Required | Not Null, Foreign Key (likely) | Variable |
| **message_sticker_format** | Text | No | Category | 0.0032 chars | - | 3 | Message Sticker Format | Required | Not Null | Categorical (3 categories) |
| **message_sticker_id** | Text | No | Category | 0.0016 chars | - | 2 | Reference to message sticker | Required | Not Null, Foreign Key (likely) | Categorical (2 categories) |
| **message_sticker_mimetype** | Text | No | Category | 0.002 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **message_sticker_sha256** | Text | No | Category | 0.0044 chars | - | 2 | Message Sticker Sha256 | Required | Not Null | Categorical (2 categories) |
| **message_sticker_signature** | Text | No | Category | 0.0064 chars | - | 2 | Message Sticker Signature | Required | Not Null | Categorical (2 categories) |
| **message_sticker_stickeranimated** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Message Sticker Stickeranimated | Numeric | None | Enum-like (1 values) |
| **message_sticker_url** | Text | No | URL | 0.0303 chars | - | 2 | URL or web address | Valid URL format; Required | Not Null | Categorical (2 categories) |
| **message_system** | Text | No | Category | 0.0 chars | - | 1 | Message System | Required | Not Null | Variable |
| **message_system_body** | Text | No | Category | 0.0 chars | - | 1 | Message System Body | Required | Not Null | Variable |
| **message_system_type** | Text | No | Category | 0.0 chars | - | 1 | Type or category classification | Required | Not Null | Variable |
| **message_system_wa_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to message system wa | Required | Not Null, Foreign Key (likely) | Variable |
| **message_template_account_id** | Float | Yes | - | 1.0 to 28,057.0 (Null: 80.6%) | 12,497.032424086465 | 129 | Reference to account | Numeric | Foreign Key (likely) | Variable |
| **message_template_allow_category_change** | Integer | Yes | Category | 0.0 to 1.0 | 0.0008 | 2 | Message Template Allow Category Change | Numeric | None | Enum-like (2 values) |
| **message_template_body** | Text | No | - | 57.7796 chars | - | 613 | Message Template Body | Required | Not Null | Variable |
| **message_template_category** | Text | No | Category | 1.57 chars | - | 5 | Message Template Category | Required | Not Null | Categorical (5 categories) |
| **message_template_complex_template_config_cards** | Text | No | Category | 0.0 chars | - | 1 | Message Template Complex Template Config Cards | Required | Not Null | Variable |
| **message_template_complex_template_config_type** | Text | No | Category | 0.0 chars | - | 1 | Type or category classification | Required | Not Null | Variable |
| **message_template_created_at** | Text | No | - | 6.386 chars | - | 650 | Message Template Created At | Required | Not Null | Variable |
| **message_template_created_from_limechat** | Integer | Yes | Category | 0.0 to 1.0 | 0.1514 | 2 | Message Template Created From Limechat | Numeric | None | Enum-like (2 values) |
| **message_template_display_id** | Float | Yes | - | 1.0 to 7,677.0 (Null: 80.6%) | 1,217.1909418425116 | 479 | Reference to message template display | Numeric | Foreign Key (likely) | Variable |
| **message_template_footer** | Text | No | - | 2.4145 chars | - | 65 | Message Template Footer | Required | Not Null | Variable |
| **message_template_header** | Text | No | Category | 0.2958 chars | - | 30 | Message Template Header | Required | Not Null | Variable |
| **message_template_id** | Float | Yes | - | 3,195.0 to 155,409.0 (Null: 80.6%) | 125,369.26505404014 | 650 | Reference to message template | Numeric | Foreign Key (likely) | Variable |
| **message_template_inbox_id** | Float | Yes | - | 585.0 to 35,098.0 (Null: 80.6%) | 26,532.213072568193 | 156 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **message_template_language** | Text | No | Category | 0.6752 chars | - | 8 | Message Template Language | Required | Not Null | Categorical (8 categories) |
| **message_template_media_url** | Text | No | URL | 0.217 chars | - | 2 | URL or web address | Valid URL format; Required | Not Null | Categorical (2 categories) |
| **message_template_namespace** | Text | No | - | 4.7484 chars | - | 96 | Message Template Namespace | Required | Not Null | Variable |
| **message_template_short_code** | Text | No | - | 3.452 chars | - | 594 | Message Template Short Code | Required | Not Null | Variable |
| **message_template_status** | Text | No | Category | 1.5526 chars | - | 5 | Status or state of record | Required | Not Null | Categorical (5 categories) |
| **message_template_template_buttons** | Text | No | - | 25.4151 chars | - | 420 | Message Template Template Buttons | Required | Not Null | Variable |
| **message_template_template_code** | Text | No | - | 5.0985 chars | - | 320 | Message Template Template Code | Required | Not Null | Variable |
| **message_template_template_type** | Float | Yes | - | 0.0 to 3.0 (Null: 80.6%) | 0.6562017498713331 | 5 | Type or category classification | Numeric | None | Enum-like (5 values) |
| **message_template_updated_at** | Text | No | - | 6.3901 chars | - | 1,045 | Message Template Updated At | Required | Not Null | Variable |
| **message_templateid** | Text | No | Category | 0.0 chars | - | 1 | Reference to message template | Required | Not Null, Foreign Key (likely) | Variable |
| **message_templatetype** | Text | No | Category | 0.0 chars | - | 1 | Type or category classification | Required | Not Null | Variable |
| **message_text** | Text | No | - | 2.6175 chars | - | 652 | Message Text | Required | Not Null | Variable |
| **message_timestamp** | Text | No | Category | 0.0119 chars | - | 12 | Message Timestamp | Required | Not Null | Variable |
| **message_type** | Text | No | Category | 0.8732 chars | - | 11 | Type or category classification | Required | Not Null | Variable |
| **message_unsupported** | Text | No | Category | 0.0745 chars | - | 2 | Message Unsupported | Required | Not Null | Categorical (2 categories) |
| **message_video_caption** | Text | No | Category | 0.0 chars | - | 1 | Reference to message veo caption | Required | Not Null, Foreign Key (likely) | Variable |
| **message_video_format** | Text | No | Category | 0.0028 chars | - | 2 | Reference to message veo format | Required | Not Null, Foreign Key (likely) | Categorical (2 categories) |
| **message_video_id** | Text | No | Category | 0.0031 chars | - | 3 | Reference to message veo | Required | Not Null, Foreign Key (likely) | Categorical (3 categories) |
| **message_video_mimetype** | Text | No | Category | 0.0018 chars | - | 2 | Type or category classification | Required | Not Null, Foreign Key (likely) | Categorical (2 categories) |
| **message_video_sha256** | Text | No | Category | 0.0088 chars | - | 3 | Reference to message veo sha256 | Required | Not Null, Foreign Key (likely) | Categorical (3 categories) |
| **message_video_signature** | Text | No | Category | 0.0 chars | - | 1 | Reference to message veo signature | Required | Not Null, Foreign Key (likely) | Variable |
| **message_video_url** | Text | No | URL | 0.0 chars | - | 1 | URL or web address | Valid URL format; Required | Not Null, Foreign Key (likely) | Variable |
| **message_wamsgid** | Text | No | Category | 0.0 chars | - | 1 | Reference to message wamsg | Required | Not Null, Foreign Key (likely) | Variable |
| **message_wanumber** | Text | No | Category | 0.0036 chars | - | 4 | Message Wanumber | Required | Not Null | Categorical (4 categories) |
| **response_bulkid** | Text | No | Category | 0.0076 chars | - | 5 | Reference to response bulk | Required | Not Null, Foreign Key (likely) | Categorical (5 categories) |
| **response_contacts** | Text | No | - | 21.8795 chars | - | 4,458 | Response Contacts | Required | Not Null | Variable |
| **response_details** | Text | No | Category | 0.0 chars | - | 1 | Response Details | Required | Not Null | Variable |
| **response_errors** | Text | No | Category | 0.0 chars | - | 1 | Response Errors | Required | Not Null | Variable |
| **response_id** | Text | No | - | 7.8091 chars | - | 2,066 | Reference to response | Required | Not Null, Foreign Key (likely) | Variable |
| **response_messages** | Text | No | - | 41.6236 chars | - | 4,463 | Response Messages | Required | Not Null | Variable |
| **response_messaging_product** | Text | No | Category | 3.5664 chars | - | 2 | Response Messaging Product | Required | Not Null | Categorical (2 categories) |
| **response_mid** | Text | No | Category | 0.1086 chars | - | 29 | Reference to response m | Required | Not Null, Foreign Key (likely) | Variable |
| **response_phone** | Text | No | - | 2.4771 chars | - | 2,062 | Response Phone | Required | Not Null | Variable |
| **response_status** | Text | No | Category | 1.4455 chars | - | 2 | Status or state of record | Required | Not Null | Categorical (2 categories) |
| **response_title** | Text | No | Title | 0.0 chars | - | 1 | Response Title | Required | Not Null | Variable |
| **response_to** | Text | No | Category | 0.0336 chars | - | 29 | Response To | Required | Not Null | Variable |
| **retriesattempted** | Float | Yes | - | 0.0 to 5.0 (Null: 15.2%) | 0.040580394007313905 | 7 | Retriesattempted | Numeric | None | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Text | No | Category | 6.3286 chars | - | 10 | Status or state of record | Required | Not Null | Categorical (10 categories) |
| **uniqueid** | Text | No | - | 21.0 chars | - | 9,998 | Reference to unique | Required | Not Null, Foreign Key (likely) | Variable |
| **updatedat** | Text | No | - | 32.8844 chars | - | 10,001 | Timestamp when record was last updated | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>12. pg_hd_message_analytics</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Analytics and metrics table for reporting purposes.

**Owner/Maintainer:** Conversations Team

**Tags:** `reporting`, `messaging`, `analytics`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred based on naming)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 979

### account_id` → `postgres_accounts.id` (inferred)
- `content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 263.4057 chars
- **Distinct Values:** 1,905

### conversation_id` → Related table (inferred based on naming)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,137

### eventn_ctx_event_id` → Related table (inferred based on naming)
- `is_replied

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.2134
- **Distinct Values:** 2

### is_template

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### message_id` → Related table (inferred based on naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `pg_hd_message_analytics`
- **Total Columns:** 15

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 979 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,510.0 | 1,285.5092 | 89 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **content** | Text | No | - | 263.4057 chars | - | 1,905 | Content | Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 8,472,691.0 to 97,616,194.0 | 91,207,940.71720003 | 9,980 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 2,137 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **is_read** | Integer | No | Category | 0.0 to 1.0 | 0.4462 | 2 | Is Read | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_replied** | Integer | No | Category | 0.0 to 1.0 | 0.2134 | 2 | Is Replied | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_template** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Is Template | Numeric; Required | Not Null | Enum-like (1 values) |
| **message_id** | Float | No | - | 426,474,586.0 to 705,202,540.0 | 663,138,806.8788992 | 9,999 | Reference to message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **read_at** | DateTime | Yes | - | - (Null: 55.4%) | - | 3,680 | Read At | Valid ISO 8601 datetime | None | Variable |
| **reply_content** | Text | No | - | 14.6483 chars | - | 1,262 | Reply Content | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 5,360 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>13. postgres2_agent_bots</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores bot configuration and interaction data.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred based on naming)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 46

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 437

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.034334763948497854 chars
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred based on naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_agent_bots`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 46 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 437 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **description** | Text | No | Description | 0.034334763948497854 chars | - | 2 | Description | Required | Not Null | Categorical (2 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 466 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hide_input_for_bot_conversations** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Reference to he input for bot conversations | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **name** | Text | No | Name | 11.141630901287554 chars | - | 436 | Human-readable name or title | Required | Not Null | Variable |
| **outgoing_url** | Text | No | URL | 57.94849785407725 chars | - | 433 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 466 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>14. postgres2_bot_analytics</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Analytics and metrics table for reporting purposes.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `reporting`, `bot`, `ai`, `analytics`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 148

### account_id` → `postgres_accounts.id` (inferred)
- `channel

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 11.8384 chars
- **Distinct Values:** 8

### conv_id` → Related table (inferred based on naming)
- `conversation_id` → Related table (inferred based on naming)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 3,484

### date

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 10.0 chars
- **Distinct Values:** 1

### distinct_id` → Related table (inferred based on naming)
- `event_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.4317 chars
- **Distinct Values:** 411

### event_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 1.7003
- **Distinct Values:** 4

### eventn_ctx_event_id` → Related table (inferred based on naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_bot_analytics`
- **Total Columns:** 21

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **_timestamp** | DateTime | No | - | - | - | 148 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 39.0 to 27,138.0 | 7,756.4852 | 86 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **channel** | Text | No | Source | 11.8384 chars | - | 8 | Channel | Required | Not Null | Categorical (8 categories) |
| **conv_id** | Float | No | - | 0.0 to 12,019,890.0 | 1,981,444.4242 | 1,496 | Reference to conv | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conversation_id** | Float | No | - | 0.0 to 81,284,613.0 | 71,851,185.57960013 | 1,496 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 3,484 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **date** | Text | No | Category | 10.0 chars | - | 1 | Date | Required | Not Null | Categorical (1 categories) |
| **distinct_id** | Text | No | - | 11.4244 chars | - | 9,312 | Reference to distinct | Required | Not Null, Foreign Key (likely) | Variable |
| **event_id** | Float | No | - | 1,057,099,562.0 to 1,057,154,132.0 | 1,057,126,400.3716 | 9,999 | Reference to event | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **event_name** | Text | No | - | 19.4317 chars | - | 411 | Event Name | Required | Not Null | Variable |
| **event_type** | Float | No | - | 0.0 to 3.0 | 1.7003 | 4 | Type or category classification | Numeric; Required | Not Null | Enum-like (4 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_id** | Float | No | - | 0.0 to 33,800.0 | 13,594.429800000004 | 106 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inserted_at** | DateTime | No | - | - | - | 178 | Inserted At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **is_outbound** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Is Outbound | Numeric; Required | Not Null | Enum-like (1 values) |
| **is_outside_working_hours** | Integer | No | Category | 0.0 to 1.0 | 0.3271 | 2 | Reference to is outse working hours | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **products** | Text | No | SerializedJSON | 4.0542 chars | - | 175 | Products | Required | Not Null | Variable |
<details>
<summary><h2>1. api_users</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** API authentication and access token management.

**Owner/Maintainer:** Platform/API Team

**Tags:** `api`, `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `api_users`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | Category | 24.0 chars | - | 14 | Unique identifier for api_users record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **email** | Text | No | Email | 23.285714285714285 chars | - | 14 | Email address | Valid email format; Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 14 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hdaccountid** | Float | No | - | 189.0 to 28,052.0 | 20,419.428571428572 | 12 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **scopes** | Text | No | SerializedJSON | 17.928571428571427 chars | - | 2 | Scopes | Required | Not Null | Categorical (2 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **token** | Text | No | Category | 28.5 chars | - | 8 | Authentication or access token | Required | Not Null, Unique (likely) | Categorical (8 categories) |

</details>

---

<details>
<summary><h2>2. api_users_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for api_users. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform/API Team

**Tags:** `raw-data`, `staging`, `api`, `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `api_users_raw`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | Category | 24.0 chars | - | 14 | Unique identifier for api_users_raw record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **email** | Text | No | Email | 23.285714285714285 chars | - | 14 | Email address | Valid email format; Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 14 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hdaccountid** | Float | No | - | 189.0 to 28,052.0 | 20,419.428571428572 | 12 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **scopes** | Text | No | SerializedJSON | 17.928571428571427 chars | - | 2 | Scopes | Required | Not Null | Categorical (2 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **token** | Text | No | Category | 28.5 chars | - | 8 | Authentication or access token | Required | Not Null, Unique (likely) | Categorical (8 categories) |

</details>

---

<details>
<summary><h2>3. broadcast_activity_aggregations</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages broadcast messaging campaigns and delivery tracking.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `campaigns`, `marketing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcast_activity_aggregations`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 9,999 | Unique identifier for broadcast_activity_aggregations record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **broadcast** | Text | No | - | 24.0 chars | - | 10,001 | Broadcast | Required | Not Null | Variable |
| **deliveredcount** | Float | No | - | 0.0 to 157,952.0 | 3,681.858 | 4,573 | Count of delivered | Numeric; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,998 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **failedbybspcount** | Float | No | - | 0.0 to 71,827.0 | 1,927.6225 | 3,482 | Count of failedbybsp | Numeric; Required | Not Null | Variable |
| **failedbyumscount** | Float | No | - | 0.0 to 96,703.0 | 294.3715 | 728 | Count of failedbyums | Numeric; Required | Not Null | Variable |
| **filteredoutbyums** | Float | Yes | - | 0.0 to 3,278.0 (Null: 82.9%) | 46.117852975495914 | 226 | Filteredoutbyums | Numeric | None | Variable |
| **optedoutbyums** | Float | Yes | - | 0.0 to 2,785.0 (Null: 22.7%) | 44.8115623383342 | 490 | Optedoutbyums | Numeric | None | Variable |
| **overallprogress** | Float | No | - | 0.0 to 207,752.0 | 6,469.946 | 4,315 | Overallprogress | Numeric; Required | Not Null | Variable |
| **readcount** | Float | No | - | 0.0 to 70,090.0 | 1,685.8446 | 3,510 | Count of read | Numeric; Required | Not Null | Variable |
| **sentbyumscount** | Float | No | - | 0.0 to 194,175.0 | 4,205.7452 | 4,767 | Count of sentbyums | Numeric; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>4. broadcast_activity_aggregations_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for broadcast_activity_aggregations. Contains unprocessed data before transformation.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `raw-data`, `staging`, `campaigns`, `marketing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcast_activity_aggregations_raw`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 10,000 | Unique identifier for broadcast_activity_aggregations_raw record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **broadcast** | Text | No | - | 24.0 chars | - | 10,000 | Broadcast | Required | Not Null | Variable |
| **deliveredcount** | Float | No | - | 0.0 to 157,952.0 | 3,743.1335 | 4,587 | Count of delivered | Numeric; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,998 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **failedbybspcount** | Float | No | - | 0.0 to 71,827.0 | 1,761.9301 | 3,352 | Count of failedbybsp | Numeric; Required | Not Null | Variable |
| **failedbyumscount** | Float | No | - | 0.0 to 96,703.0 | 264.8207 | 725 | Count of failedbyums | Numeric; Required | Not Null | Variable |
| **filteredoutbyums** | Float | Yes | - | 0.0 to 3,278.0 (Null: 77.5%) | 48.54331408262994 | 265 | Filteredoutbyums | Numeric | None | Variable |
| **optedoutbyums** | Float | Yes | - | 0.0 to 2,785.0 (Null: 29.9%) | 47.12255671279783 | 464 | Optedoutbyums | Numeric | None | Variable |
| **overallprogress** | Float | No | - | 0.0 to 207,752.0 | 6,386.1942 | 4,302 | Overallprogress | Numeric; Required | Not Null | Variable |
| **readcount** | Float | No | - | 0.0 to 102,969.0 | 1,697.952 | 3,546 | Count of read | Numeric; Required | Not Null | Variable |
| **sentbyumscount** | Float | No | - | 0.0 to 194,175.0 | 4,315.883099999999 | 4,796 | Count of sentbyums | Numeric; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>5. broadcast_reports</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Analytics and metrics table for reporting purposes.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `analytics`, `campaigns`, `reporting`, `marketing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- None identified (or table uses non-standard FK naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcast_reports`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 10,000 | Unique identifier for broadcast_reports record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 2 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **broadcast** | Text | No | - | 24.0 chars | - | 9,999 | Broadcast | Required | Not Null | Variable |
| **createdat** | Text | No | - | 31.3656 chars | - | 9,539 | Timestamp when record was created | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **reportkey** | Text | No | - | 50.0 chars | - | 9,999 | Reportkey | Required | Not Null | Variable |
| **retryreportkeys** | Text | No | - | 7.0281 chars | - | 460 | Retryreportkeys | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updatedat** | Text | No | - | 31.4576 chars | - | 9,564 | Timestamp when record was last updated | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>6. broadcast_reports_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for broadcast_reports. Contains unprocessed data before transformation.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `analytics`, `reporting`, `raw-data`, `campaigns`, `staging`, `marketing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- None identified (or table uses non-standard FK naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcast_reports_raw`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 9,998 | Unique identifier for broadcast_reports_raw record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 2 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **broadcast** | Text | No | - | 24.0 chars | - | 9,999 | Broadcast | Required | Not Null | Variable |
| **createdat** | Text | No | - | 30.9158 chars | - | 9,399 | Timestamp when record was created | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **reportkey** | Text | No | - | 50.0 chars | - | 9,998 | Reportkey | Required | Not Null | Variable |
| **retryreportkeys** | Text | No | - | 4.6386 chars | - | 304 | Retryreportkeys | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updatedat** | Text | No | - | 31.031 chars | - | 9,435 | Timestamp when record was last updated | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>7. broadcasts</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages broadcast messaging campaigns and delivery tracking.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `campaigns`, `marketing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred)
- `hdaccountid` → `postgres_accounts.id` (inferred)
- `inboxid` → `postgres_inboxes.id` (inferred)
- `name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 20.11 chars
- **Distinct Values:** 8,168

### optedmessagecount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 169,215.0
- **Average:** 6,676.5685631386405
- **Distinct Values:** 3,879
- **Null %:** 20.7%

### requestbody_accountname

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.2879 chars
- **Distinct Values:** 180

### requestbody_automatedretrysettings_all_retries

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0316 chars
- **Distinct Values:** 7

### requestbody_automatedretrysettings_paused

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0006
- **Distinct Values:** 2

### requestbody_automatedretrysettings_retry_till

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 492
- **Null %:** 95.1%

### requestbody_cohortid` → `postgres_accounts.id` (inferred)
- `requestbody_metadata_buttonpayloads

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 76.4068 chars
- **Distinct Values:** 2,770

### requestbody_metadata_complextemplatepayload_cards

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.6039 chars
- **Distinct Values:** 106

### requestbody_metadata_dynamicctautmparameters_utm_campaign

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.4962 chars
- **Distinct Values:** 147

### requestbody_metadata_dynamicctautmparameters_utm_content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0481 chars
- **Distinct Values:** 40

### requestbody_metadata_dynamicctautmparameters_utm_medium

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.3777 chars
- **Distinct Values:** 57

### requestbody_metadata_dynamicctautmparameters_utm_source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.2471 chars
- **Distinct Values:** 11

### requestbody_metadata_dynamicctautmparameters_utm_term

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0885 chars
- **Distinct Values:** 77

### requestbody_metadata_fbbroadcastid` → `broadcasts._id` (inferred)
- `requestbody_metadata_fbbroadcastname

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.8209 chars
- **Distinct Values:** 373

### requestbody_metadata_media_url_add_utm_parameters

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### requestbody_metadata_media_url_default

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2433 chars
- **Distinct Values:** 20

### requestbody_metadata_media_url_shorten_link

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### requestbody_metadata_media_url_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.7707 chars
- **Distinct Values:** 4

### requestbody_metadata_media_url_value

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 97.0862 chars
- **Distinct Values:** 6,849

### requestbody_metadata_nodename

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### requestbody_metadata_shortenctabuttonurl

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.3581
- **Distinct Values:** 2

### requestbody_metadata_substitutionindexestoshorten

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.6115 chars
- **Distinct Values:** 10

### requestbody_metadata_substitutions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 55.3345 chars
- **Distinct Values:** 921

### requestbody_metadata_utmparameters_utm_campaign

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0407 chars
- **Distinct Values:** 20

### requestbody_metadata_utmparameters_utm_content

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0044 chars
- **Distinct Values:** 4

### requestbody_metadata_utmparameters_utm_medium

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0289 chars
- **Distinct Values:** 9

### requestbody_metadata_utmparameters_utm_source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.022 chars
- **Distinct Values:** 3

### requestbody_metadata_utmparameters_utm_term

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.004 chars
- **Distinct Values:** 4

### requestbody_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.863 chars
- **Distinct Values:** 8,061

### requestbody_ratelimit

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.9604 chars
- **Distinct Values:** 2

### requestbody_templateid` → `broadcasts._id` (inferred)
- `requestbody_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.2859 chars
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### state

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 9.0
- **Average:** 1.9761784723972775
- **Distinct Values:** 7
- **Null %:** 20.7%

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.9917 chars
- **Distinct Values:** 3

### templateid` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcasts`
- **Total Columns:** 54

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 10,000 | Unique identifier for broadcasts record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 4 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **cohortid** | Text | No | - | 0.3552 chars | - | 138 | Reference to cohort | Required | Not Null, Foreign Key (likely) | Variable |
| **createdat** | Text | No | - | 32.8874 chars | - | 9,994 | Timestamp when record was created | Required | Not Null | Variable |
| **csvurl** | Text | No | URL | 138.901 chars | - | 9,892 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **events** | Text | No | SerializedJSON | 397.3511 chars | - | 9,909 | Events | Required | Not Null | Variable |
| **filteredmessagecount** | Float | Yes | - | 0.0 to 131,029.0 (Null: 80.8%) | 5,837.133402813965 | 1,242 | Count of filteredmessage | Numeric | None | Variable |
| **hdaccountid** | Float | No | - | 1.0 to 28,036.0 | 15,152.7041 | 180 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inboxid** | Float | No | - | 2.0 to 35,153.0 | 27,948.071400000004 | 252 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 20.11 chars | - | 8,168 | Human-readable name or title | Required | Not Null | Variable |
| **optedmessagecount** | Float | Yes | - | 0.0 to 169,215.0 (Null: 20.7%) | 6,676.5685631386405 | 3,879 | Count of optedmessage | Numeric | None | Variable |
| **requestbody_accountname** | Text | No | - | 10.2879 chars | - | 180 | Count of requestbody_acname | Required | Not Null | Variable |
| **requestbody_automatedretrysettings_all_retries** | Text | No | Category | 0.0316 chars | - | 7 | Requestbody Automatedretrysettings All Retries | Required | Not Null | Categorical (7 categories) |
| **requestbody_automatedretrysettings_paused** | Integer | Yes | Category | 0.0 to 1.0 | 0.0006 | 2 | Requestbody Automatedretrysettings Paused | Numeric | None | Enum-like (2 values) |
| **requestbody_automatedretrysettings_retry_till** | DateTime | Yes | - | - (Null: 95.1%) | - | 492 | Requestbody Automatedretrysettings Retry Till | Valid ISO 8601 datetime | None | Variable |
| **requestbody_cohortid** | Text | No | - | 0.3528 chars | - | 137 | Reference to requestbody cohort | Required | Not Null, Foreign Key (likely) | Variable |
| **requestbody_csvurl** | Text | No | URL | 131.1699 chars | - | 9,618 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **requestbody_inboxid** | Float | Yes | - | 2.0 to 35,153.0 (Null: 1.3%) | 28,126.349310903934 | 247 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **requestbody_metadata_buttonpayloads** | Text | No | SerializedJSON | 76.4068 chars | - | 2,770 | Requestbody Metadata Buttonpayloads | Required | Not Null | Variable |
| **requestbody_metadata_complextemplatepayload_cards** | Text | No | - | 11.6039 chars | - | 106 | Requestbody Metadata Complextemplatepayload Cards | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_campaign** | Text | No | - | 0.4962 chars | - | 147 | Requestbody Metadata Dynamicctautmparameters Utm Campaign | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_content** | Text | No | - | 0.0481 chars | - | 40 | Requestbody Metadata Dynamicctautmparameters Utm Content | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_medium** | Text | No | - | 0.3777 chars | - | 57 | Requestbody Metadata Dynamicctautmparameters Utm Medium | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_source** | Text | No | Source | 0.2471 chars | - | 11 | Requestbody Metadata Dynamicctautmparameters Utm Source | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_term** | Text | No | - | 0.0885 chars | - | 77 | Requestbody Metadata Dynamicctautmparameters Utm Term | Required | Not Null | Variable |
| **requestbody_metadata_fbbroadcastid** | Float | Yes | - | 19,026.0 to 20,318.0 (Null: 96.2%) | 19,988.36170212766 | 377 | Reference to requestbody metadata fbbroadcast | Numeric | Foreign Key (likely) | Variable |
| **requestbody_metadata_fbbroadcastname** | Text | No | - | 0.8209 chars | - | 373 | Requestbody Metadata Fbbroadcastname | Required | Not Null | Variable |
| **requestbody_metadata_media_url_add_utm_parameters** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | URL or web address | Numeric | None | Enum-like (1 values) |
| **requestbody_metadata_media_url_default** | Text | No | Category | 0.2433 chars | - | 20 | URL or web address | Required | Not Null | Variable |
| **requestbody_metadata_media_url_shorten_link** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | URL or web address | Numeric | None | Enum-like (1 values) |
| **requestbody_metadata_media_url_type** | Text | No | Category | 3.7707 chars | - | 4 | Type or category classification | Required | Not Null | Categorical (4 categories) |
| **requestbody_metadata_media_url_value** | Text | No | - | 97.0862 chars | - | 6,849 | URL or web address | Required | Not Null | Variable |
| **requestbody_metadata_nodename** | Text | No | Category | 0.0 chars | - | 1 | Requestbody Metadata Nodename | Required | Not Null | Categorical (1 categories) |
| **requestbody_metadata_shortenctabuttonurl** | Integer | Yes | Category | 0.0 to 1.0 | 0.3581 | 2 | URL or web address | Numeric | None | Enum-like (2 values) |
| **requestbody_metadata_substitutionindexestoshorten** | Text | No | Category | 1.6115 chars | - | 10 | Requestbody Metadata Substitutionindexestoshorten | Required | Not Null | Categorical (10 categories) |
| **requestbody_metadata_substitutions** | Text | No | SerializedJSON | 55.3345 chars | - | 921 | Requestbody Metadata Substitutions | Required | Not Null | Variable |
| **requestbody_metadata_utmparameters_utm_campaign** | Text | No | Category | 0.0407 chars | - | 20 | Requestbody Metadata Utmparameters Utm Campaign | Required | Not Null | Variable |
| **requestbody_metadata_utmparameters_utm_content** | Text | No | Category | 0.0044 chars | - | 4 | Requestbody Metadata Utmparameters Utm Content | Required | Not Null | Categorical (4 categories) |
| **requestbody_metadata_utmparameters_utm_medium** | Text | No | Category | 0.0289 chars | - | 9 | Requestbody Metadata Utmparameters Utm Medium | Required | Not Null | Categorical (9 categories) |
| **requestbody_metadata_utmparameters_utm_source** | Text | No | Source | 0.022 chars | - | 3 | Requestbody Metadata Utmparameters Utm Source | Required | Not Null | Categorical (3 categories) |
| **requestbody_metadata_utmparameters_utm_term** | Text | No | Category | 0.004 chars | - | 4 | Requestbody Metadata Utmparameters Utm Term | Required | Not Null | Categorical (4 categories) |
| **requestbody_name** | Text | No | - | 19.863 chars | - | 8,061 | Requestbody Name | Required | Not Null | Variable |
| **requestbody_ratelimit** | Text | No | Category | 2.9604 chars | - | 2 | Requestbody Ratelimit | Required | Not Null | Categorical (2 categories) |
| **requestbody_templateid** | Float | Yes | - | 1.0 to 7,669.0 (Null: 1.3%) | 1,360.8628901499796 | 2,893 | Reference to requestbody template | Numeric | Foreign Key (likely) | Variable |
| **requestbody_type** | Text | No | Category | 8.2859 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **state** | Float | Yes | - | 0.0 to 9.0 (Null: 20.7%) | 1.9761784723972775 | 7 | State | Numeric | None | Variable |
| **status** | Text | No | Category | 6.9917 chars | - | 3 | Status or state of record | Required | Not Null | Categorical (3 categories) |
| **templateid** | Float | No | - | 1.0 to 7,669.0 | 1,358.3726 | 2,921 | Reference to template | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **throughput** | Float | No | - | 1.0 to 980.0 | 143.4905 | 7 | Throughput | Numeric; Required | Not Null | Variable |
| **totalmessagecount** | Float | No | - | 0.0 to 171,562.0 | 6,457.386099999999 | 4,172 | Count of totalmessage | Numeric; Required | Not Null | Variable |
| **updatedat** | Text | No | - | 32.8906 chars | - | 9,626 | Timestamp when record was last updated | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>8. broadcasts_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for broadcasts. Contains unprocessed data before transformation.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `raw-data`, `staging`, `campaigns`, `marketing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred)
- `hdaccountid` → `postgres_accounts.id` (inferred)
- `inboxid` → `postgres_inboxes.id` (inferred)
- `name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 20.4716 chars
- **Distinct Values:** 8,416

### optedmessagecount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 169,215.0
- **Average:** 6,808.323686428772
- **Distinct Values:** 3,640
- **Null %:** 28.8%

### requestbody_accountname

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 9.7549 chars
- **Distinct Values:** 180

### requestbody_automatedretrysettings_all_retries

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0106 chars
- **Distinct Values:** 4

### requestbody_automatedretrysettings_paused

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0004
- **Distinct Values:** 2

### requestbody_automatedretrysettings_retry_till

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 370
- **Null %:** 96.3%

### requestbody_cohortid` → `postgres_accounts.id` (inferred)
- `requestbody_metadata_buttonpayloads

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 69.9875 chars
- **Distinct Values:** 2,626

### requestbody_metadata_complextemplatepayload_cards

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 9.6681 chars
- **Distinct Values:** 90

### requestbody_metadata_dynamicctautmparameters_utm_campaign

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.3927 chars
- **Distinct Values:** 127

### requestbody_metadata_dynamicctautmparameters_utm_content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0328 chars
- **Distinct Values:** 33

### requestbody_metadata_dynamicctautmparameters_utm_medium

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.3044 chars
- **Distinct Values:** 45

### requestbody_metadata_dynamicctautmparameters_utm_source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.1991 chars
- **Distinct Values:** 10

### requestbody_metadata_dynamicctautmparameters_utm_term

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.0637 chars
- **Distinct Values:** 64

### requestbody_metadata_fbbroadcastid` → `broadcasts._id` (inferred)
- `requestbody_metadata_fbbroadcastname

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.6052 chars
- **Distinct Values:** 277

### requestbody_metadata_media_url_add_utm_parameters

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### requestbody_metadata_media_url_default

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2361 chars
- **Distinct Values:** 19

### requestbody_metadata_media_url_shorten_link

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### requestbody_metadata_media_url_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.7869 chars
- **Distinct Values:** 4

### requestbody_metadata_media_url_value

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 93.6962 chars
- **Distinct Values:** 6,884

### requestbody_metadata_nodename

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### requestbody_metadata_shortenctabuttonurl

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.3054
- **Distinct Values:** 2

### requestbody_metadata_substitutionindexestoshorten

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.4511 chars
- **Distinct Values:** 10

### requestbody_metadata_substitutions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 51.3469 chars
- **Distinct Values:** 903

### requestbody_metadata_utmparameters_utm_campaign

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0487 chars
- **Distinct Values:** 23

### requestbody_metadata_utmparameters_utm_content

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0063 chars
- **Distinct Values:** 5

### requestbody_metadata_utmparameters_utm_medium

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0316 chars
- **Distinct Values:** 9

### requestbody_metadata_utmparameters_utm_source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.0244 chars
- **Distinct Values:** 4

### requestbody_metadata_utmparameters_utm_term

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0059 chars
- **Distinct Values:** 5

### requestbody_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 20.1173 chars
- **Distinct Values:** 8,263

### requestbody_ratelimit

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.9424 chars
- **Distinct Values:** 2

### requestbody_templateid` → `broadcasts._id` (inferred)
- `requestbody_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.2784 chars
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### state

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 9.0
- **Average:** 1.695298245614035
- **Distinct Values:** 7
- **Null %:** 28.7%

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.9896 chars
- **Distinct Values:** 3

### templateid` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `broadcasts_raw`
- **Total Columns:** 54

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 10,001 | Unique identifier for broadcasts_raw record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 4 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **cohortid** | Text | No | - | 0.4752 chars | - | 175 | Reference to cohort | Required | Not Null, Foreign Key (likely) | Variable |
| **createdat** | Text | No | - | 32.887 chars | - | 9,992 | Timestamp when record was created | Required | Not Null | Variable |
| **csvurl** | Text | No | URL | 136.5421 chars | - | 9,846 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **events** | Text | No | SerializedJSON | 378.735 chars | - | 9,857 | Events | Required | Not Null | Variable |
| **filteredmessagecount** | Float | Yes | - | 0.0 to 131,029.0 (Null: 73.4%) | 6,005.730003755163 | 1,602 | Count of filteredmessage | Numeric | None | Variable |
| **hdaccountid** | Float | No | - | 1.0 to 28,036.0 | 14,417.352200000003 | 181 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inboxid** | Float | No | - | 2.0 to 35,153.0 | 27,082.49250000001 | 254 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 20.4716 chars | - | 8,416 | Human-readable name or title | Required | Not Null | Variable |
| **optedmessagecount** | Float | Yes | - | 0.0 to 169,215.0 (Null: 28.8%) | 6,808.323686428772 | 3,640 | Count of optedmessage | Numeric | None | Variable |
| **requestbody_accountname** | Text | No | - | 9.7549 chars | - | 180 | Count of requestbody_acname | Required | Not Null | Variable |
| **requestbody_automatedretrysettings_all_retries** | Text | No | Category | 0.0106 chars | - | 4 | Requestbody Automatedretrysettings All Retries | Required | Not Null | Categorical (4 categories) |
| **requestbody_automatedretrysettings_paused** | Integer | Yes | Category | 0.0 to 1.0 | 0.0004 | 2 | Requestbody Automatedretrysettings Paused | Numeric | None | Enum-like (2 values) |
| **requestbody_automatedretrysettings_retry_till** | DateTime | Yes | - | - (Null: 96.3%) | - | 370 | Requestbody Automatedretrysettings Retry Till | Valid ISO 8601 datetime | None | Variable |
| **requestbody_cohortid** | Text | No | - | 0.4728 chars | - | 174 | Reference to requestbody cohort | Required | Not Null, Foreign Key (likely) | Variable |
| **requestbody_csvurl** | Text | No | URL | 126.0694 chars | - | 9,466 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **requestbody_inboxid** | Float | Yes | - | 2.0 to 35,153.0 (Null: 1.9%) | 27,322.53639885806 | 245 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **requestbody_metadata_buttonpayloads** | Text | No | SerializedJSON | 69.9875 chars | - | 2,626 | Requestbody Metadata Buttonpayloads | Required | Not Null | Variable |
| **requestbody_metadata_complextemplatepayload_cards** | Text | No | - | 9.6681 chars | - | 90 | Requestbody Metadata Complextemplatepayload Cards | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_campaign** | Text | No | - | 0.3927 chars | - | 127 | Requestbody Metadata Dynamicctautmparameters Utm Campaign | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_content** | Text | No | - | 0.0328 chars | - | 33 | Requestbody Metadata Dynamicctautmparameters Utm Content | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_medium** | Text | No | - | 0.3044 chars | - | 45 | Requestbody Metadata Dynamicctautmparameters Utm Medium | Required | Not Null | Variable |
| **requestbody_metadata_dynamicctautmparameters_utm_source** | Text | No | Source | 0.1991 chars | - | 10 | Requestbody Metadata Dynamicctautmparameters Utm Source | Required | Not Null | Categorical (10 categories) |
| **requestbody_metadata_dynamicctautmparameters_utm_term** | Text | No | - | 0.0637 chars | - | 64 | Requestbody Metadata Dynamicctautmparameters Utm Term | Required | Not Null | Variable |
| **requestbody_metadata_fbbroadcastid** | Float | Yes | - | 19,026.0 to 20,318.0 (Null: 97.2%) | 19,996.540925266905 | 282 | Reference to requestbody metadata fbbroadcast | Numeric | Foreign Key (likely) | Variable |
| **requestbody_metadata_fbbroadcastname** | Text | No | - | 0.6052 chars | - | 277 | Requestbody Metadata Fbbroadcastname | Required | Not Null | Variable |
| **requestbody_metadata_media_url_add_utm_parameters** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | URL or web address | Numeric | None | Enum-like (1 values) |
| **requestbody_metadata_media_url_default** | Text | No | Category | 0.2361 chars | - | 19 | URL or web address | Required | Not Null | Variable |
| **requestbody_metadata_media_url_shorten_link** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | URL or web address | Numeric | None | Enum-like (1 values) |
| **requestbody_metadata_media_url_type** | Text | No | Category | 3.7869 chars | - | 4 | Type or category classification | Required | Not Null | Categorical (4 categories) |
| **requestbody_metadata_media_url_value** | Text | No | - | 93.6962 chars | - | 6,884 | URL or web address | Required | Not Null | Variable |
| **requestbody_metadata_nodename** | Text | No | Category | 0.0 chars | - | 1 | Requestbody Metadata Nodename | Required | Not Null | Categorical (1 categories) |
| **requestbody_metadata_shortenctabuttonurl** | Integer | Yes | Category | 0.0 to 1.0 | 0.3054 | 2 | URL or web address | Numeric | None | Enum-like (2 values) |
| **requestbody_metadata_substitutionindexestoshorten** | Text | No | Category | 1.4511 chars | - | 10 | Requestbody Metadata Substitutionindexestoshorten | Required | Not Null | Categorical (10 categories) |
| **requestbody_metadata_substitutions** | Text | No | SerializedJSON | 51.3469 chars | - | 903 | Requestbody Metadata Substitutions | Required | Not Null | Variable |
| **requestbody_metadata_utmparameters_utm_campaign** | Text | No | Category | 0.0487 chars | - | 23 | Requestbody Metadata Utmparameters Utm Campaign | Required | Not Null | Variable |
| **requestbody_metadata_utmparameters_utm_content** | Text | No | Category | 0.0063 chars | - | 5 | Requestbody Metadata Utmparameters Utm Content | Required | Not Null | Categorical (5 categories) |
| **requestbody_metadata_utmparameters_utm_medium** | Text | No | Category | 0.0316 chars | - | 9 | Requestbody Metadata Utmparameters Utm Medium | Required | Not Null | Categorical (9 categories) |
| **requestbody_metadata_utmparameters_utm_source** | Text | No | Source | 0.0244 chars | - | 4 | Requestbody Metadata Utmparameters Utm Source | Required | Not Null | Categorical (4 categories) |
| **requestbody_metadata_utmparameters_utm_term** | Text | No | Category | 0.0059 chars | - | 5 | Requestbody Metadata Utmparameters Utm Term | Required | Not Null | Categorical (5 categories) |
| **requestbody_name** | Text | No | - | 20.1173 chars | - | 8,263 | Requestbody Name | Required | Not Null | Variable |
| **requestbody_ratelimit** | Text | No | Category | 2.9424 chars | - | 2 | Requestbody Ratelimit | Required | Not Null | Categorical (2 categories) |
| **requestbody_templateid** | Float | Yes | - | 1.0 to 7,669.0 (Null: 1.9%) | 1,367.417720228385 | 2,916 | Reference to requestbody template | Numeric | Foreign Key (likely) | Variable |
| **requestbody_type** | Text | No | Category | 8.2784 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **state** | Float | Yes | - | 0.0 to 9.0 (Null: 28.7%) | 1.695298245614035 | 7 | State | Numeric | None | Variable |
| **status** | Text | No | Category | 6.9896 chars | - | 3 | Status or state of record | Required | Not Null | Categorical (3 categories) |
| **templateid** | Float | No | - | 1.0 to 7,669.0 | 1,364.3954 | 2,948 | Reference to template | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **throughput** | Float | No | - | 1.0 to 980.0 | 160.1254 | 7 | Throughput | Numeric; Required | Not Null | Variable |
| **totalmessagecount** | Float | No | - | 0.0 to 171,562.0 | 6,495.0651 | 4,197 | Count of totalmessage | Numeric; Required | Not Null | Variable |
| **updatedat** | Text | No | - | 32.8911 chars | - | 9,723 | Timestamp when record was last updated | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>9. latest_broadcast_interactions</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages broadcast messaging campaigns and delivery tracking.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `campaigns`, `marketing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `latest_broadcast_interactions`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 9,999 | Unique identifier for latest_broadcast_interactions record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1,034 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **broadcastid** | Text | No | - | 24.0 chars | - | 1,794 | Reference to broadcast | Required | Not Null, Foreign Key (likely) | Variable |
| **createdat** | Text | No | - | 32.8899 chars | - | 9,992 | Timestamp when record was created | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hdaccountid** | Float | No | - | 1.0 to 28,003.0 | 14,104.0922 | 155 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updatedat** | Text | No | - | 32.8912 chars | - | 9,991 | Timestamp when record was last updated | Required | Not Null | Variable |
| **useridentifier** | Text | No | - | 11.9969 chars | - | 9,998 | Reference to userentifier | Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>10. latest_broadcast_interactions_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for latest_broadcast_interactions. Contains unprocessed data before transformation.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `raw-data`, `staging`, `campaigns`, `marketing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `latest_broadcast_interactions_raw`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 10,000 | Unique identifier for latest_broadcast_interactions_raw record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1,034 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **broadcastid** | Text | No | - | 24.0 chars | - | 1,792 | Reference to broadcast | Required | Not Null, Foreign Key (likely) | Variable |
| **createdat** | Text | No | - | 32.8852 chars | - | 9,989 | Timestamp when record was created | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hdaccountid** | Float | No | - | 1.0 to 27,991.0 | 14,162.0831 | 157 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updatedat** | Text | No | - | 32.881 chars | - | 9,995 | Timestamp when record was last updated | Required | Not Null | Variable |
| **useridentifier** | Text | No | - | 11.9971 chars | - | 9,998 | Reference to userentifier | Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>11. messages</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores message data and delivery information.

**Owner/Maintainer:** Conversations Team

**Tags:** `messaging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred)
- `error_data_error_user_msg

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0492 chars
- **Distinct Values:** 2

### error_data_error_user_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 0.0108 chars
- **Distinct Values:** 2

### error_data_erroredsyscall

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_errors

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_fbtrace_id` → `postgres_users.id` (inferred)
- `error_data_message

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.6648 chars
- **Distinct Values:** 23

### error_data_meta_api_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_meta_version

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_statuscode

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### error_data_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 5.8893 chars
- **Distinct Values:** 9

### error_data_to

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### error_data_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.4468 chars
- **Distinct Values:** 3

### eventn_ctx_event_id` → Related table (inferred)
- `inboxid` → `postgres_inboxes.id` (inferred)
- `message_account_id` → `postgres_accounts.id` (inferred)
- `message_channel

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_contacts

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_content

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_context

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_context_forwarded

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### message_context_frequently_forwarded

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### message_context_from

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_context_id` → Related table (inferred)
- `message_ctwasourceid` → Related table (inferred)
- `message_from

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0095 chars
- **Distinct Values:** 9

### message_id` → Related table (inferred)
- `message_interaction_buttonreply___ums_bidx

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 2.0
- **Average:** 0.49473684210526314
- **Distinct Values:** 4
- **Null %:** 98.1%

### message_interaction_buttonreply_payload

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.7569 chars
- **Distinct Values:** 86

### message_interaction_buttonreply_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 0.366 chars
- **Distinct Values:** 127

### message_interaction_istemplate

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0106
- **Distinct Values:** 2

### message_interaction_listreply___ums_ridx

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 8.0
- **Average:** 1.8786127167630058
- **Distinct Values:** 10
- **Null %:** 98.3%

### message_interaction_listreply___ums_sidx

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 2
- **Null %:** 98.3%

### message_interaction_listreply_description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.127 chars
- **Distinct Values:** 20

### message_interaction_listreply_payload

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0367 chars
- **Distinct Values:** 12

### message_interaction_listreply_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 0.2767 chars
- **Distinct Values:** 101

### message_interaction_nfmreply_body

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_interaction_nfmreply_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_interaction_nfmreply_response_json

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_interaction_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.4824 chars
- **Distinct Values:** 3

### message_interaction_undefined_payload

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_interaction_undefined_title

- **Type:** `Text`
- **Semantic Type:** `Title`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_location

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_location_address

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_location_latitude

- **Type:** `Float`
- **Semantic Type:** `Latitude`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_location_longitude

- **Type:** `Float`
- **Semantic Type:** `Longitude`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_location_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_location_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_messageid` → Related table (inferred)
- `message_payload_content_parameters_order_discount_value

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_items

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_parameters_order_shipping_offset

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_shipping_value

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_parameters_order_subtotal_offset

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_subtotal_value

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_tax_offset

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_order_tax_value

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_payment_settings

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_parameters_reference_id` → Related table (inferred)
- `message_payload_content_parameters_total_amount_value

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### message_payload_content_parameters_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_content_sections

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 8.4834 chars
- **Distinct Values:** 116

### message_payload_extra_body

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.3582 chars
- **Distinct Values:** 349

### message_payload_extra_buttons

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 15.0505 chars
- **Distinct Values:** 1,550

### message_payload_extra_caption

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2431 chars
- **Distinct Values:** 28

### message_payload_extra_cards

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.2549 chars
- **Distinct Values:** 44

### message_payload_extra_document_filename

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0022 chars
- **Distinct Values:** 2

### message_payload_extra_filename

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_extra_footer

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.6437 chars
- **Distinct Values:** 7

### message_payload_extra_header

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.2563 chars
- **Distinct Values:** 106

### message_payload_extra_header_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0564 chars
- **Distinct Values:** 3

### message_payload_extra_media_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 50.9801 chars
- **Distinct Values:** 1,655

### message_payload_extra_metadata_messageid` → Related table (inferred)
- `message_payload_extras_buttons

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_payload_metadata_cvf_form_input

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0001
- **Distinct Values:** 2

### message_payload_substitutions

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.6704 chars
- **Distinct Values:** 2,085

### message_payload_template_id` → Related table (inferred)
- `message_payload_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.0737 chars
- **Distinct Values:** 8

### message_reaction

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0198 chars
- **Distinct Values:** 4

### message_reaction_emoji

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0008 chars
- **Distinct Values:** 4

### message_reaction_message_id` → Related table (inferred)
- `message_sticker_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 0.0303 chars
- **Distinct Values:** 2

### message_system

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_system_body

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_system_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_system_wa_id` → Related table (inferred)
- `message_template_allow_category_change

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0008
- **Distinct Values:** 2

### message_template_body

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 57.7796 chars
- **Distinct Values:** 613

### message_template_category

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.57 chars
- **Distinct Values:** 5

### message_template_complex_template_config_cards

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_template_complex_template_config_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### message_template_created_at

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.386 chars
- **Distinct Values:** 650

### message_template_created_from_limechat

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1514
- **Distinct Values:** 2

### message_template_display_id` → Related table (inferred)
- `message_template_footer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.4145 chars
- **Distinct Values:** 65

### message_template_header

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2958 chars
- **Distinct Values:** 30

### message_template_id` → Related table (inferred)
- `message_template_inbox_id` → `postgres_inboxes.id` (inferred)
- `message_template_language

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.6752 chars
- **Distinct Values:** 8

### message_template_media_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 0.217 chars
- **Distinct Values:** 2

### message_template_namespace

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 4.7484 chars
- **Distinct Values:** 96

### message_template_short_code

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.452 chars
- **Distinct Values:** 594

### message_template_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.5526 chars
- **Distinct Values:** 5

### message_template_template_buttons

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 25.4151 chars
- **Distinct Values:** 420

### message_template_template_code

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 5.0985 chars
- **Distinct Values:** 320

### message_template_template_type

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 3.0
- **Average:** 0.6562017498713331
- **Distinct Values:** 5
- **Null %:** 80.6%

### message_template_updated_at

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.3901 chars
- **Distinct Values:** 1,045

### message_templateid` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `messages`
- **Total Columns:** 225

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | - | 24.0 chars | - | 10,001 | Unique identifier for messages record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 7,123 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **batchid** | Text | No | - | 6.9573 chars | - | 3,302 | Reference to batch | Required | Not Null, Foreign Key (likely) | Variable |
| **broadcastid** | Text | No | - | 7.9872 chars | - | 1,521 | Reference to broadcast | Required | Not Null, Foreign Key (likely) | Variable |
| **bspsourceid** | Text | No | Source | 42.3313 chars | - | 9,457 | Reference to bspsource | Required | Not Null, Foreign Key (likely) | Variable |
| **channel** | Text | No | Source | 8.0 chars | - | 1 | Channel | Required | Not Null | Categorical (1 categories) |
| **channeltype** | Text | No | Source | 17.8559 chars | - | 6 | Type or category classification | Required | Not Null | Categorical (6 categories) |
| **createdat** | Text | No | - | 32.8883 chars | - | 9,999 | Timestamp when record was created | Required | Not Null | Variable |
| **dispatchtype** | Text | No | Category | 8.0 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **error** | Text | No | Category | 0.156 chars | - | 2 | Error | Required | Not Null | Categorical (2 categories) |
| **error_data** | Text | No | - | 1.5446 chars | - | 46 | Error Data | Required | Not Null | Variable |
| **error_data_code** | Text | No | Category | 1.8177 chars | - | 26 | Error Data Code | Required | Not Null | Variable |
| **error_data_data** | Text | No | Category | 0.1114 chars | - | 5 | Error Data Data | Required | Not Null | Categorical (5 categories) |
| **error_data_errno** | Text | No | Category | 0.0 chars | - | 1 | Error Data Errno | Required | Not Null | Categorical (1 categories) |
| **error_data_error** | Text | No | Category | 0.0 chars | - | 1 | Error Data Error | Required | Not Null | Categorical (1 categories) |
| **error_data_error_data_details** | Text | No | - | 9.1338 chars | - | 84 | Error Data Error Data Details | Required | Not Null | Variable |
| **error_data_error_data_messaging_product** | Text | No | Category | 0.2248 chars | - | 2 | Error Data Error Data Messaging Product | Required | Not Null | Categorical (2 categories) |
| **error_data_error_subcode** | Float | Yes | - | 33.0 to 2,593,006.0 (Null: 99.8%) | 864,357.3333333334 | 3 | Error Data Error Subcode | Numeric | None | Enum-like (3 values) |
| **error_data_error_user_msg** | Text | No | Category | 0.0492 chars | - | 2 | Error Data Error User Msg | Required | Not Null | Categorical (2 categories) |
| **error_data_error_user_title** | Text | No | Title | 0.0108 chars | - | 2 | Error Data Error User Title | Required | Not Null | Categorical (2 categories) |
| **error_data_erroredsyscall** | Text | No | Category | 0.0 chars | - | 1 | Error Data Erroredsyscall | Required | Not Null | Categorical (1 categories) |
| **error_data_errors** | Text | No | Category | 0.0 chars | - | 1 | Error Data Errors | Required | Not Null | Categorical (1 categories) |
| **error_data_fbtrace_id** | Text | No | - | 0.7222 chars | - | 315 | Reference to error data fbtrace | Required | Not Null, Foreign Key (likely) | Variable |
| **error_data_href** | Text | No | Category | 6.2168 chars | - | 2 | Error Data Href | Required | Not Null | Categorical (2 categories) |
| **error_data_is_transient** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Error Data Is Transient | Numeric | None | Enum-like (1 values) |
| **error_data_message** | Text | No | Category | 8.6648 chars | - | 23 | Error Data Message | Required | Not Null | Variable |
| **error_data_meta_api_status** | Text | No | Category | 0.0 chars | - | 1 | Status or state of record | Required | Not Null | Categorical (1 categories) |
| **error_data_meta_version** | Text | No | Category | 0.0 chars | - | 1 | Error Data Meta Version | Required | Not Null | Categorical (1 categories) |
| **error_data_statuscode** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Status or state of record | Numeric | None | Enum-like (1 values) |
| **error_data_title** | Text | No | Title | 5.8893 chars | - | 9 | Error Data Title | Required | Not Null | Categorical (9 categories) |
| **error_data_to** | Text | No | Category | 0.0 chars | - | 1 | Error Data To | Required | Not Null | Categorical (1 categories) |
| **error_data_type** | Text | No | Category | 0.4468 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hdaccountid** | Float | No | - | 1.0 to 28,057.0 | 13,079.5251 | 201 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inboxid** | Float | No | - | 467.0 to 35,153.0 | 27,581.01019999999 | 279 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **message_account_id** | Text | No | Category | 0.1064 chars | - | 8 | Reference to account | Required | Not Null, Foreign Key (likely) | Categorical (8 categories) |
| **message_audio_format** | Text | No | Category | 0.0028 chars | - | 2 | Message Audio Format | Required | Not Null | Categorical (2 categories) |
| **message_audio_id** | Text | No | Category | 0.0031 chars | - | 3 | Reference to message audio | Required | Not Null, Foreign Key (likely) | Categorical (3 categories) |
| **message_audio_mimetype** | Text | No | Category | 0.0044 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **message_audio_sha256** | Text | No | Category | 0.0088 chars | - | 3 | Message Audio Sha256 | Required | Not Null | Categorical (3 categories) |
| **message_audio_signature** | Text | No | Category | 0.0 chars | - | 1 | Message Audio Signature | Required | Not Null | Categorical (1 categories) |
| **message_audio_url** | Text | No | URL | 0.0 chars | - | 1 | URL or web address | Valid URL format; Required | Not Null | Categorical (1 categories) |
| **message_broadcast_id** | Float | Yes | - | 19,712.0 to 20,264.0 (Null: 100.0%) | 20,070.333333333332 | 4 | Reference to message broadcast | Numeric | Foreign Key (likely) | Enum-like (4 values) |
| **message_channel** | Text | No | Source | 0.0 chars | - | 1 | Message Channel | Required | Not Null | Categorical (1 categories) |
| **message_contacts** | Text | No | Category | 0.0 chars | - | 1 | Message Contacts | Required | Not Null | Categorical (1 categories) |
| **message_content** | Text | No | Category | 0.0 chars | - | 1 | Message Content | Required | Not Null | Categorical (1 categories) |
| **message_context** | Text | No | Category | 0.0 chars | - | 1 | Message Context | Required | Not Null | Categorical (1 categories) |
| **message_context_forwarded** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Message Context Forwarded | Numeric | None | Enum-like (1 values) |
| **message_context_frequently_forwarded** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Message Context Frequently Forwarded | Numeric | None | Enum-like (1 values) |
| **message_context_from** | Text | No | Category | 0.0 chars | - | 1 | Message Context From | Required | Not Null | Categorical (1 categories) |
| **message_context_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to message context | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **message_conversational_flow_id** | Float | Yes | - | 8,451.0 to 26,398.0 (Null: 99.2%) | 19,434.0987654321 | 52 | Reference to message conversational flow | Numeric | Foreign Key (likely) | Variable |
| **message_ctwasourceid** | Text | No | Source | 0.0144 chars | - | 9 | Reference to message ctwasource | Required | Not Null, Foreign Key (likely) | Categorical (9 categories) |
| **message_ctwasourcetype** | Text | No | Source | 0.0016 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **message_destination** | Text | No | - | 10.4362 chars | - | 8,659 | Message Destination | Required | Not Null | Variable |
| **message_document_caption** | Text | No | Category | 0.0 chars | - | 1 | Message Document Caption | Required | Not Null | Categorical (1 categories) |
| **message_document_filename** | Text | No | Category | 0.0028 chars | - | 2 | Message Document Filename | Required | Not Null | Categorical (2 categories) |
| **message_document_format** | Text | No | Category | 0.005 chars | - | 3 | Message Document Format | Required | Not Null | Categorical (3 categories) |
| **message_document_id** | Text | No | Category | 0.0016 chars | - | 2 | Reference to message document | Required | Not Null, Foreign Key (likely) | Categorical (2 categories) |
| **message_document_mimetype** | Text | No | Category | 0.0101 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **message_document_sha256** | Text | No | Category | 0.0044 chars | - | 2 | Message Document Sha256 | Required | Not Null | Categorical (2 categories) |
| **message_document_signature** | Text | No | Category | 0.0128 chars | - | 3 | Message Document Signature | Required | Not Null | Categorical (3 categories) |
| **message_document_url** | Text | No | URL | 0.0605 chars | - | 3 | URL or web address | Valid URL format; Required | Not Null | Categorical (3 categories) |
| **message_errors** | Text | No | Category | 0.0745 chars | - | 2 | Message Errors | Required | Not Null | Categorical (2 categories) |
| **message_event** | Text | No | Category | 0.0 chars | - | 1 | Message Event | Required | Not Null | Categorical (1 categories) |
| **message_forwarded** | Text | No | Category | 0.0 chars | - | 1 | Message Forwarded | Required | Not Null | Categorical (1 categories) |
| **message_frequently_forwarded** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Message Frequently Forwarded | Numeric | None | Enum-like (1 values) |
| **message_from** | Text | No | Category | 0.0095 chars | - | 9 | Message From | Required | Not Null | Categorical (9 categories) |
| **message_id** | Text | No | - | 5.7184 chars | - | 777 | Reference to message | Required | Not Null, Foreign Key (likely) | Variable |
| **message_image_caption** | Text | No | Category | 0.0428 chars | - | 7 | Message Image Caption | Required | Not Null | Categorical (7 categories) |
| **message_image_format** | Text | No | Category | 0.0869 chars | - | 4 | Message Image Format | Required | Not Null | Categorical (4 categories) |
| **message_image_id** | Text | No | - | 0.0493 chars | - | 33 | Reference to message image | Required | Not Null, Foreign Key (likely) | Variable |
| **message_image_mimetype** | Text | No | Category | 0.055 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **message_image_sha256** | Text | No | - | 0.1408 chars | - | 33 | Message Image Sha256 | Required | Not Null | Variable |
| **message_image_signature** | Text | No | Category | 0.1472 chars | - | 24 | Message Image Signature | Required | Not Null | Variable |
| **message_image_url** | Text | No | URL | 0.7034 chars | - | 25 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **message_inbox_id** | Float | Yes | - | 467.0 to 35,153.0 (Null: 13.3%) | 27,553.089923910524 | 260 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **message_interaction_buttonreply___ums_bidx** | Float | Yes | - | 0.0 to 2.0 (Null: 98.1%) | 0.49473684210526314 | 4 | Reference to message interaction buttonreply   ums bx | Numeric | Foreign Key (likely) | Enum-like (4 values) |
| **message_interaction_buttonreply_payload** | Text | No | - | 0.7569 chars | - | 86 | Message Interaction Buttonreply Payload | Required | Not Null | Variable |
| **message_interaction_buttonreply_title** | Text | No | Title | 0.366 chars | - | 127 | Message Interaction Buttonreply Title | Required | Not Null | Variable |
| **message_interaction_istemplate** | Integer | Yes | Category | 0.0 to 1.0 | 0.0106 | 2 | Message Interaction Istemplate | Numeric | None | Enum-like (2 values) |
| **message_interaction_listreply___ums_ridx** | Float | Yes | - | 0.0 to 8.0 (Null: 98.3%) | 1.8786127167630058 | 10 | Reference to message interaction listreply   ums rx | Numeric | Foreign Key (likely) | Variable |
| **message_interaction_listreply___ums_sidx** | Float | Yes | - | 0.0 to 0.0 (Null: 98.3%) | 0.0 | 2 | Reference to message interaction listreply   ums sx | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **message_interaction_listreply_description** | Text | No | Description | 0.127 chars | - | 20 | Message Interaction Listreply Description | Required | Not Null | Variable |
| **message_interaction_listreply_payload** | Text | No | Category | 0.0367 chars | - | 12 | Message Interaction Listreply Payload | Required | Not Null | Variable |
| **message_interaction_listreply_title** | Text | No | Title | 0.2767 chars | - | 101 | Message Interaction Listreply Title | Required | Not Null | Variable |
| **message_interaction_nfmreply_body** | Text | No | Category | 0.0 chars | - | 1 | Message Interaction Nfmreply Body | Required | Not Null | Categorical (1 categories) |
| **message_interaction_nfmreply_name** | Text | No | Category | 0.0 chars | - | 1 | Message Interaction Nfmreply Name | Required | Not Null | Categorical (1 categories) |
| **message_interaction_nfmreply_response_json** | Text | No | Category | 0.0 chars | - | 1 | Message Interaction Nfmreply Response Json | Required | Not Null | Categorical (1 categories) |
| **message_interaction_type** | Text | No | Category | 0.4824 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **message_interaction_undefined_payload** | Text | No | Category | 0.0 chars | - | 1 | Message Interaction Undefined Payload | Required | Not Null | Categorical (1 categories) |
| **message_interaction_undefined_title** | Text | No | Title | 0.0 chars | - | 1 | Message Interaction Undefined Title | Required | Not Null | Categorical (1 categories) |
| **message_location** | Text | No | Category | 0.0 chars | - | 1 | Message Location | Required | Not Null | Categorical (1 categories) |
| **message_location_address** | Text | No | Category | 0.0 chars | - | 1 | Message Location Address | Required | Not Null | Categorical (1 categories) |
| **message_location_latitude** | Float | Yes | Latitude | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Location Latitude | Numeric | None | Enum-like (1 values) |
| **message_location_longitude** | Float | Yes | Longitude | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Location Longitude | Numeric | None | Enum-like (1 values) |
| **message_location_name** | Text | No | Category | 0.0 chars | - | 1 | Message Location Name | Required | Not Null | Categorical (1 categories) |
| **message_location_url** | Text | No | URL | 0.0 chars | - | 1 | URL or web address | Valid URL format; Required | Not Null | Categorical (1 categories) |
| **message_messageid** | Text | No | Category | 0.0 chars | - | 1 | Reference to message message | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **message_mobile** | Text | No | Category | 0.0036 chars | - | 4 | Message Mobile | Required | Not Null | Categorical (4 categories) |
| **message_name** | Text | No | - | 0.1633 chars | - | 53 | Message Name | Required | Not Null | Variable |
| **message_node_name** | Text | No | Category | 0.0009 chars | - | 2 | Message Node Name | Required | Not Null | Categorical (2 categories) |
| **message_order_catalogid** | Text | No | Category | 0.0015 chars | - | 2 | Reference to message order catalog | Required | Not Null, Foreign Key (likely) | Categorical (2 categories) |
| **message_order_productitems** | Text | No | Category | 0.0087 chars | - | 2 | Message Order Productitems | Required | Not Null | Categorical (2 categories) |
| **message_order_text** | Text | No | Category | 0.0 chars | - | 1 | Message Order Text | Required | Not Null | Categorical (1 categories) |
| **message_payload_buttons** | Text | No | - | 3.4107 chars | - | 135 | Message Payload Buttons | Required | Not Null | Variable |
| **message_payload_content** | Text | No | - | 15.3338 chars | - | 827 | Message Payload Content | Required | Not Null | Variable |
| **message_payload_content_button_text** | Text | No | Category | 0.2012 chars | - | 7 | Message Payload Content Button Text | Required | Not Null | Categorical (7 categories) |
| **message_payload_content_name** | Text | No | Category | 0.0 chars | - | 1 | Message Payload Content Name | Required | Not Null | Categorical (1 categories) |
| **message_payload_content_parameters_currency** | Text | No | Category | 0.0 chars | - | 1 | Message Payload Content Parameters Currency | Required | Not Null | Categorical (1 categories) |
| **message_payload_content_parameters_order_catalog_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to message payload content parameters order catalog | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **message_payload_content_parameters_order_discount_offset** | Float | Yes | Discount | NULL to NULL (Null: 100.0%) | NULL | 1 | Count of message_payload_content_parameters_order_dis_offset | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_discount_value** | Float | Yes | Discount | NULL to NULL (Null: 100.0%) | NULL | 1 | Count of message_payload_content_parameters_order_dis_value | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_items** | Text | No | Category | 0.0 chars | - | 1 | Message Payload Content Parameters Order Items | Required | Not Null | Categorical (1 categories) |
| **message_payload_content_parameters_order_shipping_offset** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Order Shipping Offset | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_shipping_value** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Order Shipping Value | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_status** | Text | No | Category | 0.0 chars | - | 1 | Status or state of record | Required | Not Null | Categorical (1 categories) |
| **message_payload_content_parameters_order_subtotal_offset** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Order Subtotal Offset | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_subtotal_value** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Order Subtotal Value | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_tax_offset** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Order Tax Offset | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_order_tax_value** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Order Tax Value | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_payment_settings** | Text | No | Category | 0.0 chars | - | 1 | Message Payload Content Parameters Payment Settings | Required | Not Null | Categorical (1 categories) |
| **message_payload_content_parameters_reference_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to message payload content parameters reference | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **message_payload_content_parameters_total_amount_offset** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Total Amount Offset | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_total_amount_value** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Message Payload Content Parameters Total Amount Value | Numeric | None | Enum-like (1 values) |
| **message_payload_content_parameters_type** | Text | No | Category | 0.0 chars | - | 1 | Type or category classification | Required | Not Null | Categorical (1 categories) |
| **message_payload_content_sections** | Text | No | - | 8.4834 chars | - | 116 | Message Payload Content Sections | Required | Not Null | Variable |
| **message_payload_extra_body** | Text | No | - | 6.3582 chars | - | 349 | Message Payload Extra Body | Required | Not Null | Variable |
| **message_payload_extra_buttons** | Text | No | - | 15.0505 chars | - | 1,550 | Message Payload Extra Buttons | Required | Not Null | Variable |
| **message_payload_extra_caption** | Text | No | Category | 0.2431 chars | - | 28 | Message Payload Extra Caption | Required | Not Null | Variable |
| **message_payload_extra_cards** | Text | No | - | 7.2549 chars | - | 44 | Message Payload Extra Cards | Required | Not Null | Variable |
| **message_payload_extra_document_filename** | Text | No | Category | 0.0022 chars | - | 2 | Message Payload Extra Document Filename | Required | Not Null | Categorical (2 categories) |
| **message_payload_extra_filename** | Text | No | Category | 0.0 chars | - | 1 | Message Payload Extra Filename | Required | Not Null | Categorical (1 categories) |
| **message_payload_extra_footer** | Text | No | Category | 0.6437 chars | - | 7 | Message Payload Extra Footer | Required | Not Null | Categorical (7 categories) |
| **message_payload_extra_header** | Text | No | - | 1.2563 chars | - | 106 | Message Payload Extra Header | Required | Not Null | Variable |
| **message_payload_extra_header_type** | Text | No | Category | 0.0564 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **message_payload_extra_media_url** | Text | No | URL | 50.9801 chars | - | 1,655 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **message_payload_extra_metadata_messageid** | Text | No | - | 0.7812 chars | - | 218 | Reference to message payload extra metadata message | Required | Not Null, Foreign Key (likely) | Variable |
| **message_payload_extra_metadata_phone** | Text | No | - | 0.26 chars | - | 218 | Message Payload Extra Metadata Phone | Required | Not Null | Variable |
| **message_payload_extra_metadata_region** | Text | No | Category | 0.0434 chars | - | 3 | Message Payload Extra Metadata Region | Required | Not Null | Categorical (3 categories) |
| **message_payload_extra_preview_url** | Integer | Yes | Category | 0.0 to 1.0 | 0.1069 | 2 | URL or web address | Numeric | None | Enum-like (2 values) |
| **message_payload_extras_buttons** | Text | No | Category | 0.0 chars | - | 1 | Message Payload Extras Buttons | Required | Not Null | Categorical (1 categories) |
| **message_payload_metadata_cvf_form_input** | Integer | Yes | Category | 0.0 to 1.0 | 0.0001 | 2 | Message Payload Metadata Cvf Form Input | Numeric | None | Enum-like (2 values) |
| **message_payload_substitutions** | Text | No | - | 12.6704 chars | - | 2,085 | Message Payload Substitutions | Required | Not Null | Variable |
| **message_payload_template_id** | Float | Yes | - | 1.0 to 7,677.0 (Null: 47.3%) | 1,536.0652627584898 | 1,373 | Reference to message payload template | Numeric | Foreign Key (likely) | Variable |
| **message_payload_type** | Text | No | Category | 5.0737 chars | - | 8 | Type or category classification | Required | Not Null | Categorical (8 categories) |
| **message_reaction** | Text | No | Category | 0.0198 chars | - | 4 | Message Reaction | Required | Not Null | Categorical (4 categories) |
| **message_reaction_emoji** | Text | No | Category | 0.0008 chars | - | 4 | Message Reaction Emoji | Required | Not Null | Categorical (4 categories) |
| **message_reaction_message_id** | Text | No | Category | 0.0186 chars | - | 4 | Reference to message reaction message | Required | Not Null, Foreign Key (likely) | Categorical (4 categories) |
| **message_receivedat** | DateTime | Yes | - | - (Null: 100.0%) | - | 1 | Message Receivedat | Valid ISO 8601 datetime | None | Variable |
| **message_receiver** | Text | No | - | 1.5911 chars | - | 184 | Message Receiver | Required | Not Null | Variable |
| **message_referral_catalog_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to message referral catalog | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **message_referral_product_retailer_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to message referral product retailer | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **message_reply_to** | Text | No | Category | 0.0 chars | - | 1 | Message Reply To | Required | Not Null | Categorical (1 categories) |
| **message_replyid** | Text | No | - | 2.3037 chars | - | 505 | Reference to message reply | Required | Not Null, Foreign Key (likely) | Variable |
| **message_sender** | Text | No | Category | 0.0 chars | - | 1 | Message Sender | Required | Not Null | Categorical (1 categories) |
| **message_sender_name** | Text | No | - | 1.4343 chars | - | 1,262 | Message Sender Name | Required | Not Null | Variable |
| **message_sender_phone** | Text | No | - | 1.5882 chars | - | 1,326 | Message Sender Phone | Required | Not Null | Variable |
| **message_senderid** | Text | No | - | 1.5882 chars | - | 1,326 | Reference to message sender | Required | Not Null, Foreign Key (likely) | Variable |
| **message_sticker_format** | Text | No | Category | 0.0032 chars | - | 3 | Message Sticker Format | Required | Not Null | Categorical (3 categories) |
| **message_sticker_id** | Text | No | Category | 0.0016 chars | - | 2 | Reference to message sticker | Required | Not Null, Foreign Key (likely) | Categorical (2 categories) |
| **message_sticker_mimetype** | Text | No | Category | 0.002 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **message_sticker_sha256** | Text | No | Category | 0.0044 chars | - | 2 | Message Sticker Sha256 | Required | Not Null | Categorical (2 categories) |
| **message_sticker_signature** | Text | No | Category | 0.0064 chars | - | 2 | Message Sticker Signature | Required | Not Null | Categorical (2 categories) |
| **message_sticker_stickeranimated** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Message Sticker Stickeranimated | Numeric | None | Enum-like (1 values) |
| **message_sticker_url** | Text | No | URL | 0.0303 chars | - | 2 | URL or web address | Valid URL format; Required | Not Null | Categorical (2 categories) |
| **message_system** | Text | No | Category | 0.0 chars | - | 1 | Message System | Required | Not Null | Categorical (1 categories) |
| **message_system_body** | Text | No | Category | 0.0 chars | - | 1 | Message System Body | Required | Not Null | Categorical (1 categories) |
| **message_system_type** | Text | No | Category | 0.0 chars | - | 1 | Type or category classification | Required | Not Null | Categorical (1 categories) |
| **message_system_wa_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to message system wa | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **message_template_account_id** | Float | Yes | - | 1.0 to 28,057.0 (Null: 80.6%) | 12,497.032424086465 | 129 | Reference to account | Numeric | Foreign Key (likely) | Variable |
| **message_template_allow_category_change** | Integer | Yes | Category | 0.0 to 1.0 | 0.0008 | 2 | Message Template Allow Category Change | Numeric | None | Enum-like (2 values) |
| **message_template_body** | Text | No | - | 57.7796 chars | - | 613 | Message Template Body | Required | Not Null | Variable |
| **message_template_category** | Text | No | Category | 1.57 chars | - | 5 | Message Template Category | Required | Not Null | Categorical (5 categories) |
| **message_template_complex_template_config_cards** | Text | No | Category | 0.0 chars | - | 1 | Message Template Complex Template Config Cards | Required | Not Null | Categorical (1 categories) |
| **message_template_complex_template_config_type** | Text | No | Category | 0.0 chars | - | 1 | Type or category classification | Required | Not Null | Categorical (1 categories) |
| **message_template_created_at** | Text | No | - | 6.386 chars | - | 650 | Message Template Created At | Required | Not Null | Variable |
| **message_template_created_from_limechat** | Integer | Yes | Category | 0.0 to 1.0 | 0.1514 | 2 | Message Template Created From Limechat | Numeric | None | Enum-like (2 values) |
| **message_template_display_id** | Float | Yes | - | 1.0 to 7,677.0 (Null: 80.6%) | 1,217.1909418425116 | 479 | Reference to message template display | Numeric | Foreign Key (likely) | Variable |
| **message_template_footer** | Text | No | - | 2.4145 chars | - | 65 | Message Template Footer | Required | Not Null | Variable |
| **message_template_header** | Text | No | Category | 0.2958 chars | - | 30 | Message Template Header | Required | Not Null | Variable |
| **message_template_id** | Float | Yes | - | 3,195.0 to 155,409.0 (Null: 80.6%) | 125,369.26505404014 | 650 | Reference to message template | Numeric | Foreign Key (likely) | Variable |
| **message_template_inbox_id** | Float | Yes | - | 585.0 to 35,098.0 (Null: 80.6%) | 26,532.213072568193 | 156 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **message_template_language** | Text | No | Category | 0.6752 chars | - | 8 | Message Template Language | Required | Not Null | Categorical (8 categories) |
| **message_template_media_url** | Text | No | URL | 0.217 chars | - | 2 | URL or web address | Valid URL format; Required | Not Null | Categorical (2 categories) |
| **message_template_namespace** | Text | No | - | 4.7484 chars | - | 96 | Message Template Namespace | Required | Not Null | Variable |
| **message_template_short_code** | Text | No | - | 3.452 chars | - | 594 | Message Template Short Code | Required | Not Null | Variable |
| **message_template_status** | Text | No | Category | 1.5526 chars | - | 5 | Status or state of record | Required | Not Null | Categorical (5 categories) |
| **message_template_template_buttons** | Text | No | - | 25.4151 chars | - | 420 | Message Template Template Buttons | Required | Not Null | Variable |
| **message_template_template_code** | Text | No | - | 5.0985 chars | - | 320 | Message Template Template Code | Required | Not Null | Variable |
| **message_template_template_type** | Float | Yes | - | 0.0 to 3.0 (Null: 80.6%) | 0.6562017498713331 | 5 | Type or category classification | Numeric | None | Enum-like (5 values) |
| **message_template_updated_at** | Text | No | - | 6.3901 chars | - | 1,045 | Message Template Updated At | Required | Not Null | Variable |
| **message_templateid** | Text | No | Category | 0.0 chars | - | 1 | Reference to message template | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **message_templatetype** | Text | No | Category | 0.0 chars | - | 1 | Type or category classification | Required | Not Null | Categorical (1 categories) |
| **message_text** | Text | No | - | 2.6175 chars | - | 652 | Message Text | Required | Not Null | Variable |
| **message_timestamp** | Text | No | Category | 0.0119 chars | - | 12 | Message Timestamp | Required | Not Null | Variable |
| **message_type** | Text | No | Category | 0.8732 chars | - | 11 | Type or category classification | Required | Not Null | Variable |
| **message_unsupported** | Text | No | Category | 0.0745 chars | - | 2 | Message Unsupported | Required | Not Null | Categorical (2 categories) |
| **message_video_caption** | Text | No | Category | 0.0 chars | - | 1 | Reference to message veo caption | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **message_video_format** | Text | No | Category | 0.0028 chars | - | 2 | Reference to message veo format | Required | Not Null, Foreign Key (likely) | Categorical (2 categories) |
| **message_video_id** | Text | No | Category | 0.0031 chars | - | 3 | Reference to message veo | Required | Not Null, Foreign Key (likely) | Categorical (3 categories) |
| **message_video_mimetype** | Text | No | Category | 0.0018 chars | - | 2 | Type or category classification | Required | Not Null, Foreign Key (likely) | Categorical (2 categories) |
| **message_video_sha256** | Text | No | Category | 0.0088 chars | - | 3 | Reference to message veo sha256 | Required | Not Null, Foreign Key (likely) | Categorical (3 categories) |
| **message_video_signature** | Text | No | Category | 0.0 chars | - | 1 | Reference to message veo signature | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **message_video_url** | Text | No | URL | 0.0 chars | - | 1 | URL or web address | Valid URL format; Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **message_wamsgid** | Text | No | Category | 0.0 chars | - | 1 | Reference to message wamsg | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **message_wanumber** | Text | No | Category | 0.0036 chars | - | 4 | Message Wanumber | Required | Not Null | Categorical (4 categories) |
| **response_bulkid** | Text | No | Category | 0.0076 chars | - | 5 | Reference to response bulk | Required | Not Null, Foreign Key (likely) | Categorical (5 categories) |
| **response_contacts** | Text | No | - | 21.8795 chars | - | 4,458 | Response Contacts | Required | Not Null | Variable |
| **response_details** | Text | No | Category | 0.0 chars | - | 1 | Response Details | Required | Not Null | Categorical (1 categories) |
| **response_errors** | Text | No | Category | 0.0 chars | - | 1 | Response Errors | Required | Not Null | Categorical (1 categories) |
| **response_id** | Text | No | - | 7.8091 chars | - | 2,066 | Reference to response | Required | Not Null, Foreign Key (likely) | Variable |
| **response_messages** | Text | No | - | 41.6236 chars | - | 4,463 | Response Messages | Required | Not Null | Variable |
| **response_messaging_product** | Text | No | Category | 3.5664 chars | - | 2 | Response Messaging Product | Required | Not Null | Categorical (2 categories) |
| **response_mid** | Text | No | Category | 0.1086 chars | - | 29 | Reference to response m | Required | Not Null, Foreign Key (likely) | Variable |
| **response_phone** | Text | No | - | 2.4771 chars | - | 2,062 | Response Phone | Required | Not Null | Variable |
| **response_status** | Text | No | Category | 1.4455 chars | - | 2 | Status or state of record | Required | Not Null | Categorical (2 categories) |
| **response_title** | Text | No | Title | 0.0 chars | - | 1 | Response Title | Required | Not Null | Categorical (1 categories) |
| **response_to** | Text | No | Category | 0.0336 chars | - | 29 | Response To | Required | Not Null | Variable |
| **retriesattempted** | Float | Yes | - | 0.0 to 5.0 (Null: 15.2%) | 0.040580394007313905 | 7 | Retriesattempted | Numeric | None | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Text | No | Category | 6.3286 chars | - | 10 | Status or state of record | Required | Not Null | Categorical (10 categories) |
| **uniqueid** | Text | No | - | 21.0 chars | - | 9,998 | Reference to unique | Required | Not Null, Foreign Key (likely) | Variable |
| **updatedat** | Text | No | - | 32.8844 chars | - | 10,001 | Timestamp when record was last updated | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>12. pg_hd_message_analytics</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Analytics and metrics table for reporting purposes.

**Owner/Maintainer:** Conversations Team

**Tags:** `analytics`, `messaging`, `reporting`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 979

### account_id` → `postgres_accounts.id` (inferred)
- `content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 263.4057 chars
- **Distinct Values:** 1,905

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,137

### eventn_ctx_event_id` → Related table (inferred)
- `is_replied

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.2134
- **Distinct Values:** 2

### is_template

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### message_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `pg_hd_message_analytics`
- **Total Columns:** 15

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 979 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,510.0 | 1,285.5092 | 89 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **content** | Text | No | - | 263.4057 chars | - | 1,905 | Content | Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 8,472,691.0 to 97,616,194.0 | 91,207,940.71720003 | 9,980 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 2,137 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **is_read** | Integer | No | Category | 0.0 to 1.0 | 0.4462 | 2 | Is Read | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_replied** | Integer | No | Category | 0.0 to 1.0 | 0.2134 | 2 | Is Replied | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_template** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Is Template | Numeric; Required | Not Null | Enum-like (1 values) |
| **message_id** | Float | No | - | 426,474,586.0 to 705,202,540.0 | 663,138,806.8788992 | 9,999 | Reference to message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **read_at** | DateTime | Yes | - | - (Null: 55.4%) | - | 3,680 | Read At | Valid ISO 8601 datetime | None | Variable |
| **reply_content** | Text | No | - | 14.6483 chars | - | 1,262 | Reply Content | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 5,360 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>13. postgres2_agent_bots</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores bot configuration and interaction data.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 46

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 437

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.034334763948497854 chars
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_agent_bots`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 46 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 437 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **description** | Text | No | Description | 0.034334763948497854 chars | - | 2 | Description | Required | Not Null | Categorical (2 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 466 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hide_input_for_bot_conversations** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Reference to he input for bot conversations | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **name** | Text | No | Name | 11.141630901287554 chars | - | 436 | Human-readable name or title | Required | Not Null | Variable |
| **outgoing_url** | Text | No | URL | 57.94849785407725 chars | - | 433 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 466 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>14. postgres2_bot_analytics</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Analytics and metrics table for reporting purposes.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `analytics`, `reporting`, `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 148

### account_id` → `postgres_accounts.id` (inferred)
- `channel

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 11.8384 chars
- **Distinct Values:** 8

### conv_id` → Related table (inferred)
- `conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 3,484

### date

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 10.0 chars
- **Distinct Values:** 1

### distinct_id` → Related table (inferred)
- `event_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.4317 chars
- **Distinct Values:** 411

### event_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 1.7003
- **Distinct Values:** 4

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_bot_analytics`
- **Total Columns:** 21

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **_timestamp** | DateTime | No | - | - | - | 148 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 39.0 to 27,138.0 | 7,756.4852 | 86 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **channel** | Text | No | Source | 11.8384 chars | - | 8 | Channel | Required | Not Null | Categorical (8 categories) |
| **conv_id** | Float | No | - | 0.0 to 12,019,890.0 | 1,981,444.4242 | 1,496 | Reference to conv | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conversation_id** | Float | No | - | 0.0 to 81,284,613.0 | 71,851,185.57960013 | 1,496 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 3,484 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **date** | Text | No | Category | 10.0 chars | - | 1 | Date | Required | Not Null | Categorical (1 categories) |
| **distinct_id** | Text | No | - | 11.4244 chars | - | 9,312 | Reference to distinct | Required | Not Null, Foreign Key (likely) | Variable |
| **event_id** | Float | No | - | 1,057,099,562.0 to 1,057,154,132.0 | 1,057,126,400.3716 | 9,999 | Reference to event | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **event_name** | Text | No | - | 19.4317 chars | - | 411 | Event Name | Required | Not Null | Variable |
| **event_type** | Float | No | - | 0.0 to 3.0 | 1.7003 | 4 | Type or category classification | Numeric; Required | Not Null | Enum-like (4 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_id** | Float | No | - | 0.0 to 33,800.0 | 13,594.429800000004 | 106 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inserted_at** | DateTime | No | - | - | - | 178 | Inserted At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **is_outbound** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Is Outbound | Numeric; Required | Not Null | Enum-like (1 values) |
| **is_outside_working_hours** | Integer | No | Category | 0.0 to 1.0 | 0.3271 | 2 | Reference to is outse working hours | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **products** | Text | No | SerializedJSON | 4.0542 chars | - | 175 | Products | Required | Not Null | Variable |
| **properties** | Text | No | SerializedJSON | 1,157.8719 chars | - | 9,883 | Properties | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **text** | Text | No | - | 57.6087 chars | - | 2,549 | Text | Required | Not Null | Variable |
| **timestamp** | Float | No | - | 1,704,067,200.0 to 1,704,077,570.0 | 1,704,073,386.448 | 82 | Timestamp | Numeric; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>15. postgres2_bot_analytics_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres2_bot_analytics. Contains unprocessed data before transformation.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `analytics`, `reporting`, `bot`, `raw-data`, `ai`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4

### account_id` → `postgres_accounts.id` (inferred)
- `channel

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 13.6257 chars
- **Distinct Values:** 8

### conv_id` → Related table (inferred)
- `conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 3,484

### date

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 10.0 chars
- **Distinct Values:** 1

### distinct_id` → Related table (inferred)
- `event_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.9515 chars
- **Distinct Values:** 478

### event_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 1.7003
- **Distinct Values:** 4

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_bot_analytics_raw`
- **Total Columns:** 21

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **_timestamp** | DateTime | No | - | - | - | 4 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 39.0 to 27,138.0 | 7,756.4852 | 86 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **channel** | Text | No | Source | 13.6257 chars | - | 8 | Channel | Required | Not Null | Categorical (8 categories) |
| **conv_id** | Float | No | - | 0.0 to 12,019,890.0 | 1,981,444.4242 | 1,496 | Reference to conv | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conversation_id** | Float | No | - | 0.0 to 81,284,613.0 | 71,851,185.57960013 | 1,496 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 3,484 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **date** | Text | No | Category | 10.0 chars | - | 1 | Date | Required | Not Null | Categorical (1 categories) |
| **distinct_id** | Text | No | - | 17.809 chars | - | 1,485 | Reference to distinct | Required | Not Null, Foreign Key (likely) | Variable |
| **event_id** | Float | No | - | 1,057,099,562.0 to 1,057,154,132.0 | 1,057,126,400.3716 | 9,999 | Reference to event | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **event_name** | Text | No | - | 19.9515 chars | - | 478 | Event Name | Required | Not Null | Variable |
| **event_type** | Float | No | - | 0.0 to 3.0 | 1.7003 | 4 | Type or category classification | Numeric; Required | Not Null | Enum-like (4 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_id** | Float | No | - | 0.0 to 33,800.0 | 13,594.429800000004 | 106 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inserted_at** | DateTime | No | - | - | - | 4 | Inserted At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **is_outbound** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Is Outbound | Numeric; Required | Not Null | Enum-like (1 values) |
| **is_outside_working_hours** | Integer | No | Category | 0.0 to 1.0 | 0.5189 | 2 | Reference to is outse working hours | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **products** | Text | No | SerializedJSON | 3.289 chars | - | 134 | Products | Required | Not Null | Variable |
| **properties** | Text | No | SerializedJSON | 1,130.5868 chars | - | 9,856 | Properties | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **text** | Text | No | - | 52.3779 chars | - | 1,899 | Text | Required | Not Null | Variable |
| **timestamp** | Float | No | - | 1,704,067,200.0 to 1,704,077,570.0 | 1,704,073,386.448 | 82 | Timestamp | Numeric; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>16. postgres2_bot_failing_data</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores bot configuration and interaction data.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 471

### account_id` → `postgres_accounts.id` (inferred)
- `bot_confidence

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.11616397 to 1.0
- **Average:** 0.684902463909
- **Distinct Values:** 5,484

### conv_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,997

### event_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_bot_failing_data`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **_timestamp** | DateTime | No | - | - | - | 471 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 28.0 to 27,070.0 | 2,527.7313 | 181 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **bot_confidence** | Float | Yes | - | 0.11616397 to 1.0 | 0.684902463909 | 5,484 | Reference to bot confence | Numeric | Foreign Key (likely) | Variable |
| **conv_id** | Float | No | - | 275.0 to 12,046,151.0 | 1,145,416.8120000002 | 9,956 | Reference to conv | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,997 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **event_id** | Float | No | - | 93,121,438.0 to 1,090,696,562.0 | 527,041,551.0869 | 10,000 | Reference to event | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,998 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_id** | Float | No | - | 0.0 to 33,818.0 | 4,998.432200000001 | 269 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inserted_at** | DateTime | No | - | - | - | 1 | Inserted At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **intent** | Text | No | - | 20.986 chars | - | 239 | Intent | Required | Not Null | Variable |
| **is_outside_working_hours** | Integer | No | Category | 0.0 to 1.0 | 0.2289 | 2 | Reference to is outse working hours | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **reason** | Text | No | Category | 12.582 chars | - | 2 | Reason | Required | Not Null | Categorical (2 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **text** | Text | No | - | 28.1732 chars | - | 5,571 | Text | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>17. postgres2_company_data</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres2 company data operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 20

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_company_data`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **_timestamp** | DateTime | No | - | - | - | 20 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 3.0 to 27,649.0 | 13,333.095348837209 | 430 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **auth_token** | Text | No | - | 29.967441860465115 chars | - | 430 | Authentication or access token | Required | Not Null | Variable |
| **company_name** | Text | No | Company | 12.26046511627907 chars | - | 428 | Company Name | Required | Not Null | Variable |
| **company_sheet** | Text | No | Company | 70.46976744186047 chars | - | 360 | Company Sheet | Required | Not Null | Variable |
| **convenient_name** | Text | No | - | 11.158139534883722 chars | - | 428 | Convenient Name | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 430 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **refresh_token** | Text | No | - | 29.790697674418606 chars | - | 428 | Authentication or access token | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>18. postgres2_csat_survey_responses</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Customer Satisfaction (CSAT) survey data.

**Owner/Maintainer:** Platform Team

**Tags:** `feedback`, `csat`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 289

### account_id` → `postgres_accounts.id` (inferred)
- `assigned_agent_id` → Related table (inferred)
- `contact_id` → Related table (inferred)
- `conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,995

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_csat_survey_responses`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 289 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,219.0 | 6,061.3139 | 79 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **assigned_agent_id** | Float | Yes | - | 219.0 to 50,949.0 (Null: 25.7%) | 36,353.54660390045 | 410 | Reference to assigned agent | Numeric | Foreign Key (likely) | Variable |
| **contact_id** | Float | No | - | 4,950.0 to 87,329,912.0 | 73,790,359.94189997 | 9,911 | Reference to contact | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conversation_id** | Float | No | - | 10,013,014.0 to 89,134,423.0 | 76,479,264.7855 | 9,999 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,995 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **feedback_message** | Text | No | - | 21.5945 chars | - | 4,118 | Feedback Message | Required | Not Null | Variable |
| **message_id** | Float | No | - | 467,596,542.0 to 639,049,546.0 | 549,459,678.8599001 | 9,999 | Reference to message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **rating** | Float | No | Score | 1.0 to 5.0 | 3.5854 | 5 | Rating | Numeric; Required | Not Null | Enum-like (5 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,993 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>19. postgres2_draftimprover</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres2 draftimprover operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 248

### account_id` → `postgres_accounts.id` (inferred)
- `agent_id` → Related table (inferred)
- `completion_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 345.0
- **Average:** 20.640700000000002
- **Distinct Values:** 119

### conversation_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_draftimprover`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 248 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 39.0 to 27,678.0 | 4,261.1514 | 49 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **agent_id** | Float | No | - | -1.0 to 51,847.0 | 42,325.58470000001 | 156 | Reference to agent | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **completion_tokens** | Float | No | - | 1.0 to 345.0 | 20.640700000000002 | 119 | Authentication or access token | Numeric; Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 9,657,924.0 to 103,665,290.0 | 101,723,910.61470002 | 4,075 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **latency** | Float | No | - | 0.22318400093354285 to 11.49059069599025 | 0.7803427391986686 | 10,001 | Latency | Numeric; Required | Not Null | Variable |
| **prompt_tokens** | Float | No | - | 119.0 to 395.0 | 139.8091 | 115 | Authentication or access token | Numeric; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **timestamp** | DateTime | No | - | - | - | 9,575 | Timestamp | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **total_cost** | Float | No | Cost | 0.00036799999999999995 to 0.002565 | 0.0005019901000000002 | 822 | Total Cost | Numeric; Required | Not Null | Variable |
| **total_tokens** | Float | No | - | 122.0 to 740.0 | 160.4498 | 201 | Authentication or access token | Numeric; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>20. postgres2_gpt_langgraph_qna</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres2 gpt langgraph qna operations.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,190

### answer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 352.1369 chars
- **Distinct Values:** 8,264

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,416

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gpt_langgraph_qna`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 3,190 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **answer** | Text | No | - | 352.1369 chars | - | 8,264 | Answer | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,416 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **metadata_id** | Float | No | - | 1,998,912.0 to 3,438,930.0 | 2,884,548.1365 | 9,998 | Reference to metadata | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **question** | Text | No | - | 61.7875 chars | - | 7,409 | Question | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>21. postgres2_gpt_langgraph_qna_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres2_gpt_langgraph_qna. Contains unprocessed data before transformation.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,190

### answer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 352.1369 chars
- **Distinct Values:** 8,264

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,416

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gpt_langgraph_qna_raw`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 3,190 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **answer** | Text | No | - | 352.1369 chars | - | 8,264 | Answer | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,416 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **metadata_id** | Float | No | - | 1,998,912.0 to 3,438,930.0 | 2,884,548.1365 | 9,998 | Reference to metadata | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **question** | Text | No | - | 61.7875 chars | - | 7,409 | Question | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>22. postgres2_gptanswer</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres2 gptanswer operations.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,673

### answer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 280.2102 chars
- **Distinct Values:** 9,479

### context_added_question

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 42.1956 chars
- **Distinct Values:** 9,032

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,891

### eventn_ctx_event_id` → Related table (inferred)
- `metadata_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptanswer`
- **Total Columns:** 12

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 2,673 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **answer** | Text | No | - | 280.2102 chars | - | 9,479 | Answer | Required | Not Null | Variable |
| **context_added_question** | Text | No | - | 42.1956 chars | - | 9,032 | Context Added Question | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,891 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,998 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **is_cached** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Is Cached | Numeric; Required | Not Null | Enum-like (1 values) |
| **metadata_id** | Float | No | FK | 35.0 to 668,930.0 | 608,975.6991 | 10,000 | Reference to metadata | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **question** | Text | No | - | 31.4865 chars | - | 8,807 | Question | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **translated_question** | Text | No | - | 32.8276 chars | - | 8,639 | Translated Question | Required | Not Null | Variable |
| **whatsapp_answer** | Text | No | - | 299.093 chars | - | 9,774 | Whatsapp Answer | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>23. postgres2_gptanswer_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres2_gptanswer. Contains unprocessed data before transformation.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### answer

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 232.4914 chars
- **Distinct Values:** 7,374

### context_added_question

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 42.862 chars
- **Distinct Values:** 8,336

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,940

### eventn_ctx_event_id` → Related table (inferred)
- `metadata_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptanswer_raw`
- **Total Columns:** 12

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **answer** | Text | No | - | 232.4914 chars | - | 7,374 | Answer | Required | Not Null | Variable |
| **context_added_question** | Text | No | - | 42.862 chars | - | 8,336 | Context Added Question | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,940 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,998 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **is_cached** | Integer | No | Category | 0.0 to 1.0 | 0.1362 | 2 | Is Cached | Numeric; Required | Not Null | Enum-like (2 values) |
| **metadata_id** | Float | No | - | 35.0 to 45,063.0 | 24,719.9897 | 9,999 | Reference to metadata | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **question** | Text | No | - | 29.6826 chars | - | 8,159 | Question | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **translated_question** | Text | No | - | 30.6337 chars | - | 8,061 | Translated Question | Required | Not Null | Variable |
| **whatsapp_answer** | Text | No | - | 262.486 chars | - | 6,747 | Whatsapp Answer | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>24. postgres2_gptbotcost</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores bot configuration and interaction data.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 5

### completion_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 574.0
- **Average:** 11.926400000000005
- **Distinct Values:** 168

### cost

- **Type:** `Float`
- **Semantic Type:** `Cost`
- **Nullable:** No
- **Range:** 0.0 to 0.05041551
- **Average:** 0.00213348214
- **Distinct Values:** 2,195

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,782

### embedding_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 57.0
- **Average:** 0.8595
- **Distinct Values:** 45

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptbotcost`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 5 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **completion_tokens** | Float | No | - | 0.0 to 574.0 | 11.926400000000005 | 168 | Authentication or access token | Numeric; Required | Not Null | Variable |
| **cost** | Float | No | Cost | 0.0 to 0.05041551 | 0.00213348214 | 2,195 | Cost | Numeric; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 8,782 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **embedding_tokens** | Float | No | - | 0.0 to 57.0 | 0.8595 | 45 | Authentication or access token | Numeric; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **metadata_id** | Float | No | FK | 1.0 to 123,504.0 | 24,476.7117 | 5,998 | Reference to metadata | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **process** | Text | No | Category | 10.1578 chars | - | 7 | Process | Required | Not Null | Categorical (7 categories) |
| **prompt_tokens** | Float | No | - | 0.0 to 13,864.0 | 398.7646 | 789 | Authentication or access token | Numeric; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **tavily_calls** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Tavily Calls | Numeric | None | Enum-like (1 values) |
| **total_chars** | Float | Yes | - | 0.0 to 2,517.0 | 52.4794 | 271 | Total Chars | Numeric | None | Variable |
| **total_tokens** | Float | No | - | 0.0 to 13,913.0 | 410.691 | 871 | Authentication or access token | Numeric; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>25. postgres2_gptbotcost_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres2_gptbotcost. Contains unprocessed data before transformation.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `raw-data`, `staging`, `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### completion_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 273.0
- **Average:** 11.894800000000002
- **Distinct Values:** 155

### cost

- **Type:** `Float`
- **Semantic Type:** `Cost`
- **Nullable:** No
- **Range:** 0.0 to 0.041792300000000004
- **Average:** 0.002125577275999998
- **Distinct Values:** 2,014

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,875

### embedding_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 57.0
- **Average:** 0.9183
- **Distinct Values:** 45

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptbotcost_raw`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **completion_tokens** | Float | No | - | 0.0 to 273.0 | 11.894800000000002 | 155 | Authentication or access token | Numeric; Required | Not Null | Variable |
| **cost** | Float | No | Cost | 0.0 to 0.041792300000000004 | 0.002125577275999998 | 2,014 | Cost | Numeric; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 8,875 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **embedding_tokens** | Float | No | - | 0.0 to 57.0 | 0.9183 | 45 | Authentication or access token | Numeric; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **metadata_id** | Float | No | - | 1.0 to 6,686.0 | 3,354.2251 | 5,948 | Reference to metadata | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **process** | Text | No | Category | 10.213 chars | - | 7 | Process | Required | Not Null | Categorical (7 categories) |
| **prompt_tokens** | Float | No | - | 0.0 to 13,893.0 | 412.1227 | 784 | Authentication or access token | Numeric; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **tavily_calls** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Tavily Calls | Numeric | None | Enum-like (1 values) |
| **total_chars** | Float | Yes | - | 0.0 to 1,590.0 | 49.9932 | 213 | Total Chars | Numeric | None | Variable |
| **total_tokens** | Float | No | - | 0.0 to 13,921.0 | 424.0175 | 864 | Authentication or access token | Numeric; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>26. postgres2_gptbotlatency</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores bot configuration and interaction data.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,317

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptbotlatency`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 4 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 7,317 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,997 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **metadata_id** | Float | No | FK | 106,710.0 to 233,783.0 | 131,569.2946 | 6,342 | Reference to metadata | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **process** | Text | No | Category | 11.6455 chars | - | 7 | Process | Required | Not Null | Categorical (7 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **time_taken** | Float | No | - | 0.3415517807006836 to 612.9374957671389 | 3.4933474602692884 | 9,995 | Time Taken | Numeric; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>27. postgres2_gptintentredirection</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres2 gptintentredirection operations.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 640

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,992

### eventn_ctx_event_id` → Related table (inferred)
- `metadata_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptintentredirection`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 640 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,992 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **gpt_intent** | Text | No | - | 16.4308 chars | - | 3,656 | Gpt Intent | Required | Not Null | Variable |
| **gpt_score** | Float | No | Score | 7.0 to 100.0 | 67.13065 | 18 | Gpt Score | Numeric; Required | Not Null | Variable |
| **metadata_id** | Float | No | FK | 2,704.0 to 668,905.0 | 172,875.4579 | 10,000 | Reference to metadata | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **rasa_intents** | Text | No | SerializedJSON | 417.5318 chars | - | 9,411 | Rasa Intents | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **top_rasa_intent** | Text | No | - | 15.1084 chars | - | 190 | Top Rasa Intent | Required | Not Null | Variable |
| **top_rasa_intent_score** | Float | No | Score | 0.0 to 0.5574802160263062 | 0.2956081643219292 | 9,405 | Top Rasa Intent Score | Numeric; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>28. postgres2_gptmetadata</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres2 gptmetadata operations.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 572

### account_id` → `postgres_accounts.id` (inferred)
- `conversation_id` → Related table (inferred)
- `conversation_uuid` → Related table (inferred)
- `message_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptmetadata`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 572 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | -1.0 to 39.0 | 38.978 | 3 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (3 values) |
| **conversation_id** | Float | No | - | -1.0 to 100,452,530.0 | 91,859,275.6245 | 8,207 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conversation_uuid** | Text | No | - | 35.9892 chars | - | 8,207 | Reference to conversation uu | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,979 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_id** | Float | No | - | -1.0 to 33,901.0 | 933.1791 | 4 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (4 values) |
| **message_id** | Float | No | - | -1.0 to 726,903,022.0 | 668,755,438.5564 | 8,955 | Reference to message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>29. postgres2_gptmetadata_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres2_gptmetadata. Contains unprocessed data before transformation.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2

### account_id` → `postgres_accounts.id` (inferred)
- `conversation_id` → Related table (inferred)
- `conversation_uuid` → Related table (inferred)
- `message_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gptmetadata_raw`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 2 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | -1.0 to 11,225.0 | 1,711.163 | 15 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conversation_id** | Float | No | - | -1.0 to 71,526,145.0 | 69,013,315.46449988 | 4,258 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conversation_uuid** | Text | No | - | 35.9604 chars | - | 4,257 | Reference to conversation uu | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,583 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_id** | Float | No | - | -1.0 to 33,467.0 | 7,997.3242 | 32 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **message_id** | Float | No | - | -1.0 to 498,599,883.0 | 495,993,506.7446 | 5,840 | Reference to message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>30. postgres2_gpttranslation</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Service Level Agreement tracking and metrics.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `sla`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,879

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_gpttranslation`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,879 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **metadata_id** | Float | No | FK | 480,534.0 to 494,948.0 | 487,766.1308 | 9,999 | Reference to metadata | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **source_text** | Text | No | Source | 36.8805 chars | - | 9,161 | Source Text | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **translated_text** | Text | No | - | 38.1538 chars | - | 8,674 | Translated Text | Required | Not Null | Variable |
| **translation_type** | Text | No | Category | 14.9839 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |

</details>

---

<details>
<summary><h2>31. postgres2_ndr</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres2 ndr operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,539

### account_id` → `postgres_accounts.id` (inferred)
- `awb

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 14.049645390070921 chars
- **Distinct Values:** 4,703

### conv_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,773

### eventn_ctx_event_id` → Related table (inferred)
- `template_message_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_ndr`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **_timestamp** | DateTime | No | - | - | - | 4,539 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 27,932.0 to 27,932.0 | 27,932.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **awb** | Text | No | - | 14.049645390070921 chars | - | 4,703 | Awb | Required | Not Null | Variable |
| **conv_id** | Float | No | - | 18.0 to 14,717.0 | 7,479.528109323646 | 5,509 | Reference to conv | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 5,773 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 5,779 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **modified_values** | Text | No | - | 53.16398546964193 chars | - | 520 | Modified Values | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **template_display_id** | Float | No | - | 1.0 to 8.0 | 3.392146687424321 | 6 | Reference to template display | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **template_message_id** | Float | No | - | 0.0 to 1,009,948,724.0 | 960,145,495.0280229 | 5,781 | Reference to template message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 5,776 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_entered_values** | Text | No | SerializedJSON | 37.151184916104484 chars | - | 1,109 | User Entered Values | Required | Not Null | Variable |
| **wa_phone_no** | Text | No | - | 9.998270195467912 chars | - | 4,457 | Wa Phone No | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>32. postgres2_ndr_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres2_ndr. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,544

### account_id` → `postgres_accounts.id` (inferred)
- `awb

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 14.04817820756346 chars
- **Distinct Values:** 4,703

### conv_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,773

### eventn_ctx_event_id` → Related table (inferred)
- `template_message_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_ndr_raw`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **_timestamp** | DateTime | No | - | - | - | 4,544 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 27,932.0 to 27,932.0 | 27,932.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **awb** | Text | No | - | 14.04817820756346 chars | - | 4,703 | Awb | Required | Not Null | Variable |
| **conv_id** | Float | No | - | 18.0 to 14,717.0 | 7,471.0485235710585 | 5,509 | Reference to conv | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 5,773 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 5,779 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **modified_values** | Text | No | - | 53.63581419443965 chars | - | 521 | Modified Values | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **template_display_id** | Float | No | - | 1.0 to 8.0 | 3.3919875669141772 | 6 | Reference to template display | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **template_message_id** | Float | No | - | 0.0 to 1,009,948,724.0 | 959,609,808.2085996 | 5,781 | Reference to template message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 5,786 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_entered_values** | Text | No | SerializedJSON | 37.59419789328268 chars | - | 1,111 | User Entered Values | Required | Not Null | Variable |
| **wa_phone_no** | Text | No | - | 9.998273182524606 chars | - | 4,457 | Wa Phone No | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>33. postgres2_outbound_feedbacks</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres2 outbound feedbacks operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 141

### account_id` → `postgres_accounts.id` (inferred)
- `conv_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_outbound_feedbacks`
- **Total Columns:** 12

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 141 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 51.0 to 27,138.0 | 4,824.2162 | 50 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conv_id** | Text | No | - | 6.0669 chars | - | 9,845 | Reference to conv | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,975 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **feedback** | Text | No | Category | 8.1752 chars | - | 6 | Feedback | Required | Not Null | Categorical (6 categories) |
| **flow_id** | Float | Yes | - | 0.0 to 30,219.0 | 11,281.7534 | 65 | Reference to flow | Numeric | Foreign Key (likely) | Variable |
| **followup_feedback** | Text | No | Category | 3.6241 chars | - | 10 | Followup Feedback | Required | Not Null | Categorical (10 categories) |
| **order_id** | Text | No | Category | 0.0125 chars | - | 13 | Reference to order | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,966 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>34. postgres2_outbound_feedbacks_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres2_outbound_feedbacks. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 16

### account_id` → `postgres_accounts.id` (inferred)
- `conv_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_outbound_feedbacks_raw`
- **Total Columns:** 12

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 16 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 31.0 | 30.994 | 2 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **conv_id** | Text | No | - | 5.7338 chars | - | 9,640 | Reference to conv | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,879 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **feedback** | Text | No | Category | 8.0828 chars | - | 3 | Feedback | Required | Not Null | Categorical (3 categories) |
| **flow_id** | Float | Yes | - | 0.0 to 30,249.0 (Null: 37.9%) | 933.7679433537174 | 4 | Reference to flow | Numeric | Foreign Key (likely) | Enum-like (4 values) |
| **followup_feedback** | Text | No | Category | 5.8309 chars | - | 7 | Followup Feedback | Required | Not Null | Categorical (7 categories) |
| **order_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to order | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,822 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>35. postgres2_sentimentemotionanalyzer</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres2 sentimentemotionanalyzer operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 29

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_sentimentemotionanalyzer`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 4 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Text | No | Category | 2.0 chars | - | 3 | Reference to account | Required | Not Null, Foreign Key (likely) | Categorical (3 categories) |
| **conv_id** | Text | No | Category | 3.9310344827586206 chars | - | 15 | Reference to conv | Required | Not Null, Foreign Key (likely) | Variable |
| **cost** | Float | No | Cost | 0.0027745 to 0.0034244999999999996 | 0.0030984827586206898 | 29 | Cost | Numeric; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 29 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 29 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **latency** | Float | No | - | 1.287287 to 3.034108 | 2.025382896551724 | 29 | Latency | Numeric; Required | Not Null | Variable |
| **output** | Text | No | Category | 520.4827586206897 chars | - | 29 | Output | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>36. postgres2_summarizer</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres2 summarizer operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 291

### account_id` → `postgres_accounts.id` (inferred)
- `completion_tokens

- **Type:** `Float`
- **Nullable:** No
- **Range:** 15.0 to 535.0
- **Average:** 59.52179999999999
- **Distinct Values:** 227

### conversation_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres2_summarizer`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 291 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 56.0 | 52.0258 | 4 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (4 values) |
| **completion_tokens** | Float | No | - | 15.0 to 535.0 | 59.52179999999999 | 227 | Authentication or access token | Numeric; Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 62,663,528.0 to 103,639,476.0 | 101,444,378.98619999 | 9,696 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **latency** | Float | No | - | 0.3149709808640182 to 779.8253362600226 | 1.2955289934036158 | 9,997 | Latency | Numeric; Required | Not Null | Variable |
| **number_of_messages** | Float | No | - | 0.0 to 408.0 | 16.9792 | 110 | Number Of Messages | Numeric; Required | Not Null | Variable |
| **prompt_tokens** | Float | No | - | 161.0 to 6,743.0 | 626.4462000000002 | 1,255 | Authentication or access token | Numeric; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **timestamp** | DateTime | No | - | - | - | 9,777 | Timestamp | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **total_cost** | Float | No | Cost | 0.000555 to 0.020341 | 0.0021174258000000025 | 3,982 | Total Cost | Numeric; Required | Not Null | Variable |
| **total_tokens** | Float | No | - | 179.0 to 6,771.0 | 685.968 | 1,329 | Authentication or access token | Numeric; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>37. postgres_account_users</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages account information and configurations.

**Owner/Maintainer:** Accounts/Billing Team

**Tags:** `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,298

### account_id` → `postgres_accounts.id` (inferred)
- `automation_access

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.5935346447813558
- **Distinct Values:** 2

### billable

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.9466634776369289
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,800

### crm_access

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.9142964540784363
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)
- `marketing_access

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.5957900012529758
- **Distinct Values:** 2

### role

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 2.0
- **Average:** 0.6943991980954768
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,598

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_account_users`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1,298 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 28,452.0 | 17,273.2150106503 | 1,631 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **automation_access** | Integer | Yes | Category | 0.0 to 1.0 | 0.5935346447813558 | 2 | Automation Access | Numeric | None | Enum-like (2 values) |
| **billable** | Integer | Yes | Category | 0.0 to 1.0 | 0.9466634776369289 | 2 | Billable | Numeric | None | Enum-like (2 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 6,800 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **crm_access** | Integer | Yes | Category | 0.0 to 1.0 | 0.9142964540784363 | 2 | Crm Access | Numeric | None | Enum-like (2 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 7,982 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inviter_id** | Float | Yes | - | 1.0 to 53,772.0 (Null: 37.9%) | 21,422.171641791047 | 704 | Reference to inviter | Numeric | Foreign Key (likely) | Variable |
| **marketing_access** | Integer | Yes | Category | 0.0 to 1.0 | 0.5957900012529758 | 2 | Marketing Access | Numeric | None | Enum-like (2 values) |
| **role** | Float | No | - | 0.0 to 2.0 | 0.6943991980954768 | 3 | Role | Numeric; Required | Not Null | Enum-like (3 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 5,598 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 1.0 to 53,795.0 | 30,706.33830347075 | 4,802 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>38. postgres_account_users_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_account_users. Contains unprocessed data before transformation.

**Owner/Maintainer:** Accounts/Billing Team

**Tags:** `raw-data`, `staging`, `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 853

### account_id` → `postgres_accounts.id` (inferred)
- `automation_access

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.2085
- **Distinct Values:** 2

### billable

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.9466634776369289
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,554

### crm_access

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.3635
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)
- `marketing_access

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.2089
- **Distinct Values:** 2

### role

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 2.0
- **Average:** 0.7002
- **Distinct Values:** 3

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,788

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_account_users_raw`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 853 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 28,141.0 | 14,448.6534 | 1,315 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **automation_access** | Integer | Yes | Category | 0.0 to 1.0 | 0.2085 | 2 | Automation Access | Numeric | None | Enum-like (2 values) |
| **billable** | Integer | Yes | Category | 0.0 to 1.0 | 0.9466634776369289 | 2 | Billable | Numeric | None | Enum-like (2 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 5,554 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **crm_access** | Integer | Yes | Category | 0.0 to 1.0 | 0.3635 | 2 | Crm Access | Numeric | None | Enum-like (2 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 6,428 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inviter_id** | Float | Yes | - | 1.0 to 53,031.0 (Null: 31.7%) | 19,494.76964729986 | 650 | Reference to inviter | Numeric | Foreign Key (likely) | Variable |
| **marketing_access** | Integer | Yes | Category | 0.0 to 1.0 | 0.2089 | 2 | Marketing Access | Numeric | None | Enum-like (2 values) |
| **role** | Float | No | - | 0.0 to 2.0 | 0.7002 | 3 | Role | Numeric; Required | Not Null | Enum-like (3 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 7,788 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 1.0 to 53,337.0 | 29,544.3029 | 4,174 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>39. postgres_accounts</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages account information and configurations.

**Owner/Maintainer:** Accounts/Billing Team

**Tags:** `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 527

### agent_analytic_id` → Related table (inferred)
- `assignment_logic

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1974
- **Distinct Values:** 2

### auto_resolve_duration

- **Type:** `Float`
- **Semantic Type:** `Duration`
- **Nullable:** Yes
- **Range:** 1.0 to 10.0
- **Average:** 4.6
- **Distinct Values:** 3
- **Null %:** 99.8%

### billing_email

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.2846879209699147 chars
- **Distinct Values:** 12

### concurrency_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.013920071845532105
- **Distinct Values:** 2

### concurrency_limit

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 1,000.0
- **Average:** 5.475033738191634
- **Distinct Values:** 12
- **Null %:** 0.2%

### contact_masking

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0002
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,586

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.997530309833857 chars
- **Distinct Values:** 22

### customer_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_accounts`
- **Total Columns:** 49

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 527 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **agent_analytic_id** | Float | No | - | 0.0 to 1.0 | 0.000898069151324652 | 2 | Reference to agent analytic | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **assignment_logic** | Float | No | - | 0.0 to 1.0 | 0.1974 | 2 | Assignment Logic | Numeric; Required | Not Null | Enum-like (2 values) |
| **auto_resolve_duration** | Float | Yes | Duration | 1.0 to 10.0 (Null: 99.8%) | 4.6 | 3 | Auto Resolve Duration | Numeric | None | Enum-like (3 values) |
| **billing_email** | Text | No | Category | 0.2846879209699147 chars | - | 12 | Email address | Required | Not Null | Variable |
| **concurrency_enabled** | Integer | Yes | Category | 0.0 to 1.0 | 0.013920071845532105 | 2 | Concurrency Enabled | Numeric | None | Enum-like (2 values) |
| **concurrency_limit** | Float | Yes | - | 0.0 to 1,000.0 (Null: 0.2%) | 5.475033738191634 | 12 | Concurrency Limit | Numeric | None | Variable |
| **contact_masking** | Integer | No | Category | 0.0 to 1.0 | 0.0002 | 2 | Contact Masking | Numeric; Required | Not Null | Enum-like (2 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1,586 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 2.997530309833857 chars | - | 22 | Currency | Required | Not Null | Variable |
| **customer_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to customer | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 97.3%) | - | 3 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **domain** | Text | No | - | 10.039964077233947 chars | - | 1,270 | Domain | Required | Not Null | Variable |
| **enforce_tagging** | Integer | No | Category | 0.0 to 1.0 | 0.015267175572519083 | 2 | Enforce Tagging | Numeric; Required | Not Null | Enum-like (2 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 1,586 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **feature_flags** | Float | No | - | 14.0 to 59,630.0 | 3,398.487651549169 | 52 | Feature Flags | Numeric; Required | Not Null | Variable |
| **grace_added_on** | DateTime | Yes | - | - (Null: 100.0%) | - | 1 | Grace Added On | Valid ISO 8601 datetime | None | Variable |
| **grace_extension** | Integer | No | Category | 0.0 to 1.0 | 0.026493039964077234 | 2 | Grace Extension | Numeric; Required | Not Null | Enum-like (2 values) |
| **hide_all_tab** | Integer | No | Category | 0.0 to 1.0 | 0.012348450830713965 | 2 | Reference to he all tab | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **hide_all_tab_for_supervisor** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Reference to he all tab for supervisor | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **hide_bot_conversations** | Integer | No | Category | 0.0 to 1.0 | 0.0029187247418051188 | 2 | Reference to he bot conversations | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **hide_out_of_stock** | Integer | No | Category | 0.0 to 1.0 | 0.006286484059272564 | 2 | Reference to he out of stock | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **hide_queued_tab** | Integer | No | Category | 0.0 to 1.0 | 0.005163897620116749 | 2 | Reference to he queued tab | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **hide_queued_tab_for_supervisor** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Reference to he queued tab for supervisor | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **is_enterprise** | Integer | No | Category | 0.0 to 1.0 | 0.05298607992815447 | 2 | Is Enterprise | Numeric; Required | Not Null | Enum-like (2 values) |
| **locale** | Float | No | - | 0.0 to 23.0 | 0.08419398293668612 | 9 | Locale | Numeric; Required | Not Null | Variable |
| **name** | Text | No | Name | 13.02132914234396 chars | - | 1,569 | Human-readable name or title | Required | Not Null | Variable |
| **on_grace_period** | Integer | No | Category | 0.0 to 1.0 | 0.13403682083520432 | 2 | On Grace Period | Numeric; Required | Not Null | Enum-like (2 values) |
| **on_shopify_custom_plan** | Integer | No | Category | 0.0 to 1.0 | 0.012797485406376291 | 2 | On Shopify Custom Plan | Numeric; Required | Not Null | Enum-like (2 values) |
| **partner_billed** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Partner Billed | Numeric | None | Enum-like (1 values) |
| **password** | Text | No | - | 36.0 chars | - | 1,586 | Password | Required | Not Null | Variable |
| **payment_pending** | Integer | No | Category | 0.0 to 1.0 | 0.08037718904355635 | 2 | Payment Pending | Numeric; Required | Not Null | Enum-like (2 values) |
| **preferred_billing_currency** | Float | No | - | 0.0 to 1.0 | 0.6686124831612034 | 2 | Preferred Billing Currency | Numeric; Required | Not Null | Enum-like (2 values) |
| **settings_flags** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Settings Flags | Numeric; Required | Not Null | Enum-like (1 values) |
| **shopify_access_token** | Text | No | - | 9.956443646160754 chars | - | 425 | Authentication or access token | Required | Not Null | Variable |
| **shopify_app_reinstalled** | Integer | No | Category | 0.0 to 1.0 | 0.012348450830713965 | 2 | Shopify App Reinstalled | Numeric; Required | Not Null | Enum-like (2 values) |
| **shopify_country_code** | Text | No | - | 0.5226762460709474 chars | - | 45 | Count of shopify_ry_code | Required | Not Null | Variable |
| **shopify_country_name** | Text | No | - | 1.7903008531656937 chars | - | 42 | Count of shopify_ry_name | Required | Not Null | Variable |
| **shopify_deleted** | Integer | No | Category | 0.0 to 1.0 | 0.05927256398742703 | 2 | Shopify Deleted | Numeric; Required | Not Null | Enum-like (2 values) |
| **shopify_store_url** | Text | No | URL | 7.320835204310732 chars | - | 392 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **source** | Text | No | Source | 1.7555006735518635 chars | - | 3 | Source | Required | Not Null | Categorical (3 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **support_email** | Text | No | Category | 3.0682532555006734 chars | - | 3 | Email address | Required | Not Null | Categorical (3 categories) |
| **template_last_synced_at** | DateTime | Yes | - | - (Null: 93.4%) | - | 275 | Template Last Synced At | Valid ISO 8601 datetime | None | Variable |
| **ums_enabled** | Integer | Yes | Category | 0.0 to 1.0 | 0.09788953749438707 | 2 | Ums Enabled | Numeric | None | Enum-like (2 values) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 2,111 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **username** | Text | No | - | 41.27727885047149 chars | - | 1,586 | Username | Required | Not Null | Variable |
| **website_url** | Text | No | URL | 1.1957790749887742 chars | - | 76 | URL or web address | Valid URL format; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>40. postgres_agent_agent_analytics</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Analytics and metrics table for reporting purposes.

**Owner/Maintainer:** Analytics/BI Team

**Tags:** `analytics`, `reporting`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 63

### account_id` → `postgres_accounts.id` (inferred)
- `active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### agent_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 91,137.9
- **Average:** 68.9324158918005
- **Distinct Values:** 1,767
- **Null %:** 40.8%

### agent_resolution_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 102,343.35
- **Average:** 459.8942991024288
- **Distinct Values:** 4,148
- **Null %:** 24.2%

### agent_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 26.0
- **Average:** 1.2586999999999997
- **Distinct Values:** 26

### assignee_id` → Related table (inferred)
- `average_agent_wait_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 172,818.12
- **Average:** 175.28261876584955
- **Distinct Values:** 2,600
- **Null %:** 40.8%

### contact_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,599

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_agent_agent_analytics`
- **Total Columns:** 26

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 63 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 23,996.0 | 3,922.5685 | 165 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **active** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Active | Numeric; Required | Not Null | Enum-like (1 values) |
| **agent_frt** | Float | Yes | - | 0.0 to 91,137.9 (Null: 40.8%) | 68.9324158918005 | 1,767 | Agent Frt | Numeric | None | Variable |
| **agent_resolution_time** | Float | Yes | - | 0.0 to 102,343.35 (Null: 24.2%) | 459.8942991024288 | 4,148 | Agent Resolution Time | Numeric | None | Variable |
| **agent_turns** | Float | No | - | 0.0 to 26.0 | 1.2586999999999997 | 26 | Agent Turns | Numeric; Required | Not Null | Variable |
| **assignee_id** | Float | No | - | 1.0 to 45,169.0 | 19,248.159 | 475 | Reference to assignee | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **average_agent_wait_time** | Float | Yes | - | 0.0 to 172,818.12 (Null: 40.8%) | 175.28261876584955 | 2,600 | Average Agent Wait Time | Numeric | None | Variable |
| **contact_turns** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Contact Turns | Numeric; Required | Not Null | Enum-like (1 values) |
| **conversation_id** | Float | No | - | 9,921,112.0 to 62,575,427.0 | 61,757,163.9039 | 8,048 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 6,599 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_agent_message_time** | DateTime | Yes | - | - (Null: 40.8%) | - | 4,923 | First Agent Message Time | Valid ISO 8601 datetime | None | Variable |
| **first_assigned_time** | DateTime | No | - | - | - | 6,622 | First Assigned Time | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **inbox_id** | Float | No | - | 10.0 to 30,027.0 | 7,130.9525 | 312 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **is_auto_resolved** | Integer | Yes | Category | 0.0 to 1.0 | 0.0867 | 2 | Is Auto Resolved | Numeric | None | Enum-like (2 values) |
| **is_outbound** | Integer | No | Category | 0.0 to 1.0 | 0.0007 | 2 | Is Outbound | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_outside_working_hours** | Integer | Yes | Category | 0.0 to 1.0 | 0.2527 | 2 | Reference to is outse working hours | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **is_resolved** | Integer | No | Category | 0.0 to 1.0 | 0.8042 | 2 | Is Resolved | Numeric; Required | Not Null | Enum-like (2 values) |
| **last_agent_message_time** | DateTime | Yes | - | - (Null: 40.8%) | - | 5,058 | Last Agent Message Time | Valid ISO 8601 datetime | None | Variable |
| **last_contact_message_time** | DateTime | Yes | - | - (Null: 42.7%) | - | 3,936 | Last Contact Message Time | Valid ISO 8601 datetime | None | Variable |
| **last_resolution_time** | DateTime | Yes | - | - (Null: 24.2%) | - | 6,472 | Last Resolution Time | Valid ISO 8601 datetime | None | Variable |
| **self_assign** | Integer | No | Category | 0.0 to 1.0 | 0.4531 | 2 | Self Assign | Numeric; Required | Not Null | Enum-like (2 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 8,005 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>41. postgres_agent_analytics</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Analytics and metrics table for reporting purposes.

**Owner/Maintainer:** Analytics/BI Team

**Tags:** `analytics`, `reporting`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,783

### account_id` → `postgres_accounts.id` (inferred)
- `active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### agent_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 538,887.14
- **Average:** 330.5876945442107
- **Distinct Values:** 2,157
- **Null %:** 41.5%

### agent_resolution_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** -260.19 to 702,447.42
- **Average:** 568.2310476925055
- **Distinct Values:** 3,915
- **Null %:** 22.2%

### agent_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 79.0
- **Average:** 1.2835
- **Distinct Values:** 28

### assignee_id` → Related table (inferred)
- `average_agent_wait_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 734,825.17
- **Average:** 449.8389512711865
- **Distinct Values:** 2,886
- **Null %:** 43.4%

### contact_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,997

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_agent_analytics`
- **Total Columns:** 26

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1,783 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,047.0 | 2,934.0706999999998 | 276 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **active** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Active | Numeric; Required | Not Null | Enum-like (1 values) |
| **agent_frt** | Float | Yes | - | 0.0 to 538,887.14 (Null: 41.5%) | 330.5876945442107 | 2,157 | Agent Frt | Numeric | None | Variable |
| **agent_resolution_time** | Float | Yes | - | -260.19 to 702,447.42 (Null: 22.2%) | 568.2310476925055 | 3,915 | Agent Resolution Time | Numeric | None | Variable |
| **agent_turns** | Float | No | - | 0.0 to 79.0 | 1.2835 | 28 | Agent Turns | Numeric; Required | Not Null | Variable |
| **assignee_id** | Float | No | - | 1.0 to 50,150.0 | 12,236.8013 | 1,637 | Reference to assignee | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **average_agent_wait_time** | Float | Yes | - | 0.0 to 734,825.17 (Null: 43.4%) | 449.8389512711865 | 2,886 | Average Agent Wait Time | Numeric | None | Variable |
| **contact_turns** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Contact Turns | Numeric; Required | Not Null | Enum-like (1 values) |
| **conversation_id** | Float | No | - | 9,809.0 to 76,260,479.0 | 43,181,510.6101 | 9,997 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,997 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_agent_message_time** | DateTime | Yes | - | - (Null: 42.2%) | - | 5,783 | First Agent Message Time | Valid ISO 8601 datetime | None | Variable |
| **first_assigned_time** | DateTime | No | - | - | - | 9,996 | First Assigned Time | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **inbox_id** | Float | Yes | - | 10.0 to 33,622.0 (Null: 4.3%) | 5,375.366049963414 | 612 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **is_auto_resolved** | Integer | Yes | Category | 0.0 to 1.0 | 0.0265 | 2 | Is Auto Resolved | Numeric | None | Enum-like (2 values) |
| **is_outbound** | Integer | Yes | Category | 0.0 to 1.0 | 0.0923 | 2 | Is Outbound | Numeric | None | Enum-like (2 values) |
| **is_outside_working_hours** | Integer | Yes | Category | 0.0 to 1.0 | 0.2257 | 2 | Reference to is outse working hours | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **is_resolved** | Integer | No | Category | 0.0 to 1.0 | 0.8023 | 2 | Is Resolved | Numeric; Required | Not Null | Enum-like (2 values) |
| **last_agent_message_time** | DateTime | Yes | - | - (Null: 42.2%) | - | 5,783 | Last Agent Message Time | Valid ISO 8601 datetime | None | Variable |
| **last_contact_message_time** | DateTime | Yes | - | - (Null: 47.1%) | - | 5,288 | Last Contact Message Time | Valid ISO 8601 datetime | None | Variable |
| **last_resolution_time** | DateTime | Yes | - | - (Null: 22.3%) | - | 7,772 | Last Resolution Time | Valid ISO 8601 datetime | None | Variable |
| **self_assign** | Integer | No | Category | 0.0 to 1.0 | 0.1342 | 2 | Self Assign | Numeric; Required | Not Null | Enum-like (2 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,994 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>42. postgres_attendances</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Tracks billing and usage metrics.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 77

### account_id` → `postgres_accounts.id` (inferred)
- `availability

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 4.0
- **Average:** 0.9541
- **Distinct Values:** 5

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,073

### eventn_ctx_event_id` → Related table (inferred)
- `src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,073

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_attendances`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 77 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,117.0 | 6,620.4225 | 1,208 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **availability** | Float | No | - | 0.0 to 4.0 | 0.9541 | 5 | Availability | Numeric; Required | Not Null | Enum-like (5 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 5,073 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **reason** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Reason | Numeric | None | Enum-like (1 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 5,073 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 1.0 to 50,282.0 | 22,403.296 | 230 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>43. postgres_automation_rule_analytic</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages automation rules and workflows.

**Owner/Maintainer:** Automation/Workflows Team

**Tags:** `automation`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,749

### account_id` → `postgres_accounts.id` (inferred)
- `automation_rule_id` → Related table (inferred)
- `conversation_created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 3,319

### conversation_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_automation_rule_analytic`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 2,749 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,980.0 | 20,572.8113 | 53 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **automation_rule_id** | Float | No | - | 463.0 to 4,370.0 | 3,707.6505 | 91 | Reference to automation rule | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conversation_created_at** | DateTime | No | CreationTimestamp | - | - | 3,319 | Conversation Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 52,808,608.0 to 163,129,569.0 | 108,212,191.1625 | 3,338 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,234 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **rule_name** | Text | No | - | 18.2636 chars | - | 69 | Rule Name | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,234 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>44. postgres_automation_rule_analytic_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_automation_rule_analytic. Contains unprocessed data before transformation.

**Owner/Maintainer:** Automation/Workflows Team

**Tags:** `raw-data`, `staging`, `automation`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 949

### account_id` → `postgres_accounts.id` (inferred)
- `automation_rule_id` → Related table (inferred)
- `conversation_created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,146

### conversation_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_automation_rule_analytic_raw`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 949 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 28,052.0 | 22,022.1139 | 61 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **automation_rule_id** | Float | No | - | 463.0 to 4,370.0 | 3,665.0571 | 121 | Reference to automation rule | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conversation_created_at** | DateTime | No | CreationTimestamp | - | - | 4,146 | Conversation Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 55,870,942.0 to 132,686,471.0 | 116,586,861.3691 | 4,163 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,360 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **rule_name** | Text | No | - | 19.0336 chars | - | 101 | Rule Name | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,360 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>45. postgres_automation_rules</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages automation rules and workflows.

**Owner/Maintainer:** Automation/Workflows Team

**Tags:** `automation`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 171

### account_id` → `postgres_accounts.id` (inferred)
- `actions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 182.0906862745098 chars
- **Distinct Values:** 257

### active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.6642156862745098
- **Distinct Values:** 2

### conditions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 308.50245098039215 chars
- **Distinct Values:** 329

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 328

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 8.034313725490197 chars
- **Distinct Values:** 70

### event_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 17.32107843137255 chars
- **Distinct Values:** 8

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_automation_rules`
- **Total Columns:** 15

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 171 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 24.0 to 27,586.0 | 16,688.174019607843 | 115 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **actions** | Text | No | SerializedJSON | 182.0906862745098 chars | - | 257 | Actions | Required | Not Null | Variable |
| **active** | Integer | No | Category | 0.0 to 1.0 | 0.6642156862745098 | 2 | Active | Numeric; Required | Not Null | Enum-like (2 values) |
| **conditions** | Text | No | SerializedJSON | 308.50245098039215 chars | - | 329 | Conditions | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 328 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **description** | Text | No | Description | 8.034313725490197 chars | - | 70 | Description | Required | Not Null | Variable |
| **event_name** | Text | No | Category | 17.32107843137255 chars | - | 8 | Event Name | Required | Not Null | Categorical (8 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 330 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **is_test** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Is Test | Numeric; Required | Not Null | Enum-like (1 values) |
| **name** | Text | No | Name | 14.91421568627451 chars | - | 298 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **test_numbers** | Text | No | Category | 0.23529411764705882 chars | - | 2 | Test Numbers | Required | Not Null | Categorical (2 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 407 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>46. postgres_billing_attendances</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Tracks billing and usage metrics.

**Owner/Maintainer:** Accounts/Billing Team

**Tags:** `billing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 449

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,200

### current_value

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.7790719877792629
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)
- `src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### toggled_by

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 55,131.0
- **Average:** 48,905.10743801653
- **Distinct Values:** 288
- **Null %:** 93.1%

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,200

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_billing_attendances`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 449 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 28,763.0 | 17,651.595760931836 | 707 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1,200 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **current_value** | Integer | No | Category | 0.0 to 1.0 | 0.7790719877792629 | 2 | Current Value | Numeric; Required | Not Null | Enum-like (2 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 5,237 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **previous_value** | Integer | No | Category | 0.0 to 1.0 | 0.21348100057284705 | 2 | Previous Value | Numeric; Required | Not Null | Enum-like (2 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **toggled_by** | Float | Yes | - | 1.0 to 55,131.0 (Null: 93.1%) | 48,905.10743801653 | 288 | Toggled By | Numeric | None | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 1,200 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 1.0 to 55,131.0 | 37,511.36719495895 | 3,094 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>47. postgres_billing_attendances_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_billing_attendances. Contains unprocessed data before transformation.

**Owner/Maintainer:** Accounts/Billing Team

**Tags:** `raw-data`, `staging`, `billing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 449

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,200

### current_value

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.7790719877792629
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)
- `src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### toggled_by

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 55,131.0
- **Average:** 48,905.10743801653
- **Distinct Values:** 288
- **Null %:** 93.1%

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,200

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_billing_attendances_raw`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 449 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 28,763.0 | 17,651.595760931836 | 707 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1,200 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **current_value** | Integer | No | Category | 0.0 to 1.0 | 0.7790719877792629 | 2 | Current Value | Numeric; Required | Not Null | Enum-like (2 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 5,237 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **previous_value** | Integer | No | Category | 0.0 to 1.0 | 0.21348100057284705 | 2 | Previous Value | Numeric; Required | Not Null | Enum-like (2 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **toggled_by** | Float | Yes | - | 1.0 to 55,131.0 (Null: 93.1%) | 48,905.10743801653 | 288 | Toggled By | Numeric | None | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 1,200 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 1.0 to 55,131.0 | 37,511.36719495895 | 3,094 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>48. postgres_bot_cdc_bot_csat</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores bot configuration and interaction data.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `feedback`, `csat`, `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_ab_cdc_lsn

- **Type:** `Float`
- **Nullable:** No
- **Range:** 89,320,491,998,048.0 to 89,321,918,201,280.0
- **Average:** 89,321,601,473,766.9
- **Distinct Values:** 3

### _ab_cdc_updated_at

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 39.0 chars
- **Distinct Values:** 3

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 36

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,895

### csat_comment

- **Type:** `Text`
- **Semantic Type:** `Comment`
- **Nullable:** No
- **Avg Length:** 0.0397 chars
- **Distinct Values:** 14

### csat_reason

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 1.449 chars
- **Distinct Values:** 61

### csat_score

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** Yes
- **Range:** 1.0 to 5.0
- **Average:** 3.28051948051948
- **Distinct Values:** 6
- **Null %:** 88.4%

### display_id` → Related table (inferred)
- `event_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 9.0101 chars
- **Distinct Values:** 7

### eventn_ctx_event_id` → Related table (inferred)
- `is_csat_sent

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### is_query_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1749
- **Distinct Values:** 2

### is_reminder_sent

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1943
- **Distinct Values:** 2

### message_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_bot_cdc_bot_csat`
- **Total Columns:** 20

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_ab_cdc_lsn** | Float | No | - | 89,320,491,998,048.0 to 89,321,918,201,280.0 | 89,321,601,473,766.9 | 3 |  Ab Cdc Lsn | Numeric; Required | Not Null | Enum-like (3 values) |
| **_ab_cdc_updated_at** | Text | No | Category | 39.0 chars | - | 3 |  Ab Cdc Updated At | Required | Not Null | Categorical (3 categories) |
| **_timestamp** | DateTime | No | - | - | - | 36 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 51.0 to 54.0 | 53.6136 | 2 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,895 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **csat_comment** | Text | No | Comment | 0.0397 chars | - | 14 | Csat Comment | Required | Not Null | Variable |
| **csat_reason** | Text | No | - | 1.449 chars | - | 61 | Csat Reason | Required | Not Null | Variable |
| **csat_score** | Float | Yes | Score | 1.0 to 5.0 (Null: 88.4%) | 3.28051948051948 | 6 | Csat Score | Numeric | None | Variable |
| **display_id** | Float | No | - | 8,608.0 to 5,324,628.0 | 4,489,666.318900004 | 8,000 | Reference to display | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **event_name** | Text | No | Category | 9.0101 chars | - | 7 | Event Name | Required | Not Null | Categorical (7 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_id** | Float | Yes | - | 115.0 to 33,743.0 (Null: 0.0%) | 5,024.974397439744 | 7 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **is_csat_sent** | Integer | Yes | Category | 1.0 to 1.0 | 1.0 | 1 | Is Csat Sent | Numeric | None | Enum-like (1 values) |
| **is_query_resolved** | Integer | Yes | Category | 0.0 to 1.0 | 0.1749 | 2 | Is Query Resolved | Numeric | None | Enum-like (2 values) |
| **is_reminder_sent** | Integer | Yes | Category | 0.0 to 1.0 | 0.1943 | 2 | Is Reminder Sent | Numeric | None | Enum-like (2 values) |
| **message_id** | Float | No | - | 509,540,021.0 to 738,668,456.0 | 563,652,139.0222999 | 9,997 | Reference to message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **phone** | Text | No | - | 1.8533 chars | - | 1,234 | Phone | Required | Not Null | Variable |
| **sender_id** | Text | No | - | 7.999 chars | - | 6,892 | Reference to sender | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>49. postgres_bot_cdc_bot_csat_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_bot_cdc_bot_csat. Contains unprocessed data before transformation.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `bot`, `raw-data`, `ai`, `csat`, `staging`, `feedback`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_ab_cdc_lsn

- **Type:** `Float`
- **Nullable:** No
- **Range:** 122,089,095,213,168.0 to 122,089,095,213,168.0
- **Average:** 122,089,095,213,168.0
- **Distinct Values:** 1

### _ab_cdc_updated_at

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 39.0 chars
- **Distinct Values:** 1

### _timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 18

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,987

### csat_comment

- **Type:** `Text`
- **Semantic Type:** `Comment`
- **Nullable:** No
- **Avg Length:** 0.151 chars
- **Distinct Values:** 56

### csat_reason

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.6946 chars
- **Distinct Values:** 28

### csat_score

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** Yes
- **Range:** 1.0 to 5.0
- **Average:** 3.913764510779436
- **Distinct Values:** 6
- **Null %:** 94.0%

### display_id` → Related table (inferred)
- `event_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 10.6695 chars
- **Distinct Values:** 5

### eventn_ctx_event_id` → Related table (inferred)
- `is_csat_sent

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### is_query_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1255
- **Distinct Values:** 2

### is_reminder_sent

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### message_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_bot_cdc_bot_csat_raw`
- **Total Columns:** 20

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_ab_cdc_lsn** | Float | No | - | 122,089,095,213,168.0 to 122,089,095,213,168.0 | 122,089,095,213,168.0 | 1 |  Ab Cdc Lsn | Numeric; Required | Not Null | Enum-like (1 values) |
| **_ab_cdc_updated_at** | Text | No | Category | 39.0 chars | - | 1 |  Ab Cdc Updated At | Required | Not Null | Categorical (1 categories) |
| **_timestamp** | DateTime | No | - | - | - | 18 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 39.0 to 39.0 | 39.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,987 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **csat_comment** | Text | No | Comment | 0.151 chars | - | 56 | Csat Comment | Required | Not Null | Variable |
| **csat_reason** | Text | No | Category | 0.6946 chars | - | 28 | Csat Reason | Required | Not Null | Variable |
| **csat_score** | Float | Yes | Score | 1.0 to 5.0 (Null: 94.0%) | 3.913764510779436 | 6 | Csat Score | Numeric | None | Variable |
| **display_id** | Float | No | - | 622,427.0 to 2,749,238.0 | 2,601,268.1216999986 | 9,780 | Reference to display | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **event_name** | Text | No | Category | 10.6695 chars | - | 5 | Event Name | Required | Not Null | Categorical (5 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_id** | Float | Yes | - | 894.0 to 894.0 | 894.0 | 1 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **is_csat_sent** | Integer | Yes | Category | 1.0 to 1.0 | 1.0 | 1 | Is Csat Sent | Numeric | None | Enum-like (1 values) |
| **is_query_resolved** | Integer | Yes | Category | 0.0 to 1.0 | 0.1255 | 2 | Is Query Resolved | Numeric | None | Enum-like (2 values) |
| **is_reminder_sent** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Is Reminder Sent | Numeric | None | Enum-like (1 values) |
| **message_id** | Float | No | - | 775,425,654.0 to 822,907,778.0 | 801,349,033.7265 | 9,999 | Reference to message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **phone** | Text | No | - | 11.9998 chars | - | 9,664 | Phone | Required | Not Null | Variable |
| **sender_id** | Text | No | - | 8.7673 chars | - | 9,667 | Reference to sender | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>50. postgres_broadcasts</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages broadcast messaging campaigns and delivery tracking.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `campaigns`, `marketing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 201

### account_id` → `postgres_accounts.id` (inferred)
- `content

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 328.999 chars
- **Distinct Values:** 1,885

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,977

### custom_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 10.3188 chars
- **Distinct Values:** 95

### eventn_ctx_event_id` → Related table (inferred)
- `name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 7.9475 chars
- **Distinct Values:** 1,608

### scheduled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0821
- **Distinct Values:** 2

### scheduled_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 640
- **Null %:** 91.8%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### template_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_broadcasts`
- **Total Columns:** 15

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 201 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,036.0 | 5,818.9355 | 148 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **content** | Text | No | - | 328.999 chars | - | 1,885 | Content | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,977 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **custom_attributes** | Text | No | SerializedJSON | 10.3188 chars | - | 95 | Custom Attributes | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,997 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **is_cancelled** | Integer | No | Category | 0.0 to 1.0 | 0.0042 | 2 | Is Cancelled | Numeric; Required | Not Null | Enum-like (2 values) |
| **name** | Text | No | Name | 7.9475 chars | - | 1,608 | Human-readable name or title | Required | Not Null | Variable |
| **scheduled** | Integer | No | Category | 0.0 to 1.0 | 0.0821 | 2 | Scheduled | Numeric; Required | Not Null | Enum-like (2 values) |
| **scheduled_at** | DateTime | Yes | - | - (Null: 91.8%) | - | 640 | Scheduled At | Valid ISO 8601 datetime | None | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **template_id** | Float | No | - | 709.0 to 127,727.0 | 79,128.0256 | 2,074 | Reference to template | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **total** | Float | No | - | 0.0 to 179,872.0 | 1,919.2989 | 1,897 | Total | Numeric; Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,975 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>51. postgres_channel_facebook_pages</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages communication channel configurations.

**Owner/Maintainer:** Integrations/Channels Team

**Tags:** `channels`, `integrations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 34

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 932

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 430
- **Null %:** 51.1%

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_channel_facebook_pages`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 34 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,607.0 | 12,185.130857648099 | 368 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 932 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 51.1%) | - | 430 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 1,113 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **instagram_add_on** | Integer | No | Category | 0.0 to 1.0 | 0.497789566755084 | 2 | Instagram Add On | Numeric; Required | Not Null | Enum-like (2 values) |
| **instagram_id** | Text | No | - | 8.32183908045977 chars | - | 404 | Reference to instagram | Required | Not Null, Foreign Key (likely) | Variable |
| **page_access_token** | Text | No | - | 129.4076038903625 chars | - | 1,079 | Authentication or access token | Required | Not Null | Variable |
| **page_id** | Text | No | - | 23.122900088417328 chars | - | 839 | Reference to page | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 937 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_access_token** | Text | No | - | 125.06366047745358 chars | - | 1,021 | Authentication or access token | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>52. postgres_channel_gupshup_enterprises</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages communication channel configurations.

**Owner/Maintainer:** Integrations/Channels Team

**Tags:** `channels`, `integrations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_channel_gupshup_enterprises`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 4 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,537.0 | 8,581.569711538461 | 251 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **catalog_id** | Text | No | - | 1.6899038461538463 chars | - | 33 | Reference to catalog | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 416 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 57.9%) | - | 124 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 416 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **pass** | Text | No | - | 7.966346153846154 chars | - | 346 | Pass | Required | Not Null | Variable |
| **pass_hsm** | Text | No | - | 7.997596153846154 chars | - | 346 | Pass Hsm | Required | Not Null | Variable |
| **phone_number** | Text | No | - | 11.899038461538462 chars | - | 332 | Phone Number | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 364 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user** | Text | No | - | 9.838942307692308 chars | - | 338 | User | Required | Not Null | Variable |
| **user_hsm** | Text | No | - | 9.846153846153847 chars | - | 337 | User Hsm | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>53. postgres_channel_three_sixty_dialogs</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages communication channel configurations.

**Owner/Maintainer:** Integrations/Channels Team

**Tags:** `channels`, `integrations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 32

### account_id` → `postgres_accounts.id` (inferred)
- `api_key

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.862068965517242 chars
- **Distinct Values:** 168

### catalog_id` → Related table (inferred)
- `channel_submitted

- **Type:** `Integer`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.06896551724137931
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 372

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 175
- **Null %:** 49.3%

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_channel_three_sixty_dialogs`
- **Total Columns:** 19

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 32 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 24.0 to 27,645.0 | 22,312.822281167108 | 280 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **api_key** | Text | No | - | 11.862068965517242 chars | - | 168 | Api Key | Required | Not Null | Variable |
| **catalog_id** | Text | No | Category | 0.5676392572944297 chars | - | 13 | Reference to catalog | Required | Not Null, Foreign Key (likely) | Variable |
| **channel_live** | Integer | No | Source | 0.0 to 1.0 | 0.3050397877984085 | 2 | Channel Live | Numeric; Required | Not Null | Enum-like (2 values) |
| **channel_submitted** | Integer | No | Source | 0.0 to 1.0 | 0.06896551724137931 | 2 | Channel Submitted | Numeric; Required | Not Null | Enum-like (2 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 372 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 49.3%) | - | 175 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 372 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **on_cloud** | Integer | No | Category | 0.0 to 1.0 | 0.38726790450928383 | 2 | On Cloud | Numeric; Required | Not Null | Enum-like (2 values) |
| **onboarding_started_at** | DateTime | Yes | CreationTimestamp | - (Null: 99.7%) | - | 2 | Onboarding Started At | Valid ISO 8601 datetime | None | Variable |
| **phone_number** | Text | No | - | 11.893899204244033 chars | - | 360 | Phone Number | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **template_enabled** | Integer | No | Category | 0.0 to 1.0 | 0.07161803713527852 | 2 | Template Enabled | Numeric; Required | Not Null | Enum-like (2 values) |
| **three_sixty_channel_id** | Text | No | Source | 3.647214854111406 chars | - | 167 | Reference to three sixty channel | Required | Not Null, Foreign Key (likely) | Variable |
| **three_sixty_client_id** | Text | No | - | 4.570291777188329 chars | - | 146 | Reference to three sixty client | Required | Not Null, Foreign Key (likely) | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 360 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **waba_account_id** | Text | No | - | 3.6684350132625996 chars | - | 158 | Reference to account | Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>54. postgres_channel_whatsapp_cloud_apis</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages communication channel configurations.

**Owner/Maintainer:** Platform/API Team

**Tags:** `api`, `integrations`, `channels`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 5

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_channel_whatsapp_cloud_apis`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 5 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 24.0 to 28,435.0 | 12,442.135338345865 | 108 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **auth_token** | Text | No | - | 172.08270676691728 chars | - | 128 | Authentication or access token | Required | Not Null | Variable |
| **catalog_id** | Text | No | - | 3.5037593984962405 chars | - | 34 | Reference to catalog | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 133 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 63.2%) | - | 45 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 133 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **phone_number** | Text | No | - | 16.721804511278197 chars | - | 133 | Phone Number | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 128 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **wa_business_account_id** | Text | No | - | 14.661654135338345 chars | - | 126 | Reference to account | Required | Not Null, Foreign Key (likely) | Variable |
| **wa_business_account_name** | Text | No | - | 11.969924812030076 chars | - | 116 | Count of wa_business_ac_name | Required | Not Null | Variable |
| **wa_phone_number_id** | Text | No | - | 14.503759398496241 chars | - | 126 | Reference to wa phone number | Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>55. postgres_channel_whatsapp_cloud_apis_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_channel_whatsapp_cloud_apis. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform/API Team

**Tags:** `integrations`, `raw-data`, `api`, `staging`, `channels`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_channel_whatsapp_cloud_apis_raw`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 6 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 24.0 to 28,435.0 | 12,458.814814814816 | 108 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **auth_token** | Text | No | - | 172.2 chars | - | 128 | Authentication or access token | Required | Not Null | Variable |
| **catalog_id** | Text | No | - | 3.674074074074074 chars | - | 34 | Reference to catalog | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 133 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 63.7%) | - | 45 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 133 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **phone_number** | Text | No | - | 18.651851851851852 chars | - | 135 | Phone Number | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 130 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **wa_business_account_id** | Text | No | - | 14.666666666666666 chars | - | 126 | Reference to account | Required | Not Null, Foreign Key (likely) | Variable |
| **wa_business_account_name** | Text | No | - | 11.985185185185186 chars | - | 116 | Count of wa_business_ac_name | Required | Not Null | Variable |
| **wa_phone_number_id** | Text | No | - | 14.511111111111111 chars | - | 126 | Reference to wa phone number | Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>56. postgres_contacts</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores contact and customer profile data.

**Owner/Maintainer:** Customer Data Team

**Tags:** `customer-data`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,742

### account_id` → `postgres_accounts.id` (inferred)
- `additional_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 63.7635 chars
- **Distinct Values:** 906

### address

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### conversations_count

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,977

### custom_attributes

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 2.3816 chars
- **Distinct Values:** 43

### email

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 4.1175 chars
- **Distinct Values:** 1,761

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_contacts`
- **Total Columns:** 19

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 4,742 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,089.0 | 3,078.055 | 323 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **additional_attributes** | Text | No | SerializedJSON | 63.7635 chars | - | 906 | Additional Attributes | Required | Not Null | Variable |
| **address** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Address | Required | Not Null | Categorical (1 categories) |
| **conversations_count** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Count of conversations | Numeric; Required | Not Null | Enum-like (1 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,977 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **custom_attributes** | Text | No | - | 2.3816 chars | - | 43 | Custom Attributes | Required | Not Null | Variable |
| **email** | Text | No | - | 4.1175 chars | - | 1,761 | Email address | Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **external_uuid** | Text | No | Category | 0.0 chars | - | 1 | Reference to external uu | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **identifier** | Text | No | - | 1.009 chars | - | 630 | Reference to entifier | Required | Not Null, Foreign Key (likely) | Variable |
| **instagram_username** | Text | No | - | 0.5572 chars | - | 415 | Instagram Username | Required | Not Null | Variable |
| **name** | Text | No | Name | 9.5572 chars | - | 7,553 | Human-readable name or title | Required | Not Null | Variable |
| **opt_in** | Integer | No | Category | 0.0 to 1.0 | 0.9977 | 2 | Opt In | Numeric; Required | Not Null | Enum-like (2 values) |
| **phone_number** | Text | No | - | 8.7687 chars | - | 7,292 | Phone Number | Required | Not Null | Variable |
| **pubsub_token** | Text | No | - | 24.0 chars | - | 10,000 | Authentication or access token | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,976 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>57. postgres_conv_agent_analytics</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Analytics and metrics table for reporting purposes.

**Owner/Maintainer:** Conversations Team

**Tags:** `analytics`, `conversations`, `reporting`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 729

### account_id` → `postgres_accounts.id` (inferred)
- `active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### agent_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 89,797.98
- **Average:** 136.7615272591486
- **Distinct Values:** 1,824
- **Null %:** 46.4%

### agent_resolution_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** -44.06 to 115,257.89
- **Average:** 594.6920062606719
- **Distinct Values:** 4,165
- **Null %:** 29.7%

### agent_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 25.0
- **Average:** 1.1091
- **Distinct Values:** 24

### assignee_id` → Related table (inferred)
- `average_agent_wait_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 89,797.98
- **Average:** 173.89005414488423
- **Distinct Values:** 2,014
- **Null %:** 46.4%

### contact_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,983

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_agent_analytics`
- **Total Columns:** 26

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 729 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,518.0 | 7,598.544300000001 | 242 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **active** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Active | Numeric; Required | Not Null | Enum-like (1 values) |
| **agent_frt** | Float | Yes | - | 0.0 to 89,797.98 (Null: 46.4%) | 136.7615272591486 | 1,824 | Agent Frt | Numeric | None | Variable |
| **agent_resolution_time** | Float | Yes | - | -44.06 to 115,257.89 (Null: 29.7%) | 594.6920062606719 | 4,165 | Agent Resolution Time | Numeric | None | Variable |
| **agent_turns** | Float | No | - | 0.0 to 25.0 | 1.1091 | 24 | Agent Turns | Numeric; Required | Not Null | Variable |
| **assignee_id** | Float | No | - | 1.0 to 51,601.0 | 28,778.2854 | 1,073 | Reference to assignee | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **average_agent_wait_time** | Float | Yes | - | 0.0 to 89,797.98 (Null: 46.4%) | 173.89005414488423 | 2,014 | Average Agent Wait Time | Numeric | None | Variable |
| **contact_turns** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Contact Turns | Numeric; Required | Not Null | Enum-like (1 values) |
| **conversation_id** | Float | No | - | 11,442,558.0 to 99,600,632.0 | 72,022,586.14970003 | 9,978 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,983 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,997 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_agent_message_time** | DateTime | Yes | - | - (Null: 46.2%) | - | 5,371 | First Agent Message Time | Valid ISO 8601 datetime | None | Variable |
| **first_assigned_time** | DateTime | No | - | - | - | 9,980 | First Assigned Time | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **inbox_id** | Float | No | - | 10.0 to 34,283.0 | 13,504.4864 | 537 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **is_auto_resolved** | Integer | Yes | Category | 0.0 to 1.0 | 0.1021 | 2 | Is Auto Resolved | Numeric | None | Enum-like (2 values) |
| **is_outbound** | Integer | No | Category | 0.0 to 1.0 | 0.0048 | 2 | Is Outbound | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_outside_working_hours** | Integer | Yes | Category | 0.0 to 1.0 | 0.1783 | 2 | Reference to is outse working hours | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **is_resolved** | Integer | No | Category | 0.0 to 1.0 | 0.7221 | 2 | Is Resolved | Numeric; Required | Not Null | Enum-like (2 values) |
| **last_agent_message_time** | DateTime | Yes | - | - (Null: 46.2%) | - | 5,376 | Last Agent Message Time | Valid ISO 8601 datetime | None | Variable |
| **last_contact_message_time** | DateTime | Yes | - | - (Null: 43.6%) | - | 5,631 | Last Contact Message Time | Valid ISO 8601 datetime | None | Variable |
| **last_resolution_time** | DateTime | Yes | - | - (Null: 29.7%) | - | 7,027 | Last Resolution Time | Valid ISO 8601 datetime | None | Variable |
| **self_assign** | Integer | No | Category | 0.0 to 1.0 | 0.3502 | 2 | Self Assign | Numeric; Required | Not Null | Enum-like (2 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,986 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>58. postgres_conv_agent_analytics_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_conv_agent_analytics. Contains unprocessed data before transformation.

**Owner/Maintainer:** Conversations Team

**Tags:** `analytics`, `reporting`, `raw-data`, `staging`, `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 53

### account_id` → `postgres_accounts.id` (inferred)
- `active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### agent_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 91,137.9
- **Average:** 68.96738159675238
- **Distinct Values:** 1,767
- **Null %:** 40.9%

### agent_resolution_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 102,343.35
- **Average:** 459.8904197465683
- **Distinct Values:** 4,148
- **Null %:** 24.2%

### agent_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 26.0
- **Average:** 1.2581
- **Distinct Values:** 26

### assignee_id` → Related table (inferred)
- `average_agent_wait_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 172,818.12
- **Average:** 175.37059539918812
- **Distinct Values:** 2,600
- **Null %:** 40.9%

### contact_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,600

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_agent_analytics_raw`
- **Total Columns:** 26

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 53 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 23,996.0 | 3,922.2389 | 165 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **active** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Active | Numeric; Required | Not Null | Enum-like (1 values) |
| **agent_frt** | Float | Yes | - | 0.0 to 91,137.9 (Null: 40.9%) | 68.96738159675238 | 1,767 | Agent Frt | Numeric | None | Variable |
| **agent_resolution_time** | Float | Yes | - | 0.0 to 102,343.35 (Null: 24.2%) | 459.8904197465683 | 4,148 | Agent Resolution Time | Numeric | None | Variable |
| **agent_turns** | Float | No | - | 0.0 to 26.0 | 1.2581 | 26 | Agent Turns | Numeric; Required | Not Null | Variable |
| **assignee_id** | Float | No | - | 1.0 to 48,931.0 | 19,256.3994 | 477 | Reference to assignee | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **average_agent_wait_time** | Float | Yes | - | 0.0 to 172,818.12 (Null: 40.9%) | 175.37059539918812 | 2,600 | Average Agent Wait Time | Numeric | None | Variable |
| **contact_turns** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Contact Turns | Numeric; Required | Not Null | Enum-like (1 values) |
| **conversation_id** | Float | No | - | 9,921,112.0 to 65,914,696.0 | 61,757,860.22309998 | 8,050 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 6,600 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_agent_message_time** | DateTime | Yes | - | - (Null: 40.9%) | - | 4,921 | First Agent Message Time | Valid ISO 8601 datetime | None | Variable |
| **first_assigned_time** | DateTime | No | - | - | - | 6,623 | First Assigned Time | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **inbox_id** | Float | No | - | 10.0 to 30,027.0 | 7,133.9139 | 312 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **is_auto_resolved** | Integer | Yes | Category | 0.0 to 1.0 | 0.0867 | 2 | Is Auto Resolved | Numeric | None | Enum-like (2 values) |
| **is_outbound** | Integer | No | Category | 0.0 to 1.0 | 0.0011 | 2 | Is Outbound | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_outside_working_hours** | Integer | Yes | Category | 0.0 to 1.0 | 0.2528 | 2 | Reference to is outse working hours | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **is_resolved** | Integer | No | Category | 0.0 to 1.0 | 0.8042 | 2 | Is Resolved | Numeric; Required | Not Null | Enum-like (2 values) |
| **last_agent_message_time** | DateTime | Yes | - | - (Null: 40.9%) | - | 5,056 | Last Agent Message Time | Valid ISO 8601 datetime | None | Variable |
| **last_contact_message_time** | DateTime | Yes | - | - (Null: 42.7%) | - | 3,936 | Last Contact Message Time | Valid ISO 8601 datetime | None | Variable |
| **last_resolution_time** | DateTime | Yes | - | - (Null: 24.2%) | - | 6,473 | Last Resolution Time | Valid ISO 8601 datetime | None | Variable |
| **self_assign** | Integer | No | Category | 0.0 to 1.0 | 0.4533 | 2 | Self Assign | Numeric; Required | Not Null | Enum-like (2 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 8,007 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>59. postgres_conv_agent_bot_inboxes</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `conversations`, `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `agent_bot_id` → Related table (inferred)
- `bot_percent

- **Type:** `Float`
- **Semantic Type:** `Share`
- **Nullable:** No
- **Range:** 0.0 to 100.0
- **Average:** 68.42105263157895
- **Distinct Values:** 2

### bot_percent_off

- **Type:** `Float`
- **Semantic Type:** `Share`
- **Nullable:** No
- **Range:** -5.0 to 101.0
- **Average:** 68.52947368421053
- **Distinct Values:** 8

### conv_marketing_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 21.57578947368421 chars
- **Distinct Values:** 11

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 949

### csat_with_bot

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.7463157894736843
- **Distinct Values:** 2

### delivery_medium

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_agent_bot_inboxes`
- **Total Columns:** 21

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,554.0 | 11,006.223157894738 | 409 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **agent_bot_id** | Float | No | - | 1.0 to 6,113.0 | 2,503.6431578947368 | 408 | Reference to agent bot | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **bot_percent** | Float | No | Share | 0.0 to 100.0 | 68.42105263157895 | 2 | Bot Percent | Numeric; Required | Not Null | Enum-like (2 values) |
| **bot_percent_off** | Float | No | Share | -5.0 to 101.0 | 68.52947368421053 | 8 | Bot Percent Off | Numeric; Required | Not Null | Variable |
| **conv_marketing_attributes** | Text | No | SerializedJSON | 21.57578947368421 chars | - | 11 | Conv Marketing Attributes | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 949 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **csat_with_bot** | Integer | No | Category | 0.0 to 1.0 | 0.7463157894736843 | 2 | Csat With Bot | Numeric; Required | Not Null | Enum-like (2 values) |
| **delivery_medium** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Delivery Medium | Numeric; Required | Not Null | Enum-like (1 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 950 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_id** | Float | No | - | 6.0 to 34,266.0 | 15,776.814736842109 | 950 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **international_number_allowed** | Integer | No | Quantity | 0.0 to 1.0 | 0.9978947368421053 | 2 | International Number Allowed | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_test** | Integer | No | Category | 0.0 to 1.0 | 0.028421052631578948 | 2 | Is Test | Numeric; Required | Not Null | Enum-like (2 values) |
| **only_conv_marketing** | Integer | No | Category | 0.0 to 1.0 | 0.007368421052631579 | 2 | Only Conv Marketing | Numeric; Required | Not Null | Enum-like (2 values) |
| **reply_to_comment** | Integer | No | Category | 0.0 to 1.0 | 0.031578947368421054 | 2 | Reply To Comment | Numeric; Required | Not Null | Enum-like (2 values) |
| **reply_to_template** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Reply To Template | Numeric; Required | Not Null | Enum-like (1 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Float | No | - | 0.0 to 2.0 | 0.11052631578947368 | 3 | Status or state of record | Numeric; Required | Not Null | Enum-like (3 values) |
| **test_numbers** | Text | No | SerializedJSON | 20.352631578947367 chars | - | 221 | Test Numbers | Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 886 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>60. postgres_conv_agent_bots</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `conversations`, `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 422

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.037914691943127965 chars
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_agent_bots`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 422 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **description** | Text | No | Description | 0.037914691943127965 chars | - | 2 | Description | Required | Not Null | Categorical (2 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 422 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hide_input_for_bot_conversations** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Reference to he input for bot conversations | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **name** | Text | No | Name | 11.338862559241706 chars | - | 421 | Human-readable name or title | Required | Not Null | Variable |
| **outgoing_url** | Text | No | URL | 58.11374407582938 chars | - | 419 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 422 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>61. postgres_conv_ar_internal_metadata</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- None identified (or table uses non-standard FK naming)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_ar_internal_metadata`
- **Total Columns:** 7

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 2 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Categorical (2 categories) |
| **key** | Text | No | Category | 11.0 chars | - | 2 | Key | Required | Not Null | Categorical (2 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 2 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **value** | Text | No | Category | 25.0 chars | - | 2 | Value | Required | Not Null | Categorical (2 categories) |

</details>

---

<details>
<summary><h2>62. postgres_conv_billing_plans</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `billing`, `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 13

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_billing_plans`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 73.0 | 44.76923076923077 | 13 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 13 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 13 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **pricing** | Text | No | Category | 34.0 chars | - | 1 | Pricing | Required | Not Null | Categorical (1 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **total_convs** | Float | No | - | 0.0 to 18,768.0 | 2,532.923076923077 | 8 | Total Convs | Numeric; Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 13 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **zoho_addon_code** | Text | No | Category | 22.0 chars | - | 1 | Zoho Addon Code | Required | Not Null | Categorical (1 categories) |
| **zoho_plan_code** | Text | No | Category | 21.0 chars | - | 1 | Zoho Plan Code | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>63. postgres_conv_canned_images</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### canned_response_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_canned_images`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **canned_response_id** | Float | Yes | - | 363.0 to 365.0 (Null: 99.1%) | 364.0 | 3 | Reference to canned response | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 230 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 230 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **title** | Text | No | Title | 21.408695652173915 chars | - | 26 | Title | Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 230 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>64. postgres_conv_channel_api</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `api`, `conversations`, `integrations`, `channels`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_channel_api`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 72.0 to 27,401.0 | 13,669.42857142857 | 7 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 7 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 14.3%) | - | 7 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 7 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Categorical (7 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 7 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **webhook_url** | Text | No | URL | 37.857142857142854 chars | - | 7 | URL or web address | Valid URL format; Required | Not Null | Categorical (7 categories) |

</details>

---

<details>
<summary><h2>65. postgres_conv_channel_knowlarities</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`, `integrations`, `channels`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_channel_knowlarities`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 24.0 to 27,006.0 | 6,049.846153846154 | 9 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **caller_id** | Text | No | Category | 13.038461538461538 chars | - | 11 | Reference to caller | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 26 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 34.6%) | - | 18 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 26 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **sr_api_key** | Text | No | Category | 36.0 chars | - | 8 | Sr Api Key | Required | Not Null | Categorical (8 categories) |
| **sr_number** | Text | No | Category | 28.076923076923077 chars | - | 26 | Sr Number | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 26 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>66. postgres_conv_channel_value_firsts</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`, `integrations`, `channels`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_channel_value_firsts`
- **Total Columns:** 12

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 12.0 to 481.0 | 454.94736842105266 | 4 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (4 values) |
| **auth_token** | Text | No | Category | 17.973684210526315 chars | - | 5 | Authentication or access token | Required | Not Null | Categorical (5 categories) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 38 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 92.1%) | - | 3 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 38 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **pass** | Text | No | Category | 18.5 chars | - | 8 | Pass | Required | Not Null | Categorical (8 categories) |
| **phone_number** | Text | No | Category | 12.0 chars | - | 5 | Phone Number | Required | Not Null | Categorical (5 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 37 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user** | Text | No | Category | 12.5 chars | - | 6 | User | Required | Not Null | Categorical (6 categories) |

</details>

---

<details>
<summary><h2>67. postgres_conv_channel_web_widgets</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`, `integrations`, `channels`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `closewidgetpopupsetting

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.7874125874125875 chars
- **Distinct Values:** 4

### configsetting

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 175.52027972027972 chars
- **Distinct Values:** 130

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 715

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 191
- **Null %:** 57.8%

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_channel_web_widgets`
- **Total Columns:** 25

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,563.0 | 11,983.858741258742 | 523 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **closewidgetpopupsetting** | Text | No | Category | 1.7874125874125875 chars | - | 4 | Reference to closewgetpopupsetting | Required | Not Null, Foreign Key (likely) | Categorical (4 categories) |
| **configsetting** | Text | No | - | 175.52027972027972 chars | - | 130 | Configsetting | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 715 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 57.8%) | - | 191 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 715 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **feature_flags** | Float | No | - | 0.0 to 3.0 | 2.8965034965034966 | 4 | Feature Flags | Numeric; Required | Not Null | Enum-like (4 values) |
| **firsttimepopupsetting** | Text | No | - | 16.836363636363636 chars | - | 40 | Firsttimepopupsetting | Required | Not Null | Variable |
| **hmac_token** | Text | No | - | 24.0 chars | - | 715 | Authentication or access token | Required | Not Null | Variable |
| **homepopupsetting** | Text | No | Category | 2.9944055944055945 chars | - | 12 | Homepopupsetting | Required | Not Null | Variable |
| **phone** | Text | No | - | 0.7846153846153846 chars | - | 45 | Phone | Required | Not Null | Variable |
| **pre_chat_form_enabled** | Integer | No | Category | 0.0 to 1.0 | 0.043356643356643354 | 2 | Pre Chat Form Enabled | Numeric; Required | Not Null | Enum-like (2 values) |
| **pre_chat_form_options** | Text | No | SerializedJSON | 7.321678321678322 chars | - | 30 | Pre Chat Form Options | Required | Not Null | Variable |
| **reply_time** | Float | No | - | 0.0 to 3.0 | 0.04055944055944056 | 3 | Reply Time | Numeric; Required | Not Null | Enum-like (3 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **unreadsetting** | Text | No | Category | 0.24055944055944056 chars | - | 4 | Unreadsetting | Required | Not Null | Categorical (4 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 603 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **website_token** | Text | No | - | 24.0 chars | - | 715 | Authentication or access token | Required | Not Null | Variable |
| **website_url** | Text | No | URL | 53.31188811188811 chars | - | 650 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **welcome_tagline** | Text | No | - | 2.802797202797203 chars | - | 60 | Welcome Tagline | Required | Not Null | Variable |
| **welcome_title** | Text | No | Title | 1.8447552447552447 chars | - | 68 | Welcome Title | Required | Not Null | Variable |
| **widget_color** | Text | No | - | 7.0 chars | - | 114 | Reference to wget color | Required | Not Null, Foreign Key (likely) | Variable |
| **widget_zindex** | Float | Yes | - | 98.0 to 2,147,483,001.0 (Null: 0.1%) | 2,104,976,684.3753502 | 14 | Reference to wget zindex | Numeric | Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>68. postgres_conv_channel_zokos</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`, `integrations`, `channels`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_channel_zokos`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 58.0 to 20,465.0 | 10,330.0 | 3 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (3 values) |
| **auth_token** | Text | No | Category | 36.0 chars | - | 3 | Authentication or access token | Required | Not Null | Categorical (3 categories) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 4 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 50.0%) | - | 3 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 4 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Categorical (4 categories) |
| **phone_number** | Text | No | Category | 12.0 chars | - | 4 | Phone Number | Required | Not Null | Categorical (4 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 4 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>69. postgres_conv_contact_inboxes</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`, `customer-data`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 245

### contact_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,833

### eventn_ctx_event_id` → Related table (inferred)
- `inbox_id` → `postgres_inboxes.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_contact_inboxes`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 245 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **contact_id** | Float | No | - | 9,774,981.0 to 81,341,599.0 | 77,787,210.27320006 | 9,991 | Reference to contact | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,833 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **hmac_verified** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Hmac Verified | Numeric; Required | Not Null | Enum-like (1 values) |
| **inbox_id** | Float | No | - | 73.0 to 33,788.0 | 17,414.077100000006 | 446 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **source_id** | Text | No | Source | 14.6043 chars | - | 10,000 | Reference to source | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,833 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>70. postgres_conv_contact_labels</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`, `labels`, `customer-data`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### contact_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,986

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_contact_labels`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **contact_id** | Float | No | - | 31,253,478.0 to 94,357,834.0 | 82,016,630.60190763 | 1,973 | Reference to contact | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1,986 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 1,992 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **label_id** | Float | No | - | 60,424.0 to 274,934.0 | 263,718.3458835342 | 32 | Reference to label | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 1,986 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>71. postgres_conv_conversation_analytics</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Analytics and metrics table for reporting purposes.

**Owner/Maintainer:** Conversations Team

**Tags:** `analytics`, `conversations`, `reporting`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 591

### account_id` → `postgres_accounts.id` (inferred)
- `adjusted_company_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 5,100.78
- **Average:** 281.836265060241
- **Distinct Values:** 600
- **Null %:** 90.9%

### adjusted_company_resolution_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 14,814.61
- **Average:** 92.14095195530727
- **Distinct Values:** 881
- **Null %:** 55.2%

### adjusted_open_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 2,175
- **Null %:** 71.5%

### agent_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 22.0
- **Average:** 0.3357
- **Distinct Values:** 22

### average_wait_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### bot_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 1,440.12
- **Average:** 4.269714673913043
- **Distinct Values:** 47
- **Null %:** 77.9%

### bot_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 20.0
- **Average:** 0.4839
- **Distinct Values:** 18

### company_frt

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 5,108.45
- **Average:** 315.7605366922234
- **Distinct Values:** 638
- **Null %:** 90.9%

### company_resolution_time

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 14,814.61
- **Average:** 100.17237541899442
- **Distinct Values:** 911
- **Null %:** 55.2%

### contact_turns

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 30.0
- **Average:** 1.0303
- **Distinct Values:** 26

### conv_open_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 2,522
- **Null %:** 71.5%

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,498

### csat_sent

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0023
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)
- `first_agent_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 4,847
- **Null %:** 35.7%

### first_assigned_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1,526
- **Null %:** 82.2%

### first_assignee_id` → Related table (inferred)
- `first_bot_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 2,067
- **Null %:** 77.9%

### first_contact_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 4,474
- **Null %:** 47.4%

### first_opened_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### inbox_id` → `postgres_inboxes.id` (inferred)
- `is_handled_by_bot

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.3102
- **Distinct Values:** 2

### is_handoff

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0911
- **Distinct Values:** 2

### is_outbound

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.5987
- **Distinct Values:** 2

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.4323
- **Distinct Values:** 2

### is_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.4475
- **Distinct Values:** 2

### last_agent_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,677
- **Null %:** 35.7%

### last_bot_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 2,119
- **Null %:** 77.9%

### last_contact_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 4,683
- **Null %:** 47.4%

### last_resolution_assignee_id` → Related table (inferred)
- `last_resolution_message_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 4,150
- **Null %:** 55.2%

### last_resolution_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 4,272
- **Null %:** 55.2%

### manual_agent_handoff

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0059
- **Distinct Values:** 2

### manual_handoff_agent_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_conversation_analytics`
- **Total Columns:** 44

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 591 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 11.0 to 27,084.0 | 8,592.1696 | 237 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **adjusted_company_frt** | Float | Yes | - | 0.0 to 5,100.78 (Null: 90.9%) | 281.836265060241 | 600 | Adjusted Company Frt | Numeric | None | Variable |
| **adjusted_company_resolution_time** | Float | Yes | - | 0.0 to 14,814.61 (Null: 55.2%) | 92.14095195530727 | 881 | Adjusted Company Resolution Time | Numeric | None | Variable |
| **adjusted_open_time** | DateTime | Yes | - | - (Null: 71.5%) | - | 2,175 | Adjusted Open Time | Valid ISO 8601 datetime | None | Variable |
| **agent_turns** | Float | No | - | 0.0 to 22.0 | 0.3357 | 22 | Agent Turns | Numeric; Required | Not Null | Variable |
| **average_wait_time** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Average Wait Time | Numeric | None | Enum-like (1 values) |
| **bot_frt** | Float | Yes | - | 0.0 to 1,440.12 (Null: 77.9%) | 4.269714673913043 | 47 | Bot Frt | Numeric | None | Variable |
| **bot_turns** | Float | No | - | 0.0 to 20.0 | 0.4839 | 18 | Bot Turns | Numeric; Required | Not Null | Variable |
| **company_frt** | Float | Yes | - | 0.0 to 5,108.45 (Null: 90.9%) | 315.7605366922234 | 638 | Company Frt | Numeric | None | Variable |
| **company_resolution_time** | Float | Yes | - | 0.0 to 14,814.61 (Null: 55.2%) | 100.17237541899442 | 911 | Company Resolution Time | Numeric | None | Variable |
| **contact_turns** | Float | No | - | 0.0 to 30.0 | 1.0303 | 26 | Contact Turns | Numeric; Required | Not Null | Variable |
| **conv_open_time** | DateTime | Yes | - | - (Null: 71.5%) | - | 2,522 | Conv Open Time | Valid ISO 8601 datetime | None | Variable |
| **conversation_id** | Float | No | - | 65,984,845.0 to 74,425,472.0 | 72,896,029.515 | 10,000 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 6,498 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **csat_sent** | Integer | No | Category | 0.0 to 1.0 | 0.0023 | 2 | Csat Sent | Numeric; Required | Not Null | Enum-like (2 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_agent_frt** | Float | Yes | - | 0.0 to 13,319.51 (Null: 90.9%) | 250.06490690032857 | 491 | First Agent Frt | Numeric | None | Variable |
| **first_agent_message_time** | DateTime | Yes | - | - (Null: 35.7%) | - | 4,847 | First Agent Message Time | Valid ISO 8601 datetime | None | Variable |
| **first_assigned_time** | DateTime | Yes | - | - (Null: 82.2%) | - | 1,526 | First Assigned Time | Valid ISO 8601 datetime | None | Variable |
| **first_assignee_id** | Float | Yes | - | 1.0 to 50,407.0 (Null: 82.2%) | 29,679.23085585586 | 400 | Reference to first assignee | Numeric | Foreign Key (likely) | Variable |
| **first_bot_message_time** | DateTime | Yes | - | - (Null: 77.9%) | - | 2,067 | First Bot Message Time | Valid ISO 8601 datetime | None | Variable |
| **first_contact_message_time** | DateTime | Yes | - | - (Null: 47.4%) | - | 4,474 | First Contact Message Time | Valid ISO 8601 datetime | None | Variable |
| **first_opened_at** | DateTime | Yes | - | - (Null: 100.0%) | - | 1 | First Opened At | Valid ISO 8601 datetime | None | Variable |
| **inbox_id** | Float | No | - | 115.0 to 33,610.0 | 14,385.466000000006 | 449 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **is_handled_by_bot** | Integer | No | Category | 0.0 to 1.0 | 0.3102 | 2 | Is Handled By Bot | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_handoff** | Integer | No | Category | 0.0 to 1.0 | 0.0911 | 2 | Is Handoff | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_outbound** | Integer | No | Category | 0.0 to 1.0 | 0.5987 | 2 | Is Outbound | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_outside_working_hours** | Integer | No | Category | 0.0 to 1.0 | 0.4323 | 2 | Reference to is outse working hours | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **is_resolved** | Integer | No | Category | 0.0 to 1.0 | 0.4475 | 2 | Is Resolved | Numeric; Required | Not Null | Enum-like (2 values) |
| **last_agent_message_time** | DateTime | Yes | - | - (Null: 35.7%) | - | 5,677 | Last Agent Message Time | Valid ISO 8601 datetime | None | Variable |
| **last_bot_message_time** | DateTime | Yes | - | - (Null: 77.9%) | - | 2,119 | Last Bot Message Time | Valid ISO 8601 datetime | None | Variable |
| **last_contact_message_time** | DateTime | Yes | - | - (Null: 47.4%) | - | 4,683 | Last Contact Message Time | Valid ISO 8601 datetime | None | Variable |
| **last_resolution_assignee_id** | Float | Yes | - | 1.0 to 50,192.0 (Null: 84.3%) | 30,381.87300574346 | 374 | Reference to last resolution assignee | Numeric | Foreign Key (likely) | Variable |
| **last_resolution_message_time** | DateTime | Yes | - | - (Null: 55.2%) | - | 4,150 | Last Resolution Message Time | Valid ISO 8601 datetime | None | Variable |
| **last_resolution_time** | DateTime | Yes | - | - (Null: 55.2%) | - | 4,272 | Last Resolution Time | Valid ISO 8601 datetime | None | Variable |
| **manual_agent_handoff** | Integer | No | Category | 0.0 to 1.0 | 0.0059 | 2 | Manual Agent Handoff | Numeric; Required | Not Null | Enum-like (2 values) |
| **manual_handoff_agent_id** | Float | Yes | - | 327.0 to 49,924.0 (Null: 99.4%) | 23,356.28813559322 | 15 | Reference to manual handoff agent | Numeric | Foreign Key (likely) | Variable |
| **outbound_status** | Float | Yes | - | 0.0 to 3.0 (Null: 1.2%) | 0.7015182186234818 | 4 | Status or state of record | Numeric | None | Enum-like (4 values) |
| **overall_resolution_time** | Float | Yes | - | 0.0 to 89,655.04 (Null: 55.2%) | 365.46092960893856 | 1,936 | Overall Resolution Time | Numeric | None | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Float | No | - | 0.0 to 6.0 | 3.9732 | 7 | Status or state of record | Numeric; Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 8,048 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>72. postgres_conv_conversations</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 306

### account_id` → `postgres_accounts.id` (inferred)
- `additional_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 42.5171 chars
- **Distinct Values:** 621

### agent_last_seen_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1,193
- **Null %:** 87.9%

### alert

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0015
- **Distinct Values:** 2

### alert_dispatch_id` → Related table (inferred)
- `assigned_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### assigned_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0063 chars
- **Distinct Values:** 3

### assigned_by_resource_id` → Related table (inferred)
- `assignee_id` → Related table (inferred)
- `assignee_version

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### close_dispatch_id` → Related table (inferred)
- `closed_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0086 chars
- **Distinct Values:** 3

### contact_id` → Related table (inferred)
- `contact_inbox_id` → `postgres_inboxes.id` (inferred)
- `contact_last_seen_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 285
- **Null %:** 97.1%

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,089

### crm_ticket_id` → Related table (inferred)
- `display_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)
- `frt_due

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### identifier

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0526 chars
- **Distinct Values:** 3

### in_reply_to_email

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### inbox_id` → `postgres_inboxes.id` (inferred)
- `is_conv_marketing

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### is_primary

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### last_activity_at

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 7,750

### locked

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### messages_count

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### new_filter

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### nrt_due

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### opened_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 211
- **Null %:** 97.9%

### previous_assignee_id` → Related table (inferred)
- `previous_label_list

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 6.9011 chars
- **Distinct Values:** 259

### primary_conversation_id` → Related table (inferred)
- `rasa_conv_id` → Related table (inferred)
- `resolution_due

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### resolved_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0095 chars
- **Distinct Values:** 3

### sla_policy_id` → Related table (inferred)
- `sla_tracking_started_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### starred

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0006
- **Distinct Values:** 2

### status

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 6.0
- **Average:** 3.009
- **Distinct Values:** 5

### status_changed_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 3
- **Null %:** 100.0%

### team_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_conversations`
- **Total Columns:** 51

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 306 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 524.0 | 66.68900000000001 | 67 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **additional_attributes** | Text | No | SerializedJSON | 42.5171 chars | - | 621 | Additional Attributes | Required | Not Null | Variable |
| **agent_last_seen_at** | DateTime | Yes | - | - (Null: 87.9%) | - | 1,193 | Agent Last Seen At | Valid ISO 8601 datetime | None | Variable |
| **alert** | Integer | No | Category | 0.0 to 1.0 | 0.0015 | 2 | Alert | Numeric; Required | Not Null | Enum-like (2 values) |
| **alert_dispatch_id** | Float | No | - | 0.0 to 61.0 | 0.8587 | 22 | Reference to alert dispatch | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **assigned_at** | DateTime | Yes | - | - (Null: 100.0%) | - | 1 | Assigned At | Valid ISO 8601 datetime | None | Variable |
| **assigned_by** | Text | No | Category | 0.0063 chars | - | 3 | Assigned By | Required | Not Null | Categorical (3 categories) |
| **assigned_by_resource_id** | Float | Yes | - | 1,019.0 to 1,860.0 (Null: 100.0%) | 1,350.6666666666667 | 4 | Reference to assigned by resource | Numeric | Foreign Key (likely) | Enum-like (4 values) |
| **assignee_id** | Float | Yes | - | 3.0 to 4,644.0 (Null: 88.6%) | 522.6980633802817 | 143 | Reference to assignee | Numeric | Foreign Key (likely) | Variable |
| **assignee_version** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Assignee Version | Numeric; Required | Not Null | Enum-like (1 values) |
| **close_dispatch_id** | Float | No | - | 0.0 to 61.0 | 0.8587 | 22 | Reference to close dispatch | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **closed_by** | Text | No | Category | 0.0086 chars | - | 3 | Closed By | Required | Not Null | Categorical (3 categories) |
| **contact_id** | Float | Yes | - | 303,478.0 to 78,197,325.0 | 27,008,842.451800004 | 9,090 | Reference to contact | Numeric | Foreign Key (likely) | Variable |
| **contact_inbox_id** | Float | Yes | - | 302,880.0 to 31,883,989.0 | 27,095,821.66839999 | 9,119 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **contact_last_seen_at** | DateTime | Yes | - | - (Null: 97.1%) | - | 285 | Contact Last Seen At | Valid ISO 8601 datetime | None | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 7,089 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **crm_ticket_id** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Reference to crm ticket | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **display_id** | Float | No | - | 4,522.0 to 10,767,176.0 | 3,813,587.8193 | 9,999 | Reference to display | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **external_uuid** | Text | No | Category | 0.0 chars | - | 1 | Reference to external uu | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **facebook_post_id** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Reference to facebook post | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **frt_due** | DateTime | Yes | - | - (Null: 100.0%) | - | 1 | Frt Due | Valid ISO 8601 datetime | None | Variable |
| **identifier** | Text | No | Category | 0.0526 chars | - | 3 | Reference to entifier | Required | Not Null, Foreign Key (likely) | Categorical (3 categories) |
| **in_reply_to_email** | Text | No | Category | 0.0 chars | - | 1 | Email address | Required | Not Null | Categorical (1 categories) |
| **inbox_id** | Float | No | - | 8.0 to 727.0 | 264.88740000000007 | 115 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **is_conv_marketing** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Is Conv Marketing | Numeric; Required | Not Null | Enum-like (1 values) |
| **is_primary** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Is Primary | Numeric | None | Enum-like (1 values) |
| **last_activity_at** | DateTime | No | - | - | - | 7,750 | Last Activity At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **locked** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Locked | Numeric; Required | Not Null | Enum-like (1 values) |
| **messages_count** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Count of messages | Numeric | None | Enum-like (1 values) |
| **new_filter** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | New Filter | Numeric; Required | Not Null | Enum-like (1 values) |
| **nrt_due** | DateTime | Yes | - | - (Null: 100.0%) | - | 1 | Nrt Due | Valid ISO 8601 datetime | None | Variable |
| **opened_at** | DateTime | Yes | - | - (Null: 97.9%) | - | 211 | Opened At | Valid ISO 8601 datetime | None | Variable |
| **previous_assignee_id** | Float | Yes | - | 1,019.0 to 1,860.0 (Null: 100.0%) | 1,439.5 | 3 | Reference to previous assignee | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **previous_label_list** | Text | No | SerializedJSON | 6.9011 chars | - | 259 | Previous Label List | Required | Not Null | Variable |
| **primary_conversation_id** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Reference to primary conversation | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **rasa_conv_id** | Float | No | - | 1.0 to 1.0 | 1.0 | 1 | Reference to rasa conv | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **resolution_due** | DateTime | Yes | - | - (Null: 100.0%) | - | 1 | Resolution Due | Valid ISO 8601 datetime | None | Variable |
| **resolved_by** | Text | No | Category | 0.0095 chars | - | 3 | Resolved By | Required | Not Null | Categorical (3 categories) |
| **sla_policy_id** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Reference to sla policy | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **sla_tracking_started_at** | DateTime | Yes | CreationTimestamp | - (Null: 100.0%) | - | 1 | Sla Tracking Started At | Valid ISO 8601 datetime | None | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **starred** | Integer | No | Category | 0.0 to 1.0 | 0.0006 | 2 | Starred | Numeric; Required | Not Null | Enum-like (2 values) |
| **status** | Float | No | - | 1.0 to 6.0 | 3.009 | 5 | Status or state of record | Numeric; Required | Not Null | Enum-like (5 values) |
| **status_changed_at** | DateTime | Yes | - | - (Null: 100.0%) | - | 3 | Status or state of record | Valid ISO 8601 datetime | None | Variable |
| **team_id** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Reference to team | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **unread** | Integer | No | Category | 0.0 to 1.0 | 0.8911 | 2 | Unread | Numeric; Required | Not Null | Enum-like (2 values) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 7,842 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **uuid** | Text | No | - | 36.0 chars | - | 10,000 | Reference to uu | Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>73. postgres_conv_shopify_availed_trials</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`, `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_shopify_availed_trials`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 168 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 168 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **shop_domain** | Text | No | - | 12.398809523809524 chars | - | 168 | Shop Domain | Required | Not Null | Variable |
| **shop_url** | Text | No | URL | 26.154761904761905 chars | - | 168 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **trial_end** | DateTime | No | - | - | - | 131 | Trial End | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **trial_start** | DateTime | No | CreationTimestamp | - | - | 131 | Trial Start | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 168 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>74. postgres_conv_subscriptions</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `billing`, `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `admin_cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 759

### current_term_end

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 136
- **Null %:** 25.6%

### current_term_start

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 44
- **Null %:** 25.6%

### eventn_ctx_event_id` → Related table (inferred)
- `plan_id` → Related table (inferred)
- `platform

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.6956521739130435
- **Distinct Values:** 2

### platform_subscription_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_subscriptions`
- **Total Columns:** 22

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,510.0 | 14,018.546772068512 | 499 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **admin_cancelled** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Admin Cancelled | Numeric; Required | Not Null | Enum-like (1 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 759 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **current_term_end** | DateTime | Yes | - | - (Null: 25.6%) | - | 136 | Current Term End | Valid ISO 8601 datetime | None | Variable |
| **current_term_start** | DateTime | Yes | CreationTimestamp | - (Null: 25.6%) | - | 44 | Current Term Start | Valid ISO 8601 datetime | None | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 759 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **invoice_close_date** | DateTime | Yes | - | - (Null: 58.6%) | - | 288 | Invoice Close Date | Valid ISO 8601 datetime | None | Variable |
| **invoice_id** | Float | Yes | - | 0.0 to 0.0 (Null: 35.0%) | 0.0 | 2 | Reference to invoice | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **plan_id** | Float | No | - | 1.0 to 811.0 | 316.26218708827406 | 41 | Reference to plan | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **platform** | Float | No | - | 0.0 to 1.0 | 0.6956521739130435 | 2 | Platform | Numeric; Required | Not Null | Enum-like (2 values) |
| **platform_subscription_id** | Text | No | Subscription | 9.9433465085639 chars | - | 570 | Reference to platform subscription | Required | Not Null, Foreign Key (likely) | Variable |
| **previous_billing_end** | DateTime | Yes | - | - (Null: 35.2%) | - | 15 | Previous Billing End | Valid ISO 8601 datetime | None | Variable |
| **previous_billing_start** | DateTime | Yes | CreationTimestamp | - (Null: 35.2%) | - | 16 | Previous Billing Start | Valid ISO 8601 datetime | None | Variable |
| **shopify_confirmation_url** | Text | No | URL | 12.395256916996047 chars | - | 42 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **shopify_invoice_pending** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Shopify Invoice Pending | Numeric; Required | Not Null | Enum-like (1 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Float | No | - | 0.0 to 7.0 | 2.8194993412384717 | 5 | Status or state of record | Numeric; Required | Not Null | Enum-like (5 values) |
| **trial_end** | DateTime | Yes | - | - (Null: 75.0%) | - | 166 | Trial End | Valid ISO 8601 datetime | None | Variable |
| **trial_start** | DateTime | Yes | CreationTimestamp | - (Null: 75.0%) | - | 134 | Trial Start | Valid ISO 8601 datetime | None | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 512 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>75. postgres_conv_taggings</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`, `labels`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No

### context

- **Type:** `Text`
- **Nullable:** No

### created_at

- **Type:** `DateTime`
- **Nullable:** No

### eventn_ctx_event_id` → Related table (inferred)
- `taggable_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_taggings`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | - | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **context** | Text | No | - | - | - | - | Context | Required | Not Null | Categorical (0 categories) |
| **created_at** | DateTime | No | - | - | - | - | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | - | - | - | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Categorical (0 categories) |
| **src** | Text | No | - | - | - | - | Source system identifier | Required | Not Null | Categorical (0 categories) |
| **tag_id** | Float | No | - | - | - | - | Reference to tag | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **taggable_id** | Float | No | - | - | - | - | Reference to taggable | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **taggable_type** | Text | No | - | - | - | - | Type or category classification | Required | Not Null | Categorical (0 categories) |

</details>

---

<details>
<summary><h2>76. postgres_conv_team_members</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 173

### eventn_ctx_event_id` → Related table (inferred)
- `updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 173

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_team_members`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 173 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 358 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **team_id** | Float | No | - | 2.0 to 2,090.0 | 1,725.9804469273743 | 129 | Reference to team | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 173 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 1.0 to 51,591.0 | 36,598.874301675976 | 310 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>77. postgres_conv_webhook_watchers</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `webhooks`, `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Nullable:** No

### event_name

- **Type:** `Text`
- **Nullable:** No

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_webhook_watchers`
- **Total Columns:** 15

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | - | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | - | - | - | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **created_at** | DateTime | No | - | - | - | - | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **event_name** | Text | No | - | - | - | - | Event Name | Required | Not Null | Categorical (0 categories) |
| **eventn_ctx_event_id** | Text | No | - | - | - | - | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Categorical (0 categories) |
| **failure_reason** | Text | No | - | - | - | - | Failure Reason | Required | Not Null | Categorical (0 categories) |
| **object_id** | Float | No | - | - | - | - | Reference to object | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **object_type** | Text | No | - | - | - | - | Type or category classification | Required | Not Null | Categorical (0 categories) |
| **src** | Text | No | - | - | - | - | Source system identifier | Required | Not Null | Categorical (0 categories) |
| **status** | Float | No | - | - | - | - | Status or state of record | Numeric; Required | Not Null | Enum-like (0 values) |
| **success_reason** | Text | No | - | - | - | - | Success Reason | Required | Not Null | Categorical (0 categories) |
| **updated_at** | DateTime | No | - | - | - | - | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **webhook_payload** | Text | No | - | - | - | - | Webhook Payload | Required | Not Null | Categorical (0 categories) |
| **webhook_url** | Text | No | - | - | - | - | URL or web address | Required | Not Null | Categorical (0 categories) |

</details>

---

<details>
<summary><h2>78. postgres_conv_working_hour_slots</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No

### close_hour

- **Type:** `Float`
- **Nullable:** No

### close_minutes

- **Type:** `Float`
- **Nullable:** No

### created_at

- **Type:** `DateTime`
- **Nullable:** No

### eventn_ctx_event_id` → Related table (inferred)
- `open_minutes

- **Type:** `Float`
- **Nullable:** No

### src

- **Type:** `Text`
- **Nullable:** No

### updated_at

- **Type:** `DateTime`
- **Nullable:** No

### working_hour_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conv_working_hour_slots`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | - | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **close_hour** | Float | No | - | - | - | - | Close Hour | Numeric; Required | Not Null | Enum-like (0 values) |
| **close_minutes** | Float | No | - | - | - | - | Close Minutes | Numeric; Required | Not Null | Enum-like (0 values) |
| **created_at** | DateTime | No | - | - | - | - | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | - | - | - | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Categorical (0 categories) |
| **open_hour** | Float | No | - | - | - | - | Open Hour | Numeric; Required | Not Null | Enum-like (0 values) |
| **open_minutes** | Float | No | - | - | - | - | Open Minutes | Numeric; Required | Not Null | Enum-like (0 values) |
| **src** | Text | No | - | - | - | - | Source system identifier | Required | Not Null | Categorical (0 categories) |
| **updated_at** | DateTime | No | - | - | - | - | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **working_hour_id** | Float | No | - | - | - | - | Reference to working hour | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |

</details>

---

<details>
<summary><h2>79. postgres_conversation_labels</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`, `labels`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 7,503

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,983

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conversation_labels`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 7,503 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 41,669.0 to 73,521,321.0 | 40,218,843.0449 | 9,995 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,983 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,998 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **label_id** | Float | No | - | 7.0 to 201,372.0 | 91,082.4561 | 4,001 | Reference to label | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,983 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>80. postgres_conversation_labels_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_conversation_labels. Contains unprocessed data before transformation.

**Owner/Maintainer:** Conversations Team

**Tags:** `raw-data`, `staging`, `conversations`, `labels`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,287

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,881

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conversation_labels_raw`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 3,287 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 8,454,268.0 to 133,947,240.0 | 132,681,689.8166 | 9,820 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,881 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **label_id** | Float | No | - | 68.0 to 374,486.0 | 204,603.94420000003 | 2,873 | Reference to label | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,881 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>81. postgres_conversation_trackers</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,285

### account_id` → `postgres_accounts.id` (inferred)
- `change_performed_via

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.7488 chars
- **Distinct Values:** 2

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,107

### current_assignee_id` → Related table (inferred)
- `current_status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.2435 chars
- **Distinct Values:** 7

### duration_in_previous_event

- **Type:** `Float`
- **Semantic Type:** `Duration`
- **Nullable:** No
- **Range:** 0.0 to 78,338.0
- **Average:** 1,622.4434
- **Distinct Values:** 1,350

### event_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 14.1762 chars
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)
- `previous_assignee_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_conversation_trackers`
- **Total Columns:** 16

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1,285 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 135.0 | 113.4611 | 8 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **change_performed_via** | Text | No | Category | 5.7488 chars | - | 2 | Change Performed Via | Required | Not Null | Categorical (2 categories) |
| **conversation_id** | Float | No | - | 8,611,272.0 to 101,663,003.0 | 99,387,648.97439997 | 6,932 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,107 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **current_assignee_id** | Float | Yes | - | 1.0 to 51,659.0 (Null: 80.3%) | 24,581.208016235414 | 33 | Reference to current assignee | Numeric | Foreign Key (likely) | Variable |
| **current_status** | Text | No | Category | 6.2435 chars | - | 7 | Status or state of record | Required | Not Null | Categorical (7 categories) |
| **duration_in_previous_event** | Float | No | Duration | 0.0 to 78,338.0 | 1,622.4434 | 1,350 | Duration In Previous Event | Numeric; Required | Not Null | Variable |
| **event_type** | Text | No | Category | 14.1762 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **performer_id** | Float | Yes | - | 989.0 to 50,258.0 (Null: 87.4%) | 26,083.299363057326 | 15 | Reference to performer | Numeric | Foreign Key (likely) | Variable |
| **previous_assignee_id** | Float | Yes | - | 1.0 to 51,270.0 (Null: 96.5%) | 24,180.654285714285 | 21 | Reference to previous assignee | Numeric | Foreign Key (likely) | Variable |
| **previous_status** | Text | No | Category | 5.9234 chars | - | 7 | Status or state of record | Required | Not Null | Categorical (7 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,107 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>82. postgres_csat_survey_responses</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Customer Satisfaction (CSAT) survey data.

**Owner/Maintainer:** Platform Team

**Tags:** `feedback`, `csat`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,700

### account_id` → `postgres_accounts.id` (inferred)
- `agent_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.4587 chars
- **Distinct Values:** 200

### assigned_agent_id` → Related table (inferred)
- `contact_id` → Related table (inferred)
- `contact_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.35 chars
- **Distinct Values:** 8,568

### contact_phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.6369 chars
- **Distinct Values:** 8,296

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,977

### csat_message_created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,848

### csat_scale

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 5.0 to 5.0
- **Average:** 5.0
- **Distinct Values:** 1

### eventn_ctx_event_id` → Related table (inferred)
- `inbox_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.8285 chars
- **Distinct Values:** 56

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1757
- **Distinct Values:** 2

### message_id` → `postgres_inboxes.id` (inferred)
- `rating

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** No
- **Range:** 1.0 to 5.0
- **Average:** 3.6101
- **Distinct Values:** 5

### resolved_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.6406 chars
- **Distinct Values:** 3

### response_conversation_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_csat_survey_responses`
- **Total Columns:** 23

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1,700 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,116.0 | 7,436.8793 | 59 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **agent_name** | Text | No | - | 6.4587 chars | - | 200 | Agent Name | Required | Not Null | Variable |
| **assigned_agent_id** | Float | Yes | - | 216.0 to 50,746.0 (Null: 22.9%) | 37,931.17832576249 | 274 | Reference to assigned agent | Numeric | Foreign Key (likely) | Variable |
| **contact_id** | Float | No | - | 3,029,371.0 to 84,233,061.0 | 77,832,363.01089995 | 9,681 | Reference to contact | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **contact_name** | Text | No | - | 11.35 chars | - | 8,568 | Contact Name | Required | Not Null | Variable |
| **contact_phone_number** | Text | No | - | 10.6369 chars | - | 8,296 | Contact Phone Number | Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 10,013,014.0 to 84,937,377.0 | 81,259,009.69500001 | 10,000 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,977 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **csat_message_created_at** | DateTime | No | CreationTimestamp | - | - | 9,848 | Csat Message Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **csat_scale** | Float | Yes | - | 5.0 to 5.0 | 5.0 | 1 | Csat Scale | Numeric | None | Enum-like (1 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **feedback_message** | Text | No | - | 22.5787 chars | - | 4,322 | Feedback Message | Required | Not Null | Variable |
| **inbox_id** | Float | No | - | 115.0 to 33,818.0 | 13,194.6676 | 87 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_name** | Text | No | - | 13.8285 chars | - | 56 | Inbox Name | Required | Not Null | Variable |
| **is_outside_working_hours** | Integer | No | Category | 0.0 to 1.0 | 0.1757 | 2 | Reference to is outse working hours | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **message_id** | Float | No | - | 575,103,467.0 to 606,026,765.0 | 590,376,098.4548 | 9,999 | Reference to message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **rating** | Float | No | Score | 1.0 to 5.0 | 3.6101 | 5 | Rating | Numeric; Required | Not Null | Enum-like (5 values) |
| **resolved_by** | Text | No | Category | 3.6406 chars | - | 3 | Resolved By | Required | Not Null | Categorical (3 categories) |
| **response_conversation_id** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Reference to response conversation | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,950 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>83. postgres_csat_survey_responses_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_csat_survey_responses. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `csat`, `staging`, `feedback`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6

### account_id` → `postgres_accounts.id` (inferred)
- `agent_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.5282 chars
- **Distinct Values:** 203

### assigned_agent_id` → Related table (inferred)
- `contact_id` → Related table (inferred)
- `contact_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.3095 chars
- **Distinct Values:** 8,531

### contact_phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.7166 chars
- **Distinct Values:** 8,353

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,892

### csat_message_created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,845

### csat_scale

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 5.0 to 5.0
- **Average:** 5.0
- **Distinct Values:** 1

### eventn_ctx_event_id` → Related table (inferred)
- `inbox_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.9501 chars
- **Distinct Values:** 55

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1701
- **Distinct Values:** 2

### message_id` → `postgres_inboxes.id` (inferred)
- `rating

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** No
- **Range:** 1.0 to 5.0
- **Average:** 3.6692
- **Distinct Values:** 5

### resolved_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.6527 chars
- **Distinct Values:** 3

### response_conversation_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_csat_survey_responses_raw`
- **Total Columns:** 23

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 6 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 24,887.0 | 1,649.2214999999999 | 63 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **agent_name** | Text | No | - | 6.5282 chars | - | 203 | Agent Name | Required | Not Null | Variable |
| **assigned_agent_id** | Float | Yes | - | 1.0 to 46,656.0 (Null: 37.6%) | 26,439.395028067363 | 207 | Reference to assigned agent | Numeric | Foreign Key (likely) | Variable |
| **contact_id** | Float | No | - | 3,029,608.0 to 68,022,360.0 | 63,962,974.1846 | 9,422 | Reference to contact | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **contact_name** | Text | No | - | 11.3095 chars | - | 8,531 | Contact Name | Required | Not Null | Variable |
| **contact_phone_number** | Text | No | - | 10.7166 chars | - | 8,353 | Contact Phone Number | Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 19,397,853.0 to 65,937,270.0 | 63,137,946.1795 | 9,984 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,892 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **csat_message_created_at** | DateTime | No | CreationTimestamp | - | - | 9,845 | Csat Message Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **csat_scale** | Float | Yes | - | 5.0 to 5.0 | 5.0 | 1 | Csat Scale | Numeric | None | Enum-like (1 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **feedback_message** | Text | No | - | 18.4477 chars | - | 3,846 | Feedback Message | Required | Not Null | Variable |
| **inbox_id** | Float | No | - | 115.0 to 32,105.0 | 4,186.2681 | 80 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_name** | Text | No | - | 13.9501 chars | - | 55 | Inbox Name | Required | Not Null | Variable |
| **is_outside_working_hours** | Integer | No | Category | 0.0 to 1.0 | 0.1701 | 2 | Reference to is outse working hours | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **message_id** | Float | No | - | 426,412,144.0 to 640,816,234.0 | 431,546,825.2416 | 10,000 | Reference to message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **rating** | Float | No | Score | 1.0 to 5.0 | 3.6692 | 5 | Rating | Numeric; Required | Not Null | Enum-like (5 values) |
| **resolved_by** | Text | No | Category | 3.6527 chars | - | 3 | Resolved By | Required | Not Null | Categorical (3 categories) |
| **response_conversation_id** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Reference to response conversation | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,915 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>84. postgres_ctwa_contact_trackings</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores contact and customer profile data.

**Owner/Maintainer:** Customer Data Team

**Tags:** `customer-data`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `contact_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_ctwa_contact_trackings`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 259.0 to 28,846.0 | 22,046.1299 | 18 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **contact_id** | Float | No | - | 49,786,171.0 to 172,700,220.0 | 169,960,041.2342997 | 9,242 | Reference to contact | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,829 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **ctwa_click_id** | Text | No | - | 134.8444 chars | - | 9,851 | Reference to ctwa click | Required | Not Null, Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **phone_number** | Text | No | - | 11.9953 chars | - | 9,222 | Phone Number | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,829 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>85. postgres_ctwa_contact_trackings_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_ctwa_contact_trackings. Contains unprocessed data before transformation.

**Owner/Maintainer:** Customer Data Team

**Tags:** `raw-data`, `staging`, `customer-data`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `contact_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_ctwa_contact_trackings_raw`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 259.0 to 28,846.0 | 22,046.1299 | 18 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **contact_id** | Float | No | - | 49,786,171.0 to 172,700,220.0 | 169,960,041.2342997 | 9,242 | Reference to contact | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,829 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **ctwa_click_id** | Text | No | - | 134.8444 chars | - | 9,851 | Reference to ctwa click | Required | Not Null, Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **phone_number** | Text | No | - | 11.9953 chars | - | 9,222 | Phone Number | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,829 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>86. postgres_curated_views</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres curated views operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_curated_views`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 13 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **filters** | Text | No | SerializedJSON | 45.07692307692308 chars | - | 13 | Filters | Required | Not Null | Variable |
| **name** | Text | No | Name | 25.692307692307693 chars | - | 13 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 3 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>87. postgres_curated_views_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_curated_views. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_curated_views_raw`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 13 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **filters** | Text | No | SerializedJSON | 45.07692307692308 chars | - | 13 | Filters | Required | Not Null | Variable |
| **name** | Text | No | Name | 25.692307692307693 chars | - | 13 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 3 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>88. postgres_custom_field_inboxes</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages inbox configurations and channel settings.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 150

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 203

### custom_field_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_field_inboxes`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 150 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 203 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **custom_field_id** | Float | No | - | 1.0 to 167.0 | 85.74594594594595 | 151 | Reference to custom field | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 370 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_id** | Float | No | - | 115.0 to 35,527.0 | 30,835.618918918924 | 159 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 203 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>89. postgres_custom_field_inboxes_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_custom_field_inboxes. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 150

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 203

### custom_field_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_field_inboxes_raw`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 150 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 203 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **custom_field_id** | Float | No | - | 1.0 to 167.0 | 85.74594594594595 | 151 | Reference to custom field | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 370 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_id** | Float | No | - | 115.0 to 35,527.0 | 30,835.618918918924 | 159 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 203 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>90. postgres_custom_field_options</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Custom field definitions and values.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 66

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 91

### custom_field_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_field_options`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 66 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 91 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **custom_field_id** | Float | No | - | 4.0 to 163.0 | 105.41333333333333 | 60 | Reference to custom field | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 900 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **position** | Float | Yes | - | 0.0 to 247.0 (Null: 16.5%) | 43.923772609819125 | 249 | Position | Numeric | None | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 80 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **value** | Text | No | - | 26.83888888888889 chars | - | 840 | Value | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>91. postgres_custom_field_options_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_custom_field_options. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 73

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 91

### custom_field_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_field_options_raw`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 73 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 91 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **custom_field_id** | Float | No | - | 4.0 to 163.0 | 102.88246628131022 | 60 | Reference to custom field | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 900 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **position** | Float | Yes | - | 0.0 to 247.0 (Null: 51.0%) | 41.2070805043647 | 249 | Position | Numeric | None | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 89 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **value** | Text | No | - | 26.577071290944122 chars | - | 840 | Value | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>92. postgres_custom_field_values</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Custom field definitions and values.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6,714

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,867

### custom_field_hash

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.0047 chars
- **Distinct Values:** 1,055

### custom_field_id` → Related table (inferred)
- `custom_field_option_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_field_values`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 6,714 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 79,422,859.0 to 134,887,666.0 | 127,751,391.40230003 | 9,399 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,867 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **custom_field_hash** | Text | No | - | 7.0047 chars | - | 1,055 | Custom Field Hash | Required | Not Null | Variable |
| **custom_field_id** | Float | No | - | 1.0 to 36.0 | 31.255400000000005 | 20 | Reference to custom field | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **custom_field_option_id** | Float | Yes | - | 1.0 to 657.0 (Null: 31.4%) | 81.19437563747633 | 48 | Reference to custom field option | Numeric | Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,868 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **value** | Text | No | - | 6.334 chars | - | 1,168 | Value | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>93. postgres_custom_field_values_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_custom_field_values. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,005

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,180

### custom_field_hash

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### custom_field_id` → Related table (inferred)
- `custom_field_option_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_field_values_raw`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 4,005 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 79,422,859.0 to 119,701,527.0 | 117,050,652.7498 | 8,849 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,180 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **custom_field_hash** | Text | No | Category | 0.0 chars | - | 1 | Custom Field Hash | Required | Not Null | Categorical (1 categories) |
| **custom_field_id** | Float | No | - | 1.0 to 50.0 | 40.062799999999996 | 26 | Reference to custom field | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **custom_field_option_id** | Float | Yes | - | 1.0 to 83.0 (Null: 68.4%) | 53.257839721254356 | 36 | Reference to custom field option | Numeric | Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,297 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **value** | Text | No | - | 7.198 chars | - | 5,086 | Value | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>94. postgres_custom_fields</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Custom field definitions and values.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 22

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 30

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 5.766666666666667 chars
- **Distinct Values:** 9

### enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.7333333333333333
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_fields`
- **Total Columns:** 12

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 22 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 54.0 to 28,397.0 | 23,952.166666666668 | 12 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 30 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **description** | Text | No | Description | 5.766666666666667 chars | - | 9 | Description | Required | Not Null | Categorical (9 categories) |
| **enabled** | Integer | No | Category | 0.0 to 1.0 | 0.7333333333333333 | 2 | Enabled | Numeric; Required | Not Null | Enum-like (2 values) |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 30 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **field_type** | Float | No | - | 0.0 to 7.0 | 2.3 | 5 | Type or category classification | Numeric; Required | Not Null | Enum-like (5 values) |
| **mandatory** | Integer | No | Category | 0.0 to 1.0 | 0.5 | 2 | Mandatory | Numeric; Required | Not Null | Enum-like (2 values) |
| **name** | Text | No | Name | 12.6 chars | - | 28 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 28 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>95. postgres_custom_fields_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_custom_fields. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 22

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 30

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 5.766666666666667 chars
- **Distinct Values:** 9

### enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.7333333333333333
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_fields_raw`
- **Total Columns:** 12

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 22 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 54.0 to 28,397.0 | 23,952.166666666668 | 12 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 30 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **description** | Text | No | Description | 5.766666666666667 chars | - | 9 | Description | Required | Not Null | Categorical (9 categories) |
| **enabled** | Integer | No | Category | 0.0 to 1.0 | 0.7333333333333333 | 2 | Enabled | Numeric; Required | Not Null | Enum-like (2 values) |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 30 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **field_type** | Float | No | - | 0.0 to 7.0 | 2.3 | 5 | Type or category classification | Numeric; Required | Not Null | Enum-like (5 values) |
| **mandatory** | Integer | No | Category | 0.0 to 1.0 | 0.5 | 2 | Mandatory | Numeric; Required | Not Null | Enum-like (2 values) |
| **name** | Text | No | Name | 12.6 chars | - | 28 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 28 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>96. postgres_custom_views</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres custom views operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 143

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 240

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_views`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 143 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 240 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 241 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **filters** | Text | No | SerializedJSON | 75.79253112033194 chars | - | 125 | Filters | Required | Not Null | Variable |
| **name** | Text | No | Name | 13.506224066390041 chars | - | 193 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 240 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 1.0 to 53,378.0 | 47,794.041493775934 | 86 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>97. postgres_custom_views_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_custom_views. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 147

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 240

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_custom_views_raw`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 147 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 240 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 241 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **filters** | Text | No | SerializedJSON | 76.052 chars | - | 131 | Filters | Required | Not Null | Variable |
| **name** | Text | No | Name | 13.336 chars | - | 194 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 249 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 1.0 to 53,378.0 | 46,706.024 | 86 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>98. postgres_data_access_logs</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres data access logs operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,520

### accessed_data

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.245019920318725 chars
- **Distinct Values:** 3,077

### accessed_detail

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 4.0
- **Average:** 3.6251358203549437
- **Distinct Values:** 4

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,507

### eventn_ctx_event_id` → Related table (inferred)
- `resource_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.994929373415429 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,507

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_data_access_logs`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 3,520 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **accessed_data** | Text | No | - | 13.245019920318725 chars | - | 3,077 | Accessed Data | Required | Not Null | Variable |
| **accessed_detail** | Float | No | - | 0.0 to 4.0 | 3.6251358203549437 | 4 | Accessed Detail | Numeric; Required | Not Null | Enum-like (4 values) |
| **account_id** | Float | No | - | 56.0 to 28,155.0 | 26,801.998551249548 | 10 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 5,507 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 5,522 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **ip_address** | Text | No | - | 12.032959072799711 chars | - | 136 | Ip Address | Required | Not Null | Variable |
| **resource_id** | Float | Yes | - | 30,475,464.0 to 119,766,189.0 (Null: 0.1%) | 109,886,964.65005437 | 2,862 | Reference to resource | Numeric | Foreign Key (likely) | Variable |
| **resource_type** | Text | No | Category | 6.994929373415429 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 5,507 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 1.0 to 53,150.0 | 50,440.79626946758 | 11 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>99. postgres_data_access_logs_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_data_access_logs. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,520

### accessed_data

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.245019920318725 chars
- **Distinct Values:** 3,077

### accessed_detail

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 4.0
- **Average:** 3.6251358203549437
- **Distinct Values:** 4

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,507

### eventn_ctx_event_id` → Related table (inferred)
- `resource_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.994929373415429 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,507

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_data_access_logs_raw`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 3,520 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **accessed_data** | Text | No | - | 13.245019920318725 chars | - | 3,077 | Accessed Data | Required | Not Null | Variable |
| **accessed_detail** | Float | No | - | 0.0 to 4.0 | 3.6251358203549437 | 4 | Accessed Detail | Numeric; Required | Not Null | Enum-like (4 values) |
| **account_id** | Float | No | - | 56.0 to 28,155.0 | 26,801.998551249548 | 10 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 5,507 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 5,522 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **ip_address** | Text | No | - | 12.032959072799711 chars | - | 136 | Ip Address | Required | Not Null | Variable |
| **resource_id** | Float | Yes | - | 30,475,464.0 to 119,766,189.0 (Null: 0.1%) | 109,886,964.65005437 | 2,862 | Reference to resource | Numeric | Foreign Key (likely) | Variable |
| **resource_type** | Text | No | Category | 6.994929373415429 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 5,507 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 1.0 to 53,150.0 | 50,440.79626946758 | 11 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>100. postgres_fb_account_account</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages account information and configurations.

**Owner/Maintainer:** Accounts/Billing Team

**Tags:** `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 38

### company

- **Type:** `Text`
- **Semantic Type:** `Company`
- **Nullable:** No
- **Avg Length:** 13.973387922210849 chars
- **Distinct Values:** 2,714

### company_logo

- **Type:** `Text`
- **Semantic Type:** `Company`
- **Nullable:** No
- **Avg Length:** 0.01160013647219379 chars
- **Distinct Values:** 3

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,849

### eventn_ctx_event_id` → Related table (inferred)
- `hd_account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_account_account`
- **Total Columns:** 22

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 38 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **company** | Text | No | Company | 13.973387922210849 chars | - | 2,714 | Company | Required | Not Null | Variable |
| **company_logo** | Text | No | Company | 0.01160013647219379 chars | - | 3 | Company Logo | Required | Not Null | Categorical (3 categories) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1,849 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 2,931 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **google_id** | Text | No | Category | 0.057659501876492665 chars | - | 21 | Reference to google | Required | Not Null, Foreign Key (likely) | Variable |
| **grace_added_on** | DateTime | Yes | - | - (Null: 95.0%) | - | 149 | Grace Added On | Valid ISO 8601 datetime | None | Variable |
| **grace_extension** | Integer | No | Category | 0.0 to 1.0 | 0.01501194131695667 | 2 | Grace Extension | Numeric; Required | Not Null | Enum-like (2 values) |
| **hd_account_id** | Float | Yes | - | 1.0 to 28,777.0 (Null: 2.1%) | 20,084.551916376306 | 2,870 | Reference to account | Numeric | Foreign Key (likely) | Variable |
| **is_active** | Integer | No | Category | 0.0 to 1.0 | 0.6618901398839986 | 2 | Is Active | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_enterprise** | Integer | No | Category | 0.0 to 1.0 | 0.016376663254861822 | 2 | Is Enterprise | Numeric; Required | Not Null | Enum-like (2 values) |
| **link_click_attribution_window** | Float | No | - | 1.0 to 240.0 | 24.720914363698398 | 8 | Link Click Attribution Window | Numeric; Required | Not Null | Variable |
| **messages_sent_window** | Float | No | - | 1.0 to 168.0 | 24.454793585806893 | 7 | Messages Sent Window | Numeric; Required | Not Null | Variable |
| **name** | Text | No | Name | 16.365404298874104 chars | - | 2,747 | Human-readable name or title | Required | Not Null | Variable |
| **on_grace_period** | Integer | No | Category | 0.0 to 1.0 | 0.05834186284544524 | 2 | On Grace Period | Numeric; Required | Not Null | Enum-like (2 values) |
| **payment_pending** | Integer | No | Category | 0.0 to 1.0 | 0.03002388263391334 | 2 | Payment Pending | Numeric; Required | Not Null | Enum-like (2 values) |
| **show_link_click_attribution** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Show Link Click Attribution | Numeric; Required | Not Null | Enum-like (1 values) |
| **show_messages_sent** | Integer | No | Category | 0.0 to 1.0 | 0.007505970658478335 | 2 | Show Messages Sent | Numeric; Required | Not Null | Enum-like (2 values) |
| **source** | Text | No | Source | 0.2975093824633231 chars | - | 4 | Source | Required | Not Null | Categorical (4 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **ui_mode** | Text | No | Category | 3.9669054930058 chars | - | 3 | Ui Mode | Required | Not Null | Categorical (3 categories) |

</details>

---

<details>
<summary><h2>101. postgres_fb_account_account_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_fb_account_account. Contains unprocessed data before transformation.

**Owner/Maintainer:** Accounts/Billing Team

**Tags:** `raw-data`, `staging`, `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 38

### company

- **Type:** `Text`
- **Semantic Type:** `Company`
- **Nullable:** No
- **Avg Length:** 13.973387922210849 chars
- **Distinct Values:** 2,714

### company_logo

- **Type:** `Text`
- **Semantic Type:** `Company`
- **Nullable:** No
- **Avg Length:** 0.01160013647219379 chars
- **Distinct Values:** 3

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,849

### eventn_ctx_event_id` → Related table (inferred)
- `hd_account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_account_account_raw`
- **Total Columns:** 22

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 38 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **company** | Text | No | Company | 13.973387922210849 chars | - | 2,714 | Company | Required | Not Null | Variable |
| **company_logo** | Text | No | Company | 0.01160013647219379 chars | - | 3 | Company Logo | Required | Not Null | Categorical (3 categories) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1,849 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 2,931 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **google_id** | Text | No | Category | 0.057659501876492665 chars | - | 21 | Reference to google | Required | Not Null, Foreign Key (likely) | Variable |
| **grace_added_on** | DateTime | Yes | - | - (Null: 95.0%) | - | 149 | Grace Added On | Valid ISO 8601 datetime | None | Variable |
| **grace_extension** | Integer | No | Category | 0.0 to 1.0 | 0.01501194131695667 | 2 | Grace Extension | Numeric; Required | Not Null | Enum-like (2 values) |
| **hd_account_id** | Float | Yes | - | 1.0 to 28,777.0 (Null: 2.1%) | 20,084.551916376306 | 2,870 | Reference to account | Numeric | Foreign Key (likely) | Variable |
| **is_active** | Integer | No | Category | 0.0 to 1.0 | 0.6618901398839986 | 2 | Is Active | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_enterprise** | Integer | No | Category | 0.0 to 1.0 | 0.016376663254861822 | 2 | Is Enterprise | Numeric; Required | Not Null | Enum-like (2 values) |
| **link_click_attribution_window** | Float | No | - | 1.0 to 240.0 | 24.720914363698398 | 8 | Link Click Attribution Window | Numeric; Required | Not Null | Variable |
| **messages_sent_window** | Float | No | - | 1.0 to 168.0 | 24.454793585806893 | 7 | Messages Sent Window | Numeric; Required | Not Null | Variable |
| **name** | Text | No | Name | 16.365404298874104 chars | - | 2,747 | Human-readable name or title | Required | Not Null | Variable |
| **on_grace_period** | Integer | No | Category | 0.0 to 1.0 | 0.05834186284544524 | 2 | On Grace Period | Numeric; Required | Not Null | Enum-like (2 values) |
| **payment_pending** | Integer | No | Category | 0.0 to 1.0 | 0.03002388263391334 | 2 | Payment Pending | Numeric; Required | Not Null | Enum-like (2 values) |
| **show_link_click_attribution** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Show Link Click Attribution | Numeric; Required | Not Null | Enum-like (1 values) |
| **show_messages_sent** | Integer | No | Category | 0.0 to 1.0 | 0.007505970658478335 | 2 | Show Messages Sent | Numeric; Required | Not Null | Enum-like (2 values) |
| **source** | Text | No | Source | 0.2975093824633231 chars | - | 4 | Source | Required | Not Null | Categorical (4 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **ui_mode** | Text | No | Category | 3.9669054930058 chars | - | 3 | Ui Mode | Required | Not Null | Categorical (3 categories) |

</details>

---

<details>
<summary><h2>102. postgres_fb_account_integration</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages account information and configurations.

**Owner/Maintainer:** Accounts/Billing Team

**Tags:** `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_account_integration`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 2 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 10,964.0 | 7,782.246895544193 | 1,925 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **config** | Text | No | SerializedJSON | 105.18517165814463 chars | - | 2,419 | Config | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1,246 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 2,738 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 10.739956172388604 chars | - | 23 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **uid** | Text | No | - | 8.014974433893352 chars | - | 2,368 | Reference to u | Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>103. postgres_fb_block_activities</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres fb block activities operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 21

### activity_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,237

### activity_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 7.0
- **Average:** 2.6782
- **Distinct Values:** 6

### block_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,237

### eventn_ctx_event_id` → Related table (inferred)
- `flow_id` → Related table (inferred)
- `src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,236

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_block_activities`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 21 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **activity_time** | DateTime | No | - | - | - | 4,237 | Activity Time | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **activity_type** | Float | No | - | 1.0 to 7.0 | 2.6782 | 6 | Type or category classification | Numeric; Required | Not Null | Variable |
| **block_id** | Text | No | - | 6.0552 chars | - | 506 | Reference to block | Required | Not Null, Foreign Key (likely) | Variable |
| **block_type** | Float | No | - | 1.0 to 4.0 | 1.5175 | 4 | Type or category classification | Numeric; Required | Not Null | Enum-like (4 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 4,237 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **flow_execution_id** | Float | Yes | - | 9,817,587.0 to 15,269,884.0 | 15,097,574.245199993 | 4,006 | Reference to flow execution | Numeric | Foreign Key (likely) | Variable |
| **flow_id** | Float | Yes | - | 2,476.0 to 13,933.0 | 10,967.9656 | 135 | Reference to flow | Numeric | Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 4,236 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 487,988.0 to 57,023,752.0 | 52,369,927.45149999 | 3,375 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>104. postgres_fb_block_activities_dup</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres fb block activities dup operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 20

### activity_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 9,221

### activity_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 2.0
- **Average:** 1.9377
- **Distinct Values:** 2

### block_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,221

### eventn_ctx_event_id` → Related table (inferred)
- `flow_id` → Related table (inferred)
- `src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,220

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_block_activities_dup`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 20 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **activity_time** | DateTime | No | - | - | - | 9,221 | Activity Time | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **activity_type** | Float | No | - | 1.0 to 2.0 | 1.9377 | 2 | Type or category classification | Numeric; Required | Not Null | Enum-like (2 values) |
| **block_id** | Text | No | - | 3.0 chars | - | 73 | Reference to block | Required | Not Null, Foreign Key (likely) | Variable |
| **block_type** | Float | No | - | 1.0 to 3.0 | 1.3442 | 2 | Type or category classification | Numeric; Required | Not Null | Enum-like (2 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,221 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **flow_execution_id** | Float | Yes | - | 2,377.0 to 45,620.0 | 13,839.3198 | 7,603 | Reference to flow execution | Numeric | Foreign Key (likely) | Variable |
| **flow_id** | Float | Yes | - | 166.0 to 529.0 (Null: 0.6%) | 484.0787567893784 | 13 | Reference to flow | Numeric | Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,220 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 2,803,649.0 to 10,481,104.0 | 7,516,723.535099998 | 5,928 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>105. postgres_fb_bot_builder_botcsat</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores bot configuration and interaction data.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `feedback`, `csat`, `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `conv_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 31

### csat_reason

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.9032258064516129 chars
- **Distinct Values:** 4

### csat_score

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** Yes
- **Range:** 3.0 to 5.0
- **Average:** 4.857142857142857
- **Distinct Values:** 3
- **Null %:** 54.8%

### eventn_ctx_event_id` → Related table (inferred)
- `inbox_id` → `postgres_inboxes.id` (inferred)
- `is_query_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.6129032258064516
- **Distinct Values:** 2

### message_id` → Related table (inferred)
- `node_id` → Related table (inferred)
- `sender_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_bot_builder_botcsat`
- **Total Columns:** 16

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 11,555.0 to 11,555.0 | 11,555.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **conv_id** | Float | No | - | 37,338.0 to 37,380.0 | 37,354.12903225807 | 30 | Reference to conv | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 31 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **csat_reason** | Text | No | Category | 0.9032258064516129 chars | - | 4 | Csat Reason | Required | Not Null | Categorical (4 categories) |
| **csat_score** | Float | Yes | Score | 3.0 to 5.0 (Null: 54.8%) | 4.857142857142857 | 3 | Csat Score | Numeric | None | Enum-like (3 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 31 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **flow_id** | Float | No | - | 388.0 to 435.0 | 394.06451612903226 | 2 | Reference to flow | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **inbox_id** | Float | No | - | 12,239.0 to 36,303.0 | 32,421.709677419356 | 2 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **is_query_resolved** | Integer | Yes | Category | 0.0 to 1.0 | 0.6129032258064516 | 2 | Is Query Resolved | Numeric | None | Enum-like (2 values) |
| **message_id** | Float | No | - | 1,376,195,950.0 to 1,391,460,105.0 | 1,378,215,128.516129 | 30 | Reference to message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **node_id** | Float | No | - | 177,540.0 to 195,339.0 | 179,891.2258064516 | 6 | Reference to node | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **sender_id** | Float | No | - | 146,138,923.0 to 147,158,342.0 | 146,273,354.83870968 | 30 | Reference to sender | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 31 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>106. postgres_fb_bot_builder_botcsat_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_fb_bot_builder_botcsat. Contains unprocessed data before transformation.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `bot`, `raw-data`, `ai`, `csat`, `staging`, `feedback`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `conv_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 31

### csat_reason

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.9032258064516129 chars
- **Distinct Values:** 4

### csat_score

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** Yes
- **Range:** 3.0 to 5.0
- **Average:** 4.857142857142857
- **Distinct Values:** 3
- **Null %:** 54.8%

### eventn_ctx_event_id` → Related table (inferred)
- `inbox_id` → `postgres_inboxes.id` (inferred)
- `is_query_resolved

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.6129032258064516
- **Distinct Values:** 2

### message_id` → Related table (inferred)
- `node_id` → Related table (inferred)
- `sender_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_bot_builder_botcsat_raw`
- **Total Columns:** 16

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 11,555.0 to 11,555.0 | 11,555.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **conv_id** | Float | No | - | 37,338.0 to 37,380.0 | 37,354.12903225807 | 30 | Reference to conv | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 31 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **csat_reason** | Text | No | Category | 0.9032258064516129 chars | - | 4 | Csat Reason | Required | Not Null | Categorical (4 categories) |
| **csat_score** | Float | Yes | Score | 3.0 to 5.0 (Null: 54.8%) | 4.857142857142857 | 3 | Csat Score | Numeric | None | Enum-like (3 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 31 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **flow_id** | Float | No | - | 388.0 to 435.0 | 394.06451612903226 | 2 | Reference to flow | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **inbox_id** | Float | No | - | 12,239.0 to 36,303.0 | 32,421.709677419356 | 2 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **is_query_resolved** | Integer | Yes | Category | 0.0 to 1.0 | 0.6129032258064516 | 2 | Is Query Resolved | Numeric | None | Enum-like (2 values) |
| **message_id** | Float | No | - | 1,376,195,950.0 to 1,391,460,105.0 | 1,378,215,128.516129 | 30 | Reference to message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **node_id** | Float | No | - | 177,540.0 to 195,339.0 | 179,891.2258064516 | 6 | Reference to node | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **sender_id** | Float | No | - | 146,138,923.0 to 147,158,342.0 | 146,273,354.83870968 | 30 | Reference to sender | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 31 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>107. postgres_fb_bot_builder_flow</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores bot configuration and interaction data.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 545

### eventn_ctx_event_id` → Related table (inferred)
- `is_active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.420863309352518
- **Distinct Values:** 2

### is_published

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.5557553956834532
- **Distinct Values:** 2

### production_flow_id` → Related table (inferred)
- `src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### staging_flow_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_bot_builder_flow`
- **Total Columns:** 12

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 12,008.0 | 7,683.3615107913665 | 34 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 545 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 556 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **has_changes** | Integer | No | Category | 0.0 to 1.0 | 0.45863309352517984 | 2 | Has Changes | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_active** | Integer | No | Category | 0.0 to 1.0 | 0.420863309352518 | 2 | Is Active | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_published** | Integer | No | Category | 0.0 to 1.0 | 0.5557553956834532 | 2 | Is Published | Numeric; Required | Not Null | Enum-like (2 values) |
| **production_flow_id** | Float | No | - | 48,167.0 to 62,302.0 | 53,890.56654676259 | 548 | Reference to production flow | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **staging_flow_id** | Float | No | - | 48,168.0 to 62,222.0 | 53,348.15647482014 | 556 | Reference to staging flow | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 552 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>108. postgres_fb_bot_builder_flow_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_fb_bot_builder_flow. Contains unprocessed data before transformation.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `raw-data`, `staging`, `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 545

### eventn_ctx_event_id` → Related table (inferred)
- `is_active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.420863309352518
- **Distinct Values:** 2

### is_published

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.5557553956834532
- **Distinct Values:** 2

### production_flow_id` → Related table (inferred)
- `src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### staging_flow_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_bot_builder_flow_raw`
- **Total Columns:** 12

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 12,008.0 | 7,683.3615107913665 | 34 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 545 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 556 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **has_changes** | Integer | No | Category | 0.0 to 1.0 | 0.45863309352517984 | 2 | Has Changes | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_active** | Integer | No | Category | 0.0 to 1.0 | 0.420863309352518 | 2 | Is Active | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_published** | Integer | No | Category | 0.0 to 1.0 | 0.5557553956834532 | 2 | Is Published | Numeric; Required | Not Null | Enum-like (2 values) |
| **production_flow_id** | Float | No | - | 48,167.0 to 62,302.0 | 53,890.56654676259 | 548 | Reference to production flow | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **staging_flow_id** | Float | No | - | 48,168.0 to 62,222.0 | 53,348.15647482014 | 556 | Reference to staging flow | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 552 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>109. postgres_fb_builder_user</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores user information and access permissions.

**Owner/Maintainer:** Customer Data Team

**Tags:** `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 636

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,954

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_builder_user`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 636 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 1.0 | 1.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,954 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,996 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **identity** | Text | No | - | 15.9948 chars | - | 9,880 | Reference to entity | Required | Not Null, Foreign Key (likely) | Variable |
| **ig_name** | Text | No | Category | 0.0143 chars | - | 12 | Ig Name | Required | Not Null | Variable |
| **ig_username** | Text | No | - | 2.1542 chars | - | 1,601 | Ig Username | Required | Not Null | Variable |
| **inbox_id** | Float | Yes | - | 764.0 to 927.0 (Null: 99.8%) | 910.6 | 4 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Enum-like (4 values) |
| **phone** | Text | No | Category | 0.006 chars | - | 6 | Phone | Required | Not Null | Categorical (6 categories) |
| **platform** | Text | No | Category | 4.4302 chars | - | 3 | Platform | Required | Not Null | Categorical (3 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 4,498 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **wa_optin_status** | Float | No | - | 2.0 to 2.0 | 2.0 | 1 | Status or state of record | Numeric; Required | Not Null | Enum-like (1 values) |

</details>

---

<details>
<summary><h2>110. postgres_fb_builder_user_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_fb_builder_user. Contains unprocessed data before transformation.

**Owner/Maintainer:** Customer Data Team

**Tags:** `raw-data`, `staging`, `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 635

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,954

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_builder_user_raw`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 635 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 1.0 | 1.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,954 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,996 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **identity** | Text | No | - | 15.9948 chars | - | 9,880 | Reference to entity | Required | Not Null, Foreign Key (likely) | Variable |
| **ig_name** | Text | No | Category | 0.0143 chars | - | 12 | Ig Name | Required | Not Null | Variable |
| **ig_username** | Text | No | - | 2.1542 chars | - | 1,601 | Ig Username | Required | Not Null | Variable |
| **inbox_id** | Float | Yes | - | 764.0 to 927.0 (Null: 99.8%) | 910.6 | 4 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Enum-like (4 values) |
| **phone** | Text | No | Category | 0.006 chars | - | 6 | Phone | Required | Not Null | Categorical (6 categories) |
| **platform** | Text | No | Category | 4.4302 chars | - | 3 | Platform | Required | Not Null | Categorical (3 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 4,498 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **wa_optin_status** | Float | No | - | 2.0 to 2.0 | 2.0 | 1 | Status or state of record | Numeric; Required | Not Null | Enum-like (1 values) |

</details>

---

<details>
<summary><h2>111. postgres_fb_central_orders</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3

### account_id` → `postgres_accounts.id` (inferred)
- `amount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 203,190.0
- **Average:** 977.2809080000005
- **Distinct Values:** 1,987

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0037
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,586

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 1

### customer_id` → Related table (inferred)
- `discount_codes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 36.1764 chars
- **Distinct Values:** 1,796

### email

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 17.8052 chars
- **Distinct Values:** 7,381

### eventn_ctx_event_id` → Related table (inferred)
- `items

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 605.1322 chars
- **Distinct Values:** 9,999

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.7719 chars
- **Distinct Values:** 4,579

### order_id` → Related table (inferred)
- `source_flow_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_central_orders`
- **Total Columns:** 35

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 3 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 13.0 to 747.0 | 56.4406 | 54 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **amount** | Float | Yes | - | 0.0 to 203,190.0 | 977.2809080000005 | 1,987 | Amount | Numeric | None | Variable |
| **cancelled** | Integer | No | Category | 0.0 to 1.0 | 0.0037 | 2 | Cancelled | Numeric; Required | Not Null | Enum-like (2 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 8,586 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 3.0 chars | - | 1 | Currency | Required | Not Null | Categorical (1 categories) |
| **customer_id** | Text | No | - | 10.4412 chars | - | 7,751 | Reference to customer | Required | Not Null, Foreign Key (likely) | Variable |
| **discount_amount** | Float | Yes | Discount | 0.0 to 8,398.4 | 8.08854 | 99 | Count of dis_amount | Numeric | None | Variable |
| **discount_codes** | Text | No | SerializedJSON | 36.1764 chars | - | 1,796 | Count of dis_codes | Required | Not Null | Variable |
| **email** | Text | No | - | 17.8052 chars | - | 7,381 | Email address | Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_name** | Text | No | Name | 6.5339 chars | - | 5,260 | Human-readable name or title | Required | Not Null | Variable |
| **fulfillment** | Text | No | SerializedJSON | 23.5194 chars | - | 625 | Fulfillment | Required | Not Null | Variable |
| **fulfillment_status** | Text | No | Category | 4.5227 chars | - | 4 | Status or state of record | Required | Not Null | Categorical (4 categories) |
| **gateway** | Text | No | Category | 12.5369 chars | - | 29 | Gateway | Required | Not Null | Variable |
| **integration_id** | Float | Yes | - | 21.0 to 4,971.0 (Null: 93.4%) | 976.3246951219512 | 24 | Reference to integration | Numeric | Foreign Key (likely) | Variable |
| **items** | Text | No | SerializedJSON | 605.1322 chars | - | 9,999 | Items | Required | Not Null | Variable |
| **last_name** | Text | No | Name | 5.7719 chars | - | 4,579 | Human-readable name or title | Required | Not Null | Variable |
| **order_id** | Text | No | - | 13.0 chars | - | 10,000 | Reference to order | Required | Not Null, Foreign Key (likely) | Variable |
| **order_name** | Text | No | - | 8.83 chars | - | 9,999 | Order Name | Required | Not Null | Variable |
| **order_notes** | Text | No | - | 3.5642 chars | - | 305 | Order Notes | Required | Not Null | Variable |
| **order_status_url** | Text | No | URL | 124.7358 chars | - | 10,000 | Status or state of record | Valid URL format; Required | Not Null | Variable |
| **payment_status** | Text | No | Category | 5.2992 chars | - | 7 | Status or state of record | Required | Not Null | Categorical (7 categories) |
| **phone** | Text | No | - | 10.4698 chars | - | 9,351 | Phone | Required | Not Null | Variable |
| **presentment_currency** | Text | No | Category | 3.0 chars | - | 1 | Presentment Currency | Required | Not Null | Categorical (1 categories) |
| **shipping_price** | Float | Yes | - | 0.0 to 800.0 | 9.742 | 26 | Shipping Price | Numeric | None | Variable |
| **source_flow_id** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Reference to source flow | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Text | No | Category | 0.0016 chars | - | 3 | Status or state of record | Required | Not Null | Categorical (3 categories) |
| **store_type** | Float | No | - | 1.0 to 1.0 | 1.0 | 1 | Type or category classification | Numeric; Required | Not Null | Enum-like (1 values) |
| **subtotal_price** | Float | Yes | - | 0.0 to 203,190.0 | 967.7015040000002 | 1,884 | Subtotal Price | Numeric | None | Variable |
| **tags** | Text | No | SerializedJSON | 19.2745 chars | - | 527 | Tags | Required | Not Null | Variable |
| **tracking_url** | Text | No | URL | 119.7761 chars | - | 9,942 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 8,586 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>112. postgres_fb_conv_flow_messages</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores message data and delivery information.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`, `messaging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 74

### account_id` → `postgres_accounts.id` (inferred)
- `conv_flow_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,674

### entity_id` → Related table (inferred)
- `entity_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.282 chars
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)
- `message_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 6.0
- **Average:** 4.8362
- **Distinct Values:** 5

### meta

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 77.2582 chars
- **Distinct Values:** 9,004

### node_id` → Related table (inferred)
- `ref_id` → Related table (inferred)
- `updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,682

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conv_flow_messages`
- **Total Columns:** 17

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 74 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 3.0 to 10,842.0 | 7,535.8744 | 61 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conv_flow_id** | Float | Yes | - | 992.0 to 13,839.0 | 10,496.365000000005 | 169 | Reference to conv flow | Numeric | Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 6,674 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **entity_id** | Float | Yes | - | 1,123.0 to 4,143.0 (Null: 94.4%) | 3,796.1117021276596 | 11 | Reference to entity | Numeric | Foreign Key (likely) | Variable |
| **entity_type** | Text | No | Category | 0.282 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **execution_id** | Float | Yes | - | 2,299,997.0 to 14,889,164.0 (Null: 5.6%) | 14,814,117.763777025 | 8,506 | Reference to execution | Numeric | Foreign Key (likely) | Variable |
| **message_type** | Float | No | - | 1.0 to 6.0 | 4.8362 | 5 | Type or category classification | Numeric; Required | Not Null | Enum-like (5 values) |
| **meta** | Text | No | SerializedJSON | 77.2582 chars | - | 9,004 | Meta | Required | Not Null | Variable |
| **node_id** | Float | Yes | - | 1,322.0 to 26,783.0 | 18,901.6239 | 347 | Reference to node | Numeric | Foreign Key (likely) | Variable |
| **ref_id** | Text | No | - | 18.8916 chars | - | 8,997 | Reference to ref | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Float | No | - | 0.0 to 2.0 | 1.8923 | 3 | Status or state of record | Numeric; Required | Not Null | Enum-like (3 values) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 6,682 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | Yes | - | 489,017.0 to 56,528,714.0 | 52,113,776.31980001 | 7,945 | Reference to user | Numeric | Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>113. postgres_fb_conv_flow_nodes</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 112

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,500

### data

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 418.2512 chars
- **Distinct Values:** 6,706

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conv_flow_nodes`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 112 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 6,500 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **data** | Text | No | SerializedJSON | 418.2512 chars | - | 6,706 | Data | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **flow_id** | Float | No | - | 67.0 to 55,043.0 | 35,292.968400000005 | 5,978 | Reference to flow | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **node_name** | Text | No | - | 0.1967 chars | - | 88 | Node Name | Required | Not Null | Variable |
| **oid** | Text | No | - | 36.0 chars | - | 9,982 | Reference to o | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **type** | Text | No | Category | 7.71 chars | - | 19 | Type or category classification | Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 6,309 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>114. postgres_fb_conv_flow_nodes_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_fb_conv_flow_nodes. Contains unprocessed data before transformation.

**Owner/Maintainer:** Conversations Team

**Tags:** `raw-data`, `staging`, `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 7

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,273

### data

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 426.9296 chars
- **Distinct Values:** 7,297

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conv_flow_nodes_raw`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 7 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 7,273 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **data** | Text | No | SerializedJSON | 426.9296 chars | - | 7,297 | Data | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **flow_id** | Float | No | - | 67.0 to 52,877.0 | 30,991.5558 | 6,707 | Reference to flow | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **node_name** | Text | No | - | 0.1528 chars | - | 71 | Node Name | Required | Not Null | Variable |
| **oid** | Text | No | - | 36.0 chars | - | 9,973 | Reference to o | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **type** | Text | No | Category | 7.8237 chars | - | 19 | Type or category classification | Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 7,045 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>115. postgres_fb_conversational_broadcasts</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages broadcast messaging campaigns and delivery tracking.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `conversations`, `campaigns`, `marketing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,001

### account_id` → `postgres_accounts.id` (inferred)
- `cohort_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)
- `name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 19.8266 chars
- **Distinct Values:** 8,479

### platform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.3479 chars
- **Distinct Values:** 4

### retries_attempted

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 0.0209
- **Distinct Values:** 4

### retry_settings

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 17.1668 chars
- **Distinct Values:** 3,506

### schedule_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 8,175
- **Null %:** 18.0%

### schedule_time_updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,826

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.2944 chars
- **Distinct Values:** 7

### topic_id` → Related table (inferred)
- `total_users_received

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 199,920.0
- **Average:** 7,818.170900000003
- **Distinct Values:** 4,071

### trigger_flow_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_broadcasts`
- **Total Columns:** 23

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 3,001 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 2,133.0 | 638.1781 | 41 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **cohort_id** | Text | No | Category | 0.0168 chars | - | 4 | Reference to cohort | Required | Not Null, Foreign Key (likely) | Categorical (4 categories) |
| **cohort_ids** | Text | No | - | 1.5384 chars | - | 129 | Reference to cohort s | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,761 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **draft_flow_id** | Float | Yes | - | 8.0 to 40,350.0 (Null: 10.1%) | 18,775.611840641 | 8,985 | Reference to draft flow | Numeric | Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **is_triggered** | Integer | No | Category | 0.0 to 1.0 | 0.8127 | 2 | Is Triggered | Numeric; Required | Not Null | Enum-like (2 values) |
| **name** | Text | No | Name | 19.8266 chars | - | 8,479 | Human-readable name or title | Required | Not Null | Variable |
| **platform** | Text | No | Category | 7.3479 chars | - | 4 | Platform | Required | Not Null | Categorical (4 categories) |
| **retries_attempted** | Float | No | - | 0.0 to 3.0 | 0.0209 | 4 | Retries Attempted | Numeric; Required | Not Null | Enum-like (4 values) |
| **retry_settings** | Text | No | - | 17.1668 chars | - | 3,506 | Retry Settings | Required | Not Null | Variable |
| **schedule_time** | DateTime | Yes | - | - (Null: 18.0%) | - | 8,175 | Schedule Time | Valid ISO 8601 datetime | None | Variable |
| **schedule_time_updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,826 | Schedule Time Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Text | No | Category | 8.2944 chars | - | 7 | Status or state of record | Required | Not Null | Categorical (7 categories) |
| **topic_id** | Float | Yes | - | 1.0 to 3,499.0 (Null: 99.7%) | 1,201.967741935484 | 17 | Reference to topic | Numeric | Foreign Key (likely) | Variable |
| **total_users_received** | Float | No | - | 0.0 to 199,920.0 | 7,818.170900000003 | 4,071 | Total Users Received | Numeric; Required | Not Null | Variable |
| **trigger_flow_id** | Float | Yes | - | 4.0 to 50,484.0 (Null: 13.4%) | 27,257.68994574627 | 8,540 | Reference to trigger flow | Numeric | Foreign Key (likely) | Variable |
| **ums_broadcast_id** | Text | No | - | 19.3512 chars | - | 8,064 | Reference to ums broadcast | Required | Not Null, Foreign Key (likely) | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,567 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **users_csv_url** | Text | No | URL | 123.5242 chars | - | 8,380 | URL or web address | Valid URL format; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>116. postgres_fb_conversational_broadcasts_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_fb_conversational_broadcasts. Contains unprocessed data before transformation.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `raw-data`, `staging`, `conversations`, `marketing`, `campaigns`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3

### account_id` → `postgres_accounts.id` (inferred)
- `cohort_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)
- `name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 18.9918 chars
- **Distinct Values:** 8,436

### platform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.4149 chars
- **Distinct Values:** 4

### retries_attempted

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 0.0223
- **Distinct Values:** 4

### retry_settings

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 12.8804 chars
- **Distinct Values:** 2,189

### schedule_time

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 8,236
- **Null %:** 17.3%

### schedule_time_updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,872

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.3238 chars
- **Distinct Values:** 7

### topic_id` → Related table (inferred)
- `total_users_received

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 171,562.0
- **Average:** 7,344.133799999997
- **Distinct Values:** 3,807

### trigger_flow_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_broadcasts_raw`
- **Total Columns:** 23

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 3 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 5,960.0 | 1,530.867 | 68 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **cohort_id** | Text | No | - | 0.5328 chars | - | 150 | Reference to cohort | Required | Not Null, Foreign Key (likely) | Variable |
| **cohort_ids** | Text | No | - | 1.2338 chars | - | 214 | Reference to cohort s | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,786 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **draft_flow_id** | Float | Yes | - | 8.0 to 23,481.0 (Null: 13.2%) | 10,555.32745504841 | 8,677 | Reference to draft flow | Numeric | Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **is_triggered** | Integer | No | Category | 0.0 to 1.0 | 0.8211 | 2 | Is Triggered | Numeric; Required | Not Null | Enum-like (2 values) |
| **name** | Text | No | Name | 18.9918 chars | - | 8,436 | Human-readable name or title | Required | Not Null | Variable |
| **platform** | Text | No | Category | 7.4149 chars | - | 4 | Platform | Required | Not Null | Categorical (4 categories) |
| **retries_attempted** | Float | No | - | 0.0 to 3.0 | 0.0223 | 4 | Retries Attempted | Numeric; Required | Not Null | Enum-like (4 values) |
| **retry_settings** | Text | No | - | 12.8804 chars | - | 2,189 | Retry Settings | Required | Not Null | Variable |
| **schedule_time** | DateTime | Yes | - | - (Null: 17.3%) | - | 8,236 | Schedule Time | Valid ISO 8601 datetime | None | Variable |
| **schedule_time_updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,872 | Schedule Time Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Text | No | Category | 8.3238 chars | - | 7 | Status or state of record | Required | Not Null | Categorical (7 categories) |
| **topic_id** | Float | Yes | - | 1.0 to 3,499.0 (Null: 99.7%) | 1,320.2285714285715 | 21 | Reference to topic | Numeric | Foreign Key (likely) | Variable |
| **total_users_received** | Float | No | - | 0.0 to 171,562.0 | 7,344.133799999997 | 3,807 | Total Users Received | Numeric; Required | Not Null | Variable |
| **trigger_flow_id** | Float | Yes | - | 4.0 to 33,701.0 (Null: 12.6%) | 19,787.257548032936 | 8,624 | Reference to trigger flow | Numeric | Foreign Key (likely) | Variable |
| **ums_broadcast_id** | Text | No | - | 19.5432 chars | - | 8,143 | Reference to ums broadcast | Required | Not Null, Foreign Key (likely) | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,404 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **users_csv_url** | Text | No | URL | 111.9164 chars | - | 8,510 | URL or web address | Valid URL format; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>117. postgres_fb_conversational_flow_executions</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 17

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,437

### eventn_ctx_event_id` → Related table (inferred)
- `last_executed_node_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_flow_executions`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 17 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 4,437 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **execution_source_ref_id** | Text | No | Source | 4.0879 chars | - | 3,605 | Reference to execution source ref | Required | Not Null, Foreign Key (likely) | Variable |
| **execution_source_type** | Text | No | Category | 13.9012 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **flow_id** | Float | Yes | - | 2.0 to 529.0 (Null: 0.6%) | 473.2887033497636 | 21 | Reference to flow | Numeric | Foreign Key (likely) | Variable |
| **last_executed_node_id** | Text | No | - | 2.9964 chars | - | 69 | Reference to last executed node | Required | Not Null, Foreign Key (likely) | Variable |
| **next_node_id** | Text | No | Category | 0.2919 chars | - | 25 | Reference to next node | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **tracker_metadata** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Tracker Metadata | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 4,583 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | Yes | - | 2,803,649.0 to 10,477,426.0 (Null: 0.0%) | 7,197,557.564912978 | 7,674 | Reference to user | Numeric | Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>118. postgres_fb_conversational_flow_executions_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_fb_conversational_flow_executions. Contains unprocessed data before transformation.

**Owner/Maintainer:** Conversations Team

**Tags:** `raw-data`, `staging`, `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 17

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,437

### eventn_ctx_event_id` → Related table (inferred)
- `last_executed_node_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_flow_executions_raw`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 17 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 4,437 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **execution_source_ref_id** | Text | No | Source | 4.0879 chars | - | 3,605 | Reference to execution source ref | Required | Not Null, Foreign Key (likely) | Variable |
| **execution_source_type** | Text | No | Category | 13.9012 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **flow_id** | Float | Yes | - | 2.0 to 529.0 (Null: 0.6%) | 473.2887033497636 | 21 | Reference to flow | Numeric | Foreign Key (likely) | Variable |
| **last_executed_node_id** | Text | No | - | 2.9964 chars | - | 69 | Reference to last executed node | Required | Not Null, Foreign Key (likely) | Variable |
| **next_node_id** | Text | No | Category | 0.2919 chars | - | 25 | Reference to next node | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **tracker_metadata** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Tracker Metadata | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 4,583 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | Yes | - | 2,803,649.0 to 10,477,426.0 (Null: 0.0%) | 7,197,557.564912978 | 7,674 | Reference to user | Numeric | Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>119. postgres_fb_conversational_flows</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,253

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,029

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 12
- **Null %:** 99.8%

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### dnd_duration

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.00997920997920998 chars
- **Distinct Values:** 6

### dnd_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0009702009702009702
- **Distinct Values:** 2

### dnd_start_time

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.018711018711018712 chars
- **Distinct Values:** 5

### draft_flow_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)
- `is_deleted

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0015246015246015245
- **Distinct Values:** 2

### is_draft

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.09133749133749133
- **Distinct Values:** 2

### is_two_way_broadcast

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.15384615384615385
- **Distinct Values:** 2

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 19.666528066528066 chars
- **Distinct Values:** 5,789

### platform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 8.157726957726958 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### test_mode

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.023007623007623008
- **Distinct Values:** 2

### test_mode_numbers

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 3.6334026334026333 chars
- **Distinct Values:** 171

### trigger_event_type_id` → `broadcasts._id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_flows`
- **Total Columns:** 25

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 2,253 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 10,900.0 | 4,872.199029799028 | 184 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 7,029 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 99.8%) | - | 12 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **description** | Text | No | Description | 0.0 chars | - | 1 | Description | Required | Not Null | Categorical (1 categories) |
| **dnd_duration** | Text | No | Category | 0.00997920997920998 chars | - | 6 | Dnd Duration | Required | Not Null | Categorical (6 categories) |
| **dnd_enabled** | Integer | No | Category | 0.0 to 1.0 | 0.0009702009702009702 | 2 | Dnd Enabled | Numeric; Required | Not Null | Enum-like (2 values) |
| **dnd_start_time** | Text | No | Category | 0.018711018711018712 chars | - | 5 | Dnd Start Time | Required | Not Null | Categorical (5 categories) |
| **draft_flow_id** | Float | Yes | - | 0.0 to 3,409.0 (Null: 70.7%) | 1,634.521020311762 | 1,293 | Reference to draft flow | Numeric | Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 7,088 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_id** | Float | Yes | - | 52.0 to 5,578.0 (Null: 0.8%) | 4,323.0582483587095 | 250 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **is_deleted** | Integer | No | Category | 0.0 to 1.0 | 0.0015246015246015245 | 2 | Is Deleted | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_draft** | Integer | No | Category | 0.0 to 1.0 | 0.09133749133749133 | 2 | Is Draft | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_two_way_broadcast** | Integer | No | Category | 0.0 to 1.0 | 0.15384615384615385 | 2 | Is Two Way Broadcast | Numeric; Required | Not Null | Enum-like (2 values) |
| **name** | Text | No | Name | 19.666528066528066 chars | - | 5,789 | Human-readable name or title | Required | Not Null | Variable |
| **platform** | Text | No | Category | 8.157726957726958 chars | - | 2 | Platform | Required | Not Null | Categorical (2 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **test_mode** | Integer | No | Category | 0.0 to 1.0 | 0.023007623007623008 | 2 | Test Mode | Numeric; Required | Not Null | Enum-like (2 values) |
| **test_mode_numbers** | Text | No | SerializedJSON | 3.6334026334026333 chars | - | 171 | Test Mode Numbers | Required | Not Null | Variable |
| **trigger_event_type_id** | Float | Yes | - | 1,156.0 to 2,192.0 (Null: 78.7%) | 1,338.132726089786 | 97 | Type or category classification | Numeric | Foreign Key (likely) | Variable |
| **triggers** | Text | No | SerializedJSON | 146.34428274428274 chars | - | 6,986 | Triggers | Required | Not Null | Variable |
| **type** | Text | No | Category | 9.091614691614692 chars | - | 5 | Type or category classification | Required | Not Null | Categorical (5 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 7,120 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **use_cases** | Text | No | Category | 0.0 chars | - | 1 | Use Cases | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>120. postgres_fb_conversational_flows_freetextreplies</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages conversation records and chat interactions.

**Owner/Maintainer:** Conversations Team

**Tags:** `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,717

### eventn_ctx_event_id` → Related table (inferred)
- `node_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_flows_freetextreplies`
- **Total Columns:** 7

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 4,717 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 6,728 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **execution_id** | Float | No | - | 129,924,842.0 to 194,173,711.0 | 168,690,422.4910064 | 6,477 | Reference to execution | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **node_id** | Float | No | - | 49,939.0 to 120,386.0 | 80,721.43288241416 | 62 | Reference to node | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **text** | Text | No | - | 36.67087854913037 chars | - | 6,056 | Text | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>121. postgres_fb_conversational_flows_freetextreplies_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_fb_conversational_flows_freetextreplies. Contains unprocessed data before transformation.

**Owner/Maintainer:** Conversations Team

**Tags:** `raw-data`, `staging`, `conversations`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4,717

### eventn_ctx_event_id` → Related table (inferred)
- `node_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_conversational_flows_freetextreplies_raw`
- **Total Columns:** 7

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 4,717 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 6,728 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **execution_id** | Float | No | - | 129,924,842.0 to 194,173,711.0 | 168,690,422.49100634 | 6,477 | Reference to execution | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **node_id** | Float | No | - | 49,939.0 to 120,386.0 | 80,721.43288241416 | 62 | Reference to node | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **text** | Text | No | - | 36.67087854913037 chars | - | 6,056 | Text | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>122. postgres_fb_igrn_broadcasts</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages broadcast messaging campaigns and delivery tracking.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `campaigns`, `marketing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 4

### content

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 606.6849865951742 chars
- **Distinct Values:** 720

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 744
- **Null %:** 0.4%

### custom_ref_prefix

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### eventn_ctx_event_id` → Related table (inferred)
- `max_users_to_receive

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 68,550.0
- **Average:** 9,998.743243243243
- **Distinct Values:** 374
- **Null %:** 10.7%

### ref

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 29.08847184986595 chars
- **Distinct Values:** 727

### schedule_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 746

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### topic_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_igrn_broadcasts`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 4 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **content** | Text | No | SerializedJSON | 606.6849865951742 chars | - | 720 | Content | Required | Not Null | Variable |
| **created_at** | DateTime | Yes | CreationTimestamp | - (Null: 0.4%) | - | 744 | Created At | Valid ISO 8601 datetime | None | Variable |
| **custom_ref_prefix** | Text | No | Category | 0.0 chars | - | 1 | Custom Ref Prefix | Required | Not Null | Categorical (1 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 746 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **is_triggered** | Integer | No | Category | 0.0 to 1.0 | 0.9477211796246648 | 2 | Is Triggered | Numeric; Required | Not Null | Enum-like (2 values) |
| **max_users_to_receive** | Float | Yes | - | 1.0 to 68,550.0 (Null: 10.7%) | 9,998.743243243243 | 374 | Max Users To Receive | Numeric | None | Variable |
| **ref** | Text | No | - | 29.08847184986595 chars | - | 727 | Ref | Required | Not Null | Variable |
| **schedule_time** | DateTime | No | - | - | - | 746 | Schedule Time | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **topic_id** | Float | No | - | 1.0 to 4,147.0 | 1,920.9490616621983 | 89 | Reference to topic | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **total_users_received** | Float | No | - | 0.0 to 68,550.0 | 8,381.739946380698 | 404 | Total Users Received | Numeric; Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 740 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>123. postgres_fb_igrn_broadcasts_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_fb_igrn_broadcasts. Contains unprocessed data before transformation.

**Owner/Maintainer:** Marketing/Broadcast Team

**Tags:** `raw-data`, `staging`, `campaigns`, `marketing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 5

### content

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 605.8728246318608 chars
- **Distinct Values:** 720

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 744
- **Null %:** 0.5%

### custom_ref_prefix

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### eventn_ctx_event_id` → Related table (inferred)
- `max_users_to_receive

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 68,550.0
- **Average:** 10,086.490254872564
- **Distinct Values:** 374
- **Null %:** 10.7%

### ref

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 29.089692101740294 chars
- **Distinct Values:** 727

### schedule_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 746

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### topic_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_igrn_broadcasts_raw`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 5 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **content** | Text | No | SerializedJSON | 605.8728246318608 chars | - | 720 | Content | Required | Not Null | Variable |
| **created_at** | DateTime | Yes | CreationTimestamp | - (Null: 0.5%) | - | 744 | Created At | Valid ISO 8601 datetime | None | Variable |
| **custom_ref_prefix** | Text | No | Category | 0.0 chars | - | 1 | Custom Ref Prefix | Required | Not Null | Categorical (1 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 746 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **is_triggered** | Integer | No | Category | 0.0 to 1.0 | 0.9464524765729585 | 2 | Is Triggered | Numeric; Required | Not Null | Enum-like (2 values) |
| **max_users_to_receive** | Float | Yes | - | 1.0 to 68,550.0 (Null: 10.7%) | 10,086.490254872564 | 374 | Max Users To Receive | Numeric | None | Variable |
| **ref** | Text | No | - | 29.089692101740294 chars | - | 727 | Ref | Required | Not Null | Variable |
| **schedule_time** | DateTime | No | - | - | - | 746 | Schedule Time | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **topic_id** | Float | No | - | 1.0 to 4,147.0 | 1,918.6439089692099 | 89 | Reference to topic | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **total_users_received** | Float | No | - | 0.0 to 68,550.0 | 8,370.519410977242 | 404 | Total Users Received | Numeric; Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 741 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>124. postgres_fb_igrn_optins</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres fb igrn optins operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,788

### account_id` → `postgres_accounts.id` (inferred)
- `conv_flow_id` → Related table (inferred)
- `conv_flow_message_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,982

### eventn_ctx_event_id` → Related table (inferred)
- `src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### status

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 2

### status_changed_at

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 9,982

### topic_id` → Related table (inferred)
- `updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,982

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_fb_igrn_optins`
- **Total Columns:** 15

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 2,788 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 36.0 to 8,496.0 | 4,630.1697 | 21 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conv_flow_id** | Float | Yes | - | 166.0 to 13,827.0 (Null: 26.7%) | 7,433.08463008463 | 28 | Reference to conv flow | Numeric | Foreign Key (likely) | Variable |
| **conv_flow_message_id** | Float | Yes | - | 1,111.0 to 3,941,160.0 (Null: 26.4%) | 2,650,566.1553200157 | 7,360 | Reference to conv flow message | Numeric | Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,982 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **notification_messages_token** | Text | No | - | 18.8832 chars | - | 9,998 | Authentication or access token | Required | Not Null | Variable |
| **notification_sent_id** | Float | Yes | - | 13,119,498.0 to 70,296,551.0 (Null: 73.1%) | 63,440,548.21895911 | 2,691 | Reference to notification sent | Numeric | Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Text | No | Category | 6.0 chars | - | 2 | Status or state of record | Required | Not Null | Categorical (2 categories) |
| **status_changed_at** | DateTime | No | - | - | - | 9,982 | Status or state of record | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **topic_id** | Float | No | - | 199.0 to 4,147.0 | 2,786.5388 | 29 | Reference to topic | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,982 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | Yes | - | 2,895,060.0 to 57,931,360.0 | 48,069,458.95950001 | 9,991 | Reference to user | Numeric | Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>125. postgres_hd_csat_survey_responses</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Customer Satisfaction (CSAT) survey data.

**Owner/Maintainer:** Platform Team

**Tags:** `feedback`, `csat`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 28

### account_id` → `postgres_accounts.id` (inferred)
- `agent_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.4918 chars
- **Distinct Values:** 200

### assigned_agent_id` → Related table (inferred)
- `contact_id` → Related table (inferred)
- `contact_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.4112 chars
- **Distinct Values:** 8,604

### contact_phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.6815 chars
- **Distinct Values:** 8,328

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,889

### csat_message_created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 9,893

### csat_scale

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 5.0 to 5.0
- **Average:** 5.0
- **Distinct Values:** 1

### eventn_ctx_event_id` → Related table (inferred)
- `inbox_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.9045 chars
- **Distinct Values:** 56

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1758
- **Distinct Values:** 2

### message_id` → `postgres_inboxes.id` (inferred)
- `rating

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** No
- **Range:** 1.0 to 5.0
- **Average:** 3.6771
- **Distinct Values:** 5

### resolved_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.6581 chars
- **Distinct Values:** 3

### response_conversation_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_hd_csat_survey_responses`
- **Total Columns:** 23

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 28 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 22,742.0 | 1,569.9344 | 60 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **agent_name** | Text | No | - | 6.4918 chars | - | 200 | Agent Name | Required | Not Null | Variable |
| **assigned_agent_id** | Float | Yes | - | 1.0 to 46,126.0 (Null: 38.2%) | 25,796.42780835222 | 201 | Reference to assigned agent | Numeric | Foreign Key (likely) | Variable |
| **contact_id** | Float | No | - | 3,029,608.0 to 66,555,112.0 | 63,966,601.7949 | 9,430 | Reference to contact | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **contact_name** | Text | No | - | 11.4112 chars | - | 8,604 | Contact Name | Required | Not Null | Variable |
| **contact_phone_number** | Text | No | - | 10.6815 chars | - | 8,328 | Contact Phone Number | Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 62,554,920.0 to 63,639,156.0 | 63,078,821.1584 | 9,984 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,889 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **csat_message_created_at** | DateTime | Yes | CreationTimestamp | - | - | 9,893 | Csat Message Created At | Valid ISO 8601 datetime | None | Variable |
| **csat_scale** | Float | Yes | - | 5.0 to 5.0 | 5.0 | 1 | Csat Scale | Numeric | None | Enum-like (1 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **feedback_message** | Text | No | - | 18.4746 chars | - | 3,834 | Feedback Message | Required | Not Null | Variable |
| **inbox_id** | Float | No | - | 115.0 to 30,159.0 | 4,107.601 | 78 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_name** | Text | No | - | 13.9045 chars | - | 56 | Inbox Name | Required | Not Null | Variable |
| **is_outside_working_hours** | Integer | No | Category | 0.0 to 1.0 | 0.1758 | 2 | Reference to is outse working hours | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **message_id** | Float | No | - | 426,394,302.0 to 434,909,475.0 | 430,813,082.4345 | 10,000 | Reference to message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **rating** | Float | No | Score | 1.0 to 5.0 | 3.6771 | 5 | Rating | Numeric; Required | Not Null | Enum-like (5 values) |
| **resolved_by** | Text | No | Category | 3.6581 chars | - | 3 | Resolved By | Required | Not Null | Categorical (3 categories) |
| **response_conversation_id** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Reference to response conversation | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,291 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>126. postgres_hd_csat_survey_responses_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_hd_csat_survey_responses. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `csat`, `staging`, `feedback`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 28

### account_id` → `postgres_accounts.id` (inferred)
- `agent_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 6.4918 chars
- **Distinct Values:** 200

### assigned_agent_id` → Related table (inferred)
- `contact_id` → Related table (inferred)
- `contact_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 11.4112 chars
- **Distinct Values:** 8,604

### contact_phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 10.6815 chars
- **Distinct Values:** 8,328

### conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,889

### csat_message_created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 9,893

### csat_scale

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 5.0 to 5.0
- **Average:** 5.0
- **Distinct Values:** 1

### eventn_ctx_event_id` → Related table (inferred)
- `inbox_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 13.9045 chars
- **Distinct Values:** 56

### is_outside_working_hours

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1758
- **Distinct Values:** 2

### message_id` → `postgres_inboxes.id` (inferred)
- `rating

- **Type:** `Float`
- **Semantic Type:** `Score`
- **Nullable:** No
- **Range:** 1.0 to 5.0
- **Average:** 3.6771
- **Distinct Values:** 5

### resolved_by

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.6581 chars
- **Distinct Values:** 3

### response_conversation_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_hd_csat_survey_responses_raw`
- **Total Columns:** 23

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 28 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 22,742.0 | 1,569.9344 | 60 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **agent_name** | Text | No | - | 6.4918 chars | - | 200 | Agent Name | Required | Not Null | Variable |
| **assigned_agent_id** | Float | Yes | - | 1.0 to 46,126.0 (Null: 38.2%) | 25,796.42780835222 | 201 | Reference to assigned agent | Numeric | Foreign Key (likely) | Variable |
| **contact_id** | Float | No | - | 3,029,608.0 to 66,555,112.0 | 63,966,601.7949 | 9,430 | Reference to contact | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **contact_name** | Text | No | - | 11.4112 chars | - | 8,604 | Contact Name | Required | Not Null | Variable |
| **contact_phone_number** | Text | No | - | 10.6815 chars | - | 8,328 | Contact Phone Number | Required | Not Null | Variable |
| **conversation_id** | Float | No | - | 62,554,920.0 to 63,639,156.0 | 63,078,821.1584 | 9,984 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,889 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **csat_message_created_at** | DateTime | Yes | CreationTimestamp | - | - | 9,893 | Csat Message Created At | Valid ISO 8601 datetime | None | Variable |
| **csat_scale** | Float | Yes | - | 5.0 to 5.0 | 5.0 | 1 | Csat Scale | Numeric | None | Enum-like (1 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **feedback_message** | Text | No | - | 18.4746 chars | - | 3,834 | Feedback Message | Required | Not Null | Variable |
| **inbox_id** | Float | No | - | 115.0 to 30,159.0 | 4,107.601 | 78 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_name** | Text | No | - | 13.9045 chars | - | 56 | Inbox Name | Required | Not Null | Variable |
| **is_outside_working_hours** | Integer | No | Category | 0.0 to 1.0 | 0.1758 | 2 | Reference to is outse working hours | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **message_id** | Float | No | - | 426,394,302.0 to 434,909,475.0 | 430,813,082.4345 | 10,000 | Reference to message | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **rating** | Float | No | Score | 1.0 to 5.0 | 3.6771 | 5 | Rating | Numeric; Required | Not Null | Enum-like (5 values) |
| **resolved_by** | Text | No | Category | 3.6581 chars | - | 3 | Resolved By | Required | Not Null | Categorical (3 categories) |
| **response_conversation_id** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Reference to response conversation | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,291 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>127. postgres_hd_messages</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores message data and delivery information.

**Owner/Maintainer:** Conversations Team

**Tags:** `messaging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,460

### account_id` → `postgres_accounts.id` (inferred)
- `broadcast_id` → `broadcasts._id` (inferred)
- `client_echo_id` → Related table (inferred)
- `conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,716

### echo_type

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 1.0 to 4.0
- **Average:** 3.9920844327176783
- **Distinct Values:** 3
- **Null %:** 96.2%

### email_draft

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### eventn_ctx_event_id` → Related table (inferred)
- `is_echo

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.0379
- **Distinct Values:** 2

### message_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 11.0
- **Average:** 3.7189
- **Distinct Values:** 6

### parent_message_id` → Related table (inferred)
- `sender_id` → Related table (inferred)
- `sender_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 4.0289 chars
- **Distinct Values:** 4

### source_id` → Related table (inferred)
- `template_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 98.4129 chars
- **Distinct Values:** 4,537

### template_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_hd_messages`
- **Total Columns:** 30

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1,460 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 51.0 to 27,452.0 | 11,399.7912 | 58 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **broadcast_id** | Float | Yes | - | 4,773,979.0 to 4,775,281.0 (Null: 62.0%) | 4,774,990.367561875 | 62 | Reference to broadcast | Numeric | Foreign Key (likely) | Variable |
| **client_echo_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to client echo | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **content** | Text | No | - | 437.8122 chars | - | 4,628 | Content | Required | Not Null | Variable |
| **content_attributes** | Text | No | - | 496.4759 chars | - | 9,407 | Content Attributes | Required | Not Null | Variable |
| **content_type** | Float | Yes | - | 0.0 to 5.0 (Null: 1.1%) | 0.012033572656487006 | 4 | Type or category classification | Numeric | None | Enum-like (4 values) |
| **conversation_id** | Float | No | - | 62,626,201.0 to 96,407,062.0 | 89,880,775.86720002 | 5,717 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 7,716 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **echo_type** | Float | Yes | - | 1.0 to 4.0 (Null: 96.2%) | 3.9920844327176783 | 3 | Type or category classification | Numeric | None | Enum-like (3 values) |
| **email_draft** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Email address | Numeric; Required | Not Null | Enum-like (1 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,998 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **external_source_ids** | Text | No | Source | 18.0776 chars | - | 1,756 | Reference to external source s | Required | Not Null, Foreign Key (likely) | Variable |
| **identifier** | Text | No | Category | 0.033 chars | - | 10 | Reference to entifier | Required | Not Null, Foreign Key (likely) | Categorical (10 categories) |
| **inbox_id** | Float | No | - | 695.0 to 34,116.0 | 30,702.3972 | 67 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **is_echo** | Integer | Yes | Category | 0.0 to 1.0 | 0.0379 | 2 | Is Echo | Numeric | None | Enum-like (2 values) |
| **message_type** | Float | No | - | 0.0 to 11.0 | 3.7189 | 6 | Type or category classification | Numeric; Required | Not Null | Variable |
| **parent_message_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to parent message | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **private** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Private | Numeric; Required | Not Null | Enum-like (1 values) |
| **sender_id** | Float | Yes | - | 1.0 to 92,103,150.0 (Null: 0.1%) | 412,739.54302581545 | 114 | Reference to sender | Numeric | Foreign Key (likely) | Variable |
| **sender_type** | Text | No | Category | 4.0289 chars | - | 4 | Type or category classification | Required | Not Null | Categorical (4 categories) |
| **source_id** | Text | No | Source | 4.5468 chars | - | 653 | Reference to source | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Float | Yes | - | 0.0 to 2.0 | 1.9711 | 3 | Status or state of record | Numeric | None | Enum-like (3 values) |
| **template_attributes** | Text | No | SerializedJSON | 98.4129 chars | - | 4,537 | Template Attributes | Required | Not Null | Variable |
| **template_id** | Float | Yes | - | 21,706.0 to 114,674.0 (Null: 2.1%) | 110,457.8180982535 | 279 | Reference to template | Numeric | Foreign Key (likely) | Variable |
| **ums_message_id** | Text | No | - | 20.4267 chars | - | 9,726 | Reference to ums message | Required | Not Null, Foreign Key (likely) | Variable |
| **ums_message_source** | Text | No | Source | 7.476 chars | - | 2 | Ums Message Source | Required | Not Null | Categorical (2 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 8,104 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>128. postgres_in_app_feedbacks</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres in app feedbacks operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,489

### eventn_ctx_event_id` → Related table (inferred)
- `feature_name

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 10.0 chars
- **Distinct Values:** 1

### source_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_in_app_feedbacks`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 6 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 6,489 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **feature_likability** | Integer | No | Category | 0.0 to 1.0 | 0.6523 | 2 | Feature Likability | Numeric; Required | Not Null | Enum-like (2 values) |
| **feature_name** | Text | No | Category | 10.0 chars | - | 1 | Feature Name | Required | Not Null | Categorical (1 categories) |
| **source_id** | Float | No | - | 10,863,224.0 to 103,662,327.0 | 89,567,788.80470002 | 4,930 | Reference to source | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **source_type** | Text | No | Category | 12.0 chars | - | 1 | Type or category classification | Required | Not Null | Categorical (1 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 6,489 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>129. postgres_inbox_members</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages inbox configurations and channel settings.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,512

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,818

### eventn_ctx_event_id` → Related table (inferred)
- `inbox_type

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.08588521598053134
- **Distinct Values:** 3
- **Null %:** 1.4%

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 5,817

### user_id` → `postgres_inboxes.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_inbox_members`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1,512 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 5,818 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_id** | Float | No | - | 5.0 to 33,936.0 | 10,361.078699999998 | 1,328 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **inbox_type** | Float | Yes | - | 0.0 to 1.0 (Null: 1.4%) | 0.08588521598053134 | 3 | Type or category classification | Numeric | None | Enum-like (3 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 5,817 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 1.0 to 50,815.0 | 32,722.1544 | 1,743 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>130. postgres_inboxes</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages inbox configurations and channel settings.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 455

### account_id` → `postgres_accounts.id` (inferred)
- `allow_offline_assignment

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.1813
- **Distinct Values:** 2

### auto_alert_duration

- **Type:** `Float`
- **Semantic Type:** `Duration`
- **Nullable:** No
- **Range:** 0.0 to 9,360.0
- **Average:** 718.516707416463
- **Distinct Values:** 36

### auto_close_duration

- **Type:** `Float`
- **Semantic Type:** `Duration`
- **Nullable:** No
- **Range:** 0.0 to 43,200.0
- **Average:** 828.8956805215973
- **Distinct Values:** 56

### auto_resolve_bot_duration

- **Type:** `Float`
- **Semantic Type:** `Duration`
- **Nullable:** No
- **Range:** 0.0 to 10,800.0
- **Average:** 780.5218690573214
- **Distinct Values:** 43

### auto_resolve_duration

- **Type:** `Float`
- **Semantic Type:** `Duration`
- **Nullable:** No
- **Range:** 0.0 to 525,600.0
- **Average:** 2,862.946481934257
- **Distinct Values:** 48

### auto_resolve_voice_duration

- **Type:** `Float`
- **Nullable:** Yes

### away_message

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.3697364846509101 chars
- **Distinct Values:** 5

### bot_handoff_away

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.997826677533279
- **Distinct Values:** 2

### channel_id` → Related table (inferred)
- `channel_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 20.662048356424883 chars
- **Distinct Values:** 17

### conversation_tracking_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,929

### csat_message

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 106.31676174952459 chars
- **Distinct Values:** 53

### csat_question

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 34.028796522684054 chars
- **Distinct Values:** 5

### csat_survey_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.10730779679434936
- **Distinct Values:** 2

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 963
- **Null %:** 73.6%

### email_collect_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0005433306166802499
- **Distinct Values:** 2

### enable_agent_offline

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.004618310241782124
- **Distinct Values:** 2

### enable_auto_assignment

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 2.0
- **Average:** 1.0844879108937788
- **Distinct Values:** 3

### end_time

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0488997555012225 chars
- **Distinct Values:** 12

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_inboxes`
- **Total Columns:** 50

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 455 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,296.0 | 11,350.678076609618 | 711 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **allow_offline_assignment** | Integer | Yes | Category | 0.0 to 1.0 | 0.1813 | 2 | Allow Offline Assignment | Numeric | None | Enum-like (2 values) |
| **auto_alert_duration** | Float | No | Duration | 0.0 to 9,360.0 | 718.516707416463 | 36 | Auto Alert Duration | Numeric; Required | Not Null | Variable |
| **auto_close_duration** | Float | No | Duration | 0.0 to 43,200.0 | 828.8956805215973 | 56 | Auto Close Duration | Numeric; Required | Not Null | Variable |
| **auto_resolve_bot_duration** | Float | No | Duration | 0.0 to 10,800.0 | 780.5218690573214 | 43 | Auto Resolve Bot Duration | Numeric; Required | Not Null | Variable |
| **auto_resolve_duration** | Float | No | Duration | 0.0 to 525,600.0 | 2,862.946481934257 | 48 | Auto Resolve Duration | Numeric; Required | Not Null | Variable |
| **auto_resolve_voice_duration** | Float | Yes | - | - | - | - | Auto Resolve Voice Duration | Numeric | None | Enum-like (0 values) |
| **away_message** | Text | No | Category | 0.3697364846509101 chars | - | 5 | Away Message | Required | Not Null | Categorical (5 categories) |
| **bot_handoff_away** | Integer | No | Category | 0.0 to 1.0 | 0.997826677533279 | 2 | Bot Handoff Away | Numeric; Required | Not Null | Enum-like (2 values) |
| **channel_id** | Float | No | - | 1.0 to 11,528.0 | 4,160.423526215703 | 2,520 | Reference to channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **channel_type** | Text | No | Category | 20.662048356424883 chars | - | 17 | Type or category classification | Required | Not Null | Variable |
| **conversation_tracking_enabled** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Conversation Tracking Enabled | Numeric | None | Enum-like (1 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 2,929 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **csat_message** | Text | No | - | 106.31676174952459 chars | - | 53 | Csat Message | Required | Not Null | Variable |
| **csat_question** | Text | No | Category | 34.028796522684054 chars | - | 5 | Csat Question | Required | Not Null | Categorical (5 categories) |
| **csat_survey_enabled** | Integer | No | Category | 0.0 to 1.0 | 0.10730779679434936 | 2 | Csat Survey Enabled | Numeric; Required | Not Null | Enum-like (2 values) |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 73.6%) | - | 963 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **email_collect_enabled** | Integer | No | Category | 0.0 to 1.0 | 0.0005433306166802499 | 2 | Email address | Numeric; Required | Not Null | Enum-like (2 values) |
| **enable_agent_offline** | Integer | No | Category | 0.0 to 1.0 | 0.004618310241782124 | 2 | Enable Agent Offline | Numeric; Required | Not Null | Enum-like (2 values) |
| **enable_auto_assignment** | Float | No | - | 0.0 to 2.0 | 1.0844879108937788 | 3 | Enable Auto Assignment | Numeric; Required | Not Null | Enum-like (3 values) |
| **end_time** | Text | No | Category | 0.0488997555012225 chars | - | 12 | End Time | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 3,090 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **greeting_enabled** | Integer | Yes | Category | 0.0 to 1.0 | 0.024178212442271124 | 2 | Greeting Enabled | Numeric | None | Enum-like (2 values) |
| **greeting_message** | Text | No | Category | 2.252377071447976 chars | - | 16 | Greeting Message | Required | Not Null | Variable |
| **name** | Text | No | Name | 16.373811464276013 chars | - | 2,728 | Human-readable name or title | Required | Not Null | Variable |
| **opt_in_key** | Text | No | Category | 5.233903830480847 chars | - | 11 | Opt In Key | Required | Not Null | Variable |
| **opt_in_message** | Text | No | Category | 6.7851 chars | - | 5 | Opt In Message | Required | Not Null | Categorical (5 categories) |
| **opt_out_enabled** | Integer | No | Category | 0.0 to 1.0 | 0.1752241238793806 | 2 | Opt Out Enabled | Numeric; Required | Not Null | Enum-like (2 values) |
| **opt_out_key** | Text | No | Category | 5.236348818255909 chars | - | 18 | Opt Out Key | Required | Not Null | Variable |
| **opt_out_message** | Text | No | Category | 42.5281173594132 chars | - | 28 | Opt Out Message | Required | Not Null | Variable |
| **out_of_office_message** | Text | No | - | 45.09372453137734 chars | - | 349 | Out Of Office Message | Required | Not Null | Variable |
| **send_csat_for_auto_resolved_conversation** | Integer | No | Category | 0.0 to 1.0 | 0.17370721048798252 | 2 | Send Csat For Auto Resolved Conversation | Numeric; Required | Not Null | Enum-like (2 values) |
| **send_csat_for_ooo** | Integer | No | Category | 0.0 to 1.0 | 0.17370721048798252 | 2 | Send Csat For Ooo | Numeric; Required | Not Null | Enum-like (2 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **start_time** | Text | No | Category | 0.0467264330345015 chars | - | 10 | Start Time | Required | Not Null | Categorical (10 categories) |
| **status** | Float | No | - | 1.0 to 2.0 | 1.0035316490084216 | 2 | Status or state of record | Numeric; Required | Not Null | Enum-like (2 values) |
| **timezone** | Text | No | Category | 5.255637055148058 chars | - | 13 | Timezone | Required | Not Null | Variable |
| **tracking_reminder_time** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Tracking Reminder Time | Numeric | None | Enum-like (1 values) |
| **ums_enabled** | Integer | No | Category | 0.0 to 1.0 | 0.05517115804806992 | 2 | Ums Enabled | Numeric; Required | Not Null | Enum-like (2 values) |
| **ums_incoming_enabled** | Integer | Yes | Category | 0.0 to 1.0 | 0.06030969845150774 | 2 | Ums Incoming Enabled | Numeric | None | Enum-like (2 values) |
| **ums_outgoing_enabled** | Integer | Yes | Category | 0.0 to 1.0 | 0.004618310241782124 | 2 | Ums Outgoing Enabled | Numeric | None | Enum-like (2 values) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 3,413 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **wa_csat_enabled** | Integer | No | Category | 0.0 to 1.0 | 0.00873998543335761 | 2 | Wa Csat Enabled | Numeric; Required | Not Null | Enum-like (2 values) |
| **wa_widget_access_token** | Text | No | - | 7.871267297887837 chars | - | 193 | Authentication or access token | Required | Not Null, Foreign Key (likely) | Variable |
| **wait_time_enabled** | Float | No | - | 0.0 to 1.0 | 0.04699809834284162 | 2 | Wait Time Enabled | Numeric; Required | Not Null | Enum-like (2 values) |
| **wait_time_message** | Text | No | - | 88.09915783754414 chars | - | 67 | Wait Time Message | Required | Not Null | Variable |
| **widget_bot_name** | Text | No | Category | 3.0331431676174954 chars | - | 26 | Reference to wget bot name | Required | Not Null, Foreign Key (likely) | Variable |
| **working_hours_enabled** | Integer | No | Category | 0.0 to 1.0 | 0.24123879380603097 | 2 | Working Hours Enabled | Numeric; Required | Not Null | Enum-like (2 values) |

</details>

---

<details>
<summary><h2>131. postgres_labels</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores labels and tags for categorization.

**Owner/Maintainer:** Platform Team

**Tags:** `labels`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,234

### account_id` → `postgres_accounts.id` (inferred)
- `active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### color

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.0 chars
- **Distinct Values:** 4

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,582

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.1348 chars
- **Distinct Values:** 41

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_labels`
- **Total Columns:** 16

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 2,234 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,287.0 | 10,494.8853 | 303 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **active** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Active | Numeric; Required | Not Null | Enum-like (1 values) |
| **color** | Text | No | Category | 7.0 chars | - | 4 | Color | Required | Not Null | Categorical (4 categories) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,582 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **description** | Text | No | Description | 0.1348 chars | - | 41 | Description | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,997 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **internal** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Internal | Numeric; Required | Not Null | Enum-like (1 values) |
| **label_level** | Float | No | - | 0.0 to 2.0 | 0.0811 | 3 | Label Level | Numeric; Required | Not Null | Enum-like (3 values) |
| **label_type** | Text | No | Category | 6.0 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **resource_type** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Type or category classification | Numeric; Required | Not Null | Enum-like (1 values) |
| **show_on_sidebar** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Reference to show on sebar | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **title** | Text | No | Title | 17.5563 chars | - | 8,842 | Title | Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,568 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>132. postgres_labels_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_labels. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`, `labels`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 17

### account_id` → `postgres_accounts.id` (inferred)
- `active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### color

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 7.0 chars
- **Distinct Values:** 4

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 8,969

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 1.3446 chars
- **Distinct Values:** 215

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_labels_raw`
- **Total Columns:** 16

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 17 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 476.0 | 138.6545 | 124 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **active** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Active | Numeric; Required | Not Null | Enum-like (1 values) |
| **color** | Text | No | Category | 7.0 chars | - | 4 | Color | Required | Not Null | Categorical (4 categories) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 8,969 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **description** | Text | No | Description | 1.3446 chars | - | 215 | Description | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **internal** | Integer | No | Category | 0.0 to 1.0 | 0.001 | 2 | Internal | Numeric; Required | Not Null | Enum-like (2 values) |
| **label_level** | Float | No | - | 0.0 to 2.0 | 0.0157 | 3 | Label Level | Numeric; Required | Not Null | Enum-like (3 values) |
| **label_type** | Text | No | Category | 6.0 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **resource_type** | Float | No | - | 0.0 to 1.0 | 0.0001 | 2 | Type or category classification | Numeric; Required | Not Null | Enum-like (2 values) |
| **show_on_sidebar** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Reference to show on sebar | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **title** | Text | No | Title | 21.6029 chars | - | 1,283 | Title | Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 5,109 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>133. postgres_lc_contacts_contacts</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores contact and customer profile data.

**Owner/Maintainer:** Customer Data Team

**Tags:** `customer-data`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 710

### account_id` → `postgres_accounts.id` (inferred)
- `additional_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 13.499 chars
- **Distinct Values:** 2,312

### address

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0243 chars
- **Distinct Values:** 2

### conversations_count

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 219.0
- **Average:** 2.849
- **Distinct Values:** 35

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 3,967

### custom_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 1.9994 chars
- **Distinct Values:** 2

### email

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 19.2747 chars
- **Distinct Values:** 8,328

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lc_contacts_contacts`
- **Total Columns:** 18

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 710 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 225.0 | 116.4091 | 25 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **additional_attributes** | Text | No | SerializedJSON | 13.499 chars | - | 2,312 | Additional Attributes | Required | Not Null | Variable |
| **address** | Text | No | SerializedJSON | 2.0243 chars | - | 2 | Address | Required | Not Null | Categorical (2 categories) |
| **conversations_count** | Float | No | - | 1.0 to 219.0 | 2.849 | 35 | Count of conversations | Numeric; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 3,967 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **custom_attributes** | Text | No | SerializedJSON | 1.9994 chars | - | 2 | Custom Attributes | Required | Not Null | Categorical (2 categories) |
| **email** | Text | No | - | 19.2747 chars | - | 8,328 | Email address | Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,913 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **identifier** | Text | No | Category | 0.0 chars | - | 1 | Reference to entifier | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **instagram_username** | Text | No | Category | 0.0 chars | - | 1 | Instagram Username | Required | Not Null | Categorical (1 categories) |
| **name** | Text | No | Name | 11.4404 chars | - | 9,700 | Human-readable name or title | Required | Not Null | Variable |
| **opt_in** | Integer | No | Category | 0.0 to 1.0 | 0.7718 | 2 | Opt In | Numeric; Required | Not Null | Enum-like (2 values) |
| **phone_number** | Text | No | - | 11.938 chars | - | 9,854 | Phone Number | Required | Not Null | Variable |
| **pubsub_token** | Text | No | - | 24.0 chars | - | 9,914 | Authentication or access token | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 4,611 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>134. postgres_lk2_shopify_app_event</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 25

### account_id` → `postgres_accounts.id` (inferred)
- `agent_id` → Related table (inferred)
- `conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 54

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_event`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 25 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 56.0 to 27,909.0 | 11,807.592592592593 | 13 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **agent_id** | Float | Yes | - | 1.0 to 52,230.0 (Null: 81.5%) | 40,964.4 | 8 | Reference to agent | Numeric | Foreign Key (likely) | Variable |
| **conversation_id** | Float | Yes | - | 1,644.0 to 1,380,088.0 (Null: 81.5%) | 558,762.8 | 9 | Reference to conversation | Numeric | Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 54 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 54 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 12.0 chars | - | 1 | Human-readable name or title | Required | Not Null | Categorical (1 categories) |
| **order_id** | Float | No | - | 8,940,734.0 to 28,347,984.0 | 24,895,329.111111112 | 36 | Reference to order | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 54 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>135. postgres_lk2_shopify_app_event_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_lk2_shopify_app_event. Contains unprocessed data before transformation.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `raw-data`, `staging`, `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 25

### account_id` → `postgres_accounts.id` (inferred)
- `agent_id` → Related table (inferred)
- `conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 54

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_event_raw`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 25 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 56.0 to 27,909.0 | 11,807.592592592593 | 13 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **agent_id** | Float | Yes | - | 1.0 to 52,230.0 (Null: 81.5%) | 40,964.4 | 8 | Reference to agent | Numeric | Foreign Key (likely) | Variable |
| **conversation_id** | Float | Yes | - | 1,644.0 to 1,380,088.0 (Null: 81.5%) | 558,762.8 | 9 | Reference to conversation | Numeric | Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 54 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 54 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 12.0 chars | - | 1 | Human-readable name or title | Required | Not Null | Categorical (1 categories) |
| **order_id** | Float | No | - | 8,940,734.0 to 28,347,984.0 | 24,895,329.111111112 | 36 | Reference to order | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 54 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>136. postgres_lk2_shopify_app_orderrefund</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 174

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,561

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)
- `last_updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,561

### note

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 33.573435504469984 chars
- **Distinct Values:** 2

### order_id` → Related table (inferred)
- `processed_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 305
- **Null %:** 80.6%

### shipping_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### shipping_full_refund

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### shopify_refund_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_orderrefund`
- **Total Columns:** 15

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 174 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1,561 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 3.0 chars | - | 2 | Currency | Required | Not Null | Categorical (2 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 1,566 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **is_created_on_shopify** | Integer | No | Category | 0.0 to 1.0 | 0.9974457215836526 | 2 | Is Created On Shopify | Numeric; Required | Not Null | Enum-like (2 values) |
| **last_updated_at** | DateTime | No | UpdatedTimestamp | - | - | 1,561 | Last Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **note** | Text | No | Category | 33.573435504469984 chars | - | 2 | Note | Required | Not Null | Categorical (2 categories) |
| **order_id** | Float | Yes | - | 1,214,523.0 to 28,348,009.0 (Null: 1.5%) | 8,821,745.161373947 | 1,538 | Reference to order | Numeric | Foreign Key (likely) | Variable |
| **processed_at** | DateTime | Yes | - | - (Null: 80.6%) | - | 305 | Processed At | Valid ISO 8601 datetime | None | Variable |
| **shipping_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Shipping Amount | Numeric; Required | Not Null | Enum-like (1 values) |
| **shipping_full_refund** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Shipping Full Refund | Numeric; Required | Not Null | Enum-like (1 values) |
| **shopify_refund_id** | Text | No | - | 2.3301404853128993 chars | - | 305 | Reference to shopify refund | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **user_refund_amount** | Float | No | - | 50.0 to 261,167.0 | 841.4521200510856 | 211 | User Refund Amount | Numeric; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>137. postgres_lk2_shopify_app_orderrefund_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_lk2_shopify_app_orderrefund. Contains unprocessed data before transformation.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `raw-data`, `staging`, `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 174

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,561

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)
- `last_updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,561

### note

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 33.573435504469984 chars
- **Distinct Values:** 2

### order_id` → Related table (inferred)
- `processed_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 305
- **Null %:** 80.6%

### shipping_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### shipping_full_refund

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### shopify_refund_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_orderrefund_raw`
- **Total Columns:** 15

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 174 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1,561 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 3.0 chars | - | 2 | Currency | Required | Not Null | Categorical (2 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 1,566 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **is_created_on_shopify** | Integer | No | Category | 0.0 to 1.0 | 0.9974457215836526 | 2 | Is Created On Shopify | Numeric; Required | Not Null | Enum-like (2 values) |
| **last_updated_at** | DateTime | No | UpdatedTimestamp | - | - | 1,561 | Last Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **note** | Text | No | Category | 33.573435504469984 chars | - | 2 | Note | Required | Not Null | Categorical (2 categories) |
| **order_id** | Float | Yes | - | 1,214,523.0 to 28,348,009.0 (Null: 1.5%) | 8,821,745.161373947 | 1,538 | Reference to order | Numeric | Foreign Key (likely) | Variable |
| **processed_at** | DateTime | Yes | - | - (Null: 80.6%) | - | 305 | Processed At | Valid ISO 8601 datetime | None | Variable |
| **shipping_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Shipping Amount | Numeric; Required | Not Null | Enum-like (1 values) |
| **shipping_full_refund** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Shipping Full Refund | Numeric; Required | Not Null | Enum-like (1 values) |
| **shopify_refund_id** | Text | No | - | 2.3301404853128993 chars | - | 305 | Reference to shopify refund | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **user_refund_amount** | Float | No | - | 50.0 to 261,167.0 | 841.4521200510854 | 211 | User Refund Amount | Numeric; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>138. postgres_lk2_shopify_app_shopifyorder</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 104

### account_id` → `postgres_accounts.id` (inferred)
- `agent_id` → Related table (inferred)
- `applied_discount

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** No
- **Range:** 0.0 to 76,377.0
- **Average:** 44.77312400000003
- **Distinct Values:** 736

### cancel_reason

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.6022 chars
- **Distinct Values:** 3

### cancel_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### cart_id` → Related table (inferred)
- `conversation_id` → Related table (inferred)
- `is_cod

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.4344
- **Distinct Values:** 2

### is_shopify_order

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.677 chars
- **Distinct Values:** 3,576

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 8.9985 chars
- **Distinct Values:** 10,000

### notified_feedback

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_cancellation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_confirmation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_shipped

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_upsell

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_usage

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_reorder

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### order_id` → Related table (inferred)
- `shipping_charges

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 40.0
- **Average:** 10.146
- **Distinct Values:** 3

### shopify_billing_address_id` → Related table (inferred)
- `shopify_customer_id` → Related table (inferred)
- `shopify_financial_status_id` → Related table (inferred)
- `shopify_fulfillment_status_id` → Related table (inferred)
- `shopify_order_status_id` → Related table (inferred)
- `shopify_order_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 57.0 chars
- **Distinct Values:** 9,999

### shopify_shipping_address_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_shopifyorder`
- **Total Columns:** 54

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 104 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 1.0 | 1.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **agent_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to agent | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **amount** | Float | No | - | 0.0 to 40,333.0 | 673.8161759999998 | 1,475 | Amount | Numeric; Required | Not Null | Variable |
| **applied_discount** | Float | No | Discount | 0.0 to 76,377.0 | 44.77312400000003 | 736 | Count of applied_dis | Numeric; Required | Not Null | Variable |
| **cancel_reason** | Text | No | Category | 0.6022 chars | - | 3 | Cancel Reason | Required | Not Null | Categorical (3 categories) |
| **cancel_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Cancel Tags | Required | Not Null | Categorical (1 categories) |
| **cancelled** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Cancelled | Numeric; Required | Not Null | Enum-like (1 values) |
| **cart_id** | Float | Yes | - | 1,211,275.0 to 186,789,533.0 | 79,351,993.2806 | 10,000 | Reference to cart | Numeric | Foreign Key (likely) | Variable |
| **conversation_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to conversation | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **create_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Create Tags | Required | Not Null | Categorical (1 categories) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,991 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 2.4882 chars | - | 2 | Currency | Required | Not Null | Categorical (2 categories) |
| **customer_id** | Text | No | - | 12.9989 chars | - | 7,918 | Reference to customer | Required | Not Null, Foreign Key (likely) | Variable |
| **edit_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Edit Tags | Required | Not Null | Categorical (1 categories) |
| **email** | Text | No | Email | 22.457 chars | - | 7,627 | Email address | Valid email format; Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_name** | Text | No | Name | 6.4831 chars | - | 3,929 | Human-readable name or title | Required | Not Null | Variable |
| **fixed_price** | Float | No | - | 0.0 to 40,333.0 | 572.2139000000001 | 1,360 | Fixed Price | Numeric; Required | Not Null | Variable |
| **is_cod** | Integer | No | Category | 0.0 to 1.0 | 0.4344 | 2 | Is Cod | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_shopify_order** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Is Shopify Order | Numeric; Required | Not Null | Enum-like (1 values) |
| **last_name** | Text | No | Name | 5.677 chars | - | 3,576 | Human-readable name or title | Required | Not Null | Variable |
| **name** | Text | No | Name | 8.9985 chars | - | 10,000 | Human-readable name or title | Required | Not Null | Variable |
| **notified_feedback** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Feedback | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_order_cancellation** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Order Cancellation | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_order_confirmation** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Order Confirmation | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_order_shipped** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Order Shipped | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_product_upsell** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Product Upsell | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_product_usage** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Product Usage | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_reorder** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Reorder | Numeric; Required | Not Null | Enum-like (1 values) |
| **order_id** | Text | No | - | 13.0 chars | - | 9,999 | Reference to order | Required | Not Null, Foreign Key (likely) | Variable |
| **order_notes** | Text | No | - | 1.3041 chars | - | 44 | Order Notes | Required | Not Null | Variable |
| **order_status_url** | Text | No | URL | 116.2159 chars | - | 9,999 | Status or state of record | Valid URL format; Required | Not Null | Variable |
| **phone_number** | Text | No | - | 1.3776 chars | - | 849 | Phone Number | Required | Not Null | Variable |
| **presentment_currency** | Text | No | Category | 2.4882 chars | - | 2 | Presentment Currency | Required | Not Null | Categorical (2 categories) |
| **refund_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Refund Tags | Required | Not Null | Categorical (1 categories) |
| **refunded_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Refunded Amount | Numeric; Required | Not Null | Enum-like (1 values) |
| **shipping_charges** | Float | No | - | 0.0 to 40.0 | 10.146 | 3 | Shipping Charges | Numeric; Required | Not Null | Enum-like (3 values) |
| **shopify_billing_address_id** | Float | Yes | - | 208,846.0 to 32,349,309.0 (Null: 2.9%) | 20,234,272.84181256 | 9,061 | Reference to shopify billing address | Numeric | Foreign Key (likely) | Variable |
| **shopify_customer_id** | Float | No | - | 348,683.0 to 43,008,768.0 | 27,388,399.1049 | 7,922 | Reference to shopify customer | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **shopify_financial_status_id** | Float | No | - | 5.0 to 11.0 | 6.8798 | 4 | Status or state of record | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (4 values) |
| **shopify_fulfillment_status_id** | Float | Yes | - | 12.0 to 15.0 | 12.0391 | 3 | Status or state of record | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **shopify_order_status_id** | Float | No | - | 1.0 to 3.0 | 1.1618 | 2 | Status or state of record | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **shopify_order_url** | Text | No | URL | 57.0 chars | - | 9,999 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **shopify_shipping_address_id** | Float | Yes | - | 555,317.0 to 32,349,310.0 (Null: 46.9%) | 21,658,779.531373657 | 5,095 | Reference to shopify shipping address | Numeric | Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **subtotal_price** | Float | No | - | 0.0 to 40,333.0 | 663.6701759999999 | 1,216 | Subtotal Price | Numeric; Required | Not Null | Variable |
| **tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Tags | Required | Not Null | Categorical (1 categories) |
| **total_price** | Float | No | - | 0.0 to 19,500.0 | 622.811323 | 1,417 | Total Price | Numeric; Required | Not Null | Variable |
| **total_tax** | Float | No | - | 0.0 to 730.68 | 15.953373999999998 | 435 | Total Tax | Numeric; Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,927 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_owe_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | User Owe Amount | Numeric; Required | Not Null | Enum-like (1 values) |
| **user_refund_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | User Refund Amount | Numeric; Required | Not Null | Enum-like (1 values) |

</details>

---

<details>
<summary><h2>139. postgres_lk2_shopify_app_shopifyorder_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_lk2_shopify_app_shopifyorder. Contains unprocessed data before transformation.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `raw-data`, `staging`, `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 103

### account_id` → `postgres_accounts.id` (inferred)
- `agent_id` → Related table (inferred)
- `applied_discount

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** No
- **Range:** 0.0 to 76,377.0
- **Average:** 44.77312400000003
- **Distinct Values:** 736

### cancel_reason

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.6022 chars
- **Distinct Values:** 3

### cancel_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### cart_id` → Related table (inferred)
- `conversation_id` → Related table (inferred)
- `is_cod

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.4344
- **Distinct Values:** 2

### is_shopify_order

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.677 chars
- **Distinct Values:** 3,577

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 8.9986 chars
- **Distinct Values:** 10,000

### notified_feedback

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_cancellation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_confirmation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_shipped

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_upsell

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_usage

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_reorder

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### order_id` → Related table (inferred)
- `shipping_charges

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 40.0
- **Average:** 10.146
- **Distinct Values:** 3

### shopify_billing_address_id` → Related table (inferred)
- `shopify_customer_id` → Related table (inferred)
- `shopify_financial_status_id` → Related table (inferred)
- `shopify_fulfillment_status_id` → Related table (inferred)
- `shopify_order_status_id` → Related table (inferred)
- `shopify_order_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 57.0 chars
- **Distinct Values:** 9,999

### shopify_shipping_address_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_shopifyorder_raw`
- **Total Columns:** 54

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 103 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 1.0 | 1.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **agent_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to agent | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **amount** | Float | No | - | 0.0 to 40,333.0 | 673.826176 | 1,475 | Amount | Numeric; Required | Not Null | Variable |
| **applied_discount** | Float | No | Discount | 0.0 to 76,377.0 | 44.77312400000003 | 736 | Count of applied_dis | Numeric; Required | Not Null | Variable |
| **cancel_reason** | Text | No | Category | 0.6022 chars | - | 3 | Cancel Reason | Required | Not Null | Categorical (3 categories) |
| **cancel_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Cancel Tags | Required | Not Null | Categorical (1 categories) |
| **cancelled** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Cancelled | Numeric; Required | Not Null | Enum-like (1 values) |
| **cart_id** | Float | Yes | - | 1,211,275.0 to 119,066,912.0 | 79,342,889.7938 | 10,000 | Reference to cart | Numeric | Foreign Key (likely) | Variable |
| **conversation_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to conversation | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **create_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Create Tags | Required | Not Null | Categorical (1 categories) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,991 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 2.4882 chars | - | 2 | Currency | Required | Not Null | Categorical (2 categories) |
| **customer_id** | Text | No | - | 12.9989 chars | - | 7,919 | Reference to customer | Required | Not Null, Foreign Key (likely) | Variable |
| **edit_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Edit Tags | Required | Not Null | Categorical (1 categories) |
| **email** | Text | No | Email | 22.4576 chars | - | 7,628 | Email address | Valid email format; Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_name** | Text | No | Name | 6.4837 chars | - | 3,930 | Human-readable name or title | Required | Not Null | Variable |
| **fixed_price** | Float | No | - | 0.0 to 40,333.0 | 572.2239 | 1,360 | Fixed Price | Numeric; Required | Not Null | Variable |
| **is_cod** | Integer | No | Category | 0.0 to 1.0 | 0.4344 | 2 | Is Cod | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_shopify_order** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Is Shopify Order | Numeric; Required | Not Null | Enum-like (1 values) |
| **last_name** | Text | No | Name | 5.677 chars | - | 3,577 | Human-readable name or title | Required | Not Null | Variable |
| **name** | Text | No | Name | 8.9986 chars | - | 10,000 | Human-readable name or title | Required | Not Null | Variable |
| **notified_feedback** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Feedback | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_order_cancellation** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Order Cancellation | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_order_confirmation** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Order Confirmation | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_order_shipped** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Order Shipped | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_product_upsell** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Product Upsell | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_product_usage** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Product Usage | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_reorder** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Reorder | Numeric; Required | Not Null | Enum-like (1 values) |
| **order_id** | Text | No | - | 13.0 chars | - | 9,999 | Reference to order | Required | Not Null, Foreign Key (likely) | Variable |
| **order_notes** | Text | No | - | 1.3041 chars | - | 44 | Order Notes | Required | Not Null | Variable |
| **order_status_url** | Text | No | URL | 116.2159 chars | - | 9,999 | Status or state of record | Valid URL format; Required | Not Null | Variable |
| **phone_number** | Text | No | - | 1.3776 chars | - | 849 | Phone Number | Required | Not Null | Variable |
| **presentment_currency** | Text | No | Category | 2.4882 chars | - | 2 | Presentment Currency | Required | Not Null | Categorical (2 categories) |
| **refund_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Refund Tags | Required | Not Null | Categorical (1 categories) |
| **refunded_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Refunded Amount | Numeric; Required | Not Null | Enum-like (1 values) |
| **shipping_charges** | Float | No | - | 0.0 to 40.0 | 10.146 | 3 | Shipping Charges | Numeric; Required | Not Null | Enum-like (3 values) |
| **shopify_billing_address_id** | Float | Yes | - | 208,846.0 to 32,349,309.0 (Null: 2.9%) | 20,234,455.360968046 | 9,061 | Reference to shopify billing address | Numeric | Foreign Key (likely) | Variable |
| **shopify_customer_id** | Float | No | - | 348,683.0 to 43,008,768.0 | 27,388,529.157000005 | 7,923 | Reference to shopify customer | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **shopify_financial_status_id** | Float | No | - | 5.0 to 11.0 | 6.8798 | 4 | Status or state of record | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (4 values) |
| **shopify_fulfillment_status_id** | Float | Yes | - | 12.0 to 15.0 | 12.0391 | 3 | Status or state of record | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **shopify_order_status_id** | Float | No | - | 1.0 to 3.0 | 1.1618 | 2 | Status or state of record | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **shopify_order_url** | Text | No | URL | 57.0 chars | - | 9,999 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **shopify_shipping_address_id** | Float | Yes | - | 555,317.0 to 32,349,310.0 (Null: 46.9%) | 21,659,423.65957046 | 5,096 | Reference to shopify shipping address | Numeric | Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **subtotal_price** | Float | No | - | 0.0 to 40,333.0 | 663.6801759999998 | 1,216 | Subtotal Price | Numeric; Required | Not Null | Variable |
| **tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Tags | Required | Not Null | Categorical (1 categories) |
| **total_price** | Float | No | - | 0.0 to 19,500.0 | 622.8213230000001 | 1,417 | Total Price | Numeric; Required | Not Null | Variable |
| **total_tax** | Float | No | - | 0.0 to 730.68 | 15.962815999999997 | 435 | Total Tax | Numeric; Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,927 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_owe_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | User Owe Amount | Numeric; Required | Not Null | Enum-like (1 values) |
| **user_refund_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | User Refund Amount | Numeric; Required | Not Null | Enum-like (1 values) |

</details>

---

<details>
<summary><h2>140. postgres_lk2_shopify_app_shopifyproduct</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 64

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,390

### default_variant_id` → Related table (inferred)
- `description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 613.5825 chars
- **Distinct Values:** 4,687

### eventn_ctx_event_id` → Related table (inferred)
- `price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 152,000.0
- **Average:** 2,330.878592370482
- **Distinct Values:** 854
- **Null %:** 40.0%

### product_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_shopifyproduct`
- **Total Columns:** 18

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 64 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 9,872.0 | 9,126.289 | 9 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 4,390 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **default_variant_id** | Float | Yes | - | 166.0 to 5,470,942.0 (Null: 18.0%) | 42,058.52842156624 | 8,199 | Reference to default variant | Numeric | Foreign Key (likely) | Variable |
| **description** | Text | No | Description | 613.5825 chars | - | 4,687 | Description | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **fetched_description** | Text | No | Description | 613.5825 chars | - | 4,687 | Fetched Description | Required | Not Null | Variable |
| **name** | Text | No | Name | 47.021 chars | - | 4,651 | Human-readable name or title | Required | Not Null | Variable |
| **popularity** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Popularity | Numeric; Required | Not Null | Enum-like (1 values) |
| **price** | Float | Yes | - | 0.0 to 152,000.0 (Null: 40.0%) | 2,330.878592370482 | 854 | Price | Numeric | None | Variable |
| **product_id** | Text | No | - | 13.0 chars | - | 10,000 | Reference to product | Required | Not Null, Foreign Key (likely) | Variable |
| **product_link** | Text | No | - | 20.5119 chars | - | 2,462 | Product Link | Required | Not Null | Variable |
| **purchasable** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Purchasable | Numeric; Required | Not Null | Enum-like (1 values) |
| **sale_price** | Float | Yes | - | 0.0 to 140,000.0 (Null: 18.0%) | 1,649.59369480361 | 1,046 | Sale Price | Numeric | None | Variable |
| **sku** | Text | No | - | 6.7072 chars | - | 3,759 | Sku | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 5,211 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>141. postgres_lk2_shopify_app_shopifyproduct_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_lk2_shopify_app_shopifyproduct. Contains unprocessed data before transformation.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `raw-data`, `staging`, `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 55

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,390

### default_variant_id` → Related table (inferred)
- `description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 613.5827 chars
- **Distinct Values:** 4,685

### eventn_ctx_event_id` → Related table (inferred)
- `price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 152,000.0
- **Average:** 2,330.5765767116445
- **Distinct Values:** 851
- **Null %:** 40.0%

### product_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_shopify_app_shopifyproduct_raw`
- **Total Columns:** 18

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 55 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 9,872.0 | 9,126.289 | 9 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 4,390 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **default_variant_id** | Float | Yes | - | 166.0 to 5,470,942.0 (Null: 18.0%) | 42,058.522932422544 | 8,199 | Reference to default variant | Numeric | Foreign Key (likely) | Variable |
| **description** | Text | No | Description | 613.5827 chars | - | 4,685 | Description | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **fetched_description** | Text | No | Description | 613.5827 chars | - | 4,685 | Fetched Description | Required | Not Null | Variable |
| **name** | Text | No | Name | 47.0141 chars | - | 4,651 | Human-readable name or title | Required | Not Null | Variable |
| **popularity** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Popularity | Numeric; Required | Not Null | Enum-like (1 values) |
| **price** | Float | Yes | - | 0.0 to 152,000.0 (Null: 40.0%) | 2,330.5765767116445 | 851 | Price | Numeric | None | Variable |
| **product_id** | Text | No | - | 13.0 chars | - | 10,000 | Reference to product | Required | Not Null, Foreign Key (likely) | Variable |
| **product_link** | Text | No | - | 20.5119 chars | - | 2,462 | Product Link | Required | Not Null | Variable |
| **purchasable** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Purchasable | Numeric; Required | Not Null | Enum-like (1 values) |
| **sale_price** | Float | Yes | - | 0.0 to 140,000.0 (Null: 18.0%) | 1,649.6864003415462 | 1,042 | Sale Price | Numeric | None | Variable |
| **sku** | Text | No | - | 6.7071 chars | - | 3,759 | Sku | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 5,211 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>142. postgres_lk2_store_ordermodel</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 81

### account_id` → `postgres_accounts.id` (inferred)
- `amount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 101,800.0
- **Average:** 1,376.4268030000046
- **Distinct Values:** 2,796

### attribution_id` → Related table (inferred)
- `cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.037
- **Distinct Values:** 2

### checkout_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 14.008 chars
- **Distinct Values:** 4,361

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,431

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 5

### customer_id` → Related table (inferred)
- `shipping_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 10,941.0
- **Average:** 25.779347
- **Distinct Values:** 69

### shopify_store_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_store_ordermodel`
- **Total Columns:** 33

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 81 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,607.0 | 7,886.9239 | 158 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **amount** | Float | Yes | - | 0.0 to 101,800.0 | 1,376.4268030000046 | 2,796 | Amount | Numeric | None | Variable |
| **attribution_id** | Float | Yes | - | 68,327.0 to 68,478.0 (Null: 100.0%) | 68,402.5 | 3 | Reference to attribution | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **cancelled** | Integer | No | Category | 0.0 to 1.0 | 0.037 | 2 | Cancelled | Numeric; Required | Not Null | Enum-like (2 values) |
| **checkout_token** | Text | No | - | 14.008 chars | - | 4,361 | Authentication or access token | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,431 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 3.0 chars | - | 5 | Currency | Required | Not Null | Categorical (5 categories) |
| **customer_id** | Text | No | - | 12.9926 chars | - | 9,767 | Reference to customer | Required | Not Null, Foreign Key (likely) | Variable |
| **delivery_date** | Text | No | Category | 0.0 chars | - | 1 | Delivery Date | Required | Not Null | Categorical (1 categories) |
| **email** | Text | No | Email | 22.6323 chars | - | 9,475 | Email address | Valid email format; Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,905 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_name** | Text | No | Name | 6.3815 chars | - | 5,515 | Human-readable name or title | Required | Not Null | Variable |
| **fulfillment_status** | Text | No | Category | 8.0602 chars | - | 5 | Status or state of record | Required | Not Null | Categorical (5 categories) |
| **item_names** | Text | No | SerializedJSON | 98.6283 chars | - | 5,770 | Item Names | Required | Not Null | Variable |
| **items** | Text | No | SerializedJSON | 1,217.9743 chars | - | 9,906 | Items | Required | Not Null | Variable |
| **last_name** | Text | No | Name | 5.3284 chars | - | 4,841 | Human-readable name or title | Required | Not Null | Variable |
| **name** | Text | No | Name | 9.4534 chars | - | 9,906 | Human-readable name or title | Required | Not Null | Variable |
| **order_id** | Text | No | - | 12.9979 chars | - | 9,908 | Reference to order | Required | Not Null, Foreign Key (likely) | Variable |
| **order_notes** | Text | No | - | 2.3306 chars | - | 274 | Order Notes | Required | Not Null | Variable |
| **payment_method** | Text | No | Category | 0.0018 chars | - | 3 | Payment Method | Required | Not Null | Categorical (3 categories) |
| **payment_status** | Text | No | Category | 5.3024 chars | - | 8 | Status or state of record | Required | Not Null | Categorical (8 categories) |
| **phone_number** | Text | No | - | 11.712 chars | - | 9,577 | Phone Number | Required | Not Null | Variable |
| **presentment_currency** | Text | No | Category | 2.9991 chars | - | 16 | Presentment Currency | Required | Not Null | Variable |
| **refund_status** | Text | No | Category | 0.0 chars | - | 1 | Status or state of record | Required | Not Null | Categorical (1 categories) |
| **refunded_amount** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Refunded Amount | Numeric | None | Enum-like (1 values) |
| **shipping_price** | Float | No | - | 0.0 to 10,941.0 | 25.779347 | 69 | Shipping Price | Numeric; Required | Not Null | Variable |
| **shopify_store_id** | Float | Yes | - | 5.0 to 12,974.0 (Null: 0.0%) | 3,820.2992897869367 | 158 | Reference to shopify store | Numeric | Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **subtotal_price** | Float | Yes | - | 0.0 to 101,800.0 (Null: 0.0%) | 1,350.106913073927 | 2,427 | Subtotal Price | Numeric | None | Variable |
| **tags** | Text | No | SerializedJSON | 46.925 chars | - | 4,073 | Tags | Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 6,002 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>143. postgres_lk2_store_ordermodel_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_lk2_store_ordermodel. Contains unprocessed data before transformation.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `raw-data`, `staging`, `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 65

### account_id` → `postgres_accounts.id` (inferred)
- `amount

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 862,808.0
- **Average:** 6,339.9953709999945
- **Distinct Values:** 2,402

### attribution_id` → Related table (inferred)
- `cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0992
- **Distinct Values:** 2

### checkout_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 25.4112 chars
- **Distinct Values:** 7,937

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,997

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.4492 chars
- **Distinct Values:** 2

### customer_id` → Related table (inferred)
- `shipping_price

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 26,930.0
- **Average:** 261.51525100000015
- **Distinct Values:** 373

### shopify_store_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_store_ordermodel_raw`
- **Total Columns:** 33

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 65 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 19,409.0 | 15,876.487 | 11 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **amount** | Float | Yes | - | 0.0 to 862,808.0 | 6,339.9953709999945 | 2,402 | Amount | Numeric | None | Variable |
| **attribution_id** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Reference to attribution | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **cancelled** | Integer | No | Category | 0.0 to 1.0 | 0.0992 | 2 | Cancelled | Numeric; Required | Not Null | Enum-like (2 values) |
| **checkout_token** | Text | No | - | 25.4112 chars | - | 7,937 | Authentication or access token | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,997 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 2.4492 chars | - | 2 | Currency | Required | Not Null | Categorical (2 categories) |
| **customer_id** | Text | No | - | 10.4345 chars | - | 6,233 | Reference to customer | Required | Not Null, Foreign Key (likely) | Variable |
| **delivery_date** | Text | No | Category | 0.0 chars | - | 1 | Delivery Date | Required | Not Null | Categorical (1 categories) |
| **email** | Text | No | - | 18.8776 chars | - | 5,056 | Email address | Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_name** | Text | No | Name | 6.337 chars | - | 4,234 | Human-readable name or title | Required | Not Null | Variable |
| **fulfillment_status** | Text | No | Category | 7.1268 chars | - | 4 | Status or state of record | Required | Not Null | Categorical (4 categories) |
| **item_names** | Text | No | SerializedJSON | 79.6488 chars | - | 6,228 | Item Names | Required | Not Null | Variable |
| **items** | Text | No | SerializedJSON | 1,219.1025 chars | - | 10,001 | Items | Required | Not Null | Variable |
| **last_name** | Text | No | Name | 6.305 chars | - | 4,020 | Human-readable name or title | Required | Not Null | Variable |
| **name** | Text | No | Name | 5.786 chars | - | 9,615 | Human-readable name or title | Required | Not Null | Variable |
| **order_id** | Text | No | - | 10.7007 chars | - | 10,000 | Reference to order | Required | Not Null, Foreign Key (likely) | Variable |
| **order_notes** | Text | No | - | 9.783 chars | - | 1,628 | Order Notes | Required | Not Null | Variable |
| **payment_method** | Text | No | Category | 0.0 chars | - | 1 | Payment Method | Required | Not Null | Categorical (1 categories) |
| **payment_status** | Text | No | Category | 4.664 chars | - | 6 | Status or state of record | Required | Not Null | Categorical (6 categories) |
| **phone_number** | Text | No | - | 11.0538 chars | - | 5,912 | Phone Number | Required | Not Null | Variable |
| **presentment_currency** | Text | No | Category | 2.4492 chars | - | 2 | Presentment Currency | Required | Not Null | Categorical (2 categories) |
| **refund_status** | Text | No | Category | 0.0 chars | - | 1 | Status or state of record | Required | Not Null | Categorical (1 categories) |
| **refunded_amount** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Refunded Amount | Numeric | None | Enum-like (1 values) |
| **shipping_price** | Float | No | - | 0.0 to 26,930.0 | 261.51525100000015 | 373 | Shipping Price | Numeric; Required | Not Null | Variable |
| **shopify_store_id** | Float | Yes | - | 9.0 to 10,328.0 (Null: 18.4%) | 8,862.69052579973 | 8 | Reference to shopify store | Numeric | Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **subtotal_price** | Float | Yes | - | 0.0 to 862,808.0 | 6,079.040119999997 | 1,667 | Subtotal Price | Numeric | None | Variable |
| **tags** | Text | No | SerializedJSON | 53.2 chars | - | 5,534 | Tags | Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 1,126 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>144. postgres_lk2_store_productcollectionmodel</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 77

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_store_productcollectionmodel`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 77 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 12,512.0 | 918.7357000000002 | 99 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **collection_id** | Text | No | - | 36.8821 chars | - | 9,753 | Reference to collection | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 793 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 16.0437 chars | - | 8,530 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **store_type** | Text | No | Category | 6.9958 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 2,703 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>145. postgres_lk2_store_productcollectionmodel_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_lk2_store_productcollectionmodel. Contains unprocessed data before transformation.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 26

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk2_store_productcollectionmodel_raw`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 26 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 12,512.0 | 918.7357000000002 | 99 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **collection_id** | Text | No | - | 36.8821 chars | - | 9,753 | Reference to collection | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 793 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 16.0234 chars | - | 8,518 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **store_type** | Text | No | Category | 6.9958 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 2,466 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>146. postgres_lk_account_accountmodel</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages account information and configurations.

**Owner/Maintainer:** Accounts/Billing Team

**Tags:** `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 112

### bobble_ai_account_id` → `postgres_accounts.id` (inferred)
- `checkout_provider_id` → Related table (inferred)
- `crm_id` → Related table (inferred)
- `dashboard_access_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 23.964071856287426 chars
- **Distinct Values:** 647

### eventn_ctx_event_id` → Related table (inferred)
- `logistics_id` → Related table (inferred)
- `name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 13.328842315369261 chars
- **Distinct Values:** 2,004

### payment_channels_id` → Related table (inferred)
- `shortio_authorization

- **Type:** `Text`
- **Semantic Type:** `Author`
- **Nullable:** No
- **Avg Length:** 1.0778443113772456 chars
- **Distinct Values:** 3

### shortio_domain

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.5484031936127745 chars
- **Distinct Values:** 5

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### store_id` → Related table (inferred)
- `user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_account_accountmodel`
- **Total Columns:** 19

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 112 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **bobble_ai_account_id** | Float | Yes | - | 1.0 to 1.0 (Null: 100.0%) | 1.0 | 2 | Reference to account | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **checkout_provider_id** | Float | Yes | - | 34.0 to 103.0 (Null: 99.7%) | 84.5 | 7 | Reference to checkout prover | Numeric | Foreign Key (likely) | Variable |
| **crm_id** | Float | Yes | - | 1.0 to 4,456.0 (Null: 70.3%) | 2,758.4705882352937 | 596 | Reference to crm | Numeric | Foreign Key (likely) | Variable |
| **dashboard_access_token** | Text | No | - | 23.964071856287426 chars | - | 647 | Authentication or access token | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 2,004 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **facebook_page_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to facebook page | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **gitlab_private_token** | Text | No | Category | 0.17964071856287425 chars | - | 2 | Authentication or access token | Required | Not Null | Categorical (2 categories) |
| **gitlab_project_id** | Text | No | Category | 0.0718562874251497 chars | - | 19 | Reference to gitlab project | Required | Not Null, Foreign Key (likely) | Variable |
| **is_active** | Integer | No | Category | 0.0 to 1.0 | 0.2994011976047904 | 2 | Is Active | Numeric; Required | Not Null | Enum-like (2 values) |
| **logistics_id** | Float | Yes | - | 2.0 to 5,117.0 (Null: 74.9%) | 3,624.8310139165 | 504 | Reference to logistics | Numeric | Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 13.328842315369261 chars | - | 2,004 | Human-readable name or title | Required | Not Null | Variable |
| **payment_channels_id** | Float | Yes | - | 2.0 to 1,139.0 (Null: 97.7%) | 738.4347826086956 | 46 | Reference to payment channels | Numeric | Foreign Key (likely) | Variable |
| **shortio_authorization** | Text | No | Author | 1.0778443113772456 chars | - | 3 | Shortio Authorization | Required | Not Null | Categorical (3 categories) |
| **shortio_domain** | Text | No | Category | 0.5484031936127745 chars | - | 5 | Shortio Domain | Required | Not Null | Categorical (5 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **store_id** | Float | Yes | - | 1.0 to 13,674.0 (Null: 64.1%) | 7,146.391666666666 | 717 | Reference to store | Numeric | Foreign Key (likely) | Variable |
| **user_id** | Float | Yes | - | 2.0 to 27,659.0 (Null: 0.2%) | 15,449.579789894948 | 2,000 | Reference to user | Numeric | Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>147. postgres_lk_account_accountproperties</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages account information and configurations.

**Owner/Maintainer:** Accounts/Billing Team

**Tags:** `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `broadcasts

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### cost_per_bot

- **Type:** `Float`
- **Semantic Type:** `Cost`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 0.9417472118959106
- **Distinct Values:** 22

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1

### crm

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### deal_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.45353159851301 chars
- **Distinct Values:** 269

### deal_owner

- **Type:** `Text`
- **Semantic Type:** `Owner`
- **Nullable:** No
- **Avg Length:** 12.58736059479554 chars
- **Distinct Values:** 15

### deal_stage

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 14.431226765799256 chars
- **Distinct Values:** 4

### eventn_ctx_event_id` → `broadcasts._id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_account_accountproperties`
- **Total Columns:** 24

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 28,703.0 | 22,422.32342007435 | 259 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **broadcasts** | Integer | No | Category | 0.0 to 1.0 | 0.9776951672862454 | 2 | Broadcasts | Numeric; Required | Not Null | Enum-like (2 values) |
| **cost_per_bot** | Float | No | Cost | 0.0 to 3.0 | 0.9417472118959106 | 22 | Cost Per Bot | Numeric; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **crm** | Integer | No | Category | 0.0 to 1.0 | 0.9776951672862454 | 2 | Crm | Numeric; Required | Not Null | Enum-like (2 values) |
| **deal_name** | Text | No | - | 18.45353159851301 chars | - | 269 | Deal Name | Required | Not Null | Variable |
| **deal_owner** | Text | No | Owner | 12.58736059479554 chars | - | 15 | Deal Owner | Required | Not Null | Variable |
| **deal_stage** | Text | No | Category | 14.431226765799256 chars | - | 4 | Deal Stage | Required | Not Null | Categorical (4 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 269 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **flows** | Integer | No | Category | 0.0 to 1.0 | 0.9776951672862454 | 2 | Flows | Numeric; Required | Not Null | Enum-like (2 values) |
| **free_active_contacts** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Free Active Contacts | Numeric; Required | Not Null | Enum-like (1 values) |
| **free_agents** | Float | No | - | 0.0 to 60.0 | 4.144981412639405 | 20 | Free Agents | Numeric; Required | Not Null | Variable |
| **free_bot_sessions** | Float | No | - | 0.0 to 150,000.0 | 2,473.977695167286 | 14 | Free Bot Sessions | Numeric; Required | Not Null | Variable |
| **ig** | Integer | No | Category | 0.0 to 1.0 | 0.12267657992565056 | 2 | Ig | Numeric; Required | Not Null | Enum-like (2 values) |
| **ndr** | Integer | No | Category | 0.0 to 1.0 | 0.9776951672862454 | 2 | Ndr | Numeric; Required | Not Null | Enum-like (2 values) |
| **nps** | Integer | No | Category | 0.0 to 1.0 | 0.9776951672862454 | 2 | Nps | Numeric; Required | Not Null | Enum-like (2 values) |
| **outbound_cost** | Float | No | Cost | 0.0 to 2.0 | 0.02758364312267658 | 11 | Outbound Cost | Numeric; Required | Not Null | Variable |
| **per_agent_fee** | Float | No | - | 0.0 to 3,000.0 | 1,104.2081784386617 | 28 | Per Agent Fee | Numeric; Required | Not Null | Variable |
| **pipeline** | Text | No | Category | 0.0 chars | - | 1 | Pipeline | Required | Not Null | Categorical (1 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **type_of_bot** | Text | No | Category | 6.79182156133829 chars | - | 6 | Type or category classification | Required | Not Null | Categorical (6 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 1 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>148. postgres_lk_account_accountproperties_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_lk_account_accountproperties. Contains unprocessed data before transformation.

**Owner/Maintainer:** Accounts/Billing Team

**Tags:** `raw-data`, `staging`, `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `broadcasts

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### cost_per_bot

- **Type:** `Float`
- **Semantic Type:** `Cost`
- **Nullable:** No
- **Range:** 0.0 to 3.0
- **Average:** 0.9417472118959106
- **Distinct Values:** 22

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1

### crm

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.9776951672862454
- **Distinct Values:** 2

### deal_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 18.45353159851301 chars
- **Distinct Values:** 269

### deal_owner

- **Type:** `Text`
- **Semantic Type:** `Owner`
- **Nullable:** No
- **Avg Length:** 12.58736059479554 chars
- **Distinct Values:** 15

### deal_stage

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 14.431226765799256 chars
- **Distinct Values:** 4

### eventn_ctx_event_id` → `broadcasts._id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_account_accountproperties_raw`
- **Total Columns:** 24

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 28,703.0 | 22,422.32342007435 | 259 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **broadcasts** | Integer | No | Category | 0.0 to 1.0 | 0.9776951672862454 | 2 | Broadcasts | Numeric; Required | Not Null | Enum-like (2 values) |
| **cost_per_bot** | Float | No | Cost | 0.0 to 3.0 | 0.9417472118959106 | 22 | Cost Per Bot | Numeric; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **crm** | Integer | No | Category | 0.0 to 1.0 | 0.9776951672862454 | 2 | Crm | Numeric; Required | Not Null | Enum-like (2 values) |
| **deal_name** | Text | No | - | 18.45353159851301 chars | - | 269 | Deal Name | Required | Not Null | Variable |
| **deal_owner** | Text | No | Owner | 12.58736059479554 chars | - | 15 | Deal Owner | Required | Not Null | Variable |
| **deal_stage** | Text | No | Category | 14.431226765799256 chars | - | 4 | Deal Stage | Required | Not Null | Categorical (4 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 269 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **flows** | Integer | No | Category | 0.0 to 1.0 | 0.9776951672862454 | 2 | Flows | Numeric; Required | Not Null | Enum-like (2 values) |
| **free_active_contacts** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Free Active Contacts | Numeric; Required | Not Null | Enum-like (1 values) |
| **free_agents** | Float | No | - | 0.0 to 60.0 | 4.144981412639405 | 20 | Free Agents | Numeric; Required | Not Null | Variable |
| **free_bot_sessions** | Float | No | - | 0.0 to 150,000.0 | 2,473.977695167286 | 14 | Free Bot Sessions | Numeric; Required | Not Null | Variable |
| **ig** | Integer | No | Category | 0.0 to 1.0 | 0.12267657992565056 | 2 | Ig | Numeric; Required | Not Null | Enum-like (2 values) |
| **ndr** | Integer | No | Category | 0.0 to 1.0 | 0.9776951672862454 | 2 | Ndr | Numeric; Required | Not Null | Enum-like (2 values) |
| **nps** | Integer | No | Category | 0.0 to 1.0 | 0.9776951672862454 | 2 | Nps | Numeric; Required | Not Null | Enum-like (2 values) |
| **outbound_cost** | Float | No | Cost | 0.0 to 2.0 | 0.02758364312267658 | 11 | Outbound Cost | Numeric; Required | Not Null | Variable |
| **per_agent_fee** | Float | No | - | 0.0 to 3,000.0 | 1,104.2081784386617 | 28 | Per Agent Fee | Numeric; Required | Not Null | Variable |
| **pipeline** | Text | No | Category | 0.0 chars | - | 1 | Pipeline | Required | Not Null | Categorical (1 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **type_of_bot** | Text | No | Category | 6.79182156133829 chars | - | 6 | Type or category classification | Required | Not Null | Categorical (6 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 1 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>149. postgres_lk_bifrostbridge_leadsqauredconvomapping</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres lk bifrostbridge leadsqauredconvomapping operations.

**Owner/Maintainer:** Conversations Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 777

### account_id` → `postgres_accounts.id` (inferred)
- `convo_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,882

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_bifrostbridge_leadsqauredconvomapping`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 777 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 20,465.0 to 20,465.0 | 20,465.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **convo_id** | Float | No | - | 35,552.0 to 225,534.0 | 111,482.1682 | 8,637 | Reference to convo | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,882 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **integration_id** | Float | No | - | 21.0 to 21.0 | 21.0 | 1 | Reference to integration | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **lead_id** | Text | No | - | 36.0 chars | - | 8,256 | Reference to lead | Required | Not Null, Foreign Key (likely) | Variable |
| **opportunity_id** | Text | No | - | 36.0 chars | - | 9,981 | Reference to opportunity | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,883 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>150. postgres_lk_bifrostbridge_leadsquaredusers</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores user information and access permissions.

**Owner/Maintainer:** Customer Data Team

**Tags:** `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 11

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_bifrostbridge_leadsquaredusers`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 20,465.0 to 20,465.0 | 20,465.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 11 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 198 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **integration_id** | Float | No | - | 21.0 to 21.0 | 21.0 | 1 | Reference to integration | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 16 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_email** | Text | No | Email | 33.7020202020202 chars | - | 198 | Email address | Valid email format; Required | Not Null | Variable |
| **user_id** | Text | No | - | 36.0 chars | - | 196 | Reference to user | Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>151. postgres_lk_influenced_sales</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres lk influenced sales operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_influenced_sales`
- **Total Columns:** 21

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 6 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 39.0 to 27,269.0 | 10,571.4201 | 130 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **amount** | Float | No | - | 0.0 to 865,000.0 | 1,426.0220320000008 | 2,760 | Amount | Numeric; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,895 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 3.0 chars | - | 6 | Currency | Required | Not Null | Categorical (6 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **identifier** | Text | No | - | 0.423 chars | - | 218 | Reference to entifier | Required | Not Null, Foreign Key (likely) | Variable |
| **interaction_type** | Text | No | Category | 0.0 chars | - | 1 | Type or category classification | Required | Not Null | Categorical (1 categories) |
| **last_interaction** | DateTime | Yes | - | - | - | 9,859 | Last Interaction | Valid ISO 8601 datetime | None | Variable |
| **name** | Text | No | Name | 0.8548 chars | - | 215 | Human-readable name or title | Required | Not Null | Variable |
| **order_id** | Text | No | - | 13.0 chars | - | 9,999 | Reference to order | Required | Not Null, Foreign Key (likely) | Variable |
| **phone_number** | Text | No | - | 11.9966 chars | - | 9,805 | Phone Number | Required | Not Null | Variable |
| **source** | Text | No | Source | 4.8984 chars | - | 2 | Source | Required | Not Null | Categorical (2 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,869 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **utm_campaign** | Text | No | SerializedJSON | 2.0077 chars | - | 5 | Utm Campaign | Required | Not Null | Categorical (5 categories) |
| **utm_content** | Text | No | SerializedJSON | 2.0013 chars | - | 2 | Utm Content | Required | Not Null | Categorical (2 categories) |
| **utm_medium** | Text | No | SerializedJSON | 2.0054 chars | - | 6 | Utm Medium | Required | Not Null | Categorical (6 categories) |
| **utm_source** | Text | No | SerializedJSON | 2.0058 chars | - | 5 | Utm Source | Required | Not Null | Categorical (5 categories) |
| **utm_term** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Utm Term | Required | Not Null | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>152. postgres_lk_influenced_sales_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_lk_influenced_sales. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 438

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_influenced_sales_raw`
- **Total Columns:** 21

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 438 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 51.0 to 28,101.0 | 13,808.2165 | 82 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **amount** | Float | No | - | 0.0 to 991,000.0 | 3,463.7873379999833 | 3,799 | Amount | Numeric; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 8,580 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 3.0 chars | - | 6 | Currency | Required | Not Null | Categorical (6 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,997 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **identifier** | Text | No | - | 7.155 chars | - | 281 | Reference to entifier | Required | Not Null, Foreign Key (likely) | Variable |
| **interaction_type** | Text | No | Category | 1.7006 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **last_interaction** | DateTime | Yes | - | - (Null: 0.2%) | - | 5,860 | Last Interaction | Valid ISO 8601 datetime | None | Variable |
| **name** | Text | No | Name | 8.2038 chars | - | 139 | Human-readable name or title | Required | Not Null | Variable |
| **order_id** | Text | No | - | 12.6293 chars | - | 10,001 | Reference to order | Required | Not Null, Foreign Key (likely) | Variable |
| **phone_number** | Text | No | - | 11.1976 chars | - | 5,641 | Phone Number | Required | Not Null | Variable |
| **source** | Text | No | Source | 7.7391 chars | - | 7 | Source | Required | Not Null | Categorical (7 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 8,577 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **utm_campaign** | Text | No | SerializedJSON | 2.3857 chars | - | 38 | Utm Campaign | Required | Not Null | Variable |
| **utm_content** | Text | No | SerializedJSON | 2.1168 chars | - | 9 | Utm Content | Required | Not Null | Categorical (9 categories) |
| **utm_medium** | Text | No | SerializedJSON | 2.0563 chars | - | 17 | Utm Medium | Required | Not Null | Variable |
| **utm_source** | Text | No | SerializedJSON | 2.1029 chars | - | 20 | Utm Source | Required | Not Null | Variable |
| **utm_term** | Text | No | SerializedJSON | 2.0447 chars | - | 8 | Utm Term | Required | Not Null | Categorical (8 categories) |

</details>

---

<details>
<summary><h2>153. postgres_lk_shopify_app_event</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `agent_id` → Related table (inferred)
- `conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_shopify_app_event`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 249.0 to 27,116.0 | 18,405.0 | 4 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (4 values) |
| **agent_id** | Float | Yes | - | 1.0 to 50,274.0 (Null: 28.6%) | 38,102.6 | 4 | Reference to agent | Numeric | Foreign Key (likely) | Enum-like (4 values) |
| **conversation_id** | Float | Yes | - | 2,261.0 to 66,278.0 (Null: 28.6%) | 16,070.6 | 4 | Reference to conversation | Numeric | Foreign Key (likely) | Enum-like (4 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 7 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 7 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Categorical (7 categories) |
| **name** | Text | No | Name | 12.0 chars | - | 1 | Human-readable name or title | Required | Not Null | Categorical (1 categories) |
| **order_id** | Float | No | - | 8,940,734.0 to 12,895,987.0 | 10,944,091.142857144 | 5 | Reference to order | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (5 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 7 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>154. postgres_lk_shopify_app_event_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_lk_shopify_app_event. Contains unprocessed data before transformation.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `raw-data`, `staging`, `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1

### account_id` → `postgres_accounts.id` (inferred)
- `agent_id` → Related table (inferred)
- `conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 13

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_shopify_app_event_raw`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 249.0 to 27,116.0 | 12,791.307692307691 | 5 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (5 values) |
| **agent_id** | Float | Yes | - | 1.0 to 51,882.0 (Null: 30.8%) | 39,712.666666666664 | 7 | Reference to agent | Numeric | Foreign Key (likely) | Variable |
| **conversation_id** | Float | Yes | - | 2,261.0 to 1,380,088.0 (Null: 30.8%) | 620,664.8888888889 | 8 | Reference to conversation | Numeric | Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 13 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 13 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 12.0 chars | - | 1 | Human-readable name or title | Required | Not Null | Categorical (1 categories) |
| **order_id** | Float | No | - | 8,940,734.0 to 21,306,349.0 | 15,474,764.538461538 | 11 | Reference to order | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 13 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>155. postgres_lk_shopify_app_orderrefund</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 138

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,344

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 2

### eventn_ctx_event_id` → Related table (inferred)
- `last_updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 1,344

### note

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 33.25352112676056 chars
- **Distinct Values:** 2

### order_id` → Related table (inferred)
- `processed_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 264
- **Null %:** 80.5%

### shipping_amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### shipping_full_refund

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### shopify_refund_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_shopify_app_orderrefund`
- **Total Columns:** 15

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 138 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 1,344 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 3.0 chars | - | 2 | Currency | Required | Not Null | Categorical (2 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 1,349 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **is_created_on_shopify** | Integer | No | Category | 0.0 to 1.0 | 0.9970348406226834 | 2 | Is Created On Shopify | Numeric; Required | Not Null | Enum-like (2 values) |
| **last_updated_at** | DateTime | No | UpdatedTimestamp | - | - | 1,344 | Last Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **note** | Text | No | Category | 33.25352112676056 chars | - | 2 | Note | Required | Not Null | Categorical (2 categories) |
| **order_id** | Float | Yes | - | 1,214,523.0 to 19,522,599.0 (Null: 1.7%) | 5,976,871.01055807 | 1,321 | Reference to order | Numeric | Foreign Key (likely) | Variable |
| **processed_at** | DateTime | Yes | - | - (Null: 80.5%) | - | 264 | Processed At | Valid ISO 8601 datetime | None | Variable |
| **shipping_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Shipping Amount | Numeric; Required | Not Null | Enum-like (1 values) |
| **shipping_full_refund** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Shipping Full Refund | Numeric; Required | Not Null | Enum-like (1 values) |
| **shopify_refund_id** | Text | No | - | 2.3395107487027427 chars | - | 264 | Reference to shopify refund | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **user_refund_amount** | Float | No | - | 50.0 to 30,814.0 | 584.4046627131207 | 125 | User Refund Amount | Numeric; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>156. postgres_lk_shopify_app_shopifyorder</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,291

### account_id` → `postgres_accounts.id` (inferred)
- `agent_id` → Related table (inferred)
- `applied_discount

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** No
- **Range:** 0.0 to 61,626.42
- **Average:** 209.629479
- **Distinct Values:** 1,930

### cancel_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0001
- **Distinct Values:** 2

### cart_id` → Related table (inferred)
- `conversation_id` → Related table (inferred)
- `is_cod

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.3166
- **Distinct Values:** 2

### is_shopify_order

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.7637 chars
- **Distinct Values:** 5,510

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 8.1311 chars
- **Distinct Values:** 9,994

### notified_feedback

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_cancellation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_confirmation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_shipped

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_upsell

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_usage

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_reorder

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### order_id` → Related table (inferred)
- `shipping_charges

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 8,000.0
- **Average:** 23.644699
- **Distinct Values:** 161

### shopify_billing_address_id` → Related table (inferred)
- `shopify_customer_id` → Related table (inferred)
- `shopify_financial_status_id` → Related table (inferred)
- `shopify_fulfillment_status_id` → Related table (inferred)
- `shopify_order_status_id` → Related table (inferred)
- `shopify_order_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 63.4768 chars
- **Distinct Values:** 9,999

### shopify_shipping_address_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_shopify_app_shopifyorder`
- **Total Columns:** 51

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1,291 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,314.0 | 11,051.385000000002 | 192 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **agent_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to agent | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **amount** | Float | No | - | 0.0 to 218,250.0 | 1,360.6435190000007 | 3,855 | Amount | Numeric; Required | Not Null | Variable |
| **applied_discount** | Float | No | Discount | 0.0 to 61,626.42 | 209.629479 | 1,930 | Count of applied_dis | Numeric; Required | Not Null | Variable |
| **cancel_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Cancel Tags | Required | Not Null | Categorical (1 categories) |
| **cancelled** | Integer | No | Category | 0.0 to 1.0 | 0.0001 | 2 | Cancelled | Numeric; Required | Not Null | Enum-like (2 values) |
| **cart_id** | Float | No | - | 89,297.0 to 88,804,557.0 | 39,222,920.8871 | 10,001 | Reference to cart | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conversation_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to conversation | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **create_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Create Tags | Required | Not Null | Categorical (1 categories) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 10,001 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **customer_id** | Text | No | - | 12.9952 chars | - | 9,990 | Reference to customer | Required | Not Null, Foreign Key (likely) | Variable |
| **edit_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Edit Tags | Required | Not Null | Categorical (1 categories) |
| **email** | Text | No | - | 20.661 chars | - | 8,899 | Email address | Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_name** | Text | No | Name | 6.1957 chars | - | 5,661 | Human-readable name or title | Required | Not Null | Variable |
| **fixed_price** | Float | No | - | 0.0 to 218,250.0 | 1,318.9819960000002 | 3,740 | Fixed Price | Numeric; Required | Not Null | Variable |
| **is_cod** | Integer | No | Category | 0.0 to 1.0 | 0.3166 | 2 | Is Cod | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_shopify_order** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Is Shopify Order | Numeric; Required | Not Null | Enum-like (1 values) |
| **last_name** | Text | No | Name | 5.7637 chars | - | 5,510 | Human-readable name or title | Required | Not Null | Variable |
| **name** | Text | No | Name | 8.1311 chars | - | 9,994 | Human-readable name or title | Required | Not Null | Variable |
| **notified_feedback** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Feedback | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_order_cancellation** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Order Cancellation | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_order_confirmation** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Order Confirmation | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_order_shipped** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Order Shipped | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_product_upsell** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Product Upsell | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_product_usage** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Product Usage | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_reorder** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Reorder | Numeric; Required | Not Null | Enum-like (1 values) |
| **order_id** | Text | No | - | 12.9971 chars | - | 10,000 | Reference to order | Required | Not Null, Foreign Key (likely) | Variable |
| **order_notes** | Text | No | - | 13.6181 chars | - | 683 | Order Notes | Required | Not Null | Variable |
| **order_status_url** | Text | No | URL | 126.237 chars | - | 10,001 | Status or state of record | Valid URL format; Required | Not Null | Variable |
| **phone_number** | Text | No | - | 4.0914 chars | - | 3,420 | Phone Number | Required | Not Null | Variable |
| **refund_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Refund Tags | Required | Not Null | Categorical (1 categories) |
| **refunded_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Refunded Amount | Numeric; Required | Not Null | Enum-like (1 values) |
| **shipping_charges** | Float | No | - | 0.0 to 8,000.0 | 23.644699 | 161 | Shipping Charges | Numeric; Required | Not Null | Variable |
| **shopify_billing_address_id** | Float | Yes | - | 37,614.0 to 22,608,912.0 (Null: 35.3%) | 12,813,616.233312732 | 6,459 | Reference to shopify billing address | Numeric | Foreign Key (likely) | Variable |
| **shopify_customer_id** | Float | No | - | 27,499.0 to 34,679,774.0 | 14,565,611.7394 | 9,990 | Reference to shopify customer | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **shopify_financial_status_id** | Float | No | - | 5.0 to 11.0 | 7.1879 | 7 | Status or state of record | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **shopify_fulfillment_status_id** | Float | No | - | 12.0 to 15.0 | 12.1618 | 4 | Status or state of record | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (4 values) |
| **shopify_order_status_id** | Float | No | - | 1.0 to 3.0 | 1.6351 | 3 | Status or state of record | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (3 values) |
| **shopify_order_url** | Text | No | URL | 63.4768 chars | - | 9,999 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **shopify_shipping_address_id** | Float | Yes | - | 37,614.0 to 22,608,912.0 (Null: 35.0%) | 12,611,120.24722906 | 6,495 | Reference to shopify shipping address | Numeric | Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **subtotal_price** | Float | No | - | 0.0 to 218,250.0 | 1,336.2823520000002 | 3,355 | Subtotal Price | Numeric; Required | Not Null | Variable |
| **tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Tags | Required | Not Null | Categorical (1 categories) |
| **total_price** | Float | No | - | 0.0 to 218,250.0 | 1,285.4034080000008 | 3,737 | Total Price | Numeric; Required | Not Null | Variable |
| **total_tax** | Float | No | - | 0.0 to 22,419.64 | 80.27825100000003 | 2,546 | Total Tax | Numeric; Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,987 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_owe_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | User Owe Amount | Numeric; Required | Not Null | Enum-like (1 values) |
| **user_refund_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | User Refund Amount | Numeric; Required | Not Null | Enum-like (1 values) |

</details>

---

<details>
<summary><h2>157. postgres_lk_shopify_app_shopifyorder_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_lk_shopify_app_shopifyorder. Contains unprocessed data before transformation.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `raw-data`, `staging`, `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 13

### account_id` → `postgres_accounts.id` (inferred)
- `agent_id` → Related table (inferred)
- `applied_discount

- **Type:** `Float`
- **Semantic Type:** `Discount`
- **Nullable:** No
- **Range:** 0.0 to 2,455.0
- **Average:** 5.905039
- **Distinct Values:** 86

### cancel_tags

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 2.0 chars
- **Distinct Values:** 1

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### cart_id` → Related table (inferred)
- `conversation_id` → Related table (inferred)
- `is_cod

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0083
- **Distinct Values:** 2

### is_shopify_order

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 1.0 to 1.0
- **Average:** 1.0
- **Distinct Values:** 1

### last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.767 chars
- **Distinct Values:** 4,521

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 6.0795 chars
- **Distinct Values:** 10,001

### notified_feedback

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_cancellation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_confirmation

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_order_shipped

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_upsell

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_product_usage

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### notified_reorder

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### order_id` → Related table (inferred)
- `shipping_charges

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 50.0
- **Average:** 0.27
- **Distinct Values:** 4

### shopify_billing_address_id` → Related table (inferred)
- `shopify_customer_id` → Related table (inferred)
- `shopify_financial_status_id` → Related table (inferred)
- `shopify_fulfillment_status_id` → Related table (inferred)
- `shopify_order_status_id` → Related table (inferred)
- `shopify_order_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 64.8321 chars
- **Distinct Values:** 9,999

### shopify_shipping_address_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_shopify_app_shopifyorder_raw`
- **Total Columns:** 51

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 13 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 41.0 | 40.143 | 3 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (3 values) |
| **agent_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to agent | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **amount** | Float | No | - | 0.0 to 23,324.0 | 774.1839309999999 | 665 | Amount | Numeric; Required | Not Null | Variable |
| **applied_discount** | Float | No | Discount | 0.0 to 2,455.0 | 5.905039 | 86 | Count of applied_dis | Numeric; Required | Not Null | Variable |
| **cancel_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Cancel Tags | Required | Not Null | Categorical (1 categories) |
| **cancelled** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Cancelled | Numeric; Required | Not Null | Enum-like (1 values) |
| **cart_id** | Float | No | - | 93,002.0 to 2,366,411.0 | 273,336.46059999993 | 9,999 | Reference to cart | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **conversation_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to conversation | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **create_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Create Tags | Required | Not Null | Categorical (1 categories) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 3,373 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **customer_id** | Text | No | - | 12.9998 chars | - | 8,712 | Reference to customer | Required | Not Null, Foreign Key (likely) | Variable |
| **edit_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Edit Tags | Required | Not Null | Categorical (1 categories) |
| **email** | Text | No | Email | 23.1392 chars | - | 8,692 | Email address | Valid email format; Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_name** | Text | No | Name | 6.1665 chars | - | 4,389 | Human-readable name or title | Required | Not Null | Variable |
| **fixed_price** | Float | No | - | 0.0 to 8,847.0 | 2.43129 | 12 | Fixed Price | Numeric; Required | Not Null | Variable |
| **is_cod** | Integer | No | Category | 0.0 to 1.0 | 0.0083 | 2 | Is Cod | Numeric; Required | Not Null | Enum-like (2 values) |
| **is_shopify_order** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Is Shopify Order | Numeric; Required | Not Null | Enum-like (1 values) |
| **last_name** | Text | No | Name | 5.767 chars | - | 4,521 | Human-readable name or title | Required | Not Null | Variable |
| **name** | Text | No | Name | 6.0795 chars | - | 10,001 | Human-readable name or title | Required | Not Null | Variable |
| **notified_feedback** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Feedback | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_order_cancellation** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Order Cancellation | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_order_confirmation** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Order Confirmation | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_order_shipped** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Order Shipped | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_product_upsell** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Product Upsell | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_product_usage** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Product Usage | Numeric; Required | Not Null | Enum-like (1 values) |
| **notified_reorder** | Integer | No | Category | 0.0 to 0.0 | 0.0 | 1 | Notified Reorder | Numeric; Required | Not Null | Enum-like (1 values) |
| **order_id** | Text | No | - | 13.0 chars | - | 10,001 | Reference to order | Required | Not Null, Foreign Key (likely) | Variable |
| **order_notes** | Text | No | - | 0.0451 chars | - | 33 | Order Notes | Required | Not Null | Variable |
| **order_status_url** | Text | No | URL | 128.7491 chars | - | 10,001 | Status or state of record | Valid URL format; Required | Not Null | Variable |
| **phone_number** | Text | No | - | 11.4648 chars | - | 8,334 | Phone Number | Required | Not Null | Variable |
| **refund_tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Refund Tags | Required | Not Null | Categorical (1 categories) |
| **refunded_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Refunded Amount | Numeric; Required | Not Null | Enum-like (1 values) |
| **shipping_charges** | Float | No | - | 0.0 to 50.0 | 0.27 | 4 | Shipping Charges | Numeric; Required | Not Null | Enum-like (4 values) |
| **shopify_billing_address_id** | Float | Yes | - | 33,174.0 to 1,181,302.0 (Null: 98.0%) | 765,133.4975124379 | 186 | Reference to shopify billing address | Numeric | Foreign Key (likely) | Variable |
| **shopify_customer_id** | Float | No | - | 27,261.0 to 1,463,024.0 | 89,921.7998 | 8,713 | Reference to shopify customer | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **shopify_financial_status_id** | Float | No | - | 5.0 to 11.0 | 7.980099999999998 | 4 | Status or state of record | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (4 values) |
| **shopify_fulfillment_status_id** | Float | No | - | 12.0 to 15.0 | 12.0021 | 3 | Status or state of record | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (3 values) |
| **shopify_order_status_id** | Float | No | - | 1.0 to 3.0 | 2.9575 | 3 | Status or state of record | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (3 values) |
| **shopify_order_url** | Text | No | URL | 64.8321 chars | - | 9,999 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **shopify_shipping_address_id** | Float | Yes | - | 33,174.0 to 1,181,302.0 (Null: 98.9%) | 742,236.4867256638 | 104 | Reference to shopify shipping address | Numeric | Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **subtotal_price** | Float | No | - | 0.0 to 23,324.0 | 773.9139309999998 | 664 | Subtotal Price | Numeric; Required | Not Null | Variable |
| **tags** | Text | No | SerializedJSON | 2.0 chars | - | 1 | Tags | Required | Not Null | Categorical (1 categories) |
| **total_price** | Float | No | - | 0.0 to 23,324.0 | 773.7136079999999 | 661 | Total Price | Numeric; Required | Not Null | Variable |
| **total_tax** | Float | No | - | 0.0 to 1,349.54 | 0.8330079999999999 | 38 | Total Tax | Numeric; Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 1,106 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_owe_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | User Owe Amount | Numeric; Required | Not Null | Enum-like (1 values) |
| **user_refund_amount** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | User Refund Amount | Numeric; Required | Not Null | Enum-like (1 values) |

</details>

---

<details>
<summary><h2>158. postgres_lk_store_customermodel</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres lk store customermodel operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 628

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_customermodel`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 628 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 272.0 | 65.0524 | 4 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (4 values) |
| **address** | Text | No | - | 344.218 chars | - | 8,779 | Address | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,268 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **customer_id** | Text | No | - | 36.0 chars | - | 9,996 | Reference to customer | Required | Not Null, Foreign Key (likely) | Variable |
| **email** | Text | No | Email | 22.2257 chars | - | 9,743 | Email address | Valid email format; Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_name** | Text | No | Name | 6.1337 chars | - | 5,310 | Human-readable name or title | Required | Not Null | Variable |
| **last_name** | Text | No | Name | 5.4367 chars | - | 4,503 | Human-readable name or title | Required | Not Null | Variable |
| **phone_number** | Text | No | - | 1.7975 chars | - | 1,496 | Phone Number | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **tags** | Text | No | Category | 0.0 chars | - | 1 | Tags | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 8,168 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>159. postgres_lk_store_igmedia</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres lk store igmedia operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 36

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_igmedia`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **_timestamp** | DateTime | No | - | - | - | 36 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 54.0 to 27,489.0 | 14,109.5298 | 29 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **caption** | Text | No | - | 392.5199 chars | - | 9,192 | Caption | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,956 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,998 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **ig_user_id** | Text | No | - | 17.0 chars | - | 37 | Reference to ig user | Required | Not Null, Foreign Key (likely) | Variable |
| **media_id** | Text | No | - | 17.0 chars | - | 10,000 | Reference to media | Required | Not Null, Foreign Key (likely) | Variable |
| **media_product_type** | Text | No | Category | 4.4321 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **media_type** | Text | No | Category | 7.4147 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **media_url** | Text | No | URL | 127.1902 chars | - | 9,881 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **post_link** | Text | No | URL | 41.3095 chars | - | 10,001 | Post Link | Valid URL format; Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **thumbnail_url** | Text | No | URL | 136.5052 chars | - | 4,615 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **variant_ids** | Text | No | SerializedJSON | 25.994 chars | - | 1,986 | Reference to variant s | Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>160. postgres_lk_store_ordermodel</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,315

### account_id` → `postgres_accounts.id` (inferred)
- `amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 98,671.0
- **Average:** 1,290.0230010000005
- **Distinct Values:** 3,686

### attribution_id` → Related table (inferred)
- `cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0536
- **Distinct Values:** 2

### checkout_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 16.884 chars
- **Distinct Values:** 5,277

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,994

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.7045 chars
- **Distinct Values:** 8

### customer_id` → Related table (inferred)
- `shopify_store_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_ordermodel`
- **Total Columns:** 35

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 3,315 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,220.0 | 5,775.7167 | 284 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **amount** | Float | No | - | 0.0 to 98,671.0 | 1,290.0230010000005 | 3,686 | Amount | Numeric; Required | Not Null | Variable |
| **attribution_id** | Float | Yes | - | 59,568.0 to 63,992.0 (Null: 100.0%) | 61,780.0 | 3 | Reference to attribution | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **cancelled** | Integer | No | Category | 0.0 to 1.0 | 0.0536 | 2 | Cancelled | Numeric; Required | Not Null | Enum-like (2 values) |
| **checkout_token** | Text | No | - | 16.884 chars | - | 5,277 | Authentication or access token | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,994 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 2.7045 chars | - | 8 | Currency | Required | Not Null | Categorical (8 categories) |
| **customer_id** | Text | No | - | 12.9943 chars | - | 9,854 | Reference to customer | Required | Not Null, Foreign Key (likely) | Variable |
| **delivery_date** | Text | No | Category | 0.0 chars | - | 1 | Delivery Date | Required | Not Null | Categorical (1 categories) |
| **discount_codes** | Text | No | - | 27.1293 chars | - | 2,443 | Count of dis_codes | Required | Not Null | Variable |
| **email** | Text | No | - | 21.1784 chars | - | 9,069 | Email address | Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_name** | Text | No | Name | 6.4216 chars | - | 5,834 | Human-readable name or title | Required | Not Null | Variable |
| **fulfillment_status** | Text | No | Category | 8.3862 chars | - | 7 | Status or state of record | Required | Not Null | Categorical (7 categories) |
| **item_names** | Text | No | - | 89.627 chars | - | 7,048 | Item Names | Required | Not Null | Variable |
| **items** | Text | No | SerializedJSON | 1,198.7084 chars | - | 9,921 | Items | Required | Not Null | Variable |
| **landing_site_ref** | Text | No | Category | 0.025 chars | - | 12 | Landing Site Ref | Required | Not Null | Variable |
| **last_name** | Text | No | Name | 5.6795 chars | - | 5,135 | Human-readable name or title | Required | Not Null | Variable |
| **name** | Text | No | Name | 8.8993 chars | - | 9,993 | Human-readable name or title | Required | Not Null | Variable |
| **order_id** | Text | No | - | 12.9872 chars | - | 10,000 | Reference to order | Required | Not Null, Foreign Key (likely) | Variable |
| **order_notes** | Text | No | - | 13.5664 chars | - | 613 | Order Notes | Required | Not Null | Variable |
| **order_status_url** | Text | No | URL | 14.764 chars | - | 1,180 | Status or state of record | Valid URL format; Required | Not Null | Variable |
| **payment_method** | Text | No | Category | 0.0174 chars | - | 7 | Payment Method | Required | Not Null | Categorical (7 categories) |
| **payment_status** | Text | No | Category | 5.3105 chars | - | 13 | Status or state of record | Required | Not Null | Variable |
| **phone_number** | Text | No | - | 11.726 chars | - | 9,862 | Phone Number | Required | Not Null | Variable |
| **presentment_currency** | Text | No | Category | 2.694 chars | - | 19 | Presentment Currency | Required | Not Null | Variable |
| **shipping_price** | Float | No | - | 0.0 to 2,600.0 | 19.927707 | 116 | Shipping Price | Numeric; Required | Not Null | Variable |
| **shopify_store_id** | Float | Yes | - | 4.0 to 12,913.0 (Null: 13.1%) | 3,140.2258769407704 | 265 | Reference to shopify store | Numeric | Foreign Key (likely) | Variable |
| **sold_by_limechat** | Integer | Yes | Category | 0.0 to 1.0 | 0.0013 | 2 | Sold By Limechat | Numeric | None | Enum-like (2 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **subtotal_price** | Float | Yes | - | 0.0 to 98,671.0 (Null: 0.4%) | 1,270.0422805784299 | 3,293 | Subtotal Price | Numeric | None | Variable |
| **tags** | Text | No | SerializedJSON | 33.3393 chars | - | 3,653 | Tags | Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,018 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>161. postgres_lk_store_productcollectionmodel</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 89

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_productcollectionmodel`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 89 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 12,512.0 | 620.2106 | 25 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **collection_id** | Text | No | - | 36.9533 chars | - | 1,445 | Reference to collection | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 94 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 1,445 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 17.6531 chars | - | 1,348 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **store_type** | Text | No | Category | 7.0 chars | - | 1 | Type or category classification | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 1,939 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>162. postgres_lk_store_productcollectionmodel_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_lk_store_productcollectionmodel. Contains unprocessed data before transformation.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 6

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_productcollectionmodel_raw`
- **Total Columns:** 10

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 6 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 12,512.0 | 918.7357000000002 | 99 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **collection_id** | Text | No | - | 36.8821 chars | - | 9,753 | Reference to collection | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 793 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 16.0193 chars | - | 8,516 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **store_type** | Text | No | Category | 6.9958 chars | - | 2 | Type or category classification | Required | Not Null | Categorical (2 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 2,572 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>163. postgres_lk_store_productmodel</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 25

### account_id` → `postgres_accounts.id` (inferred)
- `attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 193.3399 chars
- **Distinct Values:** 4,598

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,063

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### custom_attributes

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 33.5814 chars
- **Distinct Values:** 2,258

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### eventn_ctx_event_id` → Related table (inferred)
- `inventory_management

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Avg Length:** 7.0008 chars
- **Distinct Values:** 2

### inventory_policy

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 4.0244 chars
- **Distinct Values:** 2

### metafields

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 32.383 chars
- **Distinct Values:** 5,047

### name_synonyms

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### options

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 25.8537 chars
- **Distinct Values:** 447

### popularity

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 475,525.0
- **Average:** 154,609.2268
- **Distinct Values:** 9,861

### price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 100,320.0
- **Average:** 3,110.368362
- **Distinct Values:** 913

### product_created_on_store_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 6,765
- **Null %:** 0.4%

### product_id` → Related table (inferred)
- `reorder_time_intervals

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### sale_price

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 100,320.0
- **Average:** 2,500.416150000001
- **Distinct Values:** 1,400

### shopify_store_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_productmodel`
- **Total Columns:** 36

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 25 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 26,075.0 to 27,314.0 | 26,772.1457 | 3 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (3 values) |
| **attributes** | Text | No | SerializedJSON | 193.3399 chars | - | 4,598 | Attributes | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 2,063 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 0.0 chars | - | 1 | Currency | Required | Not Null | Categorical (1 categories) |
| **custom_attributes** | Text | No | SerializedJSON | 33.5814 chars | - | 2,258 | Custom Attributes | Required | Not Null | Variable |
| **description** | Text | No | Description | 0.0 chars | - | 1 | Description | Required | Not Null | Categorical (1 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **faqs** | Text | No | Category | 0.0 chars | - | 1 | Faqs | Required | Not Null | Categorical (1 categories) |
| **fetched_description** | Text | No | Description | 262.0439 chars | - | 5,451 | Fetched Description | Required | Not Null | Variable |
| **image** | Text | No | URL | 106.0924 chars | - | 6,582 | Image | Valid URL format; Required | Not Null | Variable |
| **inventory** | Float | Yes | - | -52.0 to 7,989.0 | 6.848500000000001 | 152 | Inventory | Numeric | None | Variable |
| **inventory_management** | Text | Yes | Category | 7.0008 chars | - | 2 | Inventory Management | Standard | None | Categorical (2 categories) |
| **inventory_policy** | Text | No | Category | 4.0244 chars | - | 2 | Inventory Policy | Required | Not Null | Categorical (2 categories) |
| **metafields** | Text | No | Category | 0.0 chars | - | 1 | Metafields | Required | Not Null | Categorical (1 categories) |
| **name** | Text | No | Name | 32.383 chars | - | 5,047 | Human-readable name or title | Required | Not Null | Variable |
| **name_synonyms** | Text | No | Category | 0.0 chars | - | 1 | Name Synonyms | Required | Not Null | Categorical (1 categories) |
| **options** | Text | No | SerializedJSON | 25.8537 chars | - | 447 | Options | Required | Not Null | Variable |
| **popularity** | Float | Yes | - | 0.0 to 475,525.0 | 154,609.2268 | 9,861 | Popularity | Numeric | None | Variable |
| **price** | Float | Yes | - | 0.0 to 100,320.0 | 3,110.368362 | 913 | Price | Numeric | None | Variable |
| **product_created_on_store_at** | DateTime | Yes | CreationTimestamp | - (Null: 0.4%) | - | 6,765 | Product Created On Store At | Valid ISO 8601 datetime | None | Variable |
| **product_id** | Text | No | - | 34.998 chars | - | 6,503 | Reference to product | Required | Not Null, Foreign Key (likely) | Variable |
| **product_link** | Text | No | URL | 64.7706 chars | - | 6,492 | Product Link | Valid URL format; Required | Not Null | Variable |
| **product_updated_on_store_at** | DateTime | Yes | UpdatedTimestamp | - (Null: 0.4%) | - | 7,981 | Product Updated On Store At | Valid ISO 8601 datetime | None | Variable |
| **purchasable** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Purchasable | Numeric; Required | Not Null | Enum-like (1 values) |
| **reorder_time_intervals** | Text | No | Category | 0.0 chars | - | 1 | Reorder Time Intervals | Required | Not Null | Categorical (1 categories) |
| **sale_price** | Float | Yes | - | 0.0 to 100,320.0 | 2,500.416150000001 | 1,400 | Sale Price | Numeric | None | Variable |
| **shopify_store_id** | Float | Yes | - | 12,242.0 to 12,933.0 | 12,662.1896 | 3 | Reference to shopify store | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **sku** | Text | No | - | 12.8054 chars | - | 9,595 | Sku | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 7,764 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **upsell_time_intervals** | Text | No | Category | 0.0 chars | - | 1 | Upsell Time Intervals | Required | Not Null | Categorical (1 categories) |
| **usage_time_intervals** | Text | No | Category | 0.0 chars | - | 1 | Usage Time Intervals | Required | Not Null | Categorical (1 categories) |
| **variant_id** | Text | No | - | 42.9986 chars | - | 10,000 | Reference to variant | Required | Not Null, Foreign Key (likely) | Variable |
| **vendor** | Text | No | Company | 8.8974 chars | - | 291 | Vendor | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>164. postgres_lk_store_store</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgres lk store store operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 52

### account_id` → `postgres_accounts.id` (inferred)
- `ayuvya_id` → Related table (inferred)
- `bebodywise_id` → Related table (inferred)
- `bigcommerce_id` → Related table (inferred)
- `biocule_id` → Related table (inferred)
- `damensch_id` → Related table (inferred)
- `domain

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 15.32441113490364 chars
- **Distinct Values:** 516

### dukaan_id` → Related table (inferred)
- `emotorad_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)
- `fb_catalog_gsheet

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.29764453961456105 chars
- **Distinct Values:** 4

### has_catalog_integration

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.03854389721627409
- **Distinct Values:** 2

### hkvitals_id` → Related table (inferred)
- `kindlife_id` → Related table (inferred)
- `littlejoy_id` → Related table (inferred)
- `manmatters_id` → Related table (inferred)
- `pilgrim_id` → Related table (inferred)
- `powerlook_id` → Related table (inferred)
- `s3_csv

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.4207708779443253 chars
- **Distinct Values:** 37

### shopg_id` → Related table (inferred)
- `shopify_id` → Related table (inferred)
- `src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### thedermaco_id` → Related table (inferred)
- `webhook_secret

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.033190578158458245 chars
- **Distinct Values:** 2

### wforwomen_id` → Related table (inferred)
- `woocommerce_id` → Related table (inferred)
- `wowskinscience_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_store`
- **Total Columns:** 30

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 52 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 28,775.0 | 18,439.755888650965 | 933 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **ayuvya_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to ayuvya | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **bebodywise_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to bebodywise | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **bigcommerce_id** | Float | Yes | - | 1.0 to 36.0 (Null: 99.5%) | 15.0 | 5 | Reference to bigcommerce | Numeric | Foreign Key (likely) | Enum-like (5 values) |
| **biocule_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to biocule | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **damensch_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to damensch | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **domain** | Text | No | - | 15.32441113490364 chars | - | 516 | Domain | Required | Not Null | Variable |
| **dukaan_id** | Float | Yes | - | 34.0 to 36.0 (Null: 99.8%) | 35.0 | 3 | Reference to dukaan | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **emotorad_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to emotorad | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 934 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **farzicom_id** | Float | Yes | - | 2.0 to 3.0 (Null: 99.6%) | 2.75 | 3 | Reference to farzicom | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **fb_catalog_gsheet** | Text | No | Category | 0.29764453961456105 chars | - | 4 | Fb Catalog Gsheet | Required | Not Null | Categorical (4 categories) |
| **has_catalog_integration** | Integer | No | Category | 0.0 to 1.0 | 0.03854389721627409 | 2 | Has Catalog Integration | Numeric; Required | Not Null | Enum-like (2 values) |
| **hkvitals_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to hkvitals | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **kindlife_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to kindlife | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **littlejoy_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to littlejoy | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **manmatters_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to manmatters | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **pilgrim_id** | Float | Yes | - | 2.0 to 2.0 (Null: 99.9%) | 2.0 | 2 | Reference to pilgrim | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **powerlook_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to powerlook | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **s3_csv** | Text | No | - | 3.4207708779443253 chars | - | 37 | S3 Csv | Required | Not Null | Variable |
| **shopg_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to shopg | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **shopify_id** | Float | Yes | - | 1.0 to 13,216.0 (Null: 5.5%) | 8,417.814269535675 | 856 | Reference to shopify | Numeric | Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **thedermaco_id** | Float | Yes | - | 1.0 to 2.0 (Null: 99.8%) | 1.5 | 3 | Reference to thedermaco | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **webhook_secret** | Text | No | Category | 0.033190578158458245 chars | - | 2 | Webhook Secret | Required | Not Null | Categorical (2 categories) |
| **wforwomen_id** | Float | Yes | - | 1.0 to 67.0 (Null: 99.7%) | 34.0 | 4 | Reference to wforwomen | Numeric | Foreign Key (likely) | Enum-like (4 values) |
| **woocommerce_id** | Float | Yes | - | 5.0 to 472.0 (Null: 98.7%) | 237.5 | 13 | Reference to woocommerce | Numeric | Foreign Key (likely) | Variable |
| **wowskinscience_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to wowskinscience | Numeric | Foreign Key (likely) | Enum-like (2 values) |

</details>

---

<details>
<summary><h2>165. postgres_lk_store_store_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_lk_store_store. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 52

### account_id` → `postgres_accounts.id` (inferred)
- `ayuvya_id` → Related table (inferred)
- `bebodywise_id` → Related table (inferred)
- `bigcommerce_id` → Related table (inferred)
- `biocule_id` → Related table (inferred)
- `damensch_id` → Related table (inferred)
- `domain

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 15.32441113490364 chars
- **Distinct Values:** 516

### dukaan_id` → Related table (inferred)
- `emotorad_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)
- `fb_catalog_gsheet

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.29764453961456105 chars
- **Distinct Values:** 4

### has_catalog_integration

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.03854389721627409
- **Distinct Values:** 2

### hkvitals_id` → Related table (inferred)
- `kindlife_id` → Related table (inferred)
- `littlejoy_id` → Related table (inferred)
- `manmatters_id` → Related table (inferred)
- `pilgrim_id` → Related table (inferred)
- `powerlook_id` → Related table (inferred)
- `s3_csv

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.4207708779443253 chars
- **Distinct Values:** 37

### shopg_id` → Related table (inferred)
- `shopify_id` → Related table (inferred)
- `src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### thedermaco_id` → Related table (inferred)
- `webhook_secret

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.033190578158458245 chars
- **Distinct Values:** 2

### wforwomen_id` → Related table (inferred)
- `woocommerce_id` → Related table (inferred)
- `wowskinscience_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_store_store_raw`
- **Total Columns:** 30

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 52 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 28,775.0 | 18,439.755888650965 | 933 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **ayuvya_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to ayuvya | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **bebodywise_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to bebodywise | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **bigcommerce_id** | Float | Yes | - | 1.0 to 36.0 (Null: 99.5%) | 15.0 | 5 | Reference to bigcommerce | Numeric | Foreign Key (likely) | Enum-like (5 values) |
| **biocule_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to biocule | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **damensch_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to damensch | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **domain** | Text | No | - | 15.32441113490364 chars | - | 516 | Domain | Required | Not Null | Variable |
| **dukaan_id** | Float | Yes | - | 34.0 to 36.0 (Null: 99.8%) | 35.0 | 3 | Reference to dukaan | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **emotorad_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to emotorad | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 934 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **farzicom_id** | Float | Yes | - | 2.0 to 3.0 (Null: 99.6%) | 2.75 | 3 | Reference to farzicom | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **fb_catalog_gsheet** | Text | No | Category | 0.29764453961456105 chars | - | 4 | Fb Catalog Gsheet | Required | Not Null | Categorical (4 categories) |
| **has_catalog_integration** | Integer | No | Category | 0.0 to 1.0 | 0.03854389721627409 | 2 | Has Catalog Integration | Numeric; Required | Not Null | Enum-like (2 values) |
| **hkvitals_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to hkvitals | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **kindlife_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to kindlife | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **littlejoy_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to littlejoy | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **manmatters_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to manmatters | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **pilgrim_id** | Float | Yes | - | 2.0 to 2.0 (Null: 99.9%) | 2.0 | 2 | Reference to pilgrim | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **powerlook_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to powerlook | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **s3_csv** | Text | No | - | 3.4207708779443253 chars | - | 37 | S3 Csv | Required | Not Null | Variable |
| **shopg_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to shopg | Numeric | Foreign Key (likely) | Enum-like (2 values) |
| **shopify_id** | Float | Yes | - | 1.0 to 13,216.0 (Null: 5.5%) | 8,417.814269535675 | 856 | Reference to shopify | Numeric | Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **thedermaco_id** | Float | Yes | - | 1.0 to 2.0 (Null: 99.8%) | 1.5 | 3 | Reference to thedermaco | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **webhook_secret** | Text | No | Category | 0.033190578158458245 chars | - | 2 | Webhook Secret | Required | Not Null | Categorical (2 categories) |
| **wforwomen_id** | Float | Yes | - | 1.0 to 67.0 (Null: 99.7%) | 34.0 | 4 | Reference to wforwomen | Numeric | Foreign Key (likely) | Enum-like (4 values) |
| **woocommerce_id** | Float | Yes | - | 5.0 to 472.0 (Null: 98.7%) | 237.5 | 13 | Reference to woocommerce | Numeric | Foreign Key (likely) | Variable |
| **wowskinscience_id** | Float | Yes | - | 1.0 to 1.0 (Null: 99.9%) | 1.0 | 2 | Reference to wowskinscience | Numeric | Foreign Key (likely) | Enum-like (2 values) |

</details>

---

<details>
<summary><h2>166. postgres_lk_test_lk_table_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_lk_test_lk_table. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_lk_test_lk_table_raw`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 7 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **age** | Float | No | - | 20.0 to 30.0 | 23.555555555555557 | 5 | Age | Numeric; Required | Not Null | Enum-like (5 values) |
| **another_col** | Text | No | Category | 0.3333333333333333 chars | - | 2 | Another Col | Required | Not Null | Categorical (2 categories) |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 9 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Categorical (9 categories) |
| **name** | Text | No | Name | 7.333333333333333 chars | - | 6 | Human-readable name or title | Required | Not Null | Categorical (6 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Text | No | Category | 1.2222222222222223 chars | - | 4 | Status or state of record | Required | Not Null | Categorical (4 categories) |

</details>

---

<details>
<summary><h2>167. postgres_messages_message_tags</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores message data and delivery information.

**Owner/Maintainer:** Conversations Team

**Tags:** `labels`, `messaging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_messages_message_tags`
- **Total Columns:** 8

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1,472 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 7,376 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **description** | Text | No | Description | 0.0028 chars | - | 2 | Description | Required | Not Null | Categorical (2 categories) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 36.2169 chars | - | 9,992 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 7,376 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>168. postgres_messages_taggables</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores message data and delivery information.

**Owner/Maintainer:** Conversations Team

**Tags:** `labels`, `messaging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 41

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 305

### eventn_ctx_event_id` → Related table (inferred)
- `taggable_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_messages_taggables`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 41 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 305 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **tag_id** | Float | No | - | 1.0 to 1.0 | 1.0 | 1 | Reference to tag | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **taggable_id** | Float | No | - | 715,185,857.0 to 717,121,899.0 | 716,868,665.7154 | 9,999 | Reference to taggable | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **taggable_type** | Text | No | Category | 7.0 chars | - | 1 | Type or category classification | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 305 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>169. postgres_sla_policies</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Service Level Agreement tracking and metrics.

**Owner/Maintainer:** Automation/Workflows Team

**Tags:** `sla`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 56

### account_id` → `postgres_accounts.id` (inferred)
- `active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.582089552238806
- **Distinct Values:** 2

### conditions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 38.47761194029851 chars
- **Distinct Values:** 63

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 67

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 7
- **Null %:** 91.0%

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 10.432835820895523 chars
- **Distinct Values:** 26

### escalations

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 198.61194029850745 chars
- **Distinct Values:** 44

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_sla_policies`
- **Total Columns:** 16

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 56 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 189.0 to 28,397.0 | 20,132.537313432837 | 39 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **active** | Integer | No | Category | 0.0 to 1.0 | 0.582089552238806 | 2 | Active | Numeric; Required | Not Null | Enum-like (2 values) |
| **conditions** | Text | No | SerializedJSON | 38.47761194029851 chars | - | 63 | Conditions | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 67 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 91.0%) | - | 7 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **description** | Text | No | Description | 10.432835820895523 chars | - | 26 | Description | Required | Not Null | Variable |
| **escalations** | Text | No | SerializedJSON | 198.61194029850745 chars | - | 44 | Escalations | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 67 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **metrics** | Text | No | SerializedJSON | 159.83582089552237 chars | - | 46 | Metrics | Required | Not Null | Variable |
| **name** | Text | No | Name | 12.014925373134329 chars | - | 55 | Human-readable name or title | Required | Not Null | Variable |
| **order** | Float | No | - | 1.0 to 7.0 | 1.8656716417910448 | 7 | Order | Numeric; Required | Not Null | Variable |
| **reminders** | Text | No | Category | 114.55223880597015 chars | - | 25 | Reminders | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 66 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>170. postgres_sla_policies_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_sla_policies. Contains unprocessed data before transformation.

**Owner/Maintainer:** Automation/Workflows Team

**Tags:** `raw-data`, `staging`, `sla`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 78

### account_id` → `postgres_accounts.id` (inferred)
- `active

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.6633663366336634
- **Distinct Values:** 2

### conditions

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 36.32673267326733 chars
- **Distinct Values:** 64

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 67

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 7
- **Null %:** 94.1%

### description

- **Type:** `Text`
- **Semantic Type:** `Description`
- **Nullable:** No
- **Avg Length:** 9.148514851485148 chars
- **Distinct Values:** 28

### escalations

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 238.44554455445544 chars
- **Distinct Values:** 51

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_sla_policies_raw`
- **Total Columns:** 16

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 78 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 189.0 to 28,397.0 | 20,251.09900990099 | 39 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **active** | Integer | No | Category | 0.0 to 1.0 | 0.6633663366336634 | 2 | Active | Numeric; Required | Not Null | Enum-like (2 values) |
| **conditions** | Text | No | SerializedJSON | 36.32673267326733 chars | - | 64 | Conditions | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 67 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 94.1%) | - | 7 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **description** | Text | No | Description | 9.148514851485148 chars | - | 28 | Description | Required | Not Null | Variable |
| **escalations** | Text | No | SerializedJSON | 238.44554455445544 chars | - | 51 | Escalations | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 67 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **metrics** | Text | No | SerializedJSON | 169.05940594059405 chars | - | 60 | Metrics | Required | Not Null | Variable |
| **name** | Text | No | Name | 12.237623762376238 chars | - | 55 | Human-readable name or title | Required | Not Null | Variable |
| **order** | Float | No | - | 1.0 to 7.0 | 1.9801980198019802 | 7 | Order | Numeric; Required | Not Null | Variable |
| **reminders** | Text | No | SerializedJSON | 123.21782178217822 chars | - | 27 | Reminders | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 100 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>171. postgres_sla_trackers</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Service Level Agreement tracking and metrics.

**Owner/Maintainer:** Automation/Workflows Team

**Tags:** `sla`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 286

### account_id` → `postgres_accounts.id` (inferred)
- `conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,309

### current_assignee_id` → Related table (inferred)
- `escalation_level

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### event

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 6.0
- **Average:** 1.5933
- **Distinct Values:** 5

### eventn_ctx_event_id` → Related table (inferred)
- `sla_policy_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_sla_trackers`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 286 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 20,465.0 to 20,465.0 | 20,465.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **conversation_id** | Float | No | - | 81,913,410.0 to 114,010,972.0 | 112,908,764.1641 | 2,479 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 6,309 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **current_assignee_id** | Float | Yes | - | 1.0 to 52,258.0 (Null: 37.2%) | 51,095.29031230083 | 40 | Reference to current assignee | Numeric | Foreign Key (likely) | Variable |
| **escalation_level** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Escalation Level | Numeric | None | Enum-like (1 values) |
| **event** | Float | No | - | 0.0 to 6.0 | 1.5933 | 5 | Event | Numeric; Required | Not Null | Enum-like (5 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **related_message_id** | Float | Yes | - | 805,619,397.0 to 819,542,314.0 (Null: 97.2%) | 810,761,389.0503597 | 140 | Reference to related message | Numeric | Foreign Key (likely) | Variable |
| **sla_policy_id** | Float | No | - | 1.0 to 5.0 | 2.2243 | 5 | Reference to sla policy | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (5 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 6,309 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>172. postgres_sla_trackers_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_sla_trackers. Contains unprocessed data before transformation.

**Owner/Maintainer:** Automation/Workflows Team

**Tags:** `raw-data`, `staging`, `sla`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 286

### account_id` → `postgres_accounts.id` (inferred)
- `conversation_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,309

### current_assignee_id` → Related table (inferred)
- `escalation_level

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** NULL to NULL
- **Average:** NULL
- **Distinct Values:** 1
- **Null %:** 100.0%

### event

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 6.0
- **Average:** 1.5933
- **Distinct Values:** 5

### eventn_ctx_event_id` → Related table (inferred)
- `sla_policy_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_sla_trackers_raw`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 286 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 20,465.0 to 20,465.0 | 20,465.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **conversation_id** | Float | No | - | 81,913,410.0 to 114,010,972.0 | 112,908,764.1641 | 2,479 | Reference to conversation | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 6,309 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **current_assignee_id** | Float | Yes | - | 1.0 to 52,258.0 (Null: 37.2%) | 51,095.29031230083 | 40 | Reference to current assignee | Numeric | Foreign Key (likely) | Variable |
| **escalation_level** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Escalation Level | Numeric | None | Enum-like (1 values) |
| **event** | Float | No | - | 0.0 to 6.0 | 1.5933 | 5 | Event | Numeric; Required | Not Null | Enum-like (5 values) |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **related_message_id** | Float | Yes | - | 805,619,397.0 to 819,542,314.0 (Null: 97.2%) | 810,761,389.0503597 | 140 | Reference to related message | Numeric | Foreign Key (likely) | Variable |
| **sla_policy_id** | Float | No | - | 1.0 to 5.0 | 2.2243 | 5 | Reference to sla policy | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (5 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 6,309 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>173. postgres_taggables</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores labels and tags for categorization.

**Owner/Maintainer:** Platform Team

**Tags:** `labels`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,881

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,913

### eventn_ctx_event_id` → Related table (inferred)
- `taggable_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_taggables`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 2,881 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,913 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **tag_id** | Float | No | - | 1.0 to 77,029.0 | 17,089.450199999996 | 771 | Reference to tag | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **taggable_id** | Float | No | - | 672,152,308.0 to 689,780,258.0 | 680,969,426.2856 | 9,992 | Reference to taggable | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **taggable_type** | Text | No | Category | 7.0 chars | - | 1 | Type or category classification | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,913 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>174. postgres_teams</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages team structures and memberships.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 105

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_teams`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 105 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 24.0 to 28,431.0 | 21,062.88529411765 | 155 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **allow_auto_assign** | Integer | No | Category | 0.0 to 1.0 | 0.8411764705882353 | 2 | Allow Auto Assign | Numeric; Required | Not Null | Enum-like (2 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 340 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 89.7%) | - | 36 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **description** | Text | No | Description | 9.76764705882353 chars | - | 116 | Description | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 340 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 12.55 chars | - | 264 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 340 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>175. postgres_teams_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_teams. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 121

### account_id` → `postgres_accounts.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_teams_raw`
- **Total Columns:** 11

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 121 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 24.0 to 28,431.0 | 21,322.09560723514 | 155 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **allow_auto_assign** | Integer | No | Category | 0.0 to 1.0 | 0.8087855297157622 | 2 | Allow Auto Assign | Numeric; Required | Not Null | Enum-like (2 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 340 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 91.0%) | - | 36 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **description** | Text | No | Description | 10.253229974160206 chars | - | 118 | Description | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 340 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **name** | Text | No | Name | 13.219638242894057 chars | - | 268 | Human-readable name or title | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 387 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>176. postgres_templates</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores message templates.

**Owner/Maintainer:** Platform Team

**Tags:** `templates`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,838

### account_id` → `postgres_accounts.id` (inferred)
- `allow_category_change

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 1.0
- **Average:** 0.023
- **Distinct Values:** 2

### body

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 316.7722 chars
- **Distinct Values:** 7,836

### category

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.1344 chars
- **Distinct Values:** 6

### complex_template_config

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 2.4928 chars
- **Distinct Values:** 18

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,926

### created_from_limechat

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.3229
- **Distinct Values:** 2

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### display_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_templates`
- **Total Columns:** 28

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1,838 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 27,578.0 | 14,750.440499999997 | 172 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **allow_category_change** | Integer | Yes | Category | 0.0 to 1.0 | 0.023 | 2 | Allow Category Change | Numeric | None | Enum-like (2 values) |
| **body** | Text | No | - | 316.7722 chars | - | 7,836 | Body | Required | Not Null | Variable |
| **category** | Text | No | Category | 3.1344 chars | - | 6 | Category | Required | Not Null | Categorical (6 categories) |
| **complex_template_config** | Text | No | Category | 2.4928 chars | - | 18 | Complex Template Config | Required | Not Null | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 2,926 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_from_limechat** | Integer | No | Category | 0.0 to 1.0 | 0.3229 | 2 | Created From Limechat | Numeric; Required | Not Null | Enum-like (2 values) |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 100.0%) | - | 1 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **display_id** | Float | No | - | 1.0 to 7,279.0 | 787.1876000000001 | 2,605 | Reference to display | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,997 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **footer** | Text | No | - | 11.58 chars | - | 381 | Footer | Required | Not Null | Variable |
| **header** | Text | No | - | 1.2183 chars | - | 307 | Header | Required | Not Null | Variable |
| **inbox_id** | Float | No | - | 107.0 to 34,375.0 | 24,573.486299999982 | 255 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **is_deleted** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Is Deleted | Numeric | None | Enum-like (1 values) |
| **language** | Text | No | Category | 1.5741 chars | - | 11 | Language | Required | Not Null | Variable |
| **media_url** | Text | No | URL | 1.3575 chars | - | 10 | URL or web address | Valid URL format; Required | Not Null | Categorical (10 categories) |
| **namespace** | Text | No | - | 10.7856 chars | - | 78 | Namespace | Required | Not Null | Variable |
| **rejection_reason** | Text | No | Category | 0.0 chars | - | 1 | Rejection Reason | Required | Not Null | Categorical (1 categories) |
| **short_code** | Text | No | - | 19.6464 chars | - | 8,412 | Short Code | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Text | No | Category | 7.9738 chars | - | 6 | Status or state of record | Required | Not Null | Categorical (6 categories) |
| **template_buttons** | Text | No | - | 131.5973 chars | - | 3,710 | Template Buttons | Required | Not Null | Variable |
| **template_code** | Text | No | - | 11.5931 chars | - | 8,630 | Template Code | Required | Not Null | Variable |
| **template_custom_parameters** | Text | No | Category | 0.0 chars | - | 1 | Template Custom Parameters | Required | Not Null | Categorical (1 categories) |
| **template_type** | Float | No | - | 0.0 to 3.0 | 0.7428 | 4 | Type or category classification | Numeric; Required | Not Null | Enum-like (4 values) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 2,840 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>177. postgres_templates_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgres_templates. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `templates`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 14

### account_id` → `postgres_accounts.id` (inferred)
- `allow_category_change

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** Yes
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### body

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 311.9602 chars
- **Distinct Values:** 6,724

### category

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.4648 chars
- **Distinct Values:** 4

### complex_template_config

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 2,882

### created_from_limechat

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.1549
- **Distinct Values:** 2

### deleted_at

- **Type:** `DateTime`
- **Semantic Type:** `DeletionTimestamp`
- **Nullable:** Yes
- **Distinct Values:** 1
- **Null %:** 100.0%

### display_id` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_templates_raw`
- **Total Columns:** 28

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 14 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 71.0 | 50.4214 | 21 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **allow_category_change** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Allow Category Change | Numeric | None | Enum-like (1 values) |
| **body** | Text | No | - | 311.9602 chars | - | 6,724 | Body | Required | Not Null | Variable |
| **category** | Text | No | Category | 5.4648 chars | - | 4 | Category | Required | Not Null | Categorical (4 categories) |
| **complex_template_config** | Text | No | Category | 0.0 chars | - | 1 | Complex Template Config | Required | Not Null | Categorical (1 categories) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 2,882 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **created_from_limechat** | Integer | No | Category | 0.0 to 1.0 | 0.1549 | 2 | Created From Limechat | Numeric; Required | Not Null | Enum-like (2 values) |
| **deleted_at** | DateTime | Yes | DeletionTimestamp | - (Null: 100.0%) | - | 1 | Deleted At | Valid ISO 8601 datetime | None | Variable |
| **display_id** | Float | No | - | 1.0 to 10,142.0 | 1,582.9088 | 3,766 | Reference to display | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,001 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **footer** | Text | No | - | 11.4843 chars | - | 346 | Footer | Required | Not Null | Variable |
| **header** | Text | No | - | 2.3689 chars | - | 617 | Header | Required | Not Null | Variable |
| **inbox_id** | Float | No | - | 10.0 to 34,219.0 | 11,598.3447 | 69 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **is_deleted** | Integer | Yes | Category | 0.0 to 0.0 | 0.0 | 1 | Is Deleted | Numeric | None | Enum-like (1 values) |
| **language** | Text | No | Category | 1.4445 chars | - | 9 | Language | Required | Not Null | Categorical (9 categories) |
| **media_url** | Text | No | URL | 1.2218 chars | - | 24 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **namespace** | Text | No | Category | 10.2384 chars | - | 7 | Namespace | Required | Not Null | Categorical (7 categories) |
| **rejection_reason** | Text | No | Category | 0.0 chars | - | 1 | Rejection Reason | Required | Not Null | Categorical (1 categories) |
| **short_code** | Text | No | - | 18.3657 chars | - | 7,318 | Short Code | Required | Not Null | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Text | No | Category | 7.9985 chars | - | 4 | Status or state of record | Required | Not Null | Categorical (4 categories) |
| **template_buttons** | Text | No | - | 119.2652 chars | - | 2,892 | Template Buttons | Required | Not Null | Variable |
| **template_code** | Text | No | - | 18.2048 chars | - | 7,498 | Template Code | Required | Not Null | Variable |
| **template_custom_parameters** | Text | No | - | 1.4028 chars | - | 156 | Template Custom Parameters | Required | Not Null | Variable |
| **template_type** | Float | No | - | 0.0 to 3.0 | 0.5401 | 4 | Type or category classification | Numeric; Required | Not Null | Enum-like (4 values) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 575 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>178. postgres_users</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores user information and access permissions.

**Owner/Maintainer:** Customer Data Team

**Tags:** `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 1,671

### address

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.3914 chars
- **Distinct Values:** 35

### availability

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 4.0
- **Average:** 0.9098
- **Distinct Values:** 5

### calling_enabled

- **Type:** `Integer`
- **Nullable:** Yes

### concurrency_enabled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.2925
- **Distinct Values:** 2

### concurrency_limit

- **Type:** `Float`
- **Nullable:** Yes
- **Range:** 0.0 to 555,555.0
- **Average:** 95.31504655120632
- **Distinct Values:** 50
- **Null %:** 0.1%

### configs

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### confirmation_sent_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,702
- **Null %:** 24.9%

### confirmation_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 5.116 chars
- **Distinct Values:** 2,191

### confirmed_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,066
- **Null %:** 15.4%

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 6,479

### current_sign_in_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 5,198
- **Null %:** 32.0%

### current_sign_in_ip

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.8198 chars
- **Distinct Values:** 1,783

### default_view_id` → Related table (inferred)
- `default_view_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 0.0 chars
- **Distinct Values:** 1

### display_name

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 0.4407 chars
- **Distinct Values:** 339

### email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 23.4187 chars
- **Distinct Values:** 6,510

### encrypted_password

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 45.066 chars
- **Distinct Values:** 5,796

### eventn_ctx_event_id` → Related table (inferred)
- `last_sign_in_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 7,865
- **Null %:** 20.3%

### last_sign_in_ip

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.8078 chars
- **Distinct Values:** 1,864

### name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 10.3066 chars
- **Distinct Values:** 5,498

### phone_number

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 3.4656 chars
- **Distinct Values:** 1,472

### provider

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.0 chars
- **Distinct Values:** 1

### pubsub_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 24.0 chars
- **Distinct Values:** 6,479

### reset_password_sent_at

- **Type:** `DateTime`
- **Nullable:** Yes
- **Distinct Values:** 937
- **Null %:** 87.8%

### reset_password_token

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.808 chars
- **Distinct Values:** 938

### shopify_deleted

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0114
- **Distinct Values:** 2

### sign_in_count

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 26,944.0
- **Average:** 57.53750000000002
- **Distinct Values:** 459

### signature

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 7.5176 chars
- **Distinct Values:** 230

### signature_type

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 5.4096 chars
- **Distinct Values:** 3

### source

- **Type:** `Text`
- **Semantic Type:** `Source`
- **Nullable:** No
- **Avg Length:** 0.385 chars
- **Distinct Values:** 2

### src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### store_url

- **Type:** `Text`
- **Semantic Type:** `URL`
- **Nullable:** No
- **Avg Length:** 1.61 chars
- **Distinct Values:** 459

### timezone

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 12.0058 chars
- **Distinct Values:** 9

### tokens

- **Type:** `Text`
- **Nullable:** No
- **Avg Length:** 225.3582 chars
- **Distinct Values:** 5,466

### ui_settings

- **Type:** `Text`
- **Semantic Type:** `SerializedJSON`
- **Nullable:** No
- **Avg Length:** 5.7313 chars
- **Distinct Values:** 3

### uid` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgres_users`
- **Total Columns:** 43

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 1,671 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **address** | Text | No | - | 0.3914 chars | - | 35 | Address | Required | Not Null | Variable |
| **availability** | Float | No | - | 0.0 to 4.0 | 0.9098 | 5 | Availability | Numeric; Required | Not Null | Enum-like (5 values) |
| **calling_enabled** | Integer | Yes | - | - | - | - | Calling Enabled | Numeric | None | Enum-like (0 values) |
| **concurrency_enabled** | Integer | No | Category | 0.0 to 1.0 | 0.2925 | 2 | Concurrency Enabled | Numeric; Required | Not Null | Enum-like (2 values) |
| **concurrency_limit** | Float | Yes | - | 0.0 to 555,555.0 (Null: 0.1%) | 95.31504655120632 | 50 | Concurrency Limit | Numeric | None | Variable |
| **configs** | Text | No | Category | 0.0 chars | - | 1 | Configs | Required | Not Null | Categorical (1 categories) |
| **confirmation_sent_at** | DateTime | Yes | - | - (Null: 24.9%) | - | 5,702 | Confirmation Sent At | Valid ISO 8601 datetime | None | Variable |
| **confirmation_token** | Text | No | - | 5.116 chars | - | 2,191 | Authentication or access token | Required | Not Null | Variable |
| **confirmed_at** | DateTime | Yes | - | - (Null: 15.4%) | - | 5,066 | Confirmed At | Valid ISO 8601 datetime | None | Variable |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 6,479 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **current_sign_in_at** | DateTime | Yes | - | - (Null: 32.0%) | - | 5,198 | Current Sign In At | Valid ISO 8601 datetime | None | Variable |
| **current_sign_in_ip** | Text | No | - | 7.8198 chars | - | 1,783 | Current Sign In Ip | Required | Not Null | Variable |
| **default_view_id** | Float | Yes | - | NULL to NULL (Null: 100.0%) | NULL | 1 | Reference to default view | Numeric | Foreign Key (likely) | Enum-like (1 values) |
| **default_view_type** | Text | No | Category | 0.0 chars | - | 1 | Type or category classification | Required | Not Null | Categorical (1 categories) |
| **display_name** | Text | No | - | 0.4407 chars | - | 339 | Display Name | Required | Not Null | Variable |
| **email** | Text | No | Email | 23.4187 chars | - | 6,510 | Email address | Valid email format; Required | Not Null, Unique (likely) | Variable |
| **encrypted_password** | Text | No | - | 45.066 chars | - | 5,796 | Encrypted Password | Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 6,478 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **helpdesk_admin** | Integer | No | Category | 0.0 to 1.0 | 0.0003 | 2 | Helpdesk Admin | Numeric; Required | Not Null | Enum-like (2 values) |
| **last_sign_in_at** | DateTime | Yes | - | - (Null: 20.3%) | - | 7,865 | Last Sign In At | Valid ISO 8601 datetime | None | Variable |
| **last_sign_in_ip** | Text | No | - | 7.8078 chars | - | 1,864 | Last Sign In Ip | Required | Not Null | Variable |
| **name** | Text | No | Name | 10.3066 chars | - | 5,498 | Human-readable name or title | Required | Not Null | Variable |
| **phone_number** | Text | No | - | 3.4656 chars | - | 1,472 | Phone Number | Required | Not Null | Variable |
| **provider** | Text | No | Category | 5.0 chars | - | 1 | Reference to prover | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |
| **pubsub_token** | Text | No | - | 24.0 chars | - | 6,479 | Authentication or access token | Required | Not Null | Variable |
| **reset_password_sent_at** | DateTime | Yes | - | - (Null: 87.8%) | - | 937 | Reset Password Sent At | Valid ISO 8601 datetime | None | Variable |
| **reset_password_token** | Text | No | - | 7.808 chars | - | 938 | Authentication or access token | Required | Not Null | Variable |
| **shopify_deleted** | Integer | No | Category | 0.0 to 1.0 | 0.0114 | 2 | Shopify Deleted | Numeric; Required | Not Null | Enum-like (2 values) |
| **sign_in_count** | Float | No | - | 0.0 to 26,944.0 | 57.53750000000002 | 459 | Count of sign_in | Numeric; Required | Not Null | Variable |
| **signature** | Text | No | - | 7.5176 chars | - | 230 | Signature | Required | Not Null | Variable |
| **signature_type** | Text | No | Category | 5.4096 chars | - | 3 | Type or category classification | Required | Not Null | Categorical (3 categories) |
| **source** | Text | No | Source | 0.385 chars | - | 2 | Source | Required | Not Null | Categorical (2 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **store_url** | Text | No | URL | 1.61 chars | - | 459 | URL or web address | Valid URL format; Required | Not Null | Variable |
| **timezone** | Text | No | Category | 12.0058 chars | - | 9 | Timezone | Required | Not Null | Categorical (9 categories) |
| **tokens** | Text | No | - | 225.3582 chars | - | 5,466 | Authentication or access token | Required | Not Null | Variable |
| **ui_settings** | Text | No | SerializedJSON | 5.7313 chars | - | 3 | Ui Settings | Required | Not Null | Categorical (3 categories) |
| **uid** | Text | No | - | 25.6602 chars | - | 7,501 | Reference to u | Required | Not Null, Foreign Key (likely) | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,627 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_type** | Float | Yes | - | 0.0 to 1.0 | 0.0018 | 2 | Type or category classification | Numeric | None | Enum-like (2 values) |
| **web_rtc_id** | Text | No | Category | 0.0 chars | - | 1 | Reference to web rtc | Required | Not Null, Foreign Key (likely) | Categorical (1 categories) |

</details>

---

<details>
<summary><h2>179. postgresfb2_central_orders</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** E-commerce integration data.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 10

### account_id` → `postgres_accounts.id` (inferred)
- `amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 227,540.0
- **Average:** 1,423.8074610000015
- **Distinct Values:** 2,773

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0068
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,523

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 8

### customer_id` → Related table (inferred)
- `email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 22.3969 chars
- **Distinct Values:** 9,345

### eventn_ctx_event_id` → Related table (inferred)
- `last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.4974 chars
- **Distinct Values:** 4,607

### order_id` → Related table (inferred)
- `source_flow_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb2_central_orders`
- **Total Columns:** 29

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 10 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 12.0 to 11,563.0 | 4,138.084100000002 | 180 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **amount** | Float | No | - | 0.0 to 227,540.0 | 1,423.8074610000015 | 2,773 | Amount | Numeric; Required | Not Null | Variable |
| **cancelled** | Integer | No | Category | 0.0 to 1.0 | 0.0068 | 2 | Cancelled | Numeric; Required | Not Null | Enum-like (2 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 4,523 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 3.0 chars | - | 8 | Currency | Required | Not Null | Categorical (8 categories) |
| **customer_id** | Text | No | - | 11.6747 chars | - | 8,833 | Reference to customer | Required | Not Null, Foreign Key (likely) | Variable |
| **discount_amount** | Float | No | Discount | 0.0 to 37,000.0 | 272.7844269999999 | 1,534 | Count of dis_amount | Numeric; Required | Not Null | Variable |
| **email** | Text | No | Email | 22.3969 chars | - | 9,345 | Email address | Valid email format; Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_name** | Text | No | Name | 6.4209 chars | - | 5,074 | Human-readable name or title | Required | Not Null | Variable |
| **fulfillment_status** | Text | No | Category | 1.351 chars | - | 5 | Status or state of record | Required | Not Null | Categorical (5 categories) |
| **integration_id** | Float | No | - | 39.0 to 13,589.0 | 5,796.0756 | 180 | Reference to integration | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **last_name** | Text | No | Name | 5.4974 chars | - | 4,607 | Human-readable name or title | Required | Not Null | Variable |
| **order_id** | Text | No | - | 12.4479 chars | - | 9,973 | Reference to order | Required | Not Null, Foreign Key (likely) | Variable |
| **order_name** | Text | No | - | 8.7155 chars | - | 9,051 | Order Name | Required | Not Null | Variable |
| **order_notes** | Text | No | - | 12.3097 chars | - | 2,904 | Order Notes | Required | Not Null | Variable |
| **payment_status** | Text | No | Category | 5.5774 chars | - | 10 | Status or state of record | Required | Not Null | Categorical (10 categories) |
| **phone** | Text | No | - | 11.2054 chars | - | 9,760 | Phone | Required | Not Null | Variable |
| **presentment_currency** | Text | No | Category | 3.0 chars | - | 12 | Presentment Currency | Required | Not Null | Variable |
| **shipping_price** | Float | No | - | 0.0 to 3,170.0 | 27.890595999999995 | 56 | Shipping Price | Numeric; Required | Not Null | Variable |
| **source_flow_id** | Float | Yes | - | 30,658.0 to 30,679.0 (Null: 100.0%) | 30,668.5 | 3 | Reference to source flow | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Text | No | Category | 1.0243 chars | - | 5 | Status or state of record | Required | Not Null | Categorical (5 categories) |
| **store_type** | Float | No | - | 1.0 to 4.0 | 1.0953 | 3 | Type or category classification | Numeric; Required | Not Null | Enum-like (3 values) |
| **subtotal_price** | Float | No | - | 0.0 to 227,540.0 | 1,396.5135260000004 | 2,527 | Subtotal Price | Numeric; Required | Not Null | Variable |
| **tags** | Text | No | SerializedJSON | 26.9285 chars | - | 2,528 | Tags | Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 4,522 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>180. postgresfb2_central_orders_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgresfb2_central_orders. Contains unprocessed data before transformation.

**Owner/Maintainer:** E-commerce/Integrations Team

**Tags:** `raw-data`, `staging`, `e-commerce`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 10

### account_id` → `postgres_accounts.id` (inferred)
- `amount

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 227,540.0
- **Average:** 1,423.8074610000015
- **Distinct Values:** 2,773

### cancelled

- **Type:** `Integer`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Range:** 0.0 to 1.0
- **Average:** 0.0068
- **Distinct Values:** 2

### created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 4,523

### currency

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 3.0 chars
- **Distinct Values:** 8

### customer_id` → Related table (inferred)
- `email

- **Type:** `Text`
- **Semantic Type:** `Email`
- **Nullable:** No
- **Avg Length:** 22.3969 chars
- **Distinct Values:** 9,345

### eventn_ctx_event_id` → Related table (inferred)
- `last_name

- **Type:** `Text`
- **Semantic Type:** `Name`
- **Nullable:** No
- **Avg Length:** 5.4974 chars
- **Distinct Values:** 4,607

### order_id` → Related table (inferred)
- `source_flow_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb2_central_orders_raw`
- **Total Columns:** 29

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 10 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 12.0 to 11,563.0 | 4,138.084100000002 | 180 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **amount** | Float | No | - | 0.0 to 227,540.0 | 1,423.8074610000015 | 2,773 | Amount | Numeric; Required | Not Null | Variable |
| **cancelled** | Integer | No | Category | 0.0 to 1.0 | 0.0068 | 2 | Cancelled | Numeric; Required | Not Null | Enum-like (2 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 4,523 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **currency** | Text | No | Category | 3.0 chars | - | 8 | Currency | Required | Not Null | Categorical (8 categories) |
| **customer_id** | Text | No | - | 11.6747 chars | - | 8,833 | Reference to customer | Required | Not Null, Foreign Key (likely) | Variable |
| **discount_amount** | Float | No | Discount | 0.0 to 37,000.0 | 272.7844269999999 | 1,534 | Count of dis_amount | Numeric; Required | Not Null | Variable |
| **email** | Text | No | Email | 22.3969 chars | - | 9,345 | Email address | Valid email format; Required | Not Null, Unique (likely) | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **first_name** | Text | No | Name | 6.4209 chars | - | 5,074 | Human-readable name or title | Required | Not Null | Variable |
| **fulfillment_status** | Text | No | Category | 1.351 chars | - | 5 | Status or state of record | Required | Not Null | Categorical (5 categories) |
| **integration_id** | Float | No | - | 39.0 to 13,589.0 | 5,796.0756 | 180 | Reference to integration | Numeric; Required | Not Null, Foreign Key (likely) | Variable |
| **last_name** | Text | No | Name | 5.4974 chars | - | 4,607 | Human-readable name or title | Required | Not Null | Variable |
| **order_id** | Text | No | - | 12.4479 chars | - | 9,973 | Reference to order | Required | Not Null, Foreign Key (likely) | Variable |
| **order_name** | Text | No | - | 8.7155 chars | - | 9,051 | Order Name | Required | Not Null | Variable |
| **order_notes** | Text | No | - | 12.3097 chars | - | 2,904 | Order Notes | Required | Not Null | Variable |
| **payment_status** | Text | No | Category | 5.5774 chars | - | 10 | Status or state of record | Required | Not Null | Categorical (10 categories) |
| **phone** | Text | No | - | 11.2054 chars | - | 9,760 | Phone | Required | Not Null | Variable |
| **presentment_currency** | Text | No | Category | 3.0 chars | - | 12 | Presentment Currency | Required | Not Null | Variable |
| **shipping_price** | Float | No | - | 0.0 to 3,170.0 | 27.890595999999995 | 56 | Shipping Price | Numeric; Required | Not Null | Variable |
| **source_flow_id** | Float | Yes | - | 30,658.0 to 30,679.0 (Null: 100.0%) | 30,668.5 | 3 | Reference to source flow | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **status** | Text | No | Category | 1.0243 chars | - | 5 | Status or state of record | Required | Not Null | Categorical (5 categories) |
| **store_type** | Float | No | - | 1.0 to 4.0 | 1.0953 | 3 | Type or category classification | Numeric; Required | Not Null | Enum-like (3 values) |
| **subtotal_price** | Float | No | - | 0.0 to 227,540.0 | 1,396.5135260000004 | 2,527 | Subtotal Price | Numeric; Required | Not Null | Variable |
| **tags** | Text | No | SerializedJSON | 26.9285 chars | - | 2,528 | Tags | Required | Not Null | Variable |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 4,522 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>181. postgresfb_block_activities</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Data table for postgresfb block activities operations.

**Owner/Maintainer:** Platform Team

**Tags:** `operational`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 11

### activity_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 7,161

### activity_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 2.0
- **Average:** 1.7915
- **Distinct Values:** 2

### block_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,161

### eventn_ctx_event_id` → Related table (inferred)
- `flow_id` → Related table (inferred)
- `src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,163

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb_block_activities`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 11 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **activity_time** | DateTime | No | - | - | - | 7,161 | Activity Time | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **activity_type** | Float | No | - | 1.0 to 2.0 | 1.7915 | 2 | Type or category classification | Numeric; Required | Not Null | Enum-like (2 values) |
| **block_id** | Text | No | - | 3.0 chars | - | 49 | Reference to block | Required | Not Null, Foreign Key (likely) | Variable |
| **block_type** | Float | No | - | 1.0 to 3.0 | 1.0036 | 2 | Type or category classification | Numeric; Required | Not Null | Enum-like (2 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 7,161 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **flow_execution_id** | Float | Yes | - | 2,377.0 to 61,123.0 | 29,305.7382 | 5,796 | Reference to flow execution | Numeric | Foreign Key (likely) | Variable |
| **flow_id** | Float | Yes | - | 166.0 to 529.0 | 434.176 | 11 | Reference to flow | Numeric | Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 7,163 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 2,803,649.0 to 11,791,569.0 | 9,751,403.218799992 | 4,554 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>182. postgresfb_block_activities_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgresfb_block_activities. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 11

### activity_time

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 7,161

### activity_type

- **Type:** `Float`
- **Nullable:** No
- **Range:** 1.0 to 2.0
- **Average:** 1.7915
- **Distinct Values:** 2

### block_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,161

### eventn_ctx_event_id` → Related table (inferred)
- `flow_id` → Related table (inferred)
- `src

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### updated_at

- **Type:** `DateTime`
- **Semantic Type:** `UpdatedTimestamp`
- **Nullable:** No
- **Distinct Values:** 7,163

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb_block_activities_raw`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 11 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **activity_time** | DateTime | No | - | - | - | 7,161 | Activity Time | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **activity_type** | Float | No | - | 1.0 to 2.0 | 1.7915 | 2 | Type or category classification | Numeric; Required | Not Null | Enum-like (2 values) |
| **block_id** | Text | No | - | 3.0 chars | - | 49 | Reference to block | Required | Not Null, Foreign Key (likely) | Variable |
| **block_type** | Float | No | - | 1.0 to 3.0 | 1.0036 | 2 | Type or category classification | Numeric; Required | Not Null | Enum-like (2 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 7,161 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 10,000 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **flow_execution_id** | Float | Yes | - | 2,377.0 to 61,123.0 | 29,305.7382 | 5,796 | Reference to flow execution | Numeric | Foreign Key (likely) | Variable |
| **flow_id** | Float | Yes | - | 166.0 to 529.0 | 434.176 | 11 | Reference to flow | Numeric | Foreign Key (likely) | Variable |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 7,163 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | 2,803,649.0 to 11,791,569.0 | 9,751,403.218799992 | 4,554 | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Variable |

</details>

---

<details>
<summary><h2>183. postgresfb_block_activities_raw_2</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgresfb_block_activities_2. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No

### activity_time

- **Type:** `DateTime`
- **Nullable:** No

### activity_type

- **Type:** `Float`
- **Nullable:** No

### block_id` → Related table (inferred)
- `created_at

- **Type:** `DateTime`
- **Nullable:** No

### eventn_ctx_event_id` → Related table (inferred)
- `flow_id` → Related table (inferred)
- `src

- **Type:** `Text`
- **Nullable:** No

### updated_at

- **Type:** `DateTime`
- **Nullable:** No

### user_id` → `postgres_users.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb_block_activities_raw_2`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | - | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **activity_time** | DateTime | No | - | - | - | - | Activity Time | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **activity_type** | Float | No | - | - | - | - | Type or category classification | Numeric; Required | Not Null | Enum-like (0 values) |
| **block_id** | Text | No | - | - | - | - | Reference to block | Required | Not Null, Foreign Key (likely) | Categorical (0 categories) |
| **block_type** | Float | No | - | - | - | - | Type or category classification | Numeric; Required | Not Null | Enum-like (0 values) |
| **created_at** | DateTime | No | - | - | - | - | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | - | - | - | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Categorical (0 categories) |
| **flow_execution_id** | Float | Yes | - | - | - | - | Reference to flow execution | Numeric | Foreign Key (likely) | Enum-like (0 values) |
| **flow_id** | Float | Yes | - | - | - | - | Reference to flow | Numeric | Foreign Key (likely) | Enum-like (0 values) |
| **src** | Text | No | - | - | - | - | Source system identifier | Required | Not Null | Categorical (0 categories) |
| **updated_at** | DateTime | No | - | - | - | - | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **user_id** | Float | No | - | - | - | - | Reference to user | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |

</details>

---

<details>
<summary><h2>184. postgresfb_builder_user</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores user information and access permissions.

**Owner/Maintainer:** Customer Data Team

**Tags:** `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 2,228

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 10,000

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb_builder_user`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 2,228 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 1.0 | 1.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 10,000 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **identity** | Text | No | - | 12.9445 chars | - | 9,931 | Reference to entity | Required | Not Null, Foreign Key (likely) | Variable |
| **ig_name** | Text | No | Category | 0.0026 chars | - | 2 | Ig Name | Required | Not Null | Categorical (2 categories) |
| **ig_username** | Text | No | - | 2.8616 chars | - | 2,071 | Ig Username | Required | Not Null | Variable |
| **inbox_id** | Float | Yes | - | 5,891.0 to 5,892.0 (Null: 99.9%) | 5,891.1 | 3 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **phone** | Text | No | - | 6.1897 chars | - | 5,207 | Phone | Required | Not Null | Variable |
| **platform** | Text | No | Category | 8.4774 chars | - | 3 | Platform | Required | Not Null | Categorical (3 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 9,998 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **wa_optin_status** | Float | No | - | 2.0 to 2.0 | 2.0 | 1 | Status or state of record | Numeric; Required | Not Null | Enum-like (1 values) |

</details>

---

<details>
<summary><h2>185. postgresfb_builder_user_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for postgresfb_builder_user. Contains unprocessed data before transformation.

**Owner/Maintainer:** Customer Data Team

**Tags:** `raw-data`, `staging`, `users`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `id` → Related table (inferred)
- `_timestamp

- **Type:** `DateTime`
- **Nullable:** No
- **Distinct Values:** 3,289

### account_id` → `postgres_accounts.id` (inferred)
- `created_at

- **Type:** `DateTime`
- **Semantic Type:** `CreationTimestamp`
- **Nullable:** No
- **Distinct Values:** 9,999

### eventn_ctx_event_id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postgresfb_builder_user_raw`
- **Total Columns:** 14

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **id** | Float | No | PK | - | - | - | Identifier | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **_timestamp** | DateTime | No | - | - | - | 3,289 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **account_id** | Float | No | - | 1.0 to 1.0 | 1.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **created_at** | DateTime | No | CreationTimestamp | - | - | 9,999 | Created At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **eventn_ctx_event_id** | Text | No | - | 32.0 chars | - | 9,999 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **identity** | Text | No | - | 16.5716 chars | - | 9,903 | Reference to entity | Required | Not Null, Foreign Key (likely) | Variable |
| **ig_name** | Text | No | Category | 0.0 chars | - | 1 | Ig Name | Required | Not Null | Categorical (1 categories) |
| **ig_username** | Text | No | - | 5.9455 chars | - | 4,329 | Ig Username | Required | Not Null | Variable |
| **inbox_id** | Float | Yes | - | 925.0 to 927.0 (Null: 100.0%) | 926.0 | 3 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Enum-like (3 values) |
| **phone** | Text | No | Category | 0.0182 chars | - | 10 | Phone | Required | Not Null | Categorical (10 categories) |
| **platform** | Text | No | Category | 8.9966 chars | - | 3 | Platform | Required | Not Null | Categorical (3 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **updated_at** | DateTime | No | UpdatedTimestamp | - | - | 10,000 | Updated At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **wa_optin_status** | Float | No | - | 2.0 to 2.0 | 2.0 | 1 | Status or state of record | Numeric; Required | Not Null | Enum-like (1 values) |

</details>

---

<details>
<summary><h2>186. postres2_bot_analytics</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Analytics and metrics table for reporting purposes.

**Owner/Maintainer:** Bot/AI Team

**Tags:** `analytics`, `reporting`, `bot`, `ai`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `account_id` → `postgres_accounts.id` (inferred)
- `channel

- **Type:** `Text`
- **Nullable:** No

### conv_id` → Related table (inferred)
- `conversation_id` → Related table (inferred)
- `inbox_id` → `postgres_inboxes.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `postres2_bot_analytics`
- **Total Columns:** 18

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **account_id** | Integer | No | - | - | - | - | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **channel** | Text | No | - | - | - | - | Channel | Required | Not Null | Categorical (0 categories) |
| **conv_id** | Integer | No | - | - | - | - | Reference to conv | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **conversation_id** | BigInteger | No | - | - | - | - | Reference to conversation | Required | Not Null, Foreign Key (likely) | Variable |
| **created_at** | Date | No | - | - | - | - | Created At | Required | Not Null | Variable |
| **date** | Date | No | - | - | - | - | Date | Required | Not Null | Variable |
| **distinct_id** | Text | No | - | - | - | - | Reference to distinct | Required | Not Null, Foreign Key (likely) | Categorical (0 categories) |
| **event_id** | BigInteger | No | - | - | - | - | Reference to event | Required | Not Null, Foreign Key (likely) | Variable |
| **event_name** | Text | No | - | - | - | - | Event Name | Required | Not Null | Categorical (0 categories) |
| **event_type** | Integer | No | - | - | - | - | Type or category classification | Numeric; Required | Not Null | Enum-like (0 values) |
| **inbox_id** | Integer | No | - | - | - | - | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **inserted_at** | DateTime | No | - | - | - | - | Inserted At | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **is_outbound** | Integer | No | - | - | - | - | Is Outbound | Numeric; Required | Not Null | Enum-like (0 values) |
| **is_outside_working_hours** | Integer | No | - | - | - | - | Reference to is outse working hours | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (0 values) |
| **products** | Text | No | - | - | - | - | Products | Required | Not Null | Categorical (0 categories) |
| **properties** | Text | No | - | - | - | - | Properties | Required | Not Null | Categorical (0 categories) |
| **text** | Text | No | - | - | - | - | Text | Required | Not Null | Categorical (0 categories) |
| **timestamp** | BigInteger | No | - | - | - | - | Timestamp | Required | Not Null | Variable |

</details>

---

<details>
<summary><h2>187. subscriptions</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Manages subscription plans and billing.

**Owner/Maintainer:** Platform Team

**Tags:** `billing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v_aibyte_transform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.3 chars
- **Distinct Values:** 2

### _id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `subscriptions`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v_aibyte_transform** | Text | No | Category | 1.3 chars | - | 2 |   V Aibyte Transform | Required | Not Null | Categorical (2 categories) |
| **_id** | Text | No | Category | 24.0 chars | - | 20 | Unique identifier for subscriptions record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **apiuserid** | Text | No | Category | 18.0 chars | - | 9 | Reference to apiuser | Required | Not Null, Foreign Key (likely) | Categorical (9 categories) |
| **channelname** | Text | No | Source | 8.0 chars | - | 1 | Channelname | Required | Not Null | Categorical (1 categories) |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 20 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **eventname** | Text | No | Category | 11.35 chars | - | 3 | Eventname | Required | Not Null | Categorical (3 categories) |
| **inboxid** | Float | Yes | - | 27,881.0 to 35,028.0 (Null: 25.0%) | 33,642.2 | 11 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **islcsubscriber** | Integer | No | Category | 0.0 to 1.0 | 0.25 | 2 | Islcsubscriber | Numeric; Required | Not Null | Enum-like (2 values) |
| **name** | Text | No | Name | 14.6 chars | - | 6 | Human-readable name or title | Required | Not Null | Categorical (6 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **umsenabled** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Umsenabled | Numeric; Required | Not Null | Enum-like (1 values) |
| **url** | Text | No | URL | 52.8 chars | - | 6 | URL or web address | Valid URL format; Required | Not Null | Categorical (6 categories) |

</details>

---

<details>
<summary><h2>188. subscriptions_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for subscriptions. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `staging`, `billing`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v_aibyte_transform

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 1.3 chars
- **Distinct Values:** 2

### _id` → Related table (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `subscriptions_raw`
- **Total Columns:** 13

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v_aibyte_transform** | Text | No | Category | 1.3 chars | - | 2 |   V Aibyte Transform | Required | Not Null | Categorical (2 categories) |
| **_id** | Text | No | Category | 24.0 chars | - | 20 | Unique identifier for subscriptions_raw record | Required | Not Null, Primary Key | Variable |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **apiuserid** | Text | No | Category | 18.0 chars | - | 9 | Reference to apiuser | Required | Not Null, Foreign Key (likely) | Categorical (9 categories) |
| **channelname** | Text | No | Source | 8.0 chars | - | 1 | Channelname | Required | Not Null | Categorical (1 categories) |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 20 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Variable |
| **eventname** | Text | No | Category | 11.35 chars | - | 3 | Eventname | Required | Not Null | Categorical (3 categories) |
| **inboxid** | Float | Yes | - | 27,881.0 to 35,028.0 (Null: 25.0%) | 33,642.2 | 11 | Reference to inbox/channel | Numeric | Foreign Key (likely) | Variable |
| **islcsubscriber** | Integer | No | Category | 0.0 to 1.0 | 0.25 | 2 | Islcsubscriber | Numeric; Required | Not Null | Enum-like (2 values) |
| **name** | Text | No | Name | 14.6 chars | - | 6 | Human-readable name or title | Required | Not Null | Categorical (6 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **umsenabled** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Umsenabled | Numeric; Required | Not Null | Enum-like (1 values) |
| **url** | Text | No | URL | 52.8 chars | - | 6 | URL or web address | Valid URL format; Required | Not Null | Categorical (6 categories) |

</details>

---

<details>
<summary><h2>189. templates</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores message templates.

**Owner/Maintainer:** Platform Team

**Tags:** `templates`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred)
- `bodycontent

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 35.0 chars
- **Distinct Values:** 2

### category

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 9.0 chars
- **Distinct Values:** 1

### createdat

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 33.0 chars
- **Distinct Values:** 2

### displayid` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)
- `header

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### inboxid` → `postgres_inboxes.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `templates`
- **Total Columns:** 19

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | Category | 24.0 chars | - | 2 | Unique identifier for templates record | Required | Not Null, Primary Key | Categorical (2 categories) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **allowcategorychange** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Allowcategorychange | Numeric; Required | Not Null | Enum-like (1 values) |
| **bodycontent** | Text | No | Category | 35.0 chars | - | 2 | Bodycontent | Required | Not Null | Categorical (2 categories) |
| **category** | Text | No | Category | 9.0 chars | - | 1 | Category | Required | Not Null | Categorical (1 categories) |
| **createdat** | Text | No | Category | 33.0 chars | - | 2 | Timestamp when record was created | Required | Not Null | Categorical (2 categories) |
| **displayid** | Float | No | - | 3.0 to 4.0 | 3.5 | 2 | Reference to display | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 2 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Categorical (2 categories) |
| **footer** | Text | No | Category | 6.0 chars | - | 1 | Footer | Required | Not Null | Categorical (1 categories) |
| **hdaccountid** | Float | No | - | 189.0 to 189.0 | 189.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **header** | Text | No | Category | 6.0 chars | - | 1 | Header | Required | Not Null | Categorical (1 categories) |
| **inboxid** | Float | No | - | 716.0 to 716.0 | 716.0 | 1 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **language** | Text | No | Category | 5.0 chars | - | 1 | Language | Required | Not Null | Categorical (1 categories) |
| **shortcode** | Text | No | Category | 14.5 chars | - | 2 | Shortcode | Required | Not Null | Categorical (2 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **templatecode** | Text | No | Category | 7.0 chars | - | 2 | Templatecode | Required | Not Null | Categorical (2 categories) |
| **templatetype** | Text | No | Category | 4.0 chars | - | 1 | Type or category classification | Required | Not Null | Categorical (1 categories) |
| **updatedat** | Text | No | Category | 33.0 chars | - | 2 | Timestamp when record was last updated | Required | Not Null | Categorical (2 categories) |

</details>

---

<details>
<summary><h2>190. templates_raw</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Raw data staging table for templates. Contains unprocessed data before transformation.

**Owner/Maintainer:** Platform Team

**Tags:** `raw-data`, `templates`, `staging`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier (inferred from column naming pattern)

**Foreign Keys:**
- `__v

- **Type:** `Float`
- **Nullable:** No
- **Range:** 0.0 to 0.0
- **Average:** 0.0
- **Distinct Values:** 1

### _id` → Related table (inferred)
- `bodycontent

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 35.0 chars
- **Distinct Values:** 2

### category

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 9.0 chars
- **Distinct Values:** 1

### createdat

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 33.0 chars
- **Distinct Values:** 2

### displayid` → Related table (inferred)
- `eventn_ctx_event_id` → Related table (inferred)
- `header

- **Type:** `Text`
- **Semantic Type:** `Category`
- **Nullable:** No
- **Avg Length:** 6.0 chars
- **Distinct Values:** 1

### inboxid` → `postgres_inboxes.id` (inferred)

**Unique Constraints:**
- `_id` - Primary key uniqueness
- Additional unique constraints may exist based on business logic

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `templates_raw`
- **Total Columns:** 19

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning | Numeric; Required | Not Null, Default: 0 | Enum-like (1 values) |
| **_id** | Text | No | Category | 24.0 chars | - | 2 | Unique identifier for templates_raw record | Required | Not Null, Primary Key | Categorical (2 categories) |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when record synced to warehouse | Valid ISO 8601 datetime; Required | Not Null | Variable |
| **allowcategorychange** | Integer | No | Category | 1.0 to 1.0 | 1.0 | 1 | Allowcategorychange | Numeric; Required | Not Null | Enum-like (1 values) |
| **bodycontent** | Text | No | Category | 35.0 chars | - | 2 | Bodycontent | Required | Not Null | Categorical (2 categories) |
| **category** | Text | No | Category | 9.0 chars | - | 1 | Category | Required | Not Null | Categorical (1 categories) |
| **createdat** | Text | No | Category | 33.0 chars | - | 2 | Timestamp when record was created | Required | Not Null | Categorical (2 categories) |
| **displayid** | Float | No | - | 3.0 to 4.0 | 3.5 | 2 | Reference to display | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (2 values) |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 2 | Event tracking ID for analytics | Required | Not Null, Foreign Key (likely) | Categorical (2 categories) |
| **footer** | Text | No | Category | 6.0 chars | - | 1 | Footer | Required | Not Null | Categorical (1 categories) |
| **hdaccountid** | Float | No | - | 189.0 to 189.0 | 189.0 | 1 | Reference to account | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **header** | Text | No | Category | 6.0 chars | - | 1 | Header | Required | Not Null | Categorical (1 categories) |
| **inboxid** | Float | No | - | 716.0 to 716.0 | 716.0 | 1 | Reference to inbox/channel | Numeric; Required | Not Null, Foreign Key (likely) | Enum-like (1 values) |
| **language** | Text | No | Category | 5.0 chars | - | 1 | Language | Required | Not Null | Categorical (1 categories) |
| **shortcode** | Text | No | Category | 14.5 chars | - | 2 | Shortcode | Required | Not Null | Categorical (2 categories) |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system identifier | Required | Not Null | Categorical (1 categories) |
| **templatecode** | Text | No | Category | 7.0 chars | - | 2 | Templatecode | Required | Not Null | Categorical (2 categories) |
| **templatetype** | Text | No | Category | 4.0 chars | - | 1 | Type or category classification | Required | Not Null | Categorical (1 categories) |
| **updatedat** | Text | No | Category | 33.0 chars | - | 2 | Timestamp when record was last updated | Required | Not Null | Categorical (2 categories) |

</details>

---

