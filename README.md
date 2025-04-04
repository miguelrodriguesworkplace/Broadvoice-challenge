# Broadvoice-challenge

# User Creation Requirements and Test Cases

## 1. Questions to Clarify Requirements

- Are all fields of the user creation window mandatory?
- What happens when a mandatory field is left blank?
- What happens when the character length of a field is not between 6 to 30?
- What happens when the email field does not have an email format?
- Can the same email be used twice?
- What happens when a user with a first or last name with less than 6 characters tries to be created (e.g., John Doe)?
- Can the fields contain special characters?
- What information will the user have when invalid information is written?
- Which of the credentials (Email, First name, Last name) are needed to log in?
- How long is the temporary password valid?  
- Is the user redirected to a change password window when they log in the first time?
- What happens when the user creation takes longer than 3 seconds?
- Are the 3 seconds about the whole creation process or the email being sent/received?
- Are the allocated spaces on the database for the first and last name correct? (e.g., varchar(12) has a limit of 12 characters instead of 30)

## 2. Test Cases

### **User creation without information**

**Description:** Create a new user without filling the fields with information.

**Steps:**  
1. Open the User Creation window.  
2. Click on the save button without filling any field.  

**Expected Result:**  
A message should appear informing that all the mandatory fields should be filled.

---

### **Invalid email field**

**Description:** Create a new user with an incorrect email format.

**Steps:**  
1. Open the User Creation window.  
2. Fill the email field with an invalid email format (e.g., `usertestgmail.com`).  
3. Click on the save button.  

**Expected Result:**  
A message should appear informing that the email is in the wrong format.

---

### **Invalid name field**

**Description:** Create a new user with a First and Last name with less than 6 or more than 30 characters.

**Steps:**  
1. Open the User Creation window.  
2. Fill the first and last name fields with an invalid character length (less than 6 characters or more than 30).  
3. Click on the save button.  

**Expected Result:**  
A message should appear informing that the first and last names do not have the correct character length.

---

### **Valid user creation**

**Description:** Create a new user with information fulfilling the requirements (correct email format and character length).

**Steps:**  
1. Open the User Creation window.  
2. Fill all the fields with valid information. (correct email format and character length) 
3. Click on the save button.  

**Expected Result:**  
The user should receive an email with a temporary password to log in.

---

### **Successful login**

**Description:** Login with an already created user.

**Pre-condition:** The user is already created.

**Steps:**  
1. The user enters the correct credentials.  
2. The user clicks on login.  

**Expected Result:**  
The user is successfully logged in and is redirected to the home page with the user's email, first and last name visible.

---

### **User creation performance**

**Description:** Testing if the creation process takes no longer than 3 seconds.

**Steps:**  
1. Open the User Creation window.  
2. Fill all the fields with valid information.  
3. Click on the save button.  

**Expected Result:**  
The process should be completed within 3 seconds.
