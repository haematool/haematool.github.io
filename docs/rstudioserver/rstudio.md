<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">

# R Studio Server v0.1beta

**The server is set up to assist with statistical analyses on medical data.**


## I. Access to R Server

!!! success "**You can access the server with the following link :**"

    <div style="text-align: center; margin: 20px 0;">
      <a href="http://134.209.84.93:8787/" target="_blank" style="padding: 10px 20px; background-color: #607D8B; color: white; text-decoration: none; border-radius: 5px; font-family: Arial, sans-serif; font-size: 16px;">
        <i class="fas fa-server"></i> Access R Studio Server
      </a>
    </div>

    <div style="text-align: center; margin-bottom: 20px;">
      <span id="status-indicator" style="display: inline-block; width: 10px; height: 10px; background-color: #4CAF50; border-radius: 50%; margin-right: 8px;"></span>
      <span id="status-text" style="font-family: Arial, sans-serif; color: #4CAF50;">Server is online</span>
    </div>

---

## II. Request Access

If you'd like to request the ID and password for the R Studio server, please fill out the form below:

<form action="https://fabform.io/f/SgfCSO0" method="POST" enctype="multipart/form-data" style="width: 100%; max-width: 600px; padding: 20px; background-color: #263238; border-radius: 6px; box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); box-sizing: border-box; margin: auto;">
  
  <div style="margin-bottom: 15px; display: flex; flex-wrap: wrap; align-items: center;">
    <i class="fas fa-user" style="font-size: 20px; color: #b0bec5; margin-right: 10px; min-width: 30px; text-align: center;"></i>
    <label for="name" style="font-size: 16px; font-weight: 500; color: #eceff1; flex: 1 1 100%;">Full Name:</label>
    <input type="text" id="name" name="name" required style="flex: 1 1 100%; padding: 8px; border: 1px solid #546e7a; border-radius: 4px; background-color: #37474f; color: #eceff1; margin-top: 10px;">
  </div>
  
  <div style="margin-bottom: 15px; display: flex; flex-wrap: wrap; align-items: center;">
    <i class="fas fa-envelope" style="font-size: 20px; color: #b0bec5; margin-right: 10px; min-width: 30px; text-align: center;"></i>
    <label for="email" style="font-size: 16px; font-weight: 500; color: #eceff1; flex: 1 1 100%;">Email:</label>
    <input type="email" id="email" name="email" required style="flex: 1 1 100%; padding: 8px; border: 1px solid #546e7a; border-radius: 4px; background-color: #37474f; color: #eceff1; margin-top: 10px;">
  </div>

  <div style="margin-bottom: 15px; display: flex; flex-wrap: wrap; align-items: center;">
    <i class="fas fa-building" style="font-size: 20px; color: #b0bec5; margin-right: 10px; min-width: 30px; text-align: center;"></i>
    <label for="institution" style="font-size: 16px; font-weight: 500; color: #eceff1; flex: 1 1 100%;">Institution/Organization:</label>
    <input type="text" id="institution" name="institution" required style="flex: 1 1 100%; padding: 8px; border: 1px solid #546e7a; border-radius: 4px; background-color: #37474f; color: #eceff1; margin-top: 10px;">
  </div>
  
  <div style="margin-bottom: 15px; display: flex; flex-wrap: wrap; align-items: flex-start;">
    <i class="fas fa-comment-alt" style="font-size: 20px; color: #b0bec5; margin-right: 10px; min-width: 30px; text-align: center;"></i>
    <label for="reason" style="font-size: 16px; font-weight: 500; color: #eceff1; flex: 1 1 100%;">Short Description:</label>
    <textarea id="reason" name="reason" required style="flex: 1 1 100%; padding: 8px; border: 1px solid #546e7a; border-radius: 4px; background-color: #37474f; color: #eceff1; margin-top: 10px; height: 100px;"></textarea>
  </div>

  <div style="margin-bottom: 15px; display: flex; flex-wrap: wrap; align-items: center;">
    <i class="fas fa-file-upload" style="font-size: 20px; color: #b0bec5; margin-right: 10px; min-width: 30px; text-align: center;"></i>
    <label for="file" style="font-size: 16px; font-weight: 500; color: #eceff1; flex: 1 1 100%;">Upload File (Optional):</label>
    <input type="file" id="file" name="file" style="flex: 1 1 100%; padding: 8px; border: 1px solid #546e7a; border-radius: 4px; background-color: #37474f; color: #eceff1; margin-top: 10px;">
  </div>
  
  <div style="text-align: right;">
    <input type="submit" value="Request Access" style="background-color: #455a64; color: white; padding: 10px 16px; border: none; border-radius: 4px; cursor: pointer; font-size: 16px; font-weight: 500;">
  </div>
</form>


---

## III. Documentation

### R Studio Server Guide <i class="fas fa-book"></i>

Welcome to the R Studio Server! This document explains how to access and use the R Studio server for your data analysis and statistical needs.

---

### 1. Accessing the Server <i class="fas fa-laptop-code"></i>

To access the R Studio server, follow these steps:

1. Open your web browser and navigate to the following link:
   - [R Studio Server](http://134.209.84.93:8787)
2. You will be directed to the login page (if required).

> **Note:** You must have an account and login credentials to access the server. If you don't have access, please use the aforementioned request form.

---

### 2. Login and Authentication <i class="fas fa-key"></i>

1. Enter your **username** and **password**.
2. Click on **Sign In**.
3. If your login is successful, you will be redirected to the R Studio interface.

> **Tip:** If you forgot your password, please [contact support](#support-and-contact).

---

### 3. Navigating the Interface <i class="fas fa-project-diagram"></i>

Once logged in, you'll see the R Studio interface split into four main panels:

#### Main Panels:

1. **Source Panel** (top-left): This is where you write and edit R scripts.
2. **Console Panel** (bottom-left): The interactive console where you can run R commands.
3. **Environment/History Panel** (top-right): View data objects, variables, and command history.
4. **Files/Plots/Packages/Help Panel** (bottom-right): Manage files, view plots, manage packages, and access help resources.

#### Writing and Running Code

- To run a line of code or a script:
  1. Write your R code in the **Source** panel.
  2. Press `Ctrl + Enter` (Windows/Linux) or `Cmd + Enter` (Mac) to run the current line or selection.
  3. Check the **Console** panel for output and any error messages.

---

### 4. Working with Projects <i class="fas fa-folder-open"></i>

Creating and managing projects in R Studio helps organize your work:

1. To create a new project:
   - Go to `File` -> `New Project`.
   - Choose whether to create a project from a new directory, an existing directory, or a Git repository.
2. Name the project and select its directory.
3. Click **Create Project** to open the new project in R Studio.

---

### 5. Installing Packages <i class="fas fa-box"></i>

You can install R packages to extend the functionality of R Studio:

1. In the **Console** panel, type the following command to install a package:
   ```r
   install.packages("package_name")
   ```
2. To load a package into your environment, use:
   ```r
   library(package_name)
   ```
3. You can also install packages from the **Packages** tab in the bottom-right panel by searching for the package name and clicking **Install**.

---

### 6. Uploading and Managing Data <i class="fas fa-upload"></i>

You can upload datasets directly to the R Studio server:

1. In the **Files** tab (bottom-right), click on **Upload**.
2. Choose the file you want to upload from your local machine.
3. The uploaded file will now appear in your file system and can be accessed in your R scripts.

To read a CSV file into R, use:
```r
data <- read.csv("your_file.csv")
```

---

### 7. Saving and Exporting Results <i class="fas fa-save"></i>

- To save your R script, go to `File` -> `Save As`, and choose the directory.
- To export a plot:
  1. Go to the **Plots** panel.
  2. Click **Export** and choose to save the plot as a PDF, PNG, or other formats.

---

### 8. Best Practices <i class="fas fa-check-circle"></i>

- **Project organization:** Always create a new project for each analysis to avoid clutter.
- **Save your work frequently:** Make sure to save scripts and data regularly.
- **Version control:** Use Git for version control to track changes to your scripts.

---

### 9. Troubleshooting <i class="fas fa-bug"></i>

#### Common Issues

- **Package not installing:** Check the console for error messages. It may be due to missing dependencies.
- **Slow performance:** Large datasets or heavy computations may slow down the server. Try to simplify your code or break tasks into smaller parts.

---

### 10. Support and Contact <i class="fas fa-life-ring"></i>

If you are encountering issues, feel free to contact us.

- **Email:** [emmanuelsleiman@gmail.com](mailto:emmanuelsleiman@gmail.com)
- **LinkedIn:** [Emmanuel Sleiman](https://fr.linkedin.com/in/emmanuel-sleiman-0354272b4)

---

This concludes the guide to using the R Studio server. We hope this document helps you get the most out of the platform!

