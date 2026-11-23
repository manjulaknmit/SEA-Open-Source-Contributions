# Online Canteen Food-Ordering System

**Case Study:** Mobile and Web Applications Engineering\
**Student Name:** Varshini D\
**USN:** NB25CSE399\
**Proposed Architecture:** Progressive Web Application (PWA)

## 1. Project Overview

The Online Canteen Food-Ordering System is a proposed Progressive Web
Application designed to reduce congestion and waiting time in a college
canteen. Students can browse the menu, place orders, make digital
payments, and receive notifications when their food is ready for pickup.

The application is intended to work across Android phones, iPhones, and
computers through a single responsive web codebase.

## 2. Problem Statement

Manual counter ordering in a college canteen can cause:

-   Long queues during short breaks and lunch hours.
-   Order miscommunication and delayed food preparation.
-   Cash-handling bottlenecks.
-   Difficulty knowing whether menu items are in stock.
-   Uncertainty about when an order will be ready.

The proposed system addresses these problems through digital ordering,
payment processing, stock availability updates, and pickup
notifications.

## 3. Proposed Solution

The selected architecture is a **Progressive Web Application (PWA)**.

A PWA provides browser access without requiring students to install an
application from an app store. Students can open a campus portal link or
scan a QR code and optionally add the application to their home screen.

The proposed PWA uses:

-   **Service Workers** for caching and improved performance during weak
    connectivity.
-   **Web App Manifest** for an app-like, home-screen-installable
    experience.
-   **Web Push API** for order-ready notifications.
-   A single responsive codebase for mobile and desktop access.

## 4. Main Features

### 4.1 Dynamic Menu Browsing and Availability Tracking

-   Displays food items under categories such as breakfast, lunch,
    beverages, and snacks.
-   Shows prices, preparation times, and dietary tags.
-   Displays live stock availability updated by canteen staff.
-   Disables unavailable items from ordering.

### 4.2 Cart Management and Order Placement

-   Allows students to select items and quantities.
-   Supports preparation notes.
-   Displays itemized order totals.
-   Generates a unique digital token number and pickup time slot after
    order submission.

### 4.3 Integrated Digital Payment Gateway

-   Supports UPI, debit cards, credit cards, and campus digital wallets.
-   Verifies payment confirmation through payment webhooks.
-   Sends verified orders to the kitchen queue.

### 4.4 Real-Time Order Tracking and Push Notifications

-   Tracks the order through these states:
    1.  Placed
    2.  Preparing
    3.  Ready for Pickup
    4.  Completed
-   Sends a Web Push notification when the food is ready for collection.

## 5. Application Workflow

1.  The student opens the PWA and browses the canteen menu.
2.  The student selects food items and adds them to the cart.
3.  The student submits the order and initiates UPI or card payment.
4.  The backend verifies the payment and generates an order token.
5.  Kitchen staff receive the order and prepare the food.
6.  Staff mark the order as **Ready** in the system.
7.  The Web Push service sends an alert to the student's device.
8.  The student visits the counter and verifies the digital token to
    collect the order.

## 6. Why a PWA?

The case study compares native mobile applications, traditional web
applications, and PWAs.

  -----------------------------------------------------------------------
  Evaluation        Native mobile app Traditional web   Progressive Web
  criterion                           app               App
  ----------------- ----------------- ----------------- -----------------
  Installation and  Requires          Opens through a   Opens in a
  access            app-store         browser URL       browser and can
                    download and                        optionally be
                    installation                        installed on the
                                                        home screen

  Cross-platform    May require       Works across      Uses one codebase
  reach             separate platform supported         across mobile and
                    codebases or a    browsers          desktop platforms
                    cross-platform                      
                    framework                           

  Push              Native            More limited      Supports Web Push
  notifications     notification      notification      through Service
                    support           options           Workers on
                                                        supported
                                                        platforms

  Offline and       Can use local     Often depends on  Can cache static
  weak-network      databases and     network access    assets and menus
  support           caching                             using Service
                                                        Workers

  Development and   Higher cost for   Lower cost and    Low-to-moderate
  maintenance       multiple platform server-side       cost with one
                    builds and store  updates           codebase and
                    processes                           background
                                                        updates
  -----------------------------------------------------------------------

A PWA is selected because it combines broad access, optional
installation, caching, notifications, and simpler maintenance.

## 7. Expected Benefits

-   **Reduced queue congestion:** Students can order before break time,
    helping distribute kitchen workload.
-   **Easy adoption:** Students can access the system through a browser
    or home-screen installation.
-   **Improved stock accuracy:** Automated stock updates help prevent
    overselling.
-   **Financial reconciliation:** Digital payment records reduce cash
    discrepancies.
-   **Better order communication:** Order tracking and notifications
    inform students when food is ready.

## 8. Development Challenges

### 8.1 Peak-Hour Traffic and Inventory Race Conditions

Many students may place orders at the same time during lunch breaks.
Database locking or optimistic concurrency control is needed to prevent
multiple students from purchasing the last available portion.

### 8.2 Browser and iOS Push Notification Differences

Push notification support differs across browsers and platforms. On iOS,
users may need to add the PWA to the Home Screen before enabling
notifications. Alternatives such as in-app status polling or SMS alerts
may be needed.

### 8.3 Payment Webhook Delays and State Synchronization

Network interruptions during payment redirects can leave transactions
pending. Idempotent payment verification and background reconciliation
jobs are needed to prevent orders from being lost or duplicated.

## 9. Conclusion

The Online Canteen Food-Ordering System proposes a PWA-based approach to
improve the college canteen experience. Browser access, Service Worker
caching, digital payments, order tracking, and Web Push notifications
address common ordering delays while keeping deployment and maintenance
manageable.

## 10. Scope Note

This README describes the proposed system in the supplied case study.
The PDF does not specify a finalized programming-language stack,
database product, hosting provider, API endpoints, or installation
commands. Those details should be added when the application
implementation is defined.
