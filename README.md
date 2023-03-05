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
  background: #141b29;
  height: 100vh;
  font-family: 'Roboto', sans-serif;
  overflow: hidden;
}

.stars {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  background: url('https://i.imgur.com/1TsDPn3.png') repeat;
  animation: animateStars 20s linear infinite;
}

@keyframes animateStars {
  0% {
    background-position: 0 0;
  }
  100% {
    background-position: 100% 100%;
  }
}

.box {
  position: relative;
  width: 400px;
  height: 500px;
  margin: 0 auto;
  margin-top: 60px;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 10px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 0 15px rgba(255, 255, 255, 0.1);
}

.form {
  position: absolute;
  inset: 20px;
  border-radius: 8px;
  background: rgba(0, 0, 0, 0.6);
  z-index: 10;
  padding: 50px;
  display: flex;
  flex-direction: column;
}

.form h2 {
  color: #fff;
  font-weight: 500;
  text-align: center;
  letter-spacing: 0.1mm;
  margin-bottom: 30px;
}

.inputBox {
  position: relative;
  width: 100%;
  margin-bottom: 20px;
}

.inputBox input {
  position: relative;
  width: 100%;
  padding: 20px 10px 10px;
  background: transparent;
  border: none;
  outline: none;
  color: #fff;
  font-size: 1em;
  letter-spacing: 0.05em;
  z-index: 10;
}

.inputBox span {
  position: absolute;
  left: 0;
  padding: 20px 0px 10px;
  font-size: 1em;
  color: #fff;
  pointer-events: none;
  letter-spacing: 0.05em;
  transition: 0.5s;
}

.inputBox input:valid ~ span,
.inputBox input:focus ~ span {
  color: #969696;
  transform: translateX(0px) translateY(-34px);
  font-size: 0.75em;
}

.inputBox i {
  position: absolute;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 2px;
  background: #fff;
  border-radius: 4px;
  transition: 0.5s;
  pointer-events: none;
  z-index: 9;
}

.inputBox input:valid ~ i,
.inputBox input:focus ~ i {
  height: 44px;
}

input[type="submit"] {
  border: none;
  outline: none;
  background: #6670f0;
  padding: 11px 25px;
  width: 100px;
  color: #fff;
  font-size: 1em;
  font-weight: 500;
  border-radius: 25px;
  margin-top: 20px;
  cursor
