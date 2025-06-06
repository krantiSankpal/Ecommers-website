# API Documentation for Ecommerce Project API

This Git repository contains the Java Spring Boot source code for an e-commerce backend system with a RESTful API for browsing products, adding to cart, placing orders, and checking out. Built with a modular MVC architecture and backed by MySQL, it includes unit tests and documentation.

**Base URL**:-  [Api Link](https://e-commerce-server-production-0873.up.railway.app)

## Api Docs


Welcome to the documentation for the Ecommerce Project API! This API provides a set of endpoints and functionalities to interact with our eCommerce platform programmatically. With this API, you can build applications, integrations, and automate various tasks related to our online store.

**Api Docs**:-  [Api Docs Link](https://e-commerce-server-production-0873.up.railway.app/swagger-ui/index.html)

## Authentication

All protected endpoints require the `Authorization` header with a valid token.

## Endpoints

### Update Cart Item

- **URL**: `/api/cart_items/{cartItemId}`
- **Method**: PUT
- **Tags**: cart-item-controller
- **Request Parameters**:
  - `cartItemId` (integer, int64, required)
- **Request Headers**:
  - `Authorization` (string, required)
- **Request Body**:
  ```json
  {
    "$ref": "#/components/schemas/CartItem"
  }
  ```
- **Responses**:
  - 200 OK
    ```json
    {
      "$ref": "#/components/schemas/CartItem"
    }
    ```

### Delete Cart Item

- **URL**: `/api/cart_items/{cartItemId}`
- **Method**: DELETE
- **Tags**: cart-item-controller
- **Request Parameters**:
  - `cartItemId` (integer, int64, required)
- **Request Headers**:
  - `Authorization` (string, required)
- **Responses**:
  - 200 OK
    ```json
    {
      "$ref": "#/components/schemas/ApiResponse"
    }
    ```

### Add Item to Cart

- **URL**: `/api/cart/add`
- **Method**: PUT
- **Tags**: cart-controller
- **Request Headers**:
  - `Authorization` (string, required)
- **Request Body**:
  ```json
  {
    "$ref": "#/components/schemas/AddItemRequest"
  }
  ```
- **Responses**:
  - 200 OK
    ```json
    {
      "$ref": "#/components/schemas/ApiResponse"
    }
    ```

... [continue documenting other endpoints](https://e-commerce-server-production-0873.up.railway.app/swagger-ui/index.html)

## Components

### Schemas

- CartItem
- ApiResponse
- AddItemRequest
- Product
- Order
- User
- AuthResponse
- ReviewRequest
- Review
- RatingRequest
- Rating
- PaymentLinkResponse
- Address
- CreateProductRequest
- PageProduct

## Servers

- Server 1:
  - URL: `http://localhost:5454`
  - Description: Generated server URL





