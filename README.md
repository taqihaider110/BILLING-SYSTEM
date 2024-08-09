# Farhan Restaurant Billing System

## Overview

The Farhan Restaurant Billing System is a console-based application designed to help manage a restaurant's billing and inventory. This application allows users to generate invoices, manage and view inventory items, and search for previous invoices.

## Features

1. **Generate Invoice**: Create and save a bill for a customer.
2. **Show all Invoices**: Display all saved invoices.
3. **Search Invoice**: Find a specific invoice by customer name.
4. **Manage Inventory**: View and add items to the restaurant's inventory (requires admin authentication).

## Installation

To use the Farhan Restaurant Billing System, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/taqihaider110/BILLING-SYSTEM.git
    ```
2. Navigate to the project directory:
    ```sh
    cd BILLING-SYSTEM
    ```
3. Compile the program using a C compiler:
    ```sh
    gcc -o restaurant_billing_system main.c
    ```
4. Run the executable:
    ```sh
    ./restaurant_billing_system
    ```

## Usage

Upon running the program, you will be presented with a menu of options:

1. **Generate Invoice**: 
    - Enter the customer's name.
    - Enter the number of items.
    - Select items from the inventory and specify quantities.
    - View the generated bill and choose whether to save it.

2. **Show all Invoices**:
    - View all previously saved invoices with itemized details and totals.

3. **Search Invoice**:
    - Enter a customer's name to find their invoice.
    - If an invoice is found, it will be displayed with all details.

4. **Manage Inventory**:
    - **View Inventory**: See all current inventory items and their prices.
    - **Add Items**: Add new items to the inventory (requires admin authentication).
    - Admin credentials are:
        - Username: Admin
        - Password: admin123

5. **Exit**: Close the application.

## File Structure

- `main.c`: The main source file containing the program logic.
- `RestaurantBill.dat`: A binary file where invoices are saved.

## Functions

### `void generateBillHeader(char name[50], char date[30])`
Generates and prints the bill header with the customer's name and date.

### `void generateBillBody(char item[30], int qty, float price)`
Generates and prints the body of the bill with item details.

### `void generateBillFooter(float total)`
Generates and prints the bill footer with total calculations, including discount and tax.

### `bool verifyUser()`
Prompts for admin credentials and verifies them.

### `void addInvItems(struct Items *add_items, size_t arr_size, size_t size)`
Allows adding new items to the inventory.

**UI REPRESENTATION**

**MENU:**

![Menu](https://github.com/user-attachments/assets/823d4ecb-d0c4-4386-b744-2060504c9cd6)

**GENERATE INVOICE:**

![Generate Invoice](https://github.com/user-attachments/assets/e16ce81b-0890-44ac-9193-a7f457a3004d)

**SHOW INVOICE:**

![Show Invoice](https://github.com/user-attachments/assets/49498795-c71f-4991-82cd-1fc88717e44c)

