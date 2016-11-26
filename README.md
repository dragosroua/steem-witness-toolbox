<<<<<<< HEAD
Steem Witness Toolbox
============

This is a helper script for witnesses maintaining the [Steem](http:/steem.io) network. It's
written in Node.JS, uses SVK's [SteemJS-Lib](https://github.com/svk31/steemjs-lib) and it's based 
on [someguy123](https://github.com/someguy123)'s [steemfeed-js](https://github.com/Someguy123/steemfeed-js). 
The heavy lifting was done by [someguy123](https://github.com/someguy123), I just added 
options for updating SBD interest rate, `account_creation_fee` and `maxmimum_block_size` arguments.

The script updates the price feed at a set interval (default is 60 minutes, can be changed via `config.json`) and 
the following witness variables:

* **account_creation_fee** - the price, in STEEM, that a user must pay in order to create an account on Steemit.com
* **sbd_interest_rate** - the APR of Steem Backed Dollars
* **maximum_block_size** - the maximum size of a block in the Steem blockchain
=======
Steem Feed JS
============

This is a STEEM Price Feed for witnesses on the [STEEM Network](https://steem.io). It's
written in Node.JS and uses SVK's [SteemJS-Lib](https://github.com/svk31/steemjs-lib).
>>>>>>> bf4d6444610bf36b24797e4085bf9ee7aba958e0

Installation
========

First, download the git repository, then edit `config.json` as needed. The interval is in minutes.

```
<<<<<<< HEAD
git clone https://github.com/dragosroua/steem-witness-toolbox.git
cd steem-witness-toolbox
cp config.example.json config.json
vi config.json
```

The following defaults are used if you leave the following fields empty in `config.json`:

```
account_creation_fee - 5 (USD)
sbd_interest_rate - 13%
maximum_block_size - 65536
=======
git clone https://github.com/Someguy123/steemfeed-js.git
cd steemfeed-js
cp config.example.json config.json
nano config.json
>>>>>>> bf4d6444610bf36b24797e4085bf9ee7aba958e0
```

I recommend using Docker, however you can also use a locally installed copy of Node v6.

**Starting Via Docker**

```
<<<<<<< HEAD
docker build -t steem-witness-toolbox .
docker run -it --rm --name witness-toolbox steem-witness-toolbox

# Check the status with docker logs
docker logs witness-toolbox
=======
docker build -t steemfeed-js .
docker run -it --rm --name feed steemfeed-js

# Check the status with docker logs
docker logs feed
>>>>>>> bf4d6444610bf36b24797e4085bf9ee7aba958e0
```

**Starting Via NodeJS (assuming you have v6 installed)**
```
npm install
npm start
```
