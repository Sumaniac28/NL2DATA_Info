
<div align="center">
  <!-- <img src="client/src/assets/HIW.png" alt="NL2Data Logo" width="200" /> -->
  <h1 align="center">NL2DATA</h1>
  <p align="center">
    An intuitive platform that transforms natural language into powerful data visualizations.
  </p>
  <p align="center">
    <a href="https://nl2data.vercel.app/">
      <img src="https://img.shields.io/badge/Live%20Project-Online-brightgreen" alt="Live Project" />
    </a>
    <a href="https://dev.to/sumaniac28/nl2data-3dh7">
      <img src="https://img.shields.io/badge/Blog%20Post-Read%20More-blue" alt="Blog Post" />
    </a>
  </p>
</div>

## ✨ Overview

In today's data-driven world, the ability to quickly and easily extract insights from databases is crucial. However, the complexity of SQL often creates a barrier for non-technical users. NL2Data is a revolutionary full-stack application designed to democratize data analysis. It provides a seamless interface where users can connect to their PostgreSQL databases, ask questions in plain English, and receive beautiful, interactive visualizations in return. Whether you're a business analyst, a product manager, or a student, NL2Data empowers you to unlock the stories hidden within your data, no SQL knowledge required.

## 🚀 Key Features

-   **Natural Language to SQL:** At its core, NL2Data features a sophisticated AI-powered engine that translates natural language queries into precise, executable SQL statements. This allows users to interact with their data in a conversational manner.

-   **Interactive & Customizable Dashboards:** Users can create personalized dashboards to organize their charts and visualizations. The drag-and-drop interface makes it easy to arrange and resize charts to create the perfect view.

-   **Diverse Chart Library:** NL2Data supports a wide range of chart types, including bar charts, line graphs, pie charts, and more. This flexibility allows users to choose the best visualization for their specific data and insights.

-   **Secure & Encrypted Database Connections:** Security is a top priority. All database credentials are encrypted, ensuring that your sensitive information is always protected. NL2Data provides a secure environment for connecting to and querying your databases.

-   **Robust User Authentication:** The application includes a complete user authentication system, allowing users to register, log in, and manage their accounts securely. This ensures that your data and projects are private and accessible only to you.

-   **Project-Based Workflow:** NL2Data is designed for organization. Users can create multiple projects, each with its own set of data sources and dashboards. This makes it easy to manage different data analysis tasks and collaborate with teams.

-   **Fully Responsive Design:** With a mobile-first approach, NL2Data is designed to work beautifully on all devices. Whether you're on a desktop, tablet, or smartphone, you'll have a seamless experience.

## 🛠️ Architecture & Tech Stack

The project is built on a modern, scalable monorepo architecture, with a clear separation between the frontend client and the backend server.

### Client (Frontend)

-   **Repository:** [Client GitHub Repo](https://github.com/Sumaniac28/NL2DATA-CLIENT)
-   **Description:** A sleek, intuitive, and responsive single-page application that provides the user interface for NL2Data.
-   **Key Technologies:**
    -   **Framework:** React & Vite
    -   **Language:** TypeScript
    -   **Styling:** Tailwind CSS
    -   **State Management:** Redux Toolkit
    -   **GraphQL Client:** Apollo Client
    -   **Charting:** Chart.js
    -   **Animations:** Framer Motion & GSAP

### Server (Backend)

-   **Repository:** [Server GitHub Repo](https://github.com/Sumaniac28/NL2DATA_SERVER)
-   **Description:** A powerful and secure Node.js application that handles the core business logic, database interactions, and AI-powered features.
-   **Key Technologies:**
    -   **Framework:** Express.js
    -   **Language:** TypeScript
    -   **Database:** PostgreSQL
    -   **ORM:** TypeORM
    -   **API:** GraphQL (Apollo Server)
    -   **AI Integration:** Anthropic Claude API
    -   **Security:** Helmet, CORS, JWT

## 🏁 Getting Started

To get NL2DATA running on your local machine, please follow these steps.

### Prerequisites

-   **Node.js:** v18 or higher
-   **Package Manager:** npm or yarn
-   **Database:** A running instance of PostgreSQL

# NL2DATA: Installation & Configuration Guide

This guide provides instructions for setting up the client and server for the NL2Data application. Since the client and server are in separate repositories, you will need to clone and configure each one individually.

---

## 1. Server Setup

First, let's set up the backend server.

#### a. Clone the server repository:
```bash
git clone https://github.com/Sumaniac28/NL2DATA_SERVER.git
cd NL2DATA_SERVER
```

#### b. Install server dependencies:
```bash
npm install
```

#### c. Configure environment variables:
Create a `.env` file in the `NL2DATA_SERVER` directory and add your specific configurations.

```env
NODE_ENV=development
PORT=5000
DB_HOST=your_db_host
DB_PORT=your_db_port
DB_USERNAME=your_db_username
DB_PASSWORD=your_db_password
DB_DATABASE=your_db_name
TEST_DB_HOST=your_test_db_host
TEST_DB_PORT=your_test_db_port
TEST_DB_USERNAME=your_test_db_username
TEST_DB_PASSWORD=your_test_db_password
TEST_DB_DATABASE=your_test_db_name
ENCRYPTION_SECRET=a_strong_secret_key_for_encryption
SECRET_KEY_ONE=a_long_and_random_secret_key
SECRET_KEY_TWO=another_long_and_random_secret_key
REACT_URL=http://localhost:3000
JWT_ACCESS_SECRET=your_jwt_secret_for_access_tokens
DB_SSL=false
CLAUDE_API_KEY=your_anthropic_claude_api_key
```

#### d. Run database migrations:
This command will set up the necessary database tables.
```bash
npm run migration:run
```

---

## 2. Client Setup

Now, let's set up the frontend client in a **separate terminal window or directory**.

#### a. Clone the client repository:
```bash
git clone https://github.com/Sumaniac28/NL2DATA-CLIENT.git
cd NL2DATA-CLIENT
```

#### b. Install client dependencies:
```bash
npm install
```

#### c. Configure environment variables:
Create a `.env` file in the `NL2DATA-CLIENT` directory. This tells the client where to send API requests.

```env
VITE_API_URL=http://localhost:5000/graphql
```

---

## 🏃‍♀️ How to Use

To run the application, you need to start both the backend server and the frontend client.

1.  **Start the backend server:**
    In your `NL2DATA_SERVER` directory, run:
    ```bash
    npm run dev
    ```

2.  **Start the frontend client:**
    In your `NL2DATA-CLIENT` directory, run:
    ```bash
    npm run dev
    ```

Once both are running, you can access the application at the URL provided by the client's development server (usually `http://localhost:3000` or a similar address).

## 🤝 Contributing

I welcome contributions from the community! If you'd like to contribute, please follow these steps:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Make your changes and commit them with descriptive messages.
4.  Push your changes to your fork.
5.  Submit a pull request to the main repository.
