# Blockchain-BlockMiner
Implementation of Practical Blockchain Mining, using Python and Flask.
A simple blockchain which can be mined, retrieved or verified using a web interface like a browser or Postman.

- Hashlib is used for generating hashes with sha256.

- Hash difficulty is 0000. See hash_operation_ok.

- This code runs on localhost on port 5000.



 # Installation

- Requires [Python](https://www.python.org/downloads/) 2.7 or higher to run.
- Requires [Postman HTTP Client](https://www.getpostman.com/).





## Install the package Required to start the server

Installing Pip
### For Linux(Ubutu/Debian)

```sh
# apt install python-pip
```

### For Mac
```sh
sudo easy_install pip (Requires Admin privilege)
```

### Installing Flask Package
```sh
pip install Flask==0.12.2
```

# Endpoints
# /mine_block
Mines a block and return the result.

# /get_chain
Returns the entire chain.

# /is_valid
Checks if block hashes correct through all the chain.

# Methods
- To get all the blocks of the Blockchain
 GET http://127.0.0.1:5000/get_chain on Postman HTTP Client
 
 Response:
 ```sh
 {
    "chain": [
        {
            "index": 1,
            "previous_hash": "0",
            "proof": 1,
            "timestamp": "2019-06-22 09:12:53.269000"
        }
    ],
    "length": 1
}
 ```
- To mine the new block of the blockchain
GET http://127.0.0.1:5000/mine_block on Postman HTTP Client

Response:
```sh
{
    "index": 2,
    "message": "Congratulations, you just mined a block!",
    "previous_hash": "9b2c42acf5eb9950d77fd8a834cc559dd9ab900d0aefc1d6f10fff3c54a14a90",
    "proof": 533,
    "timestamp": "2019-06-22 09:15:47.509000"
}
```


# Contributing

- I welcome pull requests, bug fixes and issue reports. Before proposing a change, please discuss your change by raising an issue.

# Author
- [Kumar Gaurav](https://www.linkedin.com/in/arkhaminferno/)

