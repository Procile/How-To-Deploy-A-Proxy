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
<div class="container">
  <form>
    <h2>Login</h2>
    <label for="username">Username</label>
    <input type="text" id="username" name="username" placeholder="Enter your username">
    <label for="password">Password</label>
    <input type="password" id="password" name="password" placeholder="Enter your password">
    <button type="submit">Login</button>
  </form>
  <div class="wave"></div>
  <div class="light"></div>
</div>


CSS :
.container {
  max-width: 600px;
  margin: 0 auto;
  padding: 50px 30px;
  background-color: rgba(0, 0, 0, 0.7);
  border-radius: 10px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
  position: relative;
  overflow: hidden;
}

.wave {
  position: absolute;
  top: calc(100% - 5px);
  left: 0;
  width: 100%;
  height: 150px;
  transform: translateZ(0);
  z-index: -1;
}

.wave:before,
.wave:after {
  content: "";
  display: block;
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background-repeat: repeat-x;
}

.wave:before {
  background-image: url('https://s3-us-west-2.amazonaws.com/s.cdpn.io/85486/wave-top.png');
  transform: translateZ(0);
  animation: wave 25s linear infinite;
}

.wave:after {
  background-image: url('https://s3-us-west-2.amazonaws.com/s.cdpn.io/85486/wave-bottom.png');
  transform: translateZ(0);
  animation: wave 12s linear infinite;
}

@keyframes wave {
  0% {
    background-position-x: 0;
  }
  100% {
    background-position-x: 1440px;
  }
}

.light {
  position: absolute;
  top: -25px;
  left: -25px;
  right: -25px;
  bottom: -25px;
  background: radial-gradient(ellipse at center, rgba(255, 255, 255, 0.4) 0%, rgba(255, 255, 255, 0) 80%);
  z-index: -2;
  animation: flicker 3s ease-in-out infinite;
}

@keyframes flicker {
  0% {
    opacity: 0.8;
  }
  50% {
    opacity: 1;
  }
  100% {
    opacity: 0.8;
  }
}
