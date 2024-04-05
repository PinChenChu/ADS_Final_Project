# AVL Tree-Based Order Management System Report

## Personal Information

- **Name:** Pin Chen Chu
- **UFID:** 17055846
- **UF Email:** pinchen.chu@ufl.edu

## Introduction

This report outlines the structure and functionality of a Python program designed to manage orders using an AVL tree, ensuring efficient processing with balanced tree operations. The program supports various functionalities, including order creation, cancellation, updating, and querying.

## System Overview

The system is structured around three primary classes:

### pinNode

Represents individual orders within the AVL tree.

- **Attributes include:**
  - **pinID:** The unique order ID.
  - **cstime:** Order creation time.
  - **pinvalue:** Order value.
  - **priority:** The calculated priority based on order value and creation time.
  - **dry_time:** The required time to complete the order.
  - **eta:** The estimated time of arrival or completion time.

### pinTree

Manages the AVL tree structure for organizing orders.

- **Key functionalities include:**
  - Inserting a node into the AVL tree while maintaining balance through rotations.
  - Determining node height.
  - Calculating the balance factor.
  - Finding the smallest node based on priority.

### pinorder

Handles high-level order operations like creation, cancellation, and updating.

- This includes creating new orders with specified attributes, canceling existing orders if they have not been delivered, updating order details, and printing information about orders within a specific time range.

## Function Prototypes and Descriptions

- **create_new_order(self, pinID, cstime, order_number_val, dry_time):** Creates a new order and inserts it into the AVL tree based on priority.
- **OrderDecline(self, pinID, cstime):** Cancels an order if it hasn't been delivered or is not out for delivery, adjusting the ETAs of subsequent orders as needed.
- **KnowOrderRank(self, pinID):** Determines the delivery rank of an order within the AVL tree.
- **renew_moment(self, pinID, cstime, new_dry_time):** Updates the delivery time for an existing order, recalculating ETAs for affected orders.
- **PrintTheTimeBelow(self, t0=None, t1=None):** Prints order details for orders scheduled for delivery within a specified time range.
- **NeedToBePassed(self):** Processes orders that have been delivered, removing them from the AVL tree.
- **quit(self, _=None):** Prints out all orders and their delivery times before exiting the system.

## Conclusion

The AVL tree-based order management system efficiently handles order processing through a structured approach using AVL trees. This ensures optimal performance for operations like insertion and deletion, thereby maintaining a balanced tree structure and enabling fast queries and updates.
