## 📘 AWS S3 Static Website Hosting – Project Documentation

### 🧩 Overview

This project demonstrates how to **host a static website** on **Amazon S3 (Simple Storage Service)**. The website consists of two HTML pages — `index.html` and `form.html` — that navigate between each other. AWS S3 is used to store and deliver the web content over the internet using static hosting capabilities.

---

### 🗂️ Project Structure

```
/s3-static-website/
│
├── index.html
├── form.html
└── README.md
```

* **index.html** – The homepage of the website.
* **form.html** – A simple form page linked from the index page.

---

### 🌐 Steps to Host Website on Amazon S3

#### **1. Create an S3 Bucket**

1. Log in to the **AWS Management Console**.
2. Navigate to **S3 Service** → click **Create Bucket**.
3. Enter a **unique bucket name** (e.g., `my-static-web-demo`).
4. Choose a region (e.g., `Asia Pacific (Mumbai)`).
5. **Uncheck “Block all public access”** → Confirm by acknowledging the warning.
6. Click **Create bucket**.

---

#### **2. Upload Website Files**

1. Open your newly created bucket.
2. Click **Upload** → Add your `index.html` and `form.html` files.
3. Click **Upload** to finish.

---

#### **3. Set Bucket Policy (Public Access)**

To make your site public, apply a bucket policy.

1. Go to **Permissions** → **Bucket Policy**.
2. Paste this policy (replace *your-bucket-name* with your actual bucket name):
3. Save changes.

---

#### **4. Enable Static Website Hosting**

1. Go to the **Properties** tab of your bucket.
2. Scroll down to **Static website hosting**.
3. Choose **Enable**.
4. Set the fields:

   * **Index document:** `index.html`
   * **Error document:** `form.html` *(optional)*
5. Click **Save changes**.

You’ll now get a **Bucket Website Endpoint** like:

```
http://your-bucket-name.s3-website.ap-south-1.amazonaws.com
```

---

#### **5. Test Your Website**

* Open the **Endpoint URL** in your browser.
* You should see your `index.html` page.
* Ensure navigation between `index.html` ↔ `form.html` works.

---

### 🧠 Example HTML Files

**index.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Home Page</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f9fafb;
      text-align: center;
      padding: 50px;
    }
    h1 {
      color: #333;
    }
    a, button {
      display: inline-block;
      margin-top: 20px;
      padding: 10px 20px;
      text-decoration: none;
      background-color: #007BFF;
      color: white;
      border-radius: 5px;
      border: none;
      cursor: pointer;
    }
    a:hover, button:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>
  <h1>Welcome to My Website</h1>
  <p>This is the home page.</p>

  <!-- Link to navigate to the form page -->
  <a href="form.html">Go to Form</a>
</body>
</html>

```

**form.html**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Form Page</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f9fafb;
      text-align: center;
      padding: 50px;
    }
    form {
      background-color: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      display: inline-block;
    }
    input {
      width: 90%;
      padding: 8px;
      margin: 8px 0;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    button, a {
      display: inline-block;
      margin-top: 15px;
      padding: 10px 20px;
      text-decoration: none;
      background-color: #007BFF;
      color: white;
      border-radius: 5px;
      border: none;
      cursor: pointer;
    }
    a:hover, button:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>
  <h1>Registration Form</h1>

  <form>
    <input type="text" name="name" placeholder="Enter your name" required><br>
    <input type="email" name="email" placeholder="Enter your email" required><br>
    <button type="submit">Submit</button>
  </form>

  <br>
  <!-- Link to go back to home page -->
  <a href="index.html">Back to Home</a>
</body>
</html>

```

---

### 🚀 Outcome

✅ Successfully hosted a **static website** on **Amazon S3**.
✅ Accessible via public S3 **website endpoint**.
✅ Demonstrates **HTML navigation** between multiple pages.

---

### 🏷️ Hashtags (for LinkedIn Post)

#AWS #S3 #StaticWebsite #CloudComputing #WebHosting #DevOps #AWSProjects #HTML #Frontend #CloudLearning
