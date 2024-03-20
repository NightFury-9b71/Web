
<div align="center">

![JUST_LOGO](Jessore_University_of_Science_&_Technology_logo.jpg)

</div>

<h1 align="center"> Jashore University of Science and Technology </h1>

<h2 align="center" style="color:blue"> Department of Computer Science and Engineering </h2>


<div style="display:flex; flex-direction:column;justify-content:center;align-items:center">

<div>

#### Lab Report on Web development: Sample Login and Create account and  Dashboard 

</div>

<div>

| Submitted by                                          | Submitted to  
| :--------:                                            | :-------:     
| **Abdullah Al Noman**                                 | **Abu Rafe Md Jamil**              
| Student ID: 200107                                    | Lecturer            
| 3rd year 1st semester                                 | Department of Computer Science and  Engineering 
| Department of Computer Science and Engineering        | Jashore University of Science and  Technology              
| Jashore University of Science and  Technology         

</div>


**Remarks:**
Date of Submission: 20.03.2024 

</div>

# Login Form
![alt text](<Screenshot 2024-03-20 103443.png>)
##### HTML

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shob E Maya</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div id="intro">
        <h1 id="sitename"> Shob E Maya</h1>
        <p> Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tenetur, enim eos quidem voluptates natus incidunt. Numquam iste consectetur fugiat ratione rerum maxime, hic natus eligendi, officiis vitae totam atque nihil!</p>
    </div>

    <div id="form">
        <form action="dashboard.html" method="get">
            <input type="email" id="email" placeholder="Email Or Phone" autocomplete="on" required>
            <input type="password" id="password" placeholder="Password" required> 
            <div id="showpass"><input type="checkbox" name="" id="toogle" onclick="showhide()">Show Password</div>
            <input type="submit" value="Log in" id="login" onclick="loginnow()">
            <input type="button" value="Sign Up" id="signup" onclick='window.location.href = "create.html"'>
        </form>
    </div>

    <script>
        var x = document.getElementById("toogle");
        var y = document.getElementById("password")

        function showhide(){

            if(x.checked)
                y.type = "text";
            else
                y.type = "password"
            }

        document.getElementById("password").addEventListener("click",showhide());
    </script>
    
</body>
</html>
```

##### CSS
```
*{
    padding: 0;
    margin: 0;
}

body{
    background: linear-gradient(90deg,#2e70d3,white);		
    max-height: 100vh;
    display: flex;
    align-items: center;
    overflow: hidden;
}

#intro{
    height: 100vh;
    width: 40vw;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 5%;
    text-align: center;    
}

#sitename{
    font-size: 6vh;
    text-shadow: 13px 8px #0088cc;
}


#form{
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    width: 100%;
    border-top-left-radius: 100vw;
    border-bottom-right-radius:100vw ;
    box-shadow: 10px 5px 34px;
    background-color: rgb(124, 169, 221);
}

div form > *{
    border: 1px solid green;
    display: block;
    padding: 10px;
    margin: 10px;
    border-radius: 10px;
    width: 85%;
}

#showpass{
    padding: 0px;
    border: none;
}

#toogle{
    margin-right: 6px ;
}


#login,#signup{
    display: inline;
    width: 30%;
    padding: 10px 0px;
    color: white;
    background-color: #0088cc ;
    font-weight: bold;
}

div input:hover{
    box-shadow: 1px 2px 8px;
}

#login:hover,#signup:hover{
    box-shadow: 1px 2px 14px rgb(42, 116, 226);
}
```


# Registration Form
![alt text](<Screenshot 2024-03-20 103629.png>)

##### HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Account Creation</title>
    <link rel="stylesheet" href="createStyle.css">
</head>
<body>
    <h1> Create Account </h1>

    <div>
        <form action="" method="" id="details">
            <input type="text" id="fname" placeholder="First Name" autocomplete="on" required>
            <input type="text" id="lname" placeholder="Last Name" autocomplete="on" required>
            <input type="text" id="uname" placeholder="User Name" autocomplete="on" required>
            <input type="email" id="email" placeholder="Email" autocomplete="on" required>
            <input type="tel" id="phone" placeholder="Phone" autocomplete="on" required>
            <input type="password" id="pass" placeholder="Password" autocomplete="off" required>
            <input type="password" id="repass" placeholder="Retype Password" autocomplete="off" required>
            <input type="button" value="Sign Up" id="signup" onclick="alert('Operation Successfull'); window.history.back()">
            <input type="button" value="Cancel" id="cancel" onclick="window.history.back() ">
        </form>
    </div>

</body>
</html>
```
##### CSS

```
*{
    padding: 0px;
    margin: 0px;
}

body{
    background: linear-gradient(90deg,rgb(89, 118, 199),rgb(105, 200, 212));
    height: 100vh;
    overflow: hidden;
    max-width: 100vw;
}

h1{
    text-align: center;
    margin-top: 10vh;
    font-size: 6vh;
    text-shadow: 3px 3px #0088cc;
}

form{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

form input{
    padding: 10px;
    margin: 10px;
    border-radius: 10px;
    width: 40%;
    max-width: 170px;
}

#signup,#cancel{
    background: #0088cc;
    font-weight: bold;
    color: white;
}

#signup:hover{
    box-shadow: 1px 2px 24px;
}

#cancel{
    background: red;
}

#cancel:hover{
    box-shadow: 1px 2px 24px red;
}

div input:hover{
    box-shadow: 1px 2px 8px ;
}

```

# Dashboard
![alt text](<Screenshot 2024-03-20 103607.png>)

##### HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Waiting+for+the+Sunrise&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="dashstyle.css">
</head>
<body>
    <div id = "menu">
        <button> Dashboard </button>
        <button> Profile </button>
        <button> Status </button>
        <button onclick="window.history.back()"> Log Out</button>
    </div>

    <div id="details">

        <h1> Shob E Maya </h1>

        <img src="maya.png" alt="ShobEMaya" id="maya">

    </div>
    
</body>
</html>
```
##### CSS
```
*{
    padding: 0;
    margin: 0;
}

body{
    display: flex;
    align-items: center;
    height: 100vh;
    overflow: hidden;
}

#menu{
    height: 50%;
    width: 20%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

#menu > *{
    padding: 2%;
    margin : 1%;
    background: none;
    border: none;
    font-family: "Waiting for the Sunrise", cursive;
    font-size: large;
    width: 80%;

}

#menu > *:hover{
    background: #0088cc;
    border-radius: 10px;
    color: white;
    font-weight: bold;
    box-shadow: 1px 2px 24px rgb(54, 106, 202);
    font-size: x-large;
}

#details{
    height: 100vh;
    width: 80%;
    background: linear-gradient(90deg,white,#0088cc);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

h1{
    text-align: center;
    font-size: 5vw;
    text-shadow: 3px 3px #0088cc;
    font-family: "Waiting for the Sunrise", cursive;
    animation: rad 3s linear infinite,glow 0.6s ease-in-out infinite alternate,glowt 0.5s ease-in-out infinite alternate;
    box-shadow: 2px 2px 34px rgb(212, 203, 69);
    border-radius: 50%;
    white-space: nowrap;
}

#maya{
    animation: up-down 3s linear infinite;
    position: relative;
    max-width: 50vw;
    max-height: 50vw;
}

@keyframes up-down{
    0% {top:0px;}
    24% {top:20px;}
    50% {top:50px;}
    74% {top:20px;}
    100% {top:0px}
  }

@keyframes rad{
    0%{padding: 0px 0px;}
   20%{padding: 0px 30px;}
   50%{padding: 0px 70px;}
   80%{padding: 0px 30px;}
  100%{padding: 0px 0px;}
}

@keyframes glow{
    from{
        box-shadow: 13px 8px 10px #0088cc,13px 8px 20px #0088cc,13px 8px 30px #0088cc;
    }
    to{
        box-shadow: 8px 8px 20px rgb(238, 238, 238), 13px 8px 30px #0088cc,13px 8px 40px cyan;
    }
}

@keyframes glowt{
    from{
        text-shadow: 13px 8px 10px #0088cc,13px 8px 20px #0088cc,13px 8px 30px #0088cc;
    }
    to{
        text-shadow: 8px 8px 20px rgb(238, 238, 238), 13px 8px 30px #0088cc,13px 8px 40px cyan;
    }
}


```
