<html>
<head>  
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">   
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
    <link href="style.css" rel="stylesheet">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">   
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Bad+Script&family=Pacifico&display=swap" rel="stylesheet">
    <link href="style.css" rel="stylesheet">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">       
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+Sinhala:wght@100..900&display=swap" rel="stylesheet"> 
    <link href="style.css" rel="stylesheet">
    <style>
        // <uniquifier>: Use a unique and descriptive class name
    // <weight>: Use a value from 100 to 900
    .noto-serif-sinhala-<uniquifier> {
      font-family: "Noto Serif Sinhala", serif;
      font-optical-sizing: auto;
      font-weight: <weight>;
      font-style: normal;
      font-variation-settings:
        "wdth" 100;
}
    </style>
    <style>
        .bad-script-regular {
                        font-family: "Bad Script", cursive;
                        font-weight: 400;
                        font-style: normal;
                        }
    </style>
    <style>
        .pacifico-regular {
                            font-family: "Pacifico", cursive;
                            font-weight: 400;
                            font-style: normal;
                       }
    </style>
    <style>
        h6{
                font-family: Noto Serif Sinhala, serif;
            }
    </style>
    <style>
       h1 {
               font-family: Pacifico, cursive; 
           }
    </style>
    <style>
        h2 {
             font-family: "Bad Script", cursive;   
        }
    </style>
    <style>
        .glow-on-hover {
    border: none;
    outline: none;
    color: #fff;
    background: #111;
    cursor: pointer;
    position: relative;
    z-index: 0;
    border-radius: 10px;
    font-size: 20px;
    padding: 10px 20px;
    transition: background-color 0.3s;
}

.glow-on-hover:before {
    content: '';
    background: linear-gradient(45deg, #ff0000, #ff7300, #fffb00, #48ff00, #00ffd5, #002bff, #7a00ff, #ff007a);
    position: absolute;
    top: -2px;
    left: -2px;
    background-size: 400%;
    z-index: -1;
    filter: blur(5px);
    width: calc(100% + 4px);
    height: calc(100% + 4px);
    animation: glowing 20s linear infinite;
    opacity: 0;
    transition: opacity 0.3s ease-in-out;
    border-radius: 10px;
}

.glow-on-hover:hover:before {
    opacity: 1;
}

.glow-on-hover:active {
    background: #333;
}

@keyframes glowing {
    0% { background-position: 0 0; }
    50% { background-position: 400% 0; }
    100% { background-position: 0 0; }
}

    </style>
<style>
  body {
          font-family: Satisfy&display=swap;
          font-size: 40xp;
    }
</style> 
   <style>
        header h1 {
            position: relative;
            top: 30px; 
            right: 10px; 
        }
       </style>
   </style>
    <style>
        body {
            background-image: url('Screenshot 2024-05-15 184945.png');
            background-repeat: no-repeat;
            background-attachment: fixed;
            background-size: 100% 100%;
             background-filter: blur(20px);
        }
    </style>
    <style>
        .horizontal-menu {
             width: 500;
            height: 10;
            background-color: #f7ff72;
            overflow: hidden;
            border-radius: 50%;
            box-shadow: 0 0 12px #000000;
            border-size: cover;
        }
      .horizontal-menu a {
            float: left; 
            display: block;
            color: black; 
            text-align: center;
            padding: 14px 20px; 
            text-decoration: none; 
        }
        circle-logo {
            width: 200px; 
            height: 200px; 
            border-radius: 50%;
            background-image: url('Screenshot 2024-05-17 204656.png');
            border-size: cover;
        }  
        .horizontal-menu a:hover {
            background-color: #9ea700;
        }
    </style>
    <style>
      h1 {
        fomt-family: Satisfy&display=swap;
        color: red;
          }
    </style>
    <style>
       text-box {
                    width: 400;
                   height: 300;
                    padding: 5px 15px;
                    border: 2px solid black ;
                    background: transparent;
                    background-filter: blur(20px);
                    box-shadow: 0 0 10px #000000;
                    border-radius: 12px; 
            }
    </style>
       <style>
        .circle-logo {
            width: 50px; 
            height: 50px; 
            border-radius: 50%;
        }
    </style>   
</head>
<body>
  <header>
  <h1><center><div><u><font color="white">MY WEB PAGE</font></u></div></center></h1>
  </header>
    <div class="circle-logo"></div>  
    <div class="horizontal-menu">
        <h2>
            <a href="#"><img src="Screenshot 2024-05-17 204656.png" class="circle-logo"></a>
            <a href="#">Home</a>
            <a href="#">About</a>
            <a href="#">Services</a>
        </h2>
    </div>   
    <div class="font family"><h1><font color="white">Hello, world!</font></h1></div>
    <h6><center><p><font color="white" size="5">ආයුබෝවන්!!.</font></p></center></h6>
  <center><button class="glow-on-hover">A.S.D</button></center>  
   
</body>
</html>
