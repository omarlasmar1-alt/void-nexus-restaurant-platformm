# Void Nexus Restaurant OS - Database Schema

## Authentication

### profiles
- id (UUID)
- full_name
- avatar_url
- phone
- created_at
- updated_at

### roles
- id
- name
- description

### permissions
- id
- name
- description

### user_roles
- id
- user_id
- role_id

### role_permissions
- id
- role_id
- permission_id

---

## Website

### settings
- id
- cafe_name
- phone
- email
- address
- opening_hours
- facebook
- instagram
- tiktok

### hero_content
- id
- title
- subtitle
- image_url
- button_text
- button_link

### homepage_sections
- id
- section_name
- enabled
- display_order

---

## Menu

### categories
- id
- name
- slug
- icon

### menu_items
- id
- category_id
- name
- description
- price
- image
- available
- featured

---

## Reservations

### restaurant_tables
- id
- table_number
- seats
- status

### reservations
- id
- customer_name
- phone
- email
- table_id
- guests
- reservation_date
- reservation_time
- notes
- status

---

## Loyalty

### loyalty_cards
- id
- customer_id
- card_number
- points

### rewards
- id
- name
- points_required

### loyalty_transactions
- id
- customer_id
- points
- type
- description

---

## Employees

### employees
- id
- full_name
- email
- phone
- role
- salary
- status

---

## Orders

### orders
- id
- customer_id
- total
- status
- payment_method
- created_at

### order_items
- id
- order_id
- menu_item_id
- quantity
- price

---

## Media

### media_library
- id
- file_name
- bucket
- url
- uploaded_at
