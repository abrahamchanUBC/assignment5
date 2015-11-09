# Assignment5

In this assignment we will focus on building the backend for the bookstore. You can clone the code from https://github.com/erkartik91/cpen400/ (as given in the previous assignment) to setup your own server on your local machine.

## Tasks
1. **Setup MySql Database:** You will need to install mysql on your laptop. You can find the instructions to install mysql [here](https://www.mysql.com). You will need to create the following tables for this assignment.
  ```
  products
  -- id (int) (auto increment)
  -- name (text)
  -- price (int)
  -- quanitity (int)
  -- image (text)
  
  orders
  -- id (int) (auto increment)
  -- cart (string)
  -- total (int)
  
  user
  -- id (int) (auto increment)
  -- token (text)
  
  ```

2. **Fetch products from database:** You can store the product information available at https://cpen400a.herokuapp.com/products into your own database. Follow [this](https://codeforgeek.com/2015/01/nodejs-mysql-tutorial) tutorial on how to connect to mysql from node.js to setup mysql connection in your node.js application. Once you have mysql connection setup correctly, you will need to update the /products endpoint to fetch the data from your database.

3. **Add Checkout functionality:** You will need to create a POST endpoint /checkout in your application. The end point will accept a json formatted object (cart) and total as parameters that you will store in your orders table. You will also need to update the JavaScript code in your web application to make this post request when user click on *checkout* button. This task is only considered complete when you have the checkout functionality working completely.

4. **Add authentication to AJAX calls:** Till now, all the AJAX calls that you made to your server had no authentication. However, to prevent misuse of your backend, you need to add authentication to your ajax calls. Any call to fetch product list or checkout should be accompained with a valid token. You can add some entries in your user table. You will then need to update both /products and /checkpoint endpoint to check for valid token in the request. For now, you can hard code the token from your user table in your JavaScript code. You will need to send token as one of the parameters with the ajax calls to both fetch product list and checkout cart. When you receive the reruest, you need to validate that token passed in the request exists in the user table. If there is no token or the token passed is invalid, you need to provide response with error code 401.


## Submission instructions:

* Add a folder called **assignment5** in your github repo.
* Make sure you push your changes before midnight (11:59 PM) before the day when assignment is due - late submissions will not be accepted.
* We will be downloading the code on the midnight before the due date, any changes to code after that point will not be considered for marking.

