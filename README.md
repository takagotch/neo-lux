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

var api = NeoDB.ForTestNet();
var balances = api.GetBalancesOf("xxxx");
foreach (var entry in balances)
{
  Console.WriteLine(entry.Key + " => " + entry.Value);
}

var api = NeoDB.ForMainNet();
var redPulse_token = api.GetToken("RPX");
Console.WriteLine();
Console.WriteLine();

var privKey = "xxxxprivatekeyherexxxx".HexToBytes();
var myKeys = new KeyPair(privKey);
redPulse_token.Transfer(myKeys, "xxxx", 123,)

var api = NeoDB.ForMainNet();
var redPulse_contractHash = "xxx";
var redPulse_token = new NEP5(api, redPulse_contractHash);


IEnumerator SyncBalance()
{
  var balances = NeoAPI.GetBalance(NeoAPI.Net.Test, this.keys.address);
  this.balance = balances["NEO"];
}
StartCoroutine(SyncBalance());


var api = new LocalRPCNode(10332, "http://neoscan.io");
uint startBlock = 2313827;
uint endBlock = 2320681;
var token = api.GetToken("SOUL");
var soul_tx = SnapshotTools.GetTokenTransactions(token, startBlock, endBlock);
var soul_lines = new List<string>();
foreach (var tx in soul_tx)
{
  soul_lines.Add(tx.Hash+","+tx.Serialize().ByteToHex());
}
File.AppendAllLines("soul_txs.txt", soul_lines.ToArray());


var iterator = new BlockIterator(api);
var targetContractHash = "xxxx".AddressToScriptHash();
var token = new NEP5(api, targetContractHash);
var targetAddress = "xxxx";
var tx = api.WaitForTransaction(iterator, x = > x.type == TransactionType.ContractTransaction);
if (tx != null) {
  Console.WriteLine($"Transaction {tx.Hash} is a asset transfer");
}
var tx = api.WaitForTransaction(iterator, x => x.HasOutput(targetAddress));
if (tx != null) {
  Console.WriteLine($"Transaction {tx.Hash} was sent to {targetAddress}");
}
var tx = api.WaitForTransaction(iterator, x => x.HasInput(targetAddress));
var tx = api.WaitForTransaction(iterator, x => new ScriptInspector(x.script, targetContractHash).Any(y => y.operation == "transfer"));
if(tx != null){
  Console.WriteLine($"Transaction {tx.Hash} contains transfer for {token.Name}");
  var inspector = new ScriptInspector(tx.script);
  foreach (var call in inspector.Calls) {
      if (call.operation == "transfer") {
      var from = new UInt160(call.arguments[0]);
      var to = new UInt160(call.arguments[1]);
      var amount = new BigInteger(call.arguments[2]);
      Console.WriteLine($"Transfer of {amount} from {from.ToAddress()} to {to.ToAddress()}");
    }
  }
}
var tx = api.WatiForTransaction(iterator, x => new ScriptInspector(x.script, targetContractHash).Deployments.Any());
if (tx != null) {
  Console.WriteLine($"Transaction{tx.Hash} deployed a new contract");
}


var bytes = System.IO.File.ReadAllBytes();
var team_keys = Neo.Lux.Cryptography.keyPair();
var ICO_address = "xxxx";
var amount = 50;
var tx = api.WithdrawAsset(team_keys, ICO_address, "NEO", amount, bytes);
if (tx != null) {
  Console.WriteLine("Unconfirmed tx " + tx.Hash);
} 
else {
  Console.WriteLine("Sorry, transaction failed");
}

var bytes = System.IO.File.ReadAllBytes(@"d:\code\crypto\my_ico\MyICOContract.avm");
var team_keys = Neo.Lux.Cryptography.KeyPair.FromWIF("XXXXX");
var ICO_address = "xxxx";
var amount = 50;
var tx = api.ClaimGas(team_keys, ICO_address, bytes);
if (tx != null) {
  Console.WriteLine("Unconfirmed tx " + txw.Hash);
}
else {
  Console.WriteLine("Sorry, transaction failed");
}

var api = new RemoteRPCNode("http://neoscan.io", "http://seed6.ngd.network:10332", "http://seed.neoeconomy.io:10332");

```

```sh
Install-Package NeoLux
```

```
```


