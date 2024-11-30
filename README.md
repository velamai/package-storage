# VELAM npm Package Storage Registry (PSR)

![NPM](https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white)

This is orginization's central package storage registry. It contains all the essential package files. 

1) Admin Prepares Packages:
  - Download and store package ```.tgz``` files in this GitHub repository.
2) Team Installs Directly from GitHub:
  - Use GitHub raw URLs in ```package.json``` so ```npm install``` works seamlessly.

### 2.1 Reference
``` json
{
  "dependencies": {
    "react": "https://raw.githubusercontent.com/your-org/package-storage/main/react-17.0.1.tgz"
  }
}
```
