# Web Server
1.

    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash

2. 
   
    . ~/.nvm/nvm.sh
3. 
    
    nvm install --lts

4. 
    
    node -e "console.log('Running Node.js ' + process.version)"

5.
    
    npm install -g pm2

6.
    
    mkdir app
    cd app
    touch index.js
    nano index.js

    

7.
  
    const express = require("express");
    const app = express();

    const PORT = 5000;

    app.get("/", (req, res) => {
        res.json({ message: "Hello World"  });
    })

    app.get("/health-check", (req, res) => {
        res.json({ message: "Server up and running"  });
    })

    app.listen(PORT, () => {
        console.log("Server Running on PORT", PORT);
    })

8. 
    
    npm i express

9.
    
    pm2 start index.js

10.
    
    sudo iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-ports 5000


# MySQL

1.
    
    sudo apt update
2.
    
    sudo apt install mysql-server
3.
    
    sudo systemctl status mysql
4.
    
    mysql -uroot -p;


