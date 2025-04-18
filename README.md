1️⃣ Dependencies for WINDOWS & LINUX & VPS
```
sudo apt update
sudo apt upgrade -y
```
### Install
```
curl https://download.hyper.space/api/install | bash
```

# Create a screen ro run it in background for later
```
screen -S hyperspace
```
# Run node
```
aios-cli start
```
* To continue, minimize your screen using `CTRL+A+D` or Open second terminal
* Turn back to screen: `screen -r hyperspace`

### Config Node
```console
# Download a required model
aios-cli models add hf:TheBloke/phi-2-GGUF:phi-2.Q4_K_M.gguf
# Import your private key - Create a my.pem file using nano .pem and input a privatekey (You can get a privatekey from browser and make sure to save it my.pem)
aios-cli hive import-keys ./my.pem
# Set those keys as the preferred keys for this session
aios-cli hive login
# Make sure the model is registered
aios-cli hive connect
aios-cli hive select-tier 5
```

### Check Points
```
aios-cli hive points
```


# Usefull commands
```console
# Shortcut for Start, Login and Connect to Hive commands, if you've stopped you node
aios-cli start --connect
# Update node
aios-cli version
# Stop node
aios-cli kill
```
