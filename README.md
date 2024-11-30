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
## Based on your nature of role, please follow the below steps:

### Administrator

1) Admin Packs the npm Package
  - Admin Identifies the specific version of all the npm packages to be used in the project, consulting with Development Lead and Project Manager (PM).
  - Admin opens this repository in local or in cloud code-space ```must have terminal access```
  - runs ```npm pack``` command ex: ```npm pack react@17.0.1``` The pack command must include the specific version
  - This generates a ```.tgz``` file like ```react-17.0.1.tgz```.
2) Commits the code to repository
  - Stage the new package ```git add .```
  - Commit the code ex:```git commit -m "npm: react@18.3.1 add"``` the commit message should be follow the before mentioned commit message standard for better understanding of commit history
  - Push the code ```git push```







