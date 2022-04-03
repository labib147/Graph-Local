# Sub-graph Local

Go to this link to get all the detailed instructions https://thegraph.academy/developers/local-development/


Graph ql documentation for showing data in localhost (Linux)

Go to Git of Graph protocol: https://github.com/graphprotocol 

Find graph client folder and go through the installation process: https://github.com/graphprotocol/graph-cli

### Install the followings beforehand
1. Node
2. NPM
3. Docker
4. Opening an account in Infura

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

### Opening account in Infura 
Go to Infura website, create an account and then create a new project. Go to "Project Settings" and copy the https link in the “Endpoints” section confirming the “Mainnet” option in the scroll down menu(Mainnet is selected by default) 

![image](https://user-images.githubusercontent.com/52388164/161416604-b7e9e455-604f-4470-9f91-6d68ce56d2ee.png)
Then go to your docker installation folder and find the “docker-compose.yml” file. 
![image](https://user-images.githubusercontent.com/52388164/161416618-56ef7b25-56dd-47da-bd1e-b2840ccae2b5.png)
Paste the copied link in the “ ethereum: ‘paste link here’ ” line.


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

6. `yarn graphclient build`
7. `yarn graphclient serve-dev`
8. After running the final command, a localhost tab should automatically open in your default browser. Or you can copy and paste the http link after the "Server: Serving Composed Graph: " in your desired browser to get output.
9. Then you can query your desired data and get the output. 


Example Query
```
{
  gravatars(first: 5) {
    id
    owner
    displayName
    imageUrl
  }
}
```




 


