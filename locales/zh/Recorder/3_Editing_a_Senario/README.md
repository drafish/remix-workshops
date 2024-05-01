# 编辑一个场景

Here's the first few lines of the scenario that I recorded.  The addresses on my machine will be different from your's.

```
{
    "accounts": {
    "account{0}": "0xca35b7d915458ef540ade6068dfe2f44e8fa733c",
    "account{4}": "0xdd870fa1b7c4700f2bd7f44238821c26f7392148",
    "account{3}": "0x583031d1113ad414f02576bd6afabfb302140225"
    }
```

如果您想在另一个测试网络中运行此场景，则需要将这些地址更改为您拥有测试ETH的地址，以便支付交易费用。但是除了更换地址之外，您可以快速在其他网络上运行它。  But other than swapping out the addresses, you can quickly run this on other nets.

并且您可能会更改函数的参数。

例如，这是scenario.json的一部分，提案2被其中一个地址投票支持：

```
{
      "timestamp": 1566428184043,
      "record": {
        "value": "0",
        "parameters": [
          "2"
        ],
        "to": "created{1566428035436}",
        "abi": "0xc41589e7559804ea4a2080dad19d876a024ccb05117835447d72ce08c1d020ec",
        "name": "vote",
        "inputs": "(uint8)",
        "type": "function",
        "from": "account{4}"
      }
    },
```

让我们编辑一下，以便在回放中另一个提案获胜。

将参数数组更改为：

```
"parameters": [
          "2"
        ]
```

to:

```
"parameters": [
          "1"
        ]
```
