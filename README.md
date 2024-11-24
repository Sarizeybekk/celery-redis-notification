# 🚀 Real-Time Notification System with Django and Django Channels

This project is a **real-time notification system** developed using **Django** and **Django Channels**. It delivers notifications triggered by user interactions within the system, providing instant updates about important events. With the integration of **Celery** and **Redis**, this application ensures high performance and scalability, even under heavy traffic.

---

## 📋 Features

- 🔔 **Real-time Notifications**: Instantly notify users of important system events.
- 💾 **Asynchronous Task Handling**: Efficient background task execution using Celery.
- ⚡ **WebSocket Integration**: Real-time communication powered by Django Channels.
- 📈 **Scalable and Performant**: Optimized for handling high traffic scenarios.

---

## 🛠️ Technologies Used

| Technology        | Purpose                                           |
|--------------------|---------------------------------------------------|
| **Django**         | Backend framework for developing web applications. |
| **Django Channels**| Manage WebSocket connections for real-time updates. |
| **Celery**         | Handle long-running tasks asynchronously.         |
| **Redis**          | Memory store for message passing and caching.     |

---

## ⚙️ How It Works

1. **Modular Design**:
   - Notifications are triggered using **signal handlers**.
   - Instead of directly interacting with **Django Channels**, signal handlers invoke **Celery tasks** for better modularity.

2. **Performance Optimization**:
   - WebSocket message delivery is offloaded to **Celery tasks**, improving request-response time and reducing system load.

3. **Scalability**:
   - Using Celery and Redis, the application handles asynchronous operations effectively, making it suitable for high-traffic environments.

4. **Implementation Details**:
   - Single header notifications are triggered upon saving a notification model.
   - Tasks execute in the background, maintaining seamless user interaction and real-time updates.

---

## 🧩 Installation and Setup

Follow these steps to set up the project locally:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Sarizeybekk/celery-redis-notification.git
   

2. **Navigate to the Project Directory ** 📂

   ```bash
   cd celery-redis-notification




3. **Create a Virtual Environment** 🌐
    ```bash

     python -m venv venv
4. ***Activate the Virtual Environment** ⚙️
    ```bash
On Windows:

    venv\Scripts\activate


On macOS and Linux:


    source venv/bin/activate
5. ***Install Dependencies ** 📦
      ```bash

      pip install -r requirements.txt
6. ***Apply Migrations** 🗄️


    python manage.py migrate
7. ***Create a Superuser** 👤


       python manage.py createsuperuser
   8. ***Run the Development Server** 🚀

       ```bash
       python manage.py runserver
The API will be accessible at http://127.0.0.1:8000/.
