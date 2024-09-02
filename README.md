# SecureWave

This project is a real-time chat application built with a combination of modern web technologies. It supports public and private messaging, along with real-time user presence tracking. The application allows users to engage in secure, encrypted communication, ensuring that messages remain private between the participants. The chat interface is dynamic and includes features like typing indicators, attachment uploads, and a draggable private chat window.

## Features

- **Real-time Public Chat**: Users can join a public chat room where they can exchange messages with all connected users in real-time.
- **Private Messaging**: Users can initiate private conversations with other users. These private chats are secured with a unique encryption key derived for each chat session.
- **Real-time Presence**: The application tracks and displays a list of active users in real-time.
- **Typing Indicators**: The application shows when a user is typing, giving a more interactive experience.
- **Attachment Support**: Users can upload and share files in the public chat.
- **Draggable Private Chat Window**: Private chat windows can be dragged around the screen for better user experience.

## Tech Stack

### Frontend

- **React**: The frontend is built using React, a JavaScript library for building user interfaces. React's component-based architecture allows for the efficient and organized management of the chat's UI components.
- **Next.js**: The application is built on Next.js, a React framework that enables server-side rendering and easy deployment. Next.js provides a robust environment for building scalable and high-performance web applications.
- **Bootstrap**: The UI is styled with Bootstrap, providing a responsive and consistent user experience across devices.
- **FontAwesome**: Used for icons throughout the application, enhancing the visual appearance.

### Backend

- **Node.js**: The backend is powered by Node.js, providing a scalable and efficient environment for handling real-time communication.
- **Express.js**: The Express framework is used to manage the API endpoints, including user authentication, message handling, and file uploads.
- **MongoDB**: MongoDB is the database used to store user information, messages, and attachments. It provides a flexible and scalable solution for handling the dynamic data structures of the chat application.
- **Mongoose**: Mongoose is used for modeling MongoDB data in Node.js. It provides a straightforward, schema-based solution to manage the chat's data.

### Real-Time Communication

- **Pusher**: Pusher is used to handle real-time events, such as new messages, typing indicators, and presence updates. It ensures that all users receive updates instantaneously, making the chat application responsive and interactive.

### Security

- **Web Crypto API**: The Web Crypto API is used for encrypting and decrypting messages. Each message is encrypted with AES-GCM, ensuring that only the intended recipient can read the message.
- **User-Specific Encryption**: Private chat sessions use a unique encryption key derived from the participating users' information, providing an additional layer of security.

## Code Structure

- `/pages`: Contains all the Next.js pages, including the main chat interface and API routes.
- `/components`: Houses React components such as the chat window, message list, and user interface elements.
- `/utils`: Includes utility functions for encryption, key management, and API interaction.
- `/services`: Manages services like Pusher and MongoDB interactions.

## Setup and Installation

### Prerequisites

- Node.js (v14.x or later)
- npm or yarn
- MongoDB (local or cloud instance)
- Pusher account

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/timetravel0/SecureWave.git
    cd SecureWave
    ```

2. Install dependencies:

    ```bash
    npm install
    ```

3. Create a `.env.local` file in the root of your project and add the following variables:

    ```plaintext
    NEXT_PUBLIC_PUSHER_KEY=your-pusher-key
    NEXT_PUBLIC_PUSHER_CLUSTER=your-pusher-cluster
    PUSHER_APP_ID=your-pusher-app-id
    PUSHER_SECRET=your-pusher-secret
    SECRET_KEY=your-encryption-secret
    MONGODB_URI=your-mongodb-connection-string
    MONGODB_DBNAME=your-mongodb-database-name
    ```

4. Run the application:

    ```bash
    npm run dev
    ```

    The application will be available at [http://localhost:3000](http://localhost:3000).
