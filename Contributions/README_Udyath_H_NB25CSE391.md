# Online Canteen Food-Ordering System

**Case Study:** Mobile and Web Applications Engineering\
**Student Name:** Udyath H\
**USN:** NB25CSE391\
**Target File Name:** `NB25CSE391_Canteen_Application.md`\
**Selected Architecture:** Progressive Web Application (PWA)

## 1. Introduction

The Online Canteen Food-Ordering System is a proposed application for a
college canteen. It uses a Progressive Web Application (PWA) to let
students browse the menu, place food orders, make digital payments, and
receive alerts when their orders are ready.

A PWA combines the accessibility of a web application with app-like
features such as home-screen installation, offline caching, and push
notifications. It can be accessed through a browser on mobile devices
and computers.

## 2. Problem Analysis

Manual canteen ordering can cause long queues during short breaks and
lunch hours. It can also lead to order miscommunication, delayed food
preparation, cash-handling bottlenecks, and uncertainty about item
availability or pickup time.

The proposed system addresses these problems through: - Real-time
digital menu browsing. - Online cart and order placement. - Secure
digital payment processing. - Automated notifications when orders are
ready for collection.

## 3. Comparison of Mobile, Web, and PWA Approaches

  -----------------------------------------------------------------------
  Evaluation        Native mobile     Traditional web   Progressive Web
  criterion         application       application       Application (PWA)
  ----------------- ----------------- ----------------- -----------------
  Installation and  Requires          Instant access    Instant browser
  access            downloading and   through a browser access with
                    installing from   URL; no           optional one-tap
                    Google Play Store installation      home-screen
                    or Apple App      required          installation
                    Store                               

  Cross-platform    May require       Runs in browsers  One unified
  reach             separate          on Android, iOS,  codebase for
                    codebases such as Windows, and      mobile and
                    Kotlin and Swift, macOS             desktop platforms
                    or a                                
                    cross-platform                      
                    framework                           

  Push              Native support    Limited; may rely Web Push API and
  notifications     through Firebase  on active browser Service Workers
                    Cloud Messaging   tabs, SMS, or     support
                    (FCM) or APNs     email             notifications on
                                                        supported
                                                        platforms

  Offline and       Can use local     Often fails or    Service Workers
  low-network       databases such as shows browser     can cache static
  resilience        SQLite or Realm   errors when the   assets and menus
                                      network is        for weak
                                      unavailable       connectivity

  Development and   Higher cost due   Lower cost with   Low-to-moderate
  maintenance cost  to platform       server-side       cost with one
                    builds, store     updates           codebase and
                    fees, and review                    background
                    cycles                              updates
  -----------------------------------------------------------------------

## 4. Proposed Solution: Progressive Web Application

The selected architecture for the college canteen food-ordering system
is a **Progressive Web Application (PWA)**.

Students can scan a QR code at the canteen or open a campus portal link
to start ordering without downloading a native application. Service
Workers and the Web Push API support order-ready notifications, while
caching helps the menu load during periods of weak connectivity. The
college IT team can maintain one responsive codebase instead of separate
applications for different platforms.

## 5. Four Major Functionalities

### 5.1 Dynamic Menu Browsing and Availability Tracking

-   Displays categories such as breakfast, lunch, beverages, and snacks.
-   Shows prices, preparation times, and dietary tags.
-   Displays live stock status updated by canteen staff.
-   Automatically disables unavailable items.

### 5.2 Cart Management and Order Placement

-   Allows students to select items and customize quantities.
-   Supports preparation notes.
-   Displays itemized totals.
-   Generates a unique digital token number and pickup time slot when an
    order is submitted.

### 5.3 Integrated Digital Payment Gateway

-   Supports UPI, debit cards, credit cards, and campus digital wallets.
-   Verifies payment confirmation through cryptographic webhooks.
-   Routes verified orders to the kitchen queue.

### 5.4 Real-Time Order Tracking and Push Notifications

The system tracks each order through these stages:

`Placed → Preparing → Ready for Pickup → Completed`

When food is ready, the system triggers a Web Push notification to the
student's device.

## 6. Application Workflow

The workflow diagram on page 3 of the case study shows three
participants: the Student (PWA Client), Backend and Payment API, and
Canteen (Kitchen Staff).

1.  The student browses the menu and selects items for the cart.
2.  The student submits the order and initiates UPI or card payment.
3.  The backend verifies the payment and generates an order token.
4.  Kitchen staff prepare the food using the kitchen queue display.
5.  Staff mark the order as ready and update its status.
6.  The Web Push service sends a Service Worker alert.
7.  The student receives the notification on their device.
8.  The student collects the order by verifying the digital token.

## 7. Expected Benefits

-   **Elimination of queue congestion:** Pre-ordering distributes
    kitchen workload and reduces physical billing lines.
-   **Easy student adoption:** Browser access and optional home-screen
    installation support access across devices.
-   **Accurate inventory and financial reconciliation:** Automated stock
    deduction and digital payment logs help prevent overselling and cash
    discrepancies.

## 8. Key Development Challenges

### 8.1 Peak-Hour Traffic and Inventory Race Conditions

Hundreds of students may place orders simultaneously during lunch
breaks. Without atomic database locking or optimistic concurrency
control, more than one student could attempt to purchase the last
available portion.

### 8.2 Cross-Browser Push Notifications and iOS Safari Restrictions

Push notification support differs between browsers and platforms. The
case study notes that iOS Safari requires users to add the PWA to the
Home Screen before granting push notification permissions. Fallbacks
such as in-app polling or SMS alerts may therefore be necessary.

### 8.3 Payment Webhook Latency and State Synchronization

Network interruptions during UPI or card redirects can leave
transactions pending. Idempotent payment verification webhooks and
background reconciliation jobs are needed to ensure orders are not lost
or duplicated.

## 9. Conclusion

A Progressive Web Application provides a suitable balance of
accessibility, app-like functionality, and maintainability for the
college online canteen food-ordering system. Instant browser access,
Service Worker caching, digital payments, order tracking, and Web Push
notifications can help reduce canteen queues while keeping deployment
and maintenance cost-effective.

## 10. Implementation Details

The supplied case study describes the proposed architecture and
functionality. It does not specify a finalized programming-language
stack, database product, hosting provider, API endpoints, or
installation commands. Add these details when the application
implementation is defined.
