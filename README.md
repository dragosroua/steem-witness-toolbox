Steem Witness Toolbox
============

This is a helper script for witnesses maintaining the [Steem](http:/steem.io) network. It's
written in Node.JS and uses SVK's [SteemJS-Lib](https://github.com/svk31/steemjs-lib). 
The heavy lifting was done by [someguy123](https://github.com/someguy123), I just added 
options for updating the SBD interest rate and setting up the account_creation_fee.

The script updated the price feed at a set interval (default is 60 minutes, can be changed via config.json) and 
the following witness arguments:

* **account_creation_fee** - the price, in STEEM that a user must pay in order to create an account on Steemit.com
* **sbd_interest_rate** - the APR of Steem Backed Dolls
* **maximum_block_size** - the maximum size of a block in the Steem blockchain

Installation
========

First, download the git repository, then edit `config.json` as needed. The interval is in minutes.

```
git clone https://github.com/dragosroua/steem-witness-toolbox.git
cd steem-witness-toolbox
cp config.example.json config.json
vi config.json
```

The following defaults are used if you leave these fields empty in `config,json`:

```
account_creation_fee - 5 (USD)
sbd_interest_rate - 13%
maximum_block_size - 65536
```

I recommend using Docker, however you can also use a locally installed copy of Node v6.

**Starting Via Docker**

```
docker build -t steem-witness-toolbox .
docker run -it --rm --name witness-toolbox steem-witness-toolbox

# Check the status with docker logs
docker logs witness-toolbox
```

**Starting Via NodeJS (assuming you have v6 installed)**
```
npm install
npm start
```
