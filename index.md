---
layout: default
---

Do you know how many dollars have ever been printed?

Do you know how much gold has ever been mined?

The answer to both of those questions is no. Certain government individuals may be privy to information that allows them to make an educated guess, but the fact is **nobody on earth** can answer those questions with any sort of accuracy. Bitcoin is different. 

For the first time in human history, anyone has the freedom to find out the **exact** total supply of a global monetary asset, without the need to ask for permission or rely on anyone else. All that's required is a [node](https://node.guide) and around 10 minutes of your time.  

***

### How?

Verifying the total supply of all bitcoins in existence is significantly easier than you might imagine. You can run this command any time you like, as often as you like, safe in the knowledge that you are only trusting your own hardware and open sourced software to verify for you.

Here's how...

#### Stand Alone Nodes

1. Set up your [node](https://node.guide)
2. Once initial block download is complete SSH in to your node. This is not required if you are running Bitcoin Core.
Instructions to do this will be found in your node's documentation pages. Mac + Linux users should do this via 'Terminal' and Windows users can download and use [Putty](https://www.putty.org/)
3. Enter the following command `bitcoin-cli gettxoutsetinfo`
4. Wait. Depending on your hardware, this could take up to 10 minutes

#### Stand Alone Nodes (non SSH version)

Most of the popular node implementations now come packaged with a local version of [this explorer](https://explorer.btc21.org/) which allows you to execute RPC commands through the GUI. Simple navigate to the 'RPC browser' section and click on `gettxoutsetinfo` and then execute.

Once again, depending on your hardware this may take up to 10 minutes.

<img src="https://raw.githubusercontent.com/BitcoinQnA/verify-supply/master/assets/images/RPC%20Browser.png" class=responsive width="950" height="350" maxheight="500">


#### Bitcoin Core

1. Download and install [Bitcoin Core](https://bitcoin.org/en/download) onto your computer
2. Wait for initial block download to complete
3. Open 'console' within Bitcoin Core and enter `bitcoin-cli gettxoutsetinfo`
4. Wait. Depending on your hardware, this could take up to 10 minutes


You should then see a response that looks like this...

```
{
  "height": 655987,
  "bestblock": "00000000000000000002c5f4af7514bdbfcbe6bb5beff57329f9e418024dab7e",
  "transactions": 42277264,
  "txouts": 68674534,
  "bogosize": 5155427851,
  "hash_serialized_2": "85a745a8739f6907bd0cff3ffaccbc29e5545a85aee8aca8b38daabe8a790442",
  "disk_size": 4216833480,
  "total_amount": 18537233.94446619
}
```

<br/>



