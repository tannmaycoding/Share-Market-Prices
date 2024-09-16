# Share-Market-Prices
This gives you historical prices of an NSE share. It is different from Share-Market-Prices-v2 because:
- More functionalities
   - Log In
   - Sign Up
   - Try as a guest
   - Has a database of MySQL to store the store credentials of Sign Up and use them for Log In

- Is not on **Streamlit Community Cloud**
   - This is because I wasn't able to upload on **Streamlit Community Cloud** :disappointed:

The working: 
1. Opens the landing page
2. When you press `Sign Up`:
   - Opens `pages/page_2.py`
   - In `pages/page_2.py`:
     1. Has input fields for username, email, password
     2. When you press `Sign Up`
        - Opens `share-market-login` table from database `accounts` on engine `engine`
        - Checks if there is `` ` `` in username
        - Checks if username exists
        - Checks if password exists
        - If any check is false it shows error of its own
        - When all checks are done successfully, credentials are added to the SQL table and we are redirected to `pages/page_3.py`
3. When you press `Log In`:
   - Opens `pages/page_1.py`
   - In `pages/page_1.py`:
      1. Has input fields for username or email, password
      2. When you press `Log In`: 
        - Opens `share-market-login` table from database `accounts` on engine `engine`
        - Checks if username or email exists
        - Checks if the password of the corresponding username or email is correct
        - If any check is false it shows error of its own
        - If all checks are done successfully, it will redirect to `pages/page_3.py`
