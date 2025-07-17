AI Ticket Assistant
This is a smart support ticket system I built using Node.js, MongoDB, and AI. It helps automatically organize support tickets by assigning priorities, tagging relevant skills, and routing them to the right moderators using AI. I created this to streamline customer support workflows and reduce manual effort.

What it Does
Automatically categorizes and prioritizes support tickets using AI

Assigns tickets to moderators based on skill match

Generates helpful notes for moderators

Role-based access: User, Moderator, Admin

Sends email notifications with ticket details

Processes tickets asynchronously in the background

Tech Stack
Backend: Node.js + Express

Database: MongoDB

Auth: JWT (JSON Web Token)

Background Jobs: Inngest

AI Integration: Google Gemini API

Email: Nodemailer with Mailtrap

How to Run It
Clone the repo and install dependencies:

bash
Copy
Edit
git clone <your-repo-url>
cd ai-ticket-assistant
npm install
Set up environment variables in a .env file:

ini
Copy
Edit
MONGO_URI=your_mongo_uri
JWT_SECRET=your_secret
MAILTRAP_SMTP_HOST=...
MAILTRAP_SMTP_USER=...
GEMINI_API_KEY=your_api_key
Start the app:

bash
Copy
Edit
npm run dev
Start the background event server:

bash
Copy
Edit
npm run inngest-dev
API Overview
POST /api/auth/signup – Sign up

POST /api/auth/login – Log in

POST /api/tickets – Create a ticket

GET /api/tickets – View your tickets

Admin routes available for managing users and roles

