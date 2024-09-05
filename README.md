# Host-a-Website-on-Amazon-S3

---

### Overview
Amazon S3 (Simple Storage Service) is used to store and retrieve any data online. In this project, I used Amazon S3 to host a static website by creating an S3 bucket and configuring Access Control Lists (ACLs) to make the content publicly accessible.

### How I Used Amazon S3
I created an S3 bucket to store my website files, including the HTML and image assets, and set up public access to host the site.

### Unexpected Discovery
I didn’t expect hosting a static website on Amazon S3 to be so simple! A few configurations were all it took to get everything running smoothly.

### Project Timeline
The entire process took about **30-35 minutes**, and creating the S3 bucket itself only took **3-5 minutes**.

### Steps to Set Up an S3 Bucket

1. **Region Selection**:  
   I chose the **US East (Ohio)** region for my bucket because it’s geographically close to Southern Canada, where I’m based.
   
2. **Bucket Name**:  
   S3 bucket names must be globally unique, so I ensured mine was original.
   
<img width="213" alt="Screenshot 2024-09-05 145026" src="https://github.com/user-attachments/assets/57694303-39fd-410b-9b54-51e7a53f5ade">

### Upload Website Files to S3

- **Files Uploaded**:
  1. `index.html` – the main HTML file for the site.
  2. A folder named `NextWork - Everyone should be in a job they love_files`, which contains 44 objects, including images, templates, and other essential files.
 
<img width="380" alt="Screenshot 2024-09-05 145149" src="https://github.com/user-attachments/assets/bf8cc007-6ea2-4c58-b780-248669f08cc1">

Both the HTML file and the folder are crucial for the proper display of the website.

### Static Website Hosting on S3

### Access Control Lists (ACLs)

An **Access Control List (ACL)** is a feature that allows you to manage who can control, access, and perform actions on the objects in your S3 bucket. By setting specific permissions, you can determine which users or groups have the ability to view, modify, or delete objects within the bucket.

#### Bucket Endpoints

<img width="305" alt="Screenshot 2024-09-05 145550" src="https://github.com/user-attachments/assets/8f697d11-8173-4be7-9f6c-88c3402aae67">

#### Error Handling

Initially, I encountered a **403 Forbidden** error when trying to visit the website's URL. The message was:

```
Error: Access Denied
Code: 403 Forbidden
Message: Access Denied
```

<img width="395" alt="Screenshot 2024-09-05 145435" src="https://github.com/user-attachments/assets/1ffa34be-7d16-4cde-b2ec-230ea2d5ae0c">

This happened because the default settings for the bucket's display options were set to private.

#### Resolution:
To fix this, I navigated to the **Object** section in my S3 bucket, selected the files, clicked on the **Action** button, and chose the **Make public using ACL** option. This allowed the content to be publicly accessible.

<img width="301" alt="Screenshot 2024-09-05 145707" src="https://github.com/user-attachments/assets/3ca92425-33d0-4225-9c01-3b44df6c7b33">

---

This project was a valuable learning experience in using Amazon S3 for static website hosting. Hosting static websites on S3 is quick, easy, and efficient with the right configurations!
