# Static Website with AWS S3, GitHub Actions, and Netlify

This project demonstrates how to deploy a static website using **AWS S3**, **GitHub Actions**, and **Netlify** to enable a seamless Continuous Integration and Continuous Deployment (CI/CD) pipeline. We also explore why **Netlify** was chosen over Cloudflare and S3 directly for hosting.

## Project Overview

This project automates the deployment of a static website through the following process:

1. **GitHub Actions**: Automates the deployment pipeline when changes are made to the GitHub repository.
2. **AWS S3**: Hosts the static files (HTML, CSS, etc.) of the website.
3. **Netlify**: Simplifies deployment and automatically provides HTTPS, enabling a secure connection to the website.
4. **CI/CD Workflow**: Every time you push changes to the GitHub repository, **GitHub Actions** ensures that the website is deployed automatically to **Netlify** for public access.

### Tools Used:

* **GitHub Actions**: To automate deployment whenever changes are pushed to the GitHub repository.
* **AWS S3**: Used for hosting the static files of the website.
* **Netlify**: Provides seamless integration for deploying the website with automatic HTTPS support and continuous deployment.
* **Cloudflare**: Initially considered for DNS management and HTTPS, but ultimately not required for the free deployment flow with **Netlify**.

## Steps We Followed

### 1. **Create a Static HTML Site**

We began by designing a simple static HTML site using basic HTML and CSS to demonstrate the deployment. The structure consisted of:

* `index.html`
* `style.css`
* `README.md`

### 2. **Set Up GitHub Actions for CI/CD**

* We created a GitHub repository to store the website files.
* We configured a GitHub Actions workflow that syncs the changes made to the repository with **Netlify** (via the API), so whenever a commit is pushed to the `main` branch, the website is updated automatically.

### 3. **Deployment to Netlify**

* We connected the GitHub repository to **Netlify** for hosting the static files.
* **Netlify** provides automatic HTTPS via SSL certificates, ensuring that the website has a secure connection.
* After connecting the repository to Netlify, the website was live on a custom subdomain provided by Netlify (`<your-site-name>.netlify.app`).

### 4. **Choosing Netlify Over AWS S3 + Cloudflare**

* We initially explored using **AWS S3** and **Cloudflare** for hosting the website.
* However, **Netlify** was chosen as a more streamlined solution due to its built-in features like:

  * Automatic HTTPS (SSL).
  * Simple deployment via GitHub.
  * Free tier for personal projects.
  * Easy custom domain management.

### 5. **Custom Domain**

* Although Cloudflare was initially considered for managing DNS and connecting a custom domain, it was not required with **Netlify**. Netlify handles the custom domain and SSL certificate seamlessly, simplifying the setup.

### 6. **Final Website URL**

* The final static website is deployed on **Netlify** with the URL:
  [https://pavithra-static-app.netlify.app](https://pavithra-static-app.netlify.app).

### 7. **Live Demo**

* You can visit the live demo of the website here:
  [https://pavithra-static-app.netlify.app](https://pavithra-static-app.netlify.app).
  
### 8. **Explanation Video**


## Key Features

* **Automatic Deployment**: Every change pushed to GitHub triggers an automatic deployment to Netlify via **GitHub Actions**.
* **Secure Connection (HTTPS)**: The website is served securely over HTTPS with SSL certificates automatically provided by **Netlify**.
* **Continuous Integration and Continuous Deployment (CI/CD)**: No manual intervention is required. Once a commit is made to GitHub, the website updates automatically.

## Deliverables

* **GitHub Actions CI/CD Workflow**: Automates the deployment process.
* **Cloudflare + S3 Integration Steps**: Although **Cloudflare** and **S3** were initially planned for DNS and hosting, **Netlify** was used instead for easier setup and features.
* **Live Website Link with HTTPS**: Available at [https://pavithra-static-app.netlify.app](https://pavithra-static-app.netlify.app).
* **Screenshot & Deployment Report**: Screenshots of the live website and deployment steps are included as part of the documentation.

## Conclusion

In this project, we learned how to automate the deployment of a static website with GitHub Actions, AWS S3, and **Netlify**. Although we initially considered using **Cloudflare** and **S3** for hosting, we switched to **Netlify** due to its ease of use and built-in features such as automatic HTTPS and continuous deployment from GitHub.
