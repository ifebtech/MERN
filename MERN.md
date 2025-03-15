**MERN Stack: Explanation & To-Do App Deployment .**

**1. What is the MERN Stack?**

The **MERN stack** is a combination of **MongoDB, Express.js, React.js,
and Node.js**, used to build full-stack web applications.

**1.1 Components of MERN**

-   **MongoDB** → A NoSQL database used to store application data.

-   **Express.js** → A lightweight web framework for Node.js to create
    API endpoints.

-   **React.js** → A front-end JavaScript library used for building
    interactive UIs.

-   **Node.js** → A JavaScript runtime for running server-side
    applications.

**1.2 MERN Architecture**

1.  **Frontend (React.js)** → Sends HTTP requests to the backend.

2.  **Backend (Node.js + Express.js)** → Handles requests, communicates
    with MongoDB, and sends responses.

3.  **Database (MongoDB)** → Stores user data and tasks.

------------------------------------------------------------------------

**2. Steps to Deploy the MERN To-Do App on AWS EC2**

**Step 1: Launch an EC2 Instance**

1.  Go to the **AWS EC2 Dashboard**.

2.  Click **Launch Instance**.

3.  Choose **Ubuntu 22.04 LTS** as the OS.

4.  Select **t2.micro** instance type (Free Tier eligible).

5.  Configure security groups:

    -   Allow **HTTP (80)** and **HTTPS (443)**.

    -   Allow **Custom TCP (3000, 5000)** for backend.

6.  Launch the instance and note the **Public IP** (e.g., 3.87.217.243).

**Step 2: Connect to the EC2 Instance**

Use **EC2 Instance Connect** from the AWS Console.

![](media/image1.png){width="6.5in" height="1.320138888888889in"}

![](media/image2.png){width="6.006944444444445in"
height="2.615972222222222in"}

**Step 3: Install Dependencies (Node.js, MongoDB, Git, and PM2)**

![](media/image3.png){width="6.395833333333333in"
height="2.5083333333333333in"}

**Step 4: Clone the To-Do App Repository**

![](media/image4.png){width="6.722222222222222in"
height="1.9631944444444445in"}

![](media/image5.png){width="6.243055555555555in"
height="2.7104166666666667in"}

**Step 5: Deploy Frontend Using Vercel**

![](media/image6.png){width="6.5in" height="2.3125in"}

![](media/image7.png){width="6.167028652668416in"
height="2.6805555555555554in"}

![](media/image8.png){width="6.145833333333333in"
height="3.457030839895013in"}

![](media/image9.png){width="6.208333333333333in"
height="2.548611111111111in"}

**Step 6: Configure Nginx as a Reverse Proxy**

![](media/image10.png){width="6.638888888888889in"
height="2.2784722222222222in"}

![](media/image11.png){width="6.243055555555555in"
height="0.8243055555555555in"}

**Step 7: Secure Nginx with SSL (Self-Signed
Certificate)**![](media/image12.png){width="6.527777777777778in"
height="1.4527777777777777in"}

Modify:

![](media/image13.png){width="6.972222222222222in"
height="2.861111111111111in"}

**Step 8: Test API Endpoints Using Postman and Browser for TODO-APP**

**8.1 Check if Backend is Running**

1.  Open **Postman**.

2.  Make a **GET request** to:

![](media/image14.png){width="6.826388888888889in"
height="1.1402777777777777in"}

![](media/image15.png){width="6.298611111111111in"
height="2.259027777777778in"}

![](media/image16.png){width="6.548611111111111in"
height="3.053472222222222in"}

![](media/image17.png){width="5.951388888888889in"
height="3.270138888888889in"}

**Conclusion**

By following this guide, you have successfully deployed a MERN To-Do app
on an AWS EC2 instance. The backend runs using **PM2**, the frontend is
deployed with **Vercel**, and **Nginx** acts as a reverse proxy. tested
API with Postman and ensure everything runs smoothly.
