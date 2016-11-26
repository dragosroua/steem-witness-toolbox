Steem Witness Toolbox
============

This is a helper script for witnesses maintaining the [Steem](http:/steem.io) network. It's
written in Node.JS and uses SVK's [SteemJS-Lib](https://github.com/svk31/steemjs-lib). 
The heavy lifting was done by [someguy123](https://github.com/someguy123)

Installation
========

First, download the git repository, then edit `config.json` as needed. The interval is in minutes.

```
git clone https://github.com/dragosroua/steem-witness-toolbox.git
cd steem-witness-toolbox
cp config.example.json config.json
nano config.json
```

I recommend using Docker, however you can also use a locally installed copy of Node v6.

**Starting Via Docker**

```
docker build -t steemfeed-js .
docker run -it --rm --name witness-toolbox steem-witness-toolbox

# Check the status with docker logs
docker witness-toolbox feed
```

**Starting Via NodeJS (assuming you have v6 installed)**
```
npm install
npm start
```
