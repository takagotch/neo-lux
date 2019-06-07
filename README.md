### neo-lux
---
https://github.com/CityOfZion/neo-lux

```cc
using Neo.Lux;

var privKey = "XXXXprivatekeyhereXXXX".HexToBytes();
var myKeys = new KeyPair(privKey);
var scriptHash = "xxxx";
var api = NeoDB.ForMainNet();
var result = api.CallContract(myKeys, scriptHash, "registerMailbox", new object[] { "ABCDE", "demo@phantasma.io" });


var privKey = "XXXXprivatekeyhereXXXX".HexToBytes();
var myKeys = new KeyPair(privKey);
var api = NeoDB.ForTestNet();
var result = api.SendAsset("AanTL6pTTEdnphXpyPMgbxxxxx")
















```

```sh
Install-Package NeoLux

```

```
```


