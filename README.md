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


# Steps Based on Role

## For Administrators

### Package Preparation:
- Identify the required npm package versions in consultation with the Development Lead and Project Manager (PM).
- Open this repository locally or in a cloud code-space with terminal access.
- Run the following command to generate a `.tgz` file:

```bash
npm pack react@17.0.1
```

- This will generate a `.tgz` file like `react-17.0.1.tgz`.

### Commit and Push the Package:
- Stage the new package:

```bash
git add .
```

- Commit the changes using the standard commit message format:

```bash
git commit -m "npm: react@17.0.1 add"
```

- Push the changes to the repository:

```bash
git push
```

## For the Development Team

### Modify `package.json`:
- Use the following format to reference packages from the PSR:

```json
{
  "dependencies": {
    "react": "https://raw.githubusercontent.com/velam-org/package-storage/main/react-17.0.1.tgz"
  }
}
```

### Install Dependencies:
- Run `npm install` as usual to fetch packages from the GitHub repository:

```bash
npm install
```
