# Generate NTRIP Credentials

### Generate NTRIP Credentials

NTRIP credentials are what your miner uses to stream GNSS data to the onocoy network. You generate them once inside your onocoy account.

👉 Official onocoy guide: [https://docs.onocoy.com/documentation/3.-become-a-miner/3.-connect-your-station-to-onocoy](https://docs.onocoy.com/documentation/3.-become-a-miner/3.-connect-your-station-to-onocoy)

#### Steps:

1. Go to [Reference Stations](https://console.onocoy.com/servers) and select the tab „NTRIP Credentials“. Click on „Add new credential“. Select a password and add a description about how and where you are using these credentials, if you like. Note: the username will be generated automatically. Create new credentials for each station that you would like to connect.<br>
2. Your NTRIP credentials will be generated:
   * Host: data.onocoy.com
   * Port: 2101
   * Username: (your generated username)
   * Password: (your generated password)

> 💡 Save these credentials! You will need them when setting up your ESP32 or Raspberry Pi.

&#x20;If you have reached your credential limit, feel free to write a message  at [support@onocoy.com](mailto:support@onocoy.com) telling your account email address and your plans for expansion.
