# Database Schema for Expat Dashboard

## 1. Users Table
- **user_id**: INT (Primary Key)
- **username**: VARCHAR(255)
- **email**: VARCHAR(255)
- **password**: VARCHAR(255)
- **created_at**: TIMESTAMP
- **updated_at**: TIMESTAMP

## 2. Countries Table
- **country_id**: INT (Primary Key)
- **country_name**: VARCHAR(255)
- **currency**: VARCHAR(10)
- **created_at**: TIMESTAMP
- **updated_at**: TIMESTAMP

## 3. Expat Experiences Table
- **experience_id**: INT (Primary Key)
- **user_id**: INT (Foreign Key to Users Table)
- **country_id**: INT (Foreign Key to Countries Table)
- **experience_details**: TEXT
- **created_at**: TIMESTAMP
- **updated_at**: TIMESTAMP

## Relationships
- Each user can have multiple expat experiences (One to Many).
- Each expat experience references one country (Many to One).