##🎓 Student Course Management System

A simple CLI-based **Student Course Management System** built using **MySQL** on **AWS RDS**, accessed via **MySQL CLI** from an **AWS EC2** instance.

<img width="1190" alt="Architecture" src="https://github.com/user-attachments/assets/d249c15e-167e-40ab-a4cd-af0bfea01fad" />


## 📘 Description

This mini-project demonstrates how to leverage **AWS cloud services** to set up and manage a **relational database system**. The project covers the essential CRUD operations (Create, Read, Update, Delete) for managing students, courses, and their enrollments. The system is designed for **simplicity**, using **only SQL queries** executed directly from the MySQL CLI within an EC2 instance.



### Key Features:
- **Student Management**: Add, view, update, and delete student information.
- **Course Management**: Add, view, and update course details like course name and instructor.
- **Enrollment Management**: Enroll students in courses and track their enrollments.
- **Database Connectivity**: Uses **AWS RDS** for MySQL to securely store and manage data, with **AWS EC2** acting as the interface for querying and interacting with the database.

This system demonstrates the power of using cloud infrastructure to host and manage databases, especially focusing on the integration between EC2 (as a client) and RDS (as a managed database service). **MySQL CLI** is used for interaction with the database, allowing you to practice cloud database management without requiring any frameworks or programming languages.

---

## 🧱 Architecture

### **AWS EC2 (Elastic Compute Cloud)**:
- An EC2 instance is used to run the **MySQL CLI** to interact with the RDS database.
- The EC2 instance is in a **public subnet** within the VPC, which allows SSH access from the internet.

### **AWS RDS (Relational Database Service)**:
- The database is hosted on **AWS RDS MySQL** in a **private subnet** within the same VPC as EC2.
- **RDS** takes care of **automatic backups, patching**, and **scaling** without needing manual intervention.

### **Security Groups**:
- **EC2 Security Group**: Configured to allow SSH access (port 22) from your IP.
- **RDS Security Group**: Configured to allow MySQL connections (port 3306) from the **EC2 instance** only.

### **VPC (Virtual Private Cloud)**:
- Both EC2 and RDS reside within the same **VPC** to ensure secure and private communication between them.

---

## 🛠️ **Technologies Used**

- **AWS EC2**: For creating and managing the virtual machine to access MySQL.
- **AWS RDS**: For hosting the MySQL database securely.
- **MySQL CLI**: For executing SQL queries on the RDS database via EC2.
- **Security Groups**: For secure access configuration between EC2 and RDS.

---

## **Step-1**

  **Create EC2 Instance**
   

<img width="1440" alt="Screenshot 2025-04-20 at 9 09 32 PM" src="https://github.com/user-attachments/assets/415d0096-a6b9-4628-a0ed-75941fdae9c0" />

## **Step-2**

  **Create RDS Database**
   
<img width="1440" alt="Screenshot 2025-04-20 at 9 09 57 PM" src="https://github.com/user-attachments/assets/580401bd-2257-4645-ac08-8a1a7279f062" />

## **Step-3**

  **SSH into EC2 and install dependencies**

<img width="1440" alt="Screenshot 2025-04-20 at 9 14 46 PM" src="https://github.com/user-attachments/assets/f14159d1-ad9a-43d8-b934-34ceebbb7646" />

## **Step-4**

  **Login to RDS through Ec2**
  
<img width="898" alt="Screenshot 2025-04-20 at 9 16 47 PM" src="https://github.com/user-attachments/assets/04e48d4c-3688-4fd3-acba-41c8222ae03e" />

## **Step-5**

  **Download this commands file and start executing**
  
[📥 Download the Full Guide (ZIP)](https://github.com/SNS-Srinivasu/aws-student-course-management/raw/main/student_course_system_full_guide.zip)



## 💡 **How It Works**

1. **EC2 Setup**: An EC2 instance is provisioned with **SSH access** to connect and execute MySQL commands.
2. **RDS Setup**: A MySQL RDS instance is created and configured to store the database for students, courses, and enrollments.
3. **Database Connection**: EC2 connects to RDS using the **MySQL CLI** over a private network, ensuring secure data transfers.
4. **CRUD Operations**: SQL queries are run directly via MySQL CLI to:
   - Add, update, or delete student and course records.
   - View enrollments and course details.
5. **Security**: Both the EC2 instance and RDS are tightly controlled using security groups to restrict public access and enforce safe communication.

---

## 📂 **Files Included**
- **MySQL Queries**: A set of SQL commands to create tables, insert data, and run basic queries for managing students, courses, and enrollments.
- **EC2 Instance Setup Guide**: Instructions on setting up your EC2 instance and connecting to RDS.
- **RDS Instance Setup Guide**: Detailed steps for creating and configuring an RDS instance.

---

This project serves as an excellent starting point for understanding how to use **cloud services** for **database management** and can be easily expanded with additional features such as user authentication or more complex queries.

Feel free to clone, experiment, and extend this project as needed!
