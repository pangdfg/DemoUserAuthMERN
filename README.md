# DemoUserAuthMERN

This is a MERN stack application using JSON Web Tokens (JWT) for authentication.

## Prerequisites

- Docker
- Docker Compose

## Getting Started

1. Clone the repository:
    ```sh
    git clone https://github.com/pangdfg/DemoUserAuthMERN.git
    cd DemoUserAuthMERN
    ```

2. Create a `.env` file in the `backend` directory and add the following environment variables:
    ```env
    NODE_ENV=development
    PORT=8000
    APP_ORIGIN=http://localhost:5173
    MONGO_URI=mongodb://root:example@mongo:27017/
    JWT_SECRET=myjwtsecret
    JWT_REFRESH_SECRET=myjwtrefreshsecret
    EMAIL_SENDER=your_email_sender
    RESEND_API_KEY=you_resend_api_key
    ```
> [!NOTE]
>  `EMAIL_SENDER` and `RESEND_API_KEY` get to [link](https://resend.com/)

3. Create a `.env` file in the `frontend` directory and add the following environment variable:
    ```env
    VITE_API_URL=http://localhost:8000
    ```

4. Start the application using Docker Compose:
    ```sh
    docker-compose up --build
    ```

5. Open your browser and navigate to `http://localhost:5173` to access the frontend.

## Services

- **MongoDB**: Runs on port `27017`
- **API**: Runs on port `8000`
- **Frontend**: Runs on port `5173`

## Stopping the Application

To stop the application, run:
```sh
docker-compose down -v
```

This will stop and remove the containers, but the data in the `mongo_data` volume will be preserved.
