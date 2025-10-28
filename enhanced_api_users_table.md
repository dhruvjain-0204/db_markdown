<details>
<summary><h2>api_users</h2></summary>

### 📊 Enhanced Table Metadata

**Description:** Stores API authentication credentials and access tokens for third-party integrations and external API access. This table manages API keys created by users to programmatically access the platform's REST APIs.

**Owner/Maintainer:** Platform/API Team

**Tags:** `authentication`, `api`, `security`, `access-control`

### 🔑 Keys & Constraints

**Primary Key:**
- `_id` - Unique identifier for each API user record

**Unique Constraints:**
- `token` - Authentication tokens must be unique across all API users
- `email` - Each email can only be associated with one API user

**Foreign Keys:**
- `hdaccountid` → `postgres_accounts.id` - References the helpdesk/CRM account that owns this API user

### 📋 Original Table Details

- **Schema:** `datawarehouse`
- **Raw Name:** `api_users`
- **Total Columns:** 9

### 📊 Column Details

| Column Name | Type | Nullable | Semantic Type | Range/Length | Average | Distinct Values | Description | Validation Rules | Constraints | Allowed Values |
|-------------|------|----------|---------------|--------------|---------|-----------------|-------------|------------------|-------------|----------------|
| **__v** | Float | No | - | 0.0 to 0.0 | 0.0 | 1 | Version number for document versioning (MongoDB pattern) | Must be numeric | Default: 0 | Always 0.0 |
| **_id** | Text | No | Category | 24.0 chars | - | 14 | Unique identifier for the API user record | Must be 24-character string | Primary Key, Not Null | 24-character alphanumeric string |
| **_timestamp** | DateTime | No | - | - | - | 1 | Timestamp when the record was last synced to data warehouse | Must be valid ISO 8601 datetime | Not Null | Valid datetime |
| **email** | Text | No | Email | 23.3 chars | - | 14 | Email address of the user who created the API key | Must be valid email format | Unique, Not Null | Valid email format (RFC 5322) |
| **eventn_ctx_event_id** | Text | No | Category | 32.0 chars | - | 14 | Event tracking ID for analytics and audit trail purposes | Must be 32-character hex string | Not Null | 32-character hexadecimal string |
| **hdaccountid** | Float | No | - | 189.0 to 28,052.0 | 20,419.4 | 12 | Reference to the helpdesk/CRM account that owns this API user | Must be positive integer | Foreign Key, Not Null | Integer between 189 and 28,052 |
| **scopes** | Text | No | SerializedJSON | 17.9 chars | - | 2 | JSON array of permission scopes granted to this API token (e.g., read, write, admin) | Must be valid JSON array | Not Null | Valid JSON array of scope strings |
| **src** | Text | No | Category | 6.0 chars | - | 1 | Source system or application that created this record | Must be non-empty string | Not Null | Typically "mongo" |
| **token** | Text | No | Category | 28.5 chars | - | 8 | Authentication token used for API requests (hashed or encrypted) | Must be unique 28+ character string | Unique, Not Null | Alphanumeric string, average 28.5 characters |

### 📈 Data Statistics

- **Total Records:** 14 rows
- **Distinct Accounts:** 12 accounts have API users
- **Distinct Tokens:** 8 unique active tokens
- **Distinct Emails:** 14 unique email addresses
- **Average Email Length:** 23.3 characters
- **Scope Variations:** 2 different permission scope combinations

</details>

---
