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
<!DOCTYPE html>
<html>
  <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fredoka+One&display=swap" rel="stylesheet">
<head>
  <title>Login</title>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body onload="popup()">
  <div class="box">
    <div class="form" action="#">
      <h2>Login</h2>
      <div class="inputBox">
        <input type="text" name="username" required>
        <span>Username</span>
        <i></i>
      </div>
      <div class="inputBox">
        <input type="password" name="password" id="password" required>
        <span>Password</span>
        <i></i>
      </div>
      <input type="submit" value="login">
    </div>
  </div>
  <div id="popup">
    <p>Join the <a href="https://discord.gg/thingsnetwork">Things Network</a> and explore the world of Unblockers!</p>
  </div>
</body>
</html>

CSS :
body {
  background: #0a0a0a;
  background-image: url("https://cdn.pixabay.com/photo/2020/02/23/15/00/ocean-4875542_1280.jpg");
  background-size: cover;
  background-position: center center;
  background-attachment: fixed;
  overflow: hidden;
  font-family: 'Open Sans', sans-serif;
}

.form-container {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 40px;
  border-radius: 10px;
  background-color: rgba(0, 0, 0, 0.8);
  box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.5);
}

.form-title {
  font-size: 2rem;
  font-weight: bold;
  color: #fff;
  text-align: center;
  margin-bottom: 40px;
}

.form-input {
  display: flex;
  flex-direction: column;
  margin-bottom: 20px;
}

.form-input label {
  font-size: 1.2rem;
  font-weight: bold;
  color: #fff;
  margin-bottom: 10px;
}

.form-input input {
  padding: 10px;
  border-radius: 5px;
  border: none;
  background-color: rgba(255, 255, 255, 0.2);
  color: #fff;
  font-size: 1.1rem;
  margin-bottom: 10px;
}

.form-input input:focus {
  outline: none;
  background-color: rgba(255, 255, 255, 0.4);
}

.form-button {
  display: flex;
  justify
