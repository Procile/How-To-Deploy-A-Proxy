# Get A Domain -
### If you haven't already, get a domain :
##### PorkBun : https://porkbun.com/
##### FreeNom : https://freenom.com/ (currently not working)

# Add It To Cloudflare -
(skip this step if you don't plan on adding a custom domain)
(for this demonstration i'm going to be using freenom)
##### So first add the nameservers that cloudfare gives you
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-03%207.09.26%20PM.png)
##### into your domain's nameservers (delete the old ones)
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-03%207.11.45%20PM.png)

# Deploy On Render
##### Go to your dashboard, and make a new web service
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-03%207.20.38%20PM.png)
##### Add the github proxy repo that you want to host (i'm going to use hypertabs) then press continue
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-03%207.26.07%20PM.png)
##### Make sure your runtime is set to "Node" Your Build Command to "npm install" Your Start Command to "npm start"
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-03%207.28.40%20PM.png)
##### Press Create Web Service at the bottom
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-03%207.31.40%20PM.png)
##### Wait until it finishes building
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-03%207.33.19%20PM.png)
##### Once Done it should look like this
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-03%207.36.59%20PM.png)
##### (You should have recived a domain from render, if you want to add a custom one go to the next step)
# Custom Domain
##### On the web service dashboard go to settings
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-04%2010.51.39%20AM.png)
#### Look for "Custom Domain"
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-04%2010.55.57%20AM.png)
##### Add your Custom Domain 
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-04%2010.57.33%20AM.png)
##### You should see the records render gives you
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-04%2010.58.18%20AM.png)
##### Go To Cloudflare and Setup the records render gives you
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-04%2010.59.33%20AM.png)
##### Set SSL/TLS to "Full"
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-04%2011.00.42%20AM.png)
##### Go Back To render and click on verify, and you should see them like this :
![](https://github.com/TheNearEnd/How-To-Deploy-A-Proxy/blob/main/images/Screenshot%202023-03-04%2011.04.01%20AM.png)
###### You Might have to wait sometime
# Done

<!DOCTYPE<!DOCTYPE html>
<html>
  <head>
    <title>Login</title>
    <style>
      body {
        background-color: #0a192f;
        font-family: Arial, sans-serif;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
      }
      h2 {
        color: #ffffff;
        text-align: center;
        margin-bottom: 30px;
      }
      form {
        background-color: #2b2d42;
        width: 400px;
        margin: 0 auto;
        padding: 30px;
        border-radius: 10px;
        box-shadow: 0px 0px 10px #cccccc;
      }
      label {
        display: block;
        margin-bottom: 10px;
        color: #ffffff;
        font-size: 14px;
      }
      input[type="text"], input[type="password"] {
        padding: 10px;
        width: 100%;
        border-radius: 5px;
        border: none;
        background-color: #1d1f2f;
        color: #ffffff;
        margin-bottom: 20px;
      }
      input[type="text"]::placeholder, input[type="password"]::placeholder {
        color: #ffffff;
      }
      input[type="submit"] {
        background-color: #e0e1dd;
        color: #000000;
        padding: 10px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        width: 100%;
        font-size: 14px;
        font-weight: bold;
        letter-spacing: 1px;
        transition: background-color 0.3s ease-in-out;
      }
      input[type="submit"]:hover {
        background-color: #ffffff;
      }
    </style>
  </head>
  <body>
    <h2>Login to Space Portal</h2>
    <form action="your_login_script.php" method="post">
      <label for="username">Username:</label>
      <input type="text" id="username" name="username" placeholder="Enter your username" required>
      <label for="password">Password:</label>
      <input type="password" id="password" name="password" placeholder="Enter your password" required>
      <input type="submit" value="Login">
    </form>
  </body>
</html>

