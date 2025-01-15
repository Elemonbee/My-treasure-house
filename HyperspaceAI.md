# Hyperspace Ai

* Official website: [https://hyper.space/](https://hyper.space/)
* X account (formerly Twitter): [https://x.com/HyperspaceAI](https://x.com/HyperspaceAI)
---
## 1.Node types
* You can run Hyperspace Ai's Node in different ways: Browser, Client, and CLI.
* You can choose to run the node in a way that suits your needs or preferences.
![111](https://github.com/user-attachments/assets/098818aa-bb4d-4804-bbd2-13eb062a9252)
---
## 2.Run a Linux CLI Node
* The CLI node is a command line interface for accessing functionality similar to that of the aiOS desktop application. If you prefer to use the terminal, you can use the CLI node.
* For the full tutorial, check out the [official repository](https://github.com/hyperspaceai/aios-cli?tab=readme-ov-file).
---
### 2.1 Install
``````
curl https://download.hyper.space/api/install | bash
``````
![222](https://github.com/user-attachments/assets/1cc5f3e0-fa3f-4ddb-8eaa-0737640dd0c8)

---
### 2.2 Run node
#### Run the daemon
* Open a new terminal window via the desktop or use `screen -S hyperspace` to open:
![333](https://github.com/user-attachments/assets/76929aac-7a8d-48dd-b013-39c47646a602)
* Run the daemon
```
aios-cli start
```
* Then use `screen -r hyperspace` to return to the previous window
* Check if the daemon is running successfully
```
aios-cli status
```
![444](https://github.com/user-attachments/assets/aa15561b-794f-4c30-960e-8d0a50b359ba)
#### Check the list of available models
```
aios-cli models available
```
* Install one of them to local(I downloaded the model from the official tutorial example)
```
aios-cli models add hf:TheBloke/Mistral-7B-Instruct-v0.1-GGUF:mistral-7b-instruct-v0.1.Q4_K_S.gguf
```
#### Import your private key (Optional)
* Will generate a new private key for you during installation and connection, if you want to use an existing private key then use this command.
```
aios-cli hive import-keys ./my.pem
```
* If you want to edit your private key, then you can use `nano my.pem` to do that.
#### Access Hive (server) using these keys
```
aios-cli hive login
```
* Connect to the network
```
aios-cli hive connect
```
#### Choose the tier (relate to the multiplier of your points)
```
aios-cli hive select-tier 5
```
#### Inference using models
`aios-cli infer [OPTIONS]`
#### Shortcuts for starting, logging in, and connecting to Hive
```
aios-cli start --connect
```
#### Check your points
```
aios-cli hive points
```
![55555](https://github.com/user-attachments/assets/b9aed69a-77e9-4ec2-acbc-5987a795fa3d)
---
### 2.3 Terminate the process
* To stop the node from running, you can use the following command (if manually stopping or restarting your computer causes the node to terminate, you can then use a shortcut to connect)
```
aios-cli kill
```
---
## For a full tutorial and more detailed instructions, pls check out the [**official repository**](https://https://github.com/hyperspaceai/aios-cli?tab=readme-ov-file). 
---
