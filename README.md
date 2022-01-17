# Testing trading strategies with the Freqtrade crypto bot.

This is the strategy folder of the Freqtrade bot, https://www.freqtrade.io/en/stable/.

## Deploying the bot to run 24/7 on the AWS cloud
- Register on AWS.
- Create a Linux (Debian) EC2 instance.
- `ssh` using the key pair .pem file: `ssh -i "KeyPair.pem" admin@****`.
- Follow the installation instructions here: https://www.freqtrade.io/en/stable/installation/.
- Do not forget to check the requirements before setting up.
- To activate the virtual environment, run the command `source ./.env/bin/activate` in the freqtrade folder.
- To end the ssh session, but keep the bot running, use the command `screen` and then detach from the running process with the key binding `Ctrl + A Ctrl + D`. To resume the session use `screen -r`. See https://www.tecmint.com/keep-remote-ssh-sessions-running-after-disconnection/.

## Comments/ Limitations
  - The bot does not have the ability to short sell.
  - You can only buy pairs, not perpetual contracts or other instruments. Therefore it is impossible to create market neutral strategies or take advantage of the funding rates etc.
