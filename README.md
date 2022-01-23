# Testing trading strategies with the Freqtrade crypto bot.

This is the strategy folder for the Freqtrade bot.

To set up, see the https://www.freqtrade.io/en/stable/ or the udemy course https://www.udemy.com/course/build-a-crypto-bot-100-functional-algorithmic-trading-freqtrade/.

## Deploying the bot to run 24/7 on the AWS cloud
- Register on AWS.
- Create a Linux (Debian) EC2 instance.
- In the CMD, `ssh` using the key pair .pem file: `ssh -i "KeyPair.pem" admin@****`.
- Follow the installation instructions here: https://www.freqtrade.io/en/stable/installation/.
- Do not forget to check the requirements before setting up.
- To activate the virtual environment, run the command `source ./.env/bin/activate` in the freqtrade folder.
- To end the ssh session, but keep the bot running, use the command `screen` and then detach from the running process with the key binding `Ctrl + A Ctrl + D`. To resume the session use `screen -r`. See https://www.tecmint.com/keep-remote-ssh-sessions-running-after-disconnection/.

## config.json file for MAC
- max open trades: -1 for unlimited (limited by pairlist), or 10
- stake amount: unlimited
- blacklist DAI/USDT, USDC/USDT (stable coins)

## Comments/ Limitations
  - The bot does not have the ability to short sell.
  - You can only buy pairs, not perpetual contracts or other instruments. Therefore it is impossible to create market neutral strategies or take advantage of the funding rates etc.
