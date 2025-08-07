# 🗺️ CivicMap: Local Issue Mapping Platform

CivicMap is a Spring MVC-based web application that helps citizens report local civic issues and enables authorities to manage and resolve them efficiently. It provides three roles: **Admin**, **Citizen**, and **Authority**, each with specific functionalities.

---

## 🚀 Features

### 👤 Citizen
- Register and log in
- Report local issues with title, description, location, and image
- View submitted issues and their resolution status

### 🛠️ Authority
- Log in to view issues assigned to their jurisdiction
- Update issue status and mark them as resolved/unresolved

### 🧑‍💼 Admin
- Manage authority accounts
- View all citizens and issues
- Monitor system-wide activities

---

## 🔧 Tech Stack

- **Backend:** Java, Spring MVC, JDBC
- **Frontend:** JSP, HTML, CSS (Inline), Bootstrap
- **Database:** MySQL (`civicmapdb`)
- **Tools:** Eclipse, Apache Tomcat, XAMPP (for MySQL)

---

## 🗃️ Database Structure

Database Name: `civicmapdb`  
Contains the following tables:

- `citizen(id, name, email, password, mobile)`
- `authority(id, name, email, password, area)`
- `issues(id, citizen_id, authority_id, title, description, location, status, image_path)`

Use the included SQL file (`/database/civicmapdb.sql`) to create the database and tables.

---

## 📁 Project Structure
CivicMap/
├── src/
│ └── com.r3sys/
│ ├── controller/
│ ├── dao/
│ └── model/
├── WebContent/
│ ├── WEB-INF/
│ │ └── views/
│ │ ├── admin/
│ │ ├── citizen/
│ │ └── authority/
│ └── jsp/
├── pom.xml
├── spring-servlet.xml
├── config.xml
└── web.xml
