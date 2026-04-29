# ☕ Java & Bean Café Website

A Java Web Application deployed using Apache Tomcat on Ubuntu Server (VirtualBox)

---

## 📌 Project Overview

The **Java & Bean Café Website** is a dynamic web application designed to simulate a café system where users can browse menu items, view products, and interact with the system.

This project demonstrates **Java web development and server deployment** by hosting the application on **Apache Tomcat** running inside an **Ubuntu Server virtual machine (VirtualBox)**.

---

## 🚀 Features

- 📋 Dynamic café menu display  
- 🛒 Product browsing interface  
- 🔐 Backend processing using Java (Servlets/JSP)  
- 🌐 Deployment using Apache Tomcat  
- 🗄️ Database connectivity (MySQL)  
- 🧑‍💼 Optional admin functionalities  

---

## 🖥️ System Architecture

### Frontend
- HTML, CSS, JavaScript  

### Backend
- Java Servlets & JSP  

### Web Server
- Apache Tomcat  

### Database
- MySQL / MariaDB  

### Environment
- Ubuntu Server (VirtualBox VM)

---

## 🧰 Technologies Used

- ☕ Java (JDK 8 or higher)  
- 🐱 Apache Tomcat  
- 🐧 Ubuntu Server  
- 📦 VirtualBox  
- 🛢️ MySQL / MariaDB  
- 💻 VS Code / IntelliJ IDEA / Eclipse  
- 🔧 Git & GitHub  

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/java-bean-cafe.git
cd java-bean-cafe
```

---

### 2. Set Up Ubuntu Server (VirtualBox)

- Install VirtualBox  
- Create a VM and install Ubuntu Server  
- Configure networking (Bridge or NAT with port forwarding)  

---

### 3. Install Java

```bash
sudo apt update
sudo apt install openjdk-11-jdk -y
java -version
```

---

### 4. Install Apache Tomcat

```bash
sudo apt install tomcat9 -y
```

Start and enable Tomcat:

```bash
sudo systemctl start tomcat9
sudo systemctl enable tomcat9
```

---

### 5. Deploy the Application

#### Option A: WAR File Deployment

1. Build your project into a `.war` file  
2. Copy it to Tomcat webapps directory:

```bash
sudo cp java-bean-cafe.war /var/lib/tomcat9/webapps/
```

3. Restart Tomcat:

```bash
sudo systemctl restart tomcat9
```

---

#### Option B: Project Folder Deployment

```bash
sudo cp -r java-bean-cafe /var/lib/tomcat9/webapps/
```

---

### 6. Access the Website

Open your browser and go to:

```
http://localhost:8080/java-bean-cafe
```

---

## 🗄️ Database Setup

### Install MySQL

```bash
sudo apt install mysql-server -y
```

### Create Database

```bash
sudo mysql
```

```sql
CREATE DATABASE cafe_db;
CREATE USER 'cafe_user'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON cafe_db.* TO 'cafe_user'@'localhost';
FLUSH PRIVILEGES;
```

Update your Java database connection (JDBC) with these credentials.

---

## 📂 Project Structure

```
java-bean-cafe/
│── src/
│── webapp/ or WebContent/
│── WEB-INF/
│   └── web.xml
│── lib/
│── css/
│── js/
│── images/
│── database/
│── README.md
```

---

## 🔐 Security Considerations

- Use strong database credentials  
- Restrict Tomcat Manager access  
- Enable firewall (UFW) on Ubuntu  
- Avoid running Tomcat as root  
- Regularly update system packages  

---

## 🧪 Testing

- Access via browser (localhost:8080)  
- Check servlet responses  
- Verify database connectivity  

Monitor Tomcat logs:

```
/var/log/tomcat9/catalina.out
```

---

## 📈 Future Improvements

- Online ordering system  
- User login & authentication  
- Payment integration  
- Admin dashboard with analytics  

---

## 👨‍💻 Author

Developed by: **Your Name**

---

## 📄 License

This project is for educational purposes only.