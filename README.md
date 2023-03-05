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

HTML :
<form>
  <h1>Space Login</h1>
  <div class="form-group">
    <label for="username">Username:</label>
    <input type="text" id="username" name="username" placeholder="Enter your username">
  </div>
  <div class="form-group">
    <label for="password">Password:</label>
    <input type="password" id="password" name="password" placeholder="Enter your password">
  </div>
  <button type="submit">Login</button>
</form>

CSS :
form {
  width: 400px;
  margin: 0 auto;
  padding: 30px;
  background: #00171f;
  color: #fff;
  font-family: Arial, sans-serif;
  border-radius: 10px;
  box-shadow: 0px 0px 30px rgba(255, 255, 255, 0.1);
  transform: translateY(-20px);
  transition: all 0.3s ease-in-out;
}

form:hover {
  transform: translateY(-10px);
  box-shadow: 0px 0px 40px rgba(255, 255, 255, 0.2);
}

h1 {
  text-align: center;
  font-size: 36px;
  margin-bottom: 30px;
}

.form-group {
  position: relative;
}

label {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  left: 20px;
  font-size: 20px;
}

input[type="text"], input[type="password"] {
  width: 100%;
  padding: 10px 20px;
  border-radius: 5px;
  border: none;
  background: #3c4d5a;
  color: #fff;
  font-size: 16px;
  font-weight: 300;
  box-shadow: none;
}

input[type="text"]:focus, input[type="password"]:focus {
  outline: none;
  box-shadow: none;
}

button[type="submit"] {
  display: block;
  width: 100%;
  padding: 10px;
  border-radius: 5px;
  border: none;
  background: #3ca8c8;
  color: #fff;
  font-size: 16px;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.3s ease-in-out;
}

button[type="submit"]:hover {
  background: #31859b;
}
