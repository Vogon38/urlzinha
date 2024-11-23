# **URLzinha**

This repository serves as the main project for **Urlzinha**, a URL shortener application. It combines two microservices as Git submodules:
1. [**URL Generation**](https://github.com/Vogon38/urlzinha-generate-url-rocketseat): Handles the creation of shortened URLs.
2. [**URL Redirection**](https://github.com/Vogon38/urlzinha-redirect-url-rocketseat): Manages redirection based on the shortened URLs.

---

## **Context**
**URLzinha** is designed as a microservices architecture to demonstrate practical integration of AWS services. Each subproject has its own repository and purpose:
- **URL Generation**: Provides a POST endpoint to generate shortened URLs with an expiration time.
- **URL Redirection**: Offers a GET endpoint to redirect users to the original URL or return an error if expired.

---

## **Technologies**
- **Language**: Java (AWS SDK v2, Jackson)
- **AWS Services**: Lambda, S3, API Gateway
- **Version Control**: Git submodules

---

## **How to Work with Submodules**

### **Cloning the Repository**
To clone this repository and initialize the submodules:
```bash
git clone https://github.com/Vogon38/urlzinha.git
cd urlzinha
git submodule update --init --recursive
```

### **Updating Submodules** ###
If the submodules have been updated, you can pull the latest changes:
```bash
git submodule update --remote
```

### **Committing Submodule Changes** ###
When the submodules are updated, add and commit the changes in the main repository:
```bash
git add .
git commit -m "Updated submodules"
git push origin main
```

### **Working on Submodules** ###
You can navigate into the submodule directories and work on the projects individually:
```bash
cd url-generation
# Make changes
git add .
git commit -m "Your changes"
git push origin main
cd ../url-redirection
# Make changes
git add .
git commit -m "Your changes"
git push origin main
```

### **Acknowledgments** ###
This project was developed as part of a course offered by [RocketSeat](https://www.rocketseat.com.br).
It demonstrates the integration of AWS services with microservices architecture.