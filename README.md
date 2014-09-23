# TeamSpeak 3 Music Bot

## Installing

### TeamSpeak 3 client

Tipp: For the client to make it work, setup the client with GUI first and then copy the settings files back to headless server. (Set it to auto connet on startup to your server)

```shell
$ sudo apt-get install xvfb libglib2.0-0 libpng12-0 libxcursor1 libxinerama1 \
  libxrandr2 libfontconfig1 pulseaudio

$ wget https://raw.github.com/mrshankly/tsmusicbot/master/Xvfb

$ sudo mv Xvfb /etc/init.d

$ sudo chmod 755 /etc/init.d/Xvfb

$ sudo useradd -r debian-xvfb

$ sudo /etc/init.d/Xvfb start
```

Install the teamspeak 3 client, to start it do:

```shell
$ cd <teamspeak3_directory>
$ DISPLAY=:99 ./ts3client_runscript.sh ts3server://SERVERIP?port=SERVERPORT&nickname=NAME&password=PASSWORD
```

It's probably a good idea to run the teamspeak 3 client with something like `screen` or
`tmux`.

### Pulseaudio
