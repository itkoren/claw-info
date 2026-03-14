## Installation ##
### OS ###
#### Option 1: No Config ####
```
lume create openclaw --os macos --ipsw latest
lume run openclaw --clipboard
```
- System Settings -> General -> Sharing -> Remote Login -> On
- System Settings -> Energy -> Prevent automatic sleeping when the display is off -> On

#### Option 2: Unattended ####
```
lume create openclaw --os macos --ipsw latest --unattended tahoe
```

### Save a Golden Image ###
```
lume stop openclaw
lume clone openclaw openclaw-backup
```

### Reset Anytime
```
lume delete openclaw
lume clone openclaw-backup openclaw
```

### OpenClaw ###
```
lume get openclaw
```
- Copy the IP Address [IP] (usually 192.168.64.x)
```
lume stop openclaw
lume run openclaw --no-display
ssh openclaw@[IP]
```
