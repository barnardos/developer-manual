## wifi-location-changer setup instructions

Open your terminal and run the commands below:


```bash
brew install wget
wget "https://raw.githubusercontent.com/barnardos/developer-manual/master/locationchanger"
wget "https://raw.githubusercontent.com/barnardos/developer-manual/master/LocationChanger.plist"
sudo mv locationchanger /usr/local/bin
mv LocationChanger.plist ~/Library/LaunchAgents/
launchctl load ~/Library/LaunchAgents/LocationChanger.plist
```
