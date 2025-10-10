# 🌐 Carbon Stack

A simple and modern **landing page portfolio** for **Toyosi**, an aspiring **DevOps & Cloud Engineer**.  
This project uses **Node.js** and **Express.js** to serve a static HTML file from the `public` folder.

---

## 🚀 Project Setup

### 1️⃣  Download This Repository
Download the project files as a ZIP folder.
cd carbon_stack

2️⃣ Install Dependencies

Run this command inside the project directory to install required packages.

npm install

3️⃣ Start the Server Locally
npm start


Then open your browser and visit:

http://localhost:3000

🗂 Project Structure
carbon_stack/
├── public/
│   └── index.html
├── server.js
├── package.json
└── README.md


☁️ Deploying to AWS Elastic Beanstalk
Step 1️⃣ — Create a New GitHub Repository

Log in to your GitHub account.

Click “New Repository”.

Give it a name, for example toyosi-portfolio.

Leave it public or private depending on your preference.

Don’t initialize with a README — you already have one.

Then, connect your local project to this new remote repository:

git init
git remote add origin https://github.com/<your-username>/toyosi-portfolio.git
git add .
git commit -m "Initial commit - Toyosi Portfolio Landing Page"
git push -u origin main

Step 2️⃣ — Create a CodePipeline on AWS

Open the AWS Management Console.

Go to CodePipeline → Create Pipeline.

Set your source provider to GitHub and connect your GitHub account.

Select your toyosi-portfolio repository and the main branch.

For deploy provider, choose AWS Elastic Beanstalk.

Step 3️⃣ — Create an Elastic Beanstalk Environment

Go to AWS Elastic Beanstalk → Create New Application.

Give it a name like toyosi-portfolio-app.

Choose Platform: Node.js.

Choose the region closest to you.

AWS will automatically detect your server.js as the startup file.

Once deployed, Elastic Beanstalk will provide you with a live URL such as:

http://toyosi-portfolio-env.eba-xxxxxx.us-east-1.elasticbeanstalk.com

💡 Notes

All static files are served from the /public directory.

To customize the landing page, edit public/index.html.

Make sure your server.js listens on the port defined by process.env.PORT for Elastic Beanstalk compatibility.

Example:

const PORT = process.env.PORT || 3000;
app.listen(PORT, () => console.log(`Server running on port ${PORT}`));

👩🏽‍💻 Author

Toyosi
Aspiring DevOps & Cloud Engineer
Built under the guidance of Code Dynasty