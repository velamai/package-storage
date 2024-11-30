# **VELAM npm Package Storage Registry (PSR)**  

![NPM](https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white)

The **VELAM npm Package Storage Registry (PSR)** is the organization’s centralized repository for storing and managing essential npm package `.tgz` files. It enables the team to consistently use specific versions of packages directly from GitHub, ensuring seamless and controlled dependency management across all projects.

---

## **How It Works**

### **1. Admin Prepares Packages:**
- Download and store `.tgz` files for specific package versions in this GitHub repository.
  
### **2. Team Installs Directly from GitHub:**
- Use GitHub raw URLs in `package.json` to ensure `npm install` fetches the correct package version.

#### **Reference Example:**
```json
{
  "dependencies": {
    "react": "https://raw.githubusercontent.com/velam-org/package-storage/main/react-17.0.1.tgz"
  }
}
