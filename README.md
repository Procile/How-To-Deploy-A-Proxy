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
  background: linear-gradient(to bottom, #0d1145, #0a0e34);
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Fredoka One', cursive;
  color: #d1d1e9;
  overflow: hidden;
  position: relative; /* added */
}

#stars {
  width: 1px;
  height: 1px;
  background-color: #fff;
  box-shadow: 0 0 2px #fff;
  position: absolute;
  top: 0;
  left: 0;
}

/* Add the following CSS for the star animations */

@keyframes twinkle {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}

#stars:after {
  content: " ";
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  animation: twinkle 1s infinite;
}

/* Add a container to hold multiple stars */
#stars-container {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1; /* make sure the stars are behind everything else */
}

/* Create a JavaScript function to add stars dynamically */
function createStar() {
  var star = document.createElement("div");
  star.classList.add("star");
  star.style.top = Math.random() * 100 + "%";
  star.style.left = Math.random() * 100 + "%";
  document.getElementById("stars-container").appendChild(star);
}

/* Call the createStar() function multiple times to add more stars */
for (var i = 0; i < 100; i++) {
  createStar();
}

JS :
<!DOCTYPE html>
<html>
  <link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fredoka+One&display=swap" rel="stylesheet">
<head>
  <title>Login</title>
  <link rel="stylesheet" type="text/css" href="style.css">
  <script src="script.js"></script>
  </script>
</head>
<body onload="popup()">
<div class="wave"></div>
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
      <input type="submit" value="login" form="login-form">
    </div>
  </div>
  <div id="popup">
    <p>Join the <a href="https://discord.gg/thingsnetwork">Things Network</a> and explore the world of Unblockers!</p>
  </div>
</body>
</html>

