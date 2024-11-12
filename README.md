# Ecommerce Store - T3A2-A

Our E-commerce Store is a sophisticated MERN stack application designed to provide businesses with a complete online retail solution. This platform seamlessly integrates secure payment processing, user authentication, and inventory management into a user-friendly shopping experience.

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
    -   [Additional Features](#additional-features-post-mvp)

<br>

-   [Packages, Dependencies and Third-Party Services](#packages-dependencies-and-third-party-services)

    -   [Backend](#backend)
    -   [Frontend](#frontend)
    -   [Development](#development)
    -   [Deployment Services](#deployment-services)

<br>

-   [Dataflow & Application Architecture](#dataflow-and-application-architecture)

    -   [Dataflow Diagram](#dataflow-diagram)
    -   [Application Architecture Diagram](#application-architecture-diagram)

<br>

-   [User Stories & Personas](#user-stories-and-personas)

    -   [Persona 1](#persona-1)
    -   [Persona 2](#persona-2)
    -   [Persona 3](#persona-3)
    -   [User Story 1](#user-story-1)
    -   [User Story 2](#user-story-2)
    -   [User Story 3](#user-story-3)

<br>

-   [Task Management and Project Progress](#task-management-and-project-progress)
    -   [Trello Board](#trello-board)
    -   [Key Milestones](#key-milestones)

<br>

## Features and Functionality

### MVP Features

1. **User Authentication and Management**

    - Secure registration and login system
    - JWT-based authentication
    - Password reset via email
    - User profile management
    - Role-based access (Customer/Admin)
    - Order history tracking
    - Address management

2. **Product Management**

    - Product catalog with detailed information
    - Multiple product images
    - Category organization
    - Search functionality
    - Stock level tracking
    - Product availability status
    - Basic sorting options

3. **Shopping Experience**

    - Intuitive shopping cart
    - Real-time stock updates
    - Mobile-responsive design
    - Product image galleries
    - Cart persistence
    - Guest checkout option
    - Basic product filtering

4. **Payment and Checkout**

    - Stripe payment integration
    - Secure checkout process
    - Order confirmation system
    - Email notifications
    - Basic shipping options
    - Order tracking
    - Transaction history

5. **Admin Features**
    - Product CRUD operations
    - Basic inventory management
    - Order processing system
    - Category management

### Additional Features (Post-MVP)

1. **Enhanced Shopping Features**

    - Product reviews and ratings
    - Wishlist functionality
    - Recently viewed products
    - Social sharing

2. **Advanced Commerce Features**

    - Multiple payment methods
    - Discount code system

3. **Advanced Admin Tools**
    - Advanced analytics
    - Bulk product management
    - Advanced user management
    - Sales reports
    - Customer insights
    - Staff accounts

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

-   `Axios` (version 1.6.7)

    For handling API communications, Axios provides a robust solution with features like request/response interceptors and automatic JSON transformation. This is crucial for maintaining smooth communication between our frontend and backend, especially for operations like cart updates and order processing.

<br>

### Development

-   `nodemon` (version 3.0.3)

    During development, nodemon dramatically improves our workflow by automatically restarting the server when code changes are detected. This is particularly valuable when working on API endpoints and backend business logic, ensuring we can quickly test and iterate on features.

<br>

-   `dotenv` (version 16.4.1)

    Security is paramount in e-commerce, and dotenv helps us manage sensitive configuration data like API keys and database credentials safely across different environments. It's essential for maintaining secure configurations between development, testing, and production environments.

<br>

### Deployment Services

-   `Vercel`
    For our e-commerce frontend, Vercel is the ideal choice due to its seamless integration with React applications. Its zero-configuration deployment process means we can focus more on developing features rather than dealing with deployment complexities. The platform's edge network ensures our store loads quickly for customers worldwide, while the automatic preview deployments for each pull request enable our team to confidently review changes before they go live. The built-in analytics help us understand user behaviour and optimise the shopping experience.

<br>

-   `Render`

    We chose Render for our backend deployment because it strikes the perfect balance between simplicity and power for a Node.js/Express API. Unlike more complex platforms like AWS, Render allows us to deploy our API with minimal configuration while still providing enterprise-grade features. Its automatic scaling capabilities ensure our store can handle traffic spikes during peak shopping periods or sales events. The seamless integration with MongoDB Atlas and built-in SSL security makes it ideal for handling sensitive customer data and payment processing through Stripe.

<br>

-   `MongoDB Atlas`

    For an e-commerce platform that needs to handle dynamic product catalogs, user sessions, and order processing, MongoDB Atlas provides the flexibility and scalability we need. Its document-based structure perfectly matches our data models for products, users, and orders, while the ability to perform complex queries helps with features like product filtering and search. The automated backups and security features protect our customer data, while the global distribution ensures fast database access regardless of customer location. The built-in monitoring helps us optimise performance and identify potential issues before they impact the shopping experience.

<br>

These packages and their dependencies work together to provide a robust, secure, and efficient full-stack e-commerce application, handling everything from database operations and payment processing to user interface components and testing.

<br>

## Dataflow & Application Architecture

Explanation of dataflow diagram here...

**--IMAGE of Dataflow Diagram--**

<br>

Explanation of application architecture here...

**--IMAGE of Application Architecture Diagram--**

<br>

## User Stories & Personas

Introduction to section here...

### Persona 1

Persona 1 details here...

<br>

### Persona 2

Persona 2 details here...

<br>

### Persona 3

Persona 3 details here...

<br>

### User Story 1

User Story 1 details here...

<br>

### User Story 2

User Story 2 details here...

<br>

### User Story 3

User Story 3 details here...

<br>

## Wireframes

We designed three breakpoints for the following devices:

- Mobile
- Tablet
- Desktop


### **Desktop view (PLACEHOLDER)**

![Image of the desktop wireframe for all pages](/docs/wireframes/wireframe-desktop.png)

### **Tablet view (PLACEHOLDER)**

![Image of the desktop wireframe for all pages](/docs/wireframes/wireframe-tablet.png)

### **Mobile view (PLACEHOLDER)**

![Image of the desktop wireframe for all pages](/docs/wireframes/wireframe-mobile.png)

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
  <img src="docs/trello-screenshots/trello-1.png" alt="Trello Board Screenshot 1" width="300">
</details>

---

<br>

### Key Milestones

1. Project Initialisation

    - Task here

2. MVP Features (Frontend)

    - Task here

3. MVP Features (Backend)

    - Task here

4. Stretch Features

    - Task here

5. Documentation and Deployment
    - Write API documentation
    - Prepare deployment scripts
    - Finalize README and user guide

<br>
<br>
