# 📌 Spotify API Testing with Postman

This project demonstrates end-to-end API testing of Spotify using Postman, covering authentication, playlist lifecycle, and edge case validation.

---

## 🚀 What This Project Does

- Implements OAuth 2.0 Authorization Code Flow  
- Automatically manages access & refresh tokens  
- Executes full playlist lifecycle:
  - Create playlist  
  - Add tracks  
  - Replace tracks  
  - Remove tracks  
- Validates responses using Postman test scripts  
- Handles negative and edge cases  

---

## ⚙️ How to Run Locally

### 1. Create Spotify App

Go to:
https://developer.spotify.com/dashboard

Steps:
1. Log in  
2. Click **Create App**  
3. Copy:
   - Client ID  
   - Client Secret  
4. Add Redirect URI:
https://oauth.pstmn.io/v1/callback

---

### 2. Generate Authorization Code

Open this URL (replace values):
https://accounts.spotify.com/authorize?client_id=YOUR_CLIENT_ID&response_type=code&redirect_uri=https://oauth.pstmn.io/v1/callback&scope=user-read-private%20playlist-modify-private


After login:
- You’ll get a `code` in the URL  
- Copy that code  

---

### 3. Configure Environment

Import the environment file into Postman and update:

client_id = YOUR_CLIENT_ID
client_secret = YOUR_CLIENT_SECRET
redirect_uri = https://oauth.pstmn.io/v1/callback
code = YOUR_AUTHORIZATION_CODE
base_url = https://api.spotify.com/v1

---

### 4. Run Collection

- Import the collection  
- Select the environment  
- Run using **Collection Runner**

---

## 🎥 Demo

[Watch Demo](assets/demo.mp4)

---

## 📂 Project Structure

collection/ → Postman collection
environment/ → Environment variables
assets/ → Demo + screenshots
README.md


---

## ⚠️ Notes

- Requires Spotify premium account  
- Tokens expire but are handled via refresh logic  

---

## 🧠 Key Learnings

- OAuth 2.0 authentication flow  
- Token lifecycle handling  
- Chained API testing  
- Automated validation using Postman scripts  
- Handling real-world API edge cases  