# Database Schema Specification

## Data Models

### 1. `users` Table (Students & Admins)
| Field Name | Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `user_id` | String | PK, NOT NULL | Student ID or Admin ID (e.g., `"67010042"`) |
| `full_name` | String | NOT NULL | First and Last Name |
| `role` | String | NOT NULL | `"STUDENT"` or `"ADMIN"` |
| `line_id` | String | NOT NULL | Line Messaging Contact ID |
| `batch` | Integer | NULLABLE | Batch Year (e.g., `67`, `68`, `69`) |
| `major` | String | NULLABLE | `"Mechatronics"`, `"Robotics"`, `"AI"` |
| `password` | String | NOT NULL | Password / PIN |

### 2. `items` Table
| Field Name | Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `item_id` | String | PK, NOT NULL | Equipment Code (e.g., `"EQ-MULT-01"`) |
| `name` | String | NOT NULL | Item Name |
| `category` | String | NOT NULL | Measurement, Microcontroller, Tool, Sensor |
| `total_qty` | Integer | NOT NULL | Total Quantity |
| `available_qty`| Integer | NOT NULL | Remaining Stock |
| `location` | String | NOT NULL | Cabinet / Shelf ID |
| `borrow_count` | Integer | DEFAULT 0 | Historical borrow frequency |

### 3. `loans` Table
| Field Name | Type | Constraints | Description |
| :--- | :--- | :--- | :--- |
| `loan_id` | String | PK, NOT NULL | Unique Loan Code |
| `item_id` | String | FK, NOT NULL | Reference to `items.item_id` |
| `student_id` | String | FK, NOT NULL | Reference to `users.user_id` |
| `checkout_date`| ISO String | NOT NULL | Checkout Date (`YYYY-MM-DD`) |
| `due_date` | ISO String | NOT NULL | Due Date (`YYYY-MM-DD`) |
| `return_date` | ISO String | NULLABLE | Actual Return Date |
| `status` | String | NOT NULL | `"ACTIVE"`, `"RETURNED"`, `"OVERDUE"` |