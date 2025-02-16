# **SUBVERSION**  

Subversion software is also known as **SVN**. It is an open-source version control system. Through Subversion, we can look at the previous version of a file and track the changes over time.  

## **Types of Version Control Systems**  

- **Centralized Version Control System (CVCS):** There is a single central server that stores all the versions.  
- **Distributed Version Control System (DVCS):** Each user has a copy of the full repository.  

## **Why Do We Use Version Control?**  

- To track all the changes and keep the history.  
- We can roll back to the previous version when needed.  
- We can merge new features.  

## **Installing & Setting up SVN on Windows**  

1. Download and install SVN (**TortoiseSVN**).  
2. After installation, restart your system.  
3. Verify the installation:  
   ```sh
   svn --version
   ```  

## **SVN Commands**  

### **Step 1: Initialize the Repository**  
```sh
svnadmin create ~/svn_repo/my_project
```  

### **Step 2: Checkout the Repository**  
```sh
svn checkout file:///path/to/svn_repo/my_project
```  

### **Step 3: Add Files to the Directory**  
- Navigate to your working directory.  
- Add new files.  
- Commit the changes.  

```sh
cd my_project
svn add file.txt
svn commit -m "Added file.txt"
```  

### **Step 4: Update Your Working Copy and View Logs**  
```sh
svn update
svn log
```  

### **Step 5: Reverting Changes**  
```sh
svn revert file.txt
```  

### **Step 6: Creating a Branch and Merging Changes**  
```sh
svn copy file:///C:/svn_repos/my_repo/trunk file:///C:/svn_repos/my_repo/branches/feature-branch -m "Creating feature branch"
svn merge file:///C:/svn_repos/my_repo/branches/feature-branch
```  

---

# **MERCURIAL (HG)**  

**Mercurial** is a **distributed version control system (DVCS)** designed for efficient handling of projects of all sizes. The functionality of Mercurial is similar to Git, but it emphasizes **simplicity and ease of use**. Mercurial is written in **Python** and is known for its **intuitive commands, robust performance, and cross-platform compatibility**.  

## **Features of Mercurial**  

- **Distributed Version Control:** Every developer has a full copy of the repository, enabling offline work and independent branching.  
- **Lightweight and Fast:** Efficient handling of large projects and binary files.  
- **Cross-Platform:** It works on Windows, macOS, and Linux.  
- **Extensible:** It supports plugins for additional functionality.  
- **Simple and Intuitive Commands:** Commands are easy to learn and use, with a consistent syntax.  

## **Installing & Setting up Mercurial on Windows**  

1. Download and install Mercurial (**TortoiseHg**).  
2. After installation, restart your system.  
3. Verify the installation:  
   ```sh
   hg --version
   ```  

## **Mercurial Commands**  

### **Step 1: Creating and Initializing the Repository**  
```sh
hg init my-hg-repo
```  

### **Step 2: Adding Files and Committing Changes**  
```sh
hg add file.txt
hg commit -m "Added newfile.txt"
```  

### **Step 3: Cloning, Updating, and Reverting**  
```sh
hg clone https://example.com/repo
hg pull
hg update
hg log
```  

### **Step 4: Branching and Merging**  
```sh
hg branch new-feature
hg merge
```  
