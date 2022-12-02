# Vending-Machine-Api

## Day 1
20 Days of Code

### Goals
To see how well you can structure a database if given the opportunity.

### Summary
Design a database diagram for a vending machine that allows users with a role of “seller” to add, update or remove products, while users with a role of “buyer” role can deposit coins into the machine and make purchases.

### Database Diagram Tool
https://dbdiagram.io/home

<br/>

### Database Table Structure

Table: `users`
| Name | Type | Comments |
| --- | --- | --- |
| `id` | autoincrement |  |
| `uuid` | string | UUID to allow easy migration between envs without breaking FK in the logic |
| `username` | string |  |
| `role` | string | If the user is a seller or buyer. |
| `password` | string | hjdkjsd |
| `created_at` | timestamp |  |
| `updated_at` | timestamp |  |

<br/>

Table: `products`
| Name | Type | Comments |
| --- | --- | --- |
| `id` | autoincrement |  |
| `uuid` | string | UUID to allow easy migration between envs without breaking FK in the logic |
| `title` | string | Title of the product  |
| `cost` | string | Price of the product |
| `sellerId` | string | ID of the seller who created the product |
| `created_at` | timestamp |  |
| `updated_at` | timestamp |  |
| `deleted_at` | timestamp |  |
 
 <br/>

Table: `deposits`
| Name | Type | Comments |
| --- | --- | --- |
| `id` | autoincrement |  |
| `uuid` | string | UUID to allow easy migration between envs without breaking FK in the logic |
| `buyerId` | string | ID of the buyer  |
| `amount` | string | How much the product was bought for |
| `created_at` | timestamp |  |
| `updated_at` | timestamp |  |
