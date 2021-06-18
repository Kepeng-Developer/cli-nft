# cli-nft
command line cleos nft contract
NFT - Non Funglible Token on vexanium
## create
```bash
./cleos --url http://api.vex.proit.id:8080 push action stdvexassets create '{"author": "<author account>", "category":"painting","owner": "<owner account>", "idata": "{\"name\":\"I Kadek Oka Sugawa\"}", "mdata": "{\"name\": \"Lukisan Monalisa\"}", "requireclaim": 0}' -p <author account>
```
#### example idata more than one
idata is imutable can not be change
```python
string idata = "{\"name\": I Kadek, \"date\": 18/06/2021, \"time\": \"17:11\" }";
```
## list
```bash
./cleos --url http://api.vex.proit.id:8080 get table stdvexassets <account> sassets
```
## update
```bash
./cleos --url http://api.vex.proit.id:8080 push action stdvexassets update '{"author": "<author account>", "owner": "<owner account>", "assetid": <asset id> "mdata": "{\"name\": \"Red Diamond\"}"}' -p <account>
```
## transfer
```bash
./cleos --url http://api.vex.proit.id:8080 push action stdvexassets transfer '{"from": "<account>", "to": "<account>", "assetids": [<assetid>], "memo": "NFT Transfer" }' -p <account_from>
```
## burn
```bash
./cleos --url http://api.vex.proit.id:8080 push action stdvexassets burn '{"owner": "<owner account>", "assetids": [<asset id>], "memo":"First NFT Burn"}' -p <owner account>
```

