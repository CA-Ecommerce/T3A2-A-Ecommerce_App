# Vinyl Vibe - T3A2-A

Vinyl Vibe is a sophisticated e-commerce store built using the MERN stack. This platform seamlessly integrates secure payment processing, user authentication, and inventory management into a user-friendly shopping experience.

At its core, the application serves as a bridge between businesses and their customers, offering a modern, responsive interface for browsing products, managing purchases, and processing secure transactions. Built with scalability in mind, it accommodates both small businesses and larger enterprises, providing essential tools for inventory management, order processing, and customer engagement.

The platform combines React's powerful frontend capabilities with Express.js's robust backend, MongoDB's flexible data management, and industry-standard security practices. With features like Stripe integration for payments and automated email notifications through Resend, it delivers a comprehensive solution for modern e-commerce needs.

Key aspects include:

-   Secure user authentication and authorization
-   Comprehensive product management system
-   Streamlined checkout process with Stripe integration
-   Responsive design for all devices
-   Admin dashboard for business operations
-   Real-time inventory tracking
-   Automated email notifications for orders and updates

<br>

## Table of Contents

-   [Features and Functionality](#features-and-functionality)
    -   [MVP Features](#mvp-features)
    -   [Additional Features](#additional-enhanced-features-post-mvp)

<br>

-   [Packages, Dependencies and Third-Party Services](#packages-dependencies-and-third-party-services)
    -   [Backend](#backend)
    -   [Frontend](#frontend)
    -   [Development](#development)
    -   [Deployment Services](#deployment-services)

<br>

-   [Dataflow and Application Architecture](#dataflow-and-application-architecture)
    -   [Dataflow Diagram](#dataflow-diagram)
    -   [Application Architecture Diagram](#application-architecture-diagram)

<br>

-   [User Stories & Personas](#user-stories--personas)
    -   [Persona 1](#persona-1)
    -   [Persona 2](#persona-2)
    -   [Persona 3](#persona-3)
    -   [Persona 4](#persona-4)

<br>

-   [Site Map](#site-map)

<br>

-   [Wire Frames](#wire-frames)

<br>

-   [Task Management and Project Progress](#task-management-and-project-progress)
    -   [Trello Board](#trello-board)

<br>

## Features and Functionality

### MVP Features

1. **Shopping Experience**

    - Intuitive shopping cart
    - Mobile-responsive design
    - Cart persistence
    - Product catalog with detailed information
    - Multiple product images
    - Basic product filtering
    - Basic sorting options
    - Search functionality

<br>

2. **Payment and Checkout**

    - Handoff to Stripe for payment processing
    - Basic email notifications/confirmations

<br>

3. **User Authentication and Management**

    - Secure registration and login system
    - JWT-based authentication
    - Password reset via email
    - Role-based access (Customer/Admin)
    - User profile management
    - Address management
    - Order/transaction history

<br>

4. **Admin Management Features**

    - Product CRUD operations
    - Order CRUD operations
    - Customer CRUD operations
    - Search functionality

<br>

### Additional Enhanced Features (Post-MVP)

1. **Enhanced Shopping Experience Features**

    - Product reviews and ratings
    - Wishlist functionality
    - Recently viewed products
    - Social sharing
    - Real-time stock updates

<br>

2. **Enhanced Payment and Checkout Features**
    - Custom checkout flow
    - Multiple payment methods
    - Discount code system
    - Guest checkout option
    - Shipping options

<br>

3. **Enhanced User Authentication and Management Features**
    - Order tracking

<br>

4. **Enhanced Admin Management Features**
    - Advanced analytics
    - Sales reports
    - Bulk product management
    - Inventory management

<br>

Each feature is designed to enhance the overall shopping experience while providing businesses with powerful tools to manage their online presence effectively.

<br>
<br>

## Packages, Dependencies and Third-Party Services

The E-commerce Store utilises carefully selected technologies that work together to create a robust online shopping experience. Here's a detailed overview of our technology choices and why they're essential for our project:

### Backend

-   `Express.js` (version 4.18.2)
    -   body-parser
    -   cors
    -   compression
    
    We chose Express.js as our backend framework for its minimalist yet powerful approach. Its middleware system is perfect for our e-commerce needs, allowing us to easily implement authentication, request processing, and error handling. The large ecosystem of middleware packages helps us solve common e-commerce challenges like CORS for secure client-server communication and compression for faster response times.

<br>

-   `MongoDB` (version 6.3.0)

    -   mongodb (version 6.3.0)
    -   mongoose (version 8.1.1)

    MongoDB's flexible schema design is ideal for our e-commerce platform where product attributes can vary significantly. Mongoose adds a crucial layer of structure and validation, ensuring our product data, user profiles, and order information maintain consistency. The schema-based approach helps prevent errors in critical operations like order processing and inventory management.

<br>

-   `JSON Web Token` (version 9.0.2)

    -   jsonwebtoken

    JWT provides a secure and scalable solution for user authentication in our e-commerce platform. It enables stateless authentication, perfect for maintaining user sessions across multiple devices while accessing protected routes like user profiles, order history, and admin functions.

<br>

-   `Stripe` (version 14.14.0)

    For handling payments, Stripe is our go-to choice due to its robust security features and comprehensive API. It manages complex payment flows while ensuring PCI compliance, handling multiple currencies, and providing detailed transaction analytics - crucial features for any modern e-commerce platform.

<br>

-   `Resend` (version 3.2.0)

    Email communication is vital for e-commerce, and Resend provides a modern, developer-friendly solution. We use it for sending order confirmations, shipping updates, password resets, and marketing communications, with excellent delivery rates and easy-to-use templates.

<br>

-   `Jest` (version 29.7.0)

    -   supertest

    Testing is crucial for maintaining reliability in e-commerce systems. Jest provides a comprehensive testing solution for our backend, allowing us to verify critical paths like checkout processes, inventory updates, and user authentication flows with confidence.

<br>

-   `Bruno` (version 1.35.0)

    -   bruno-api

    Bruno is a tool that allows us to test our API endpoints and ensure they are working as expected. It provides a user-friendly interface for sending requests and viewing responses, making it easier to debug and develop our API.

<br>

### Frontend

-   `React` (version 18.2.0)

    -   react-dom
    -   react-router-dom (version 6.22.0)

    React forms the foundation of our frontend, chosen for its component-based architecture that perfectly suits our e-commerce UI needs. It enables us to create reusable components for product cards, shopping carts, and checkout forms while maintaining excellent performance through its virtual DOM system.

<br>

-   `Vite` (version 5.1.0)

    -   @vitejs/plugin-react

    Vite significantly improves our development workflow with its lightning-fast hot module replacement and optimised build process. This means faster development cycles and better performance for our customers, crucial for maintaining a competitive e-commerce platform.

<br>

-   `Axios` (version 1.6.7)

    For handling API communications, Axios provides a robust solution with features like request/response interceptors and automatic JSON transformation. This is crucial for maintaining smooth communication between our frontend and backend, especially for operations like cart updates and order processing.

<br>

-   `Zustand` (version 4.5.4)

    Zustand is a state management library that provides a simple and efficient way to manage state in our React application. It allows us to create and share global state variables across components, making it easier to maintain a consistent and responsive user interface.

<br>

-   `Tailwind CSS` (version 3.4.1)

    -   postcss
    -   autoprefixer

    Tailwind CSS enables us to build a consistent and responsive design system efficiently. Its utility-first approach allows rapid UI development while maintaining a professional look across our product catalog, shopping cart, and checkout process. The built-in responsive design utilities ensure our store looks great on all devices.

<br>

-   `shadcn/ui` (version 0.8.0)

    -   @radix-ui/react-\* (various components)
    -   class-variance-authority
    -   clsx
    -   tailwind-merge

    We leverage shadcn/ui to provide a consistent and accessible component library. Its integration with Tailwind CSS and focus on customization allows us to maintain brand consistency while providing a polished user experience across all interactive elements of our store.

<br>

-   `Vitest` (version 1.2.0)

    -   @testing-library/react
    -   @testing-library/jest-dom

    Vitest ensures our frontend components and user interactions work flawlessly. Its compatibility with Vite makes it perfect for testing critical user flows like add-to-cart functionality, checkout processes, and form validations in a way that mimics real user behaviour.

<br>

### Development

-   `nodemon` (version 3.0.3)

    During development, nodemon dramatically improves our workflow by automatically restarting the server when code changes are detected. This is particularly valuable when working on API endpoints and backend business logic, ensuring we can quickly test and iterate on features.

<br>

-   `dotenv` (version 16.4.1)

    Security is paramount in e-commerce, and dotenv helps us manage sensitive configuration data like API keys and database credentials safely across different environments. It's essential for maintaining secure configurations between development, testing, and production environments.

<br>

### Deployment Services

-   `Netlify`
    For our e-commerce frontend, Netlify is the ideal choice due to its seamless integration with React applications. Its zero-configuration deployment process means we can focus more on developing features rather than dealing with deployment complexities. The platform's edge network ensures our store loads quickly for customers worldwide, while the automatic preview deployments for each pull request enable our team to confidently review changes before they go live. The built-in analytics help us understand user behaviour and optimise the shopping experience.

<br>

-   `Render`

    We chose Render for our backend deployment because it strikes the perfect balance between simplicity and power for a Node.js/Express API. Unlike more complex platforms like AWS, Render allows us to deploy our API with minimal configuration while still providing enterprise-grade features. Its automatic scaling capabilities ensure our store can handle traffic spikes during peak shopping periods or sales events. The seamless integration with MongoDB Atlas and built-in SSL security makes it ideal for handling sensitive customer data and payment processing through Stripe.

<br>

-   `MongoDB Atlas`

    For an e-commerce platform that needs to handle dynamic product catalogs, user sessions, and order processing, MongoDB Atlas provides the flexibility and scalability we need. Its document-based structure perfectly matches our data models for products, users, and orders, while the ability to perform complex queries helps with features like product filtering and search. The automated backups and security features protect our customer data, while the global distribution ensures fast database access regardless of customer location. The built-in monitoring helps us optimise performance and identify potential issues before they impact the shopping experience.

<br>

These packages and their dependencies work together to provide a robust, secure, and efficient full-stack e-commerce application, handling everything from database operations and payment processing to user interface components and testing.

<br>
<br>

## Dataflow Diagram

![Dataflow_Diagram_V4](docs/Dataflow-Diagram/dataflow-diagram-V4.JPG)

### External Entities
External entities represent the User/Admin or systems that interact with the application from the outside. These entities provide input or receive output from the system.

#### User
-   Represents the customer interacting with the eCommerce store.
-   Actions:
    -   Authenticates to log in or register
    -   Browse products
    -   Add items to shopping cart
    -   Proceed to checkout
    -   Payment


#### Admin
-   Represents the store administrator who can manage the store and perform CRUD operations.
-   Actions:
    -   Manages Product, Orders and Users via CRUD operations
    -   View the admin dashboard tools


#### Guest
- Represents a guest browsing the store without logging in.
- Actions:
    - Browse products
    - Add items to shopping cart
    - Proceed to checkout (Checkout will then require login)


#### Payment Gateway (Stripe)
-   Third party service used to securely process payments.
-   Actions:
    -   Processes payment details submitted by customer during checkout
    -   Returns a payment confirmation or failure status


#### Email service (Resend)

-   Third party email service used for sending transactional emails.
-   Actions:
    -   Sends order confirmation emails to the customer upon successful order payment
    -   Sends additional updates related to orders or account activities

<br>

### Processes (Customer Store)
Processes represent the core operations or functions that process, manipulate, or route data within the system.

#### User Signup (1)
- Users can signup with a new login to the website
- Inputs: New login credentials (email and password)
- Outputs: User account creation enabling login access

#### User Login (1.5)
- The standard user login which can access all areas of the website excluding the admin dashboard.
- Inputs: Login credentials (email and password)
- Outputs: Successful JWT token for a User login

#### Admin Login (1.5)
- Admin role able to access all areas of website including admin dashboard
- Inputs: Login credentials (email and password)
- Outputs: Successful JWT token for Admin login

#### User Authentication (2)
- Validates user credentials during login or registration
- Inputs: User credentials (email and password)
- Outputs: Authentication token (JWT) on success or error message on failure

#### Add to Cart (3)
- Adds products to shopping cart to view and use for checkout
- Inputs: Product data
- Outputs: Adds product data to cart

#### Shopping cart (4)
- Handles the uesr's shopping cart operations. Shows a list of products that have been added to cart, with product details (Price, SKU, Quantity, etc)
- Inputs: Product selections (add, remove, modify quantities)
- Outputs: List of selected items with quantities and pricing

#### Checkout and Payment (5)
- Manages the checkout process and interfaces with the payment gateway (via stripe)
- Inputs: Shopping cart details and payment details
- Outputs: Order confirmation on success or error message on failure

#### Successful Order Page (6)
- Displays a confirmation message and order details upon successful checkout

#### Continue Shopping (7)
- Allows users to return to browsing and shopping with a reset cart after successfully completing a checkout
- This process ensures users can continue their shopping journey with a refreshed cart, enabling them to explore and add new products

<br>

### Processes (Admin Dashboard) 

#### Admin Dashboard
- Provides the admin with tools for managing the store via CRUD operations
- Inputs: Admin actions for product, user and order management
- Outputs: Updated product, user and order details displayed and stored

#### Product Management
- Handles the management of product inventory, including creating, updating, viewing, and deleting products
- Inputs: Product data provided by the admin for CRUD operations (e.g. product name, price, stock quantity)
- Outputs: Updated product records stored in the database and reflected in the store's product listings

#### Order Management
- Manages the lifecycle of orders, from creation to tracking and fulfilment
- Inputs: Shopping cart details, payment confirmation from the payment gateway and user information
- Outputs: New order records stored in the database and a confirmation email sent to the user via Resend

#### User Management
- Oversees the management of user accounts within the system, including creating, updating, viewing and deleting user records
- Inputs: User data provided by the admin for CRUD operations (e.g. user profile information)
- Outputs: Updated user records stored in the database and reflected in the admin dashboard

<br>

### Data Stores

Where the data is stored in the system and is accessed or updated by the processes.

#### User Database
-   Stores user account information (name, email)
-   Contents:
    -   User Profiles (name, email, address)
    -   Login credentials (hashed passwords)
    -   Order history

#### Products Database
-   Stores product information
-   Contents:
    -   Product details (ID, SKU, name, description, price, stock level)

#### Orders Database
-   Stores records of all orders placed by users
-   Contents:
    -   Order details (items purchased, quantities and total price)
    -   Payment status


<br>
<br>

## Application Architecture Diagram

![Application Architecture Diagram](docs/application-architechture-diagram/app-arch-diagram.png)

![Application Architecture Diagram Description](docs/application-architechture-diagram/app-arch-frontend.png)

![Application Architecture Diagram Description](docs/application-architechture-diagram/app-arch-backend.png)

<br>
<br>

## User Stories & Personas

<strong>Vinyl Vibe</strong> is an expanding Record Store with a <em>cult following</em>!

After many years of struggling to keep the doors open as <strong>Groovy Records</strong>, the resurgence of the Vinyl Record market in the past 5 years has seen them outgrow the crude, hardcoded, HTML page that owner Norm Gleeson's nephew created in the 90s, attached below (image reference 1).

Norm has a large inventory of rare and hard to find records from both famous and obscure Australian artists, including highly sort after records that never made it into International markets. He is the go to guru for all things Aus Music!

Word of the treasure trove of rare and hard to find records at <strong>Vinyl Vibe</strong> has travelled far and wide through Facebook and Reddit. They've identified a growing market of customers who want buy from Norm, <em>but don't live in the area.</em>

Norm needs an effective modern website that can connect and sell to their customers, be they local, interstate, or international!


### Persona 1
![Persona 1](docs/user-stories/user-stories-1.png)

<br>

### Persona 2
![Persona 2](docs/user-stories/user-stories-2.png)

<br>

### Persona 3
![Persona 3](docs/user-stories/user-stories-3.png)

<br>

### Persona 4
![Persona 4](docs/user-stories/user-stories-4.png)

<br>

NB: Please find the first text based draft of Persona 1's user story below in Reference 2. 

---

<details>
  <summary>Image References</summary>

  <br>

-   Reference 1

    <img src="docs/user-stories/reference-1.png" alt="Groovy Records Webpage Reference" width="300">

    <br>
-   Reference 2

    <img src="docs/user-stories/reference-2.png" alt="First Draft of Persona 1" width="300">

    <br>
</details>

---

<br>
<br>

## Site Map

Our e-commerce platform's structure is designed to provide intuitive navigation for both customers and administrators. The site map illustrates the hierarchical organization of pages and features, ensuring a logical flow from browsing products to completing purchases. We've organised the navigation to minimise the number of clicks required to reach any destination while maintaining a clear separation between customer-facing pages and administrative functions.

The following site map outlines the complete structure of our application:

![Image of the desktop wireframe for all pages](docs/wireframes/site-map.png)

<br>
<br>

## Wire Frames

We designed three breakpoints for the following devices:

-   Mobile
-   Tablet
-   Desktop

You can view the Figma file [here](https://www.figma.com/design/FcoiuafqXz3Ca4uVnaOFhp/%5BCODER-ACADEMY%5D-Ecommerce-App?node-id=14-65499&node-type=canvas).

### **Desktop view**

![Image of the desktop wireframe for all pages](docs/wireframes/wireframe-desktop.png)

### **Tablet view**

![Image of the desktop wireframe for all pages](docs/wireframes/wireframe-tablet.png)

### **Mobile view**

![Image of the desktop wireframe for all pages](docs/wireframes/wireframe-mobile.png)

### **Hi-Fi Wireframe**

![Image of the desktop wireframe for all pages](docs/wireframes/wireframe-hi-fi.png)

<br>
<br>

## Task Management and Project Progress

Throughout the development of this project we utilised Trello as our primary task management tool. This approach allowed us to effectively organise, prioritise, and track the progress of various features and tasks.

### Trello Board

You can view our project's Trello board [here](https://trello.com/b/lGrFjkAu).

The board is organised into the following lists:

-   Backlog
-   To Do
-   In Progress
-   Testing
-   Done

<br>

---

<details>
  <summary>View Trello Board Screenshots ⬇️</summary>
  <br>
  <img src="docs/trello-screenshots/trello-1.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-2.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-3.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-4.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-5.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-6.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-7.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-8.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-9.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-10.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-11.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-12.png" alt="Trello Board Screenshot 1" width="300">
</details>

---

<br>


