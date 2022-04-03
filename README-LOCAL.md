# Sub-graph Local

Go to this link to get all the detailed instructions https://thegraph.academy/developers/local-development/


Graph ql documentation for showing data in localhost (Linux)

Go to Git of Graph protocol: https://github.com/graphprotocol 

Find graph client folder and go through the installation process: https://github.com/graphprotocol/graph-cli

### Install the followings beforehand
1. Node
2. NPM
3. Docker

### Installation of node - 
1. `sudo apt install nodejs`
2. `sudo apt update`
3. `curl -sL https://deb.nodesource.com/setup_16.x | sudo bash -`
4. `sudo apt install -y nodejs`
5. `node -v`

After running the final command, you should get the following output `v16.14.2`

### Installation of npm -

1. `sudo npm install -g npm@latest`
2.  `npm -v` 
3.  This should show an output as follows `8.5.0`
4.  If this does not update to your required version, then try `sudo npm install -g npm@8.5.0`

### Installation of Docker & Docker Compose 

1. `sudo apt-get update`
2. `sudo apt-get install docker-ce docker-ce-cli containerd.io`
3. `docker -v`
4. After running the previous command you should get the following output `Docker version 20.10.7`
5. `mkdir -p ~/.docker/cli-plugins/`
6. `curl -SL https://github.com/docker/compose/releases/download/v2.2.3/docker-compose-linux-x86_64 -o ~/.docker/cli-plugins/docker-compose`
7. `chmod +x ~/.docker/cli-plugins/docker-compose`
8. `docker compose version`
9. After running the previous command, you should get the following output `Docker Compose version v2.2.3`

After this you can watch this 30 min video that explains the entire process step by step: https://www.youtube.com/watch?v=jxhNsSicEzA

The project might throw an error in the end because of the version of the dependencies. So, be sure to update the graph-cli & graph-ts to their latest versions.
```
    npm i @graphprotocol/client-cli@latest or npm i -D @graphprotocol/client-cli@latest
    npm i @graphprotocol/graph-cli@latest or npm i -D @graphprotocol/graph-cli@latest 
    npm i @graphprotocol/graph-ts@latest or  npm i -D @graphprotocol/graph-ts@latest
    npm i @graphprotocol/graph-ts@latest
```
Afther updating the package.json file should show the following devDependencies:
```
    "@graphprotocol/client-cli": "^0.0.2",
    "@graphprotocol/graph-cli": "^0.29.0",
    "@graphprotocol/graph-ts": "^0.26.0",    
    "typescript": "^4.6.2"
```

Type the following commands in the terminal step by step
1. Use `npm run codegen` or `yarn run codegen` to run codegen
2. `yarn run build`
3. `yarn create-local`
4. `yarn deploy-local`
5. Then copy the end point of the "Queries(HTTP)" and paste it in the endpoint of the "graphclientrc.yml" file 

 ###file:///home/office/Pictures/Screenshot%20from%202022-04-03%2012-47-36.png![image](https://user-images.githubusercontent.com/52388164/161415769-b180bac1-2fb7-43c1-af6a-1fc842107dfa.png)

6. 



 


