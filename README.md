# Testing trading strategies with the Freqtrade crypto bot.

This is the strategy folder of the Freqtrade bot, https://www.freqtrade.io/en/stable/.

## Comments/ Limitations
  - The bot does not have the ability to short sell.
  - You can only buy pairs, not perpetual contracts or other instruments. Therefore it is impossible to create market neutral strategies or take advantage of the funding rates etc.

## Deploying the bot to run 24/7 on the AWS cloud
- Register on AWS.
- Create an Linux (Debian) EC2 instance.
- `ssh` using the key pair .pem file.
- Follow the installation instructions here https://www.freqtrade.io/en/stable/installation/.
- To activate the virtual environment, run the command `source ./.env/bin/activate` in the freqtrade folder.
- To end the ssh session, but keep the bot running, using the command `screen`. See https://www.tecmint.com/keep-remote-ssh-sessions-running-after-disconnection/.
