This is the frontend for the Farmers Compensation System. The application allows users to register, log in, submit compensation requests, and manage profiles. Admins and inspectors have advanced features for user and request management.

docker run --name ds-lab-pg --rm \
-e POSTGRES_PASSWORD=pass123 \
-e POSTGRES_USER=postgres \
-e POSTGRES_DB=farmers \
-d -p --net=host \
-v ds-lab-vol:/var/lib/postgresql/data \
postgres:14

# Database Connection with PostgreSQL 14:
Database: farmers User: postgres Password: pass123 Click Apply and ok.

# Postman

All POST and GET requests are available via Postman at: https://team16-ds-2023.postman.co/workspace/team16_ds_2023-Workspace~3cd744a2-c049-4360-bd8f-9ca1f2d04773/collection/32323426-a2872f8c-0bbc-484a-b9df-fe3a42d70434?action=share&creator=32323426&active-environment=32323426-99e68ea4-e233-411d-a520-3c68b62279f4

# User Features

Sign Up: Requires email, username, password, full_name, address, afm, identity_id (2 letters + 6 numbers).
Login: Use email and password. If the user exists, login happens automatically.
Default Role: Farmer
Profile Management: View and edit personal information.
Role Request: Request promotion to Inspector.
Compensation Request: Submit, edit, or delete compensation requests.

# Admin Features

Automatic Admin Account: username: admin, password: admin
User Management: View all users, see details, edit, and delete users.
Role Assignment: Grant Inspector role to users.
Declarations: Create new declarations for users.
User Requests: Approve or reject role requests from users.
Create New User: Add new users manually.

# Inspector Features
View Requests: Inspect compensation requests submitted by users.
Decision Management: Approve or reject requests.
Compensation Management: Set compensation amount for approved requests.
On-site Check: Optionally perform on-site verification of farmland.
Profile Management: View and edit own details.

# Running the Frontend

Ensure the backend is running and connected to PostgreSQL.
Open the frontend in the browser using the npm run dev link.
Users can sign up and login.
Admins log in with credentials admin/admin to access management features.
Inspectors can manage and review requests after being assigned the role.

# Technologies

React.js / Next.js (Frontend framework)
Node.js / npm (Package management)
Postman (API testing)

# Frontend Usage Instructions

Download the Frontend Code
Click on Code in the repository and download the project.
Install Dependencies
Open a terminal in the frontend project folder and run:
npm install
This will install all necessary dependencies.
Run the Frontend
After installation, start the development server:
npm run dev
Once the server starts, click the link shown in the terminal to open the application in your browser.
User Signup and Login
A new user can sign up and then log in using the credentials they created.
To log in as admin, enter username: admin and password: admin.
