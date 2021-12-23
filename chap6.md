チャプター６

```
アドレス5個
getnewaddress

tb1q2tsumy3d27wywc5h7qesrj9gpf8yq77lm347tk
#公開鍵
03fcc8546e8feca858b6b41861962c5f22bcde8e4e63af2ac2368de59c5bfeb584

tb1qlqgank4p07n2v983nvxvgudsw0d897e0evec2z
#公開鍵
0322c3d0ff973d84460dc8f182e05a16c78c53786c113dfd26c55fbd7edc93adff

tb1qc5ypny9gt665l7v8scdg8dg9gjkskrn022d63p
#公開鍵
02719cf88e506ac458fbfffa7c820fb3223837fecbff7083b5f40f81860126c6dd

tb1qduwfeu8fnne6tv00wymlkkpnjzfyay6zxkwcx3
#公開鍵
027419777d0385d51d313236204632fbe750a3574c1ad225cf461e1117fdc227d0

tb1qp5mxckz2p533umtggxw3jewwwq8c92zduygjsg
#公開鍵
021dfcdb8c9c2ca894efc4b705622efb23fb2f1c5edc856787ac4a9518fa27b571


使用するUTXO
listunspent

 {
    "txid": "5e520ff7e726583acf2e0423a3ab4bfabd8ca2ef22f1fcc4a89685c4063480f8",
    "vout": 0,
    "address": "tb1qc9fnvvc75ptaazps4zkkc2m68uypjesl4xx5ud",
    "label": "",
    "scriptPubKey": "0014c15336331ea057de8830a8ad6c2b7a3f0819661f",
    "amount": 0.10000000,
    "confirmations": 1058,
    "spendable": true,
    "solvable": true,
    "desc": "wpkh([f22e986b/0'/0'/32']02f0696d231fce587bbb60584214f48bb4055d138def2854fb8f1fcb6b7eb91d5e)#hupjmmer",
    "safe": true
  }

```

トランザクションの作成

```

createrawtransaction  '[{"txid":"5e520ff7e726583acf2e0423a3ab4bfabd8ca2ef22f1fcc4a89685c4063480f8","vout":0}]' '[{"tb1q2tsumy3d27wywc5h7qesrj9gpf8yq77lm347tk":0.018}, {"tb1qlqgank4p07n2v983nvxvgudsw0d897e0evec2z":0.02},
{"tb1qc5ypny9gt665l7v8scdg8dg9gjkskrn022d63p":0.02},
{"tb1qduwfeu8fnne6tv00wymlkkpnjzfyay6zxkwcx3":0.02},
{"tb1qp5mxckz2p533umtggxw3jewwwq8c92zduygjsg":0.02}]'


0200000001f8803406c48596a8c4fcf122efa28cbdfa4baba323042ecf3a5826e7f70f525e0000000000ffffffff0540771b000000000016001452e1cd922d579c476297f03301c8a80a4e407bdf80841e0000000000160014f811d9daa17fa6a614f19b0cc471b073da72fb2f80841e0000000000160014c5081990a85eb54ff987861a83b50544ad0b0e6f80841e00000000001600146f1c9cf0e99cf3a5b1ef7137fb583390924e934280841e00000000001600140d366c584a0d231e6d68419d1965ce700f82a84d00000000

```

トランザクションの署名
```
signrawtransactionwithwallet 0200000001f8803406c48596a8c4fcf122efa28cbdfa4baba323042ecf3a5826e7f70f525e0000000000ffffffff0540771b000000000016001452e1cd922d579c476297f03301c8a80a4e407bdf80841e0000000000160014f811d9daa17fa6a614f19b0cc471b073da72fb2f80841e0000000000160014c5081990a85eb54ff987861a83b50544ad0b0e6f80841e00000000001600146f1c9cf0e99cf3a5b1ef7137fb583390924e934280841e00000000001600140d366c584a0d231e6d68419d1965ce700f82a84d00000000

{
  "hex": "02000000000101f8803406c48596a8c4fcf122efa28cbdfa4baba323042ecf3a5826e7f70f525e0000000000ffffffff0540771b000000000016001452e1cd922d579c476297f03301c8a80a4e407bdf80841e0000000000160014f811d9daa17fa6a614f19b0cc471b073da72fb2f80841e0000000000160014c5081990a85eb54ff987861a83b50544ad0b0e6f80841e00000000001600146f1c9cf0e99cf3a5b1ef7137fb583390924e934280841e00000000001600140d366c584a0d231e6d68419d1965ce700f82a84d0247304402200dd1c6eead20c40a8ccfcef32723852229c1357467e222b37bccba66e15aeffc02201ddcccef96614cfce8d13108048f5ecad33b65fb6d8243c907f1853820f046a5012102f0696d231fce587bbb60584214f48bb4055d138def2854fb8f1fcb6b7eb91d5e00000000",
  "complete": true
}


decoderawtransaction 02000000000101f8803406c48596a8c4fcf122efa28cbdfa4baba323042ecf3a5826e7f70f525e0000000000ffffffff0540771b000000000016001452e1cd922d579c476297f03301c8a80a4e407bdf80841e0000000000160014f811d9daa17fa6a614f19b0cc471b073da72fb2f80841e0000000000160014c5081990a85eb54ff987861a83b50544ad0b0e6f80841e00000000001600146f1c9cf0e99cf3a5b1ef7137fb583390924e934280841e00000000001600140d366c584a0d231e6d68419d1965ce700f82a84d0247304402200dd1c6eead20c40a8ccfcef32723852229c1357467e222b37bccba66e15aeffc02201ddcccef96614cfce8d13108048f5ecad33b65fb6d8243c907f1853820f046a5012102f0696d231fce587bbb60584214f48bb4055d138def2854fb8f1fcb6b7eb91d5e00000000

{
  "txid": "008e3e0e73344656752212cdbf132b8d5444cff6480e2271b7ed9098da470221",
  "hash": "060f0e75c1306f38927a460b4a29093a48c8399fbbfd28756b1ea13886651281",
  "version": 2,
  "size": 315,
  "vsize": 234,
  "weight": 933,
  "locktime": 0,
  "vin": [
    {
      "txid": "5e520ff7e726583acf2e0423a3ab4bfabd8ca2ef22f1fcc4a89685c4063480f8",
      "vout": 0,
      "scriptSig": {
        "asm": "",
        "hex": ""
      },
      "txinwitness": [
        "304402200dd1c6eead20c40a8ccfcef32723852229c1357467e222b37bccba66e15aeffc02201ddcccef96614cfce8d13108048f5ecad33b65fb6d8243c907f1853820f046a501",
        "02f0696d231fce587bbb60584214f48bb4055d138def2854fb8f1fcb6b7eb91d5e"
      ],
      "sequence": 4294967295
    }
  ],
  "vout": [
    {
      "value": 0.01800000,
      "n": 0,
      "scriptPubKey": {
        "asm": "0 52e1cd922d579c476297f03301c8a80a4e407bdf",
        "hex": "001452e1cd922d579c476297f03301c8a80a4e407bdf",
        "address": "tb1q2tsumy3d27wywc5h7qesrj9gpf8yq77lm347tk",
        "type": "witness_v0_keyhash"
      }
    },
    {
      "value": 0.02000000,
      "n": 1,
      "scriptPubKey": {
        "asm": "0 f811d9daa17fa6a614f19b0cc471b073da72fb2f",
        "hex": "0014f811d9daa17fa6a614f19b0cc471b073da72fb2f",
        "address": "tb1qlqgank4p07n2v983nvxvgudsw0d897e0evec2z",
        "type": "witness_v0_keyhash"
      }
    },
    {
      "value": 0.02000000,
      "n": 2,
      "scriptPubKey": {
        "asm": "0 c5081990a85eb54ff987861a83b50544ad0b0e6f",
        "hex": "0014c5081990a85eb54ff987861a83b50544ad0b0e6f",
        "address": "tb1qc5ypny9gt665l7v8scdg8dg9gjkskrn022d63p",
        "type": "witness_v0_keyhash"
      }
    },
    {
      "value": 0.02000000,
      "n": 3,
      "scriptPubKey": {
        "asm": "0 6f1c9cf0e99cf3a5b1ef7137fb583390924e9342",
        "hex": "00146f1c9cf0e99cf3a5b1ef7137fb583390924e9342",
        "address": "tb1qduwfeu8fnne6tv00wymlkkpnjzfyay6zxkwcx3",
        "type": "witness_v0_keyhash"
      }
    },
    {
      "value": 0.02000000,
      "n": 4,
      "scriptPubKey": {
        "asm": "0 0d366c584a0d231e6d68419d1965ce700f82a84d",
        "hex": "00140d366c584a0d231e6d68419d1965ce700f82a84d",
        "address": "tb1qp5mxckz2p533umtggxw3jewwwq8c92zduygjsg",
        "type": "witness_v0_keyhash"
      }
    }
  ]
}


```
５つのアウトプットにしたものを送金
```
sendrawtransaction 02000000000101f8803406c48596a8c4fcf122efa28cbdfa4baba323042ecf3a5826e7f70f525e0000000000ffffffff0540771b000000000016001452e1cd922d579c476297f03301c8a80a4e407bdf80841e0000000000160014f811d9daa17fa6a614f19b0cc471b073da72fb2f80841e0000000000160014c5081990a85eb54ff987861a83b50544ad0b0e6f80841e00000000001600146f1c9cf0e99cf3a5b1ef7137fb583390924e934280841e00000000001600140d366c584a0d231e6d68419d1965ce700f82a84d0247304402200dd1c6eead20c40a8ccfcef32723852229c1357467e222b37bccba66e15aeffc02201ddcccef96614cfce8d13108048f5ecad33b65fb6d8243c907f1853820f046a5012102f0696d231fce587bbb60584214f48bb4055d138def2854fb8f1fcb6b7eb91d5e00000000

# できたtxid

008e3e0e73344656752212cdbf132b8d5444cff6480e2271b7ed9098da470221


gettransaction 008e3e0e73344656752212cdbf132b8d5444cff6480e2271b7ed9098da470221

{
  "amount": 0.00000000,
  "fee": -0.00200000,
  "confirmations": 921,
  "blockhash": "0000009c426c23aa163391d356dc58ed660ad2ae56af8d08e0ef3deac7edc98f",
  "blockheight": 68846,
  "blockindex": 1,
  "blocktime": 1639633391,
  "txid": "008e3e0e73344656752212cdbf132b8d5444cff6480e2271b7ed9098da470221",
  "walletconflicts": [
  ],
  "time": 1639633373,
  "timereceived": 1639633373,
  "bip125-replaceable": "no",
  "details": [
    {
      "address": "tb1q2tsumy3d27wywc5h7qesrj9gpf8yq77lm347tk",
      "category": "send",
      "amount": -0.01800000,
      "label": "",
      "vout": 0,
      "fee": -0.00200000,
      "abandoned": false
    },
    {
      "address": "tb1qlqgank4p07n2v983nvxvgudsw0d897e0evec2z",
      "category": "send",
      "amount": -0.02000000,
      "label": "",
      "vout": 1,
      "fee": -0.00200000,
      "abandoned": false
    },
    {
      "address": "tb1qc5ypny9gt665l7v8scdg8dg9gjkskrn022d63p",
      "category": "send",
      "amount": -0.02000000,
      "label": "",
      "vout": 2,
      "fee": -0.00200000,
      "abandoned": false
    },
    {
      "address": "tb1qduwfeu8fnne6tv00wymlkkpnjzfyay6zxkwcx3",
      "category": "send",
      "amount": -0.02000000,
      "label": "",
      "vout": 3,
      "fee": -0.00200000,
      "abandoned": false
    },
    {
      "address": "tb1qp5mxckz2p533umtggxw3jewwwq8c92zduygjsg",
      "category": "send",
      "amount": -0.02000000,
      "label": "",
      "vout": 4,
      "fee": -0.00200000,
      "abandoned": false
    },
    {
      "address": "tb1q2tsumy3d27wywc5h7qesrj9gpf8yq77lm347tk",
      "category": "receive",
      "amount": 0.01800000,
      "label": "",
      "vout": 0
    },
    {
      "address": "tb1qlqgank4p07n2v983nvxvgudsw0d897e0evec2z",
      "category": "receive",
      "amount": 0.02000000,
      "label": "",
      "vout": 1
    },
    {
      "address": "tb1qc5ypny9gt665l7v8scdg8dg9gjkskrn022d63p",
      "category": "receive",
      "amount": 0.02000000,
      "label": "",
      "vout": 2
    },
    {
      "address": "tb1qduwfeu8fnne6tv00wymlkkpnjzfyay6zxkwcx3",
      "category": "receive",
      "amount": 0.02000000,
      "label": "",
      "vout": 3
    },
    {
      "address": "tb1qp5mxckz2p533umtggxw3jewwwq8c92zduygjsg",
      "category": "receive",
      "amount": 0.02000000,
      "label": "",
      "vout": 4
    }
  ],
  "hex": "02000000000101f8803406c48596a8c4fcf122efa28cbdfa4baba323042ecf3a5826e7f70f525e0000000000ffffffff0540771b000000000016001452e1cd922d579c476297f03301c8a80a4e407bdf80841e0000000000160014f811d9daa17fa6a614f19b0cc471b073da72fb2f80841e0000000000160014c5081990a85eb54ff987861a83b50544ad0b0e6f80841e00000000001600146f1c9cf0e99cf3a5b1ef7137fb583390924e934280841e00000000001600140d366c584a0d231e6d68419d1965ce700f82a84d0247304402200dd1c6eead20c40a8ccfcef32723852229c1357467e222b37bccba66e15aeffc02201ddcccef96614cfce8d13108048f5ecad33b65fb6d8243c907f1853820f046a5012102f0696d231fce587bbb60584214f48bb4055d138def2854fb8f1fcb6b7eb91d5e00000000"
}


```
# Bech32のアドレス
'''
getnewaddress hoge bech32

tb1qkx5cglrqjrvpkcrlgqshr7ae4q7qya7vr5x2q2
'''

# base53アドレス
'''
getnewaddress hogehoge legacy
miYzxaQwQFfXdfxARr6JjUAiESk4PpsGuD
'''

# P2SHのアドレス
'''
createmultisig 2 '["03fcc8546e8feca858b6b41861962c5f22bcde8e4e63af2ac2368de59c5bfeb584","0322c3d0ff973d84460dc8f182e05a16c78c53786c113dfd26c55fbd7edc93adff","02719cf88e506ac458fbfffa7c820fb3223837fecbff7083b5f40f81860126c6dd"]' legacy

{
  "address": "2MyWtb4FqPy47EHvT9tVs4yH44pBc7CtM1j",
  "redeemScript": "522103fcc8546e8feca858b6b41861962c5f22bcde8e4e63af2ac2368de59c5bfeb584210322c3d0ff973d84460dc8f182e05a16c78c53786c113dfd26c55fbd7edc93adff2102719cf88e506ac458fbfffa7c820fb3223837fecbff7083b5f40f81860126c6dd53ae",
  "descriptor": "sh(multi(2,03fcc8546e8feca858b6b41861962c5f22bcde8e4e63af2ac2368de59c5bfeb584,0322c3d0ff973d84460dc8f182e05a16c78c53786c113dfd26c55fbd7edc93adff,02719cf88e506ac458fbfffa7c820fb3223837fecbff7083b5f40f81860126c6dd))#fhq8erkm"
}
'''

# P2WSHのアドレス

'''

createmultisig 2 '["03fcc8546e8feca858b6b41861962c5f22bcde8e4e63af2ac2368de59c5bfeb584","0322c3d0ff973d84460dc8f182e05a16c78c53786c113dfd26c55fbd7edc93adff","02719cf88e506ac458fbfffa7c820fb3223837fecbff7083b5f40f81860126c6dd"]' bech32

}
  "address": "tb1q87q20jrh9f9cek7dmge0sjddxrf70ncappskfpxqm468zlpcuccs68udu8",
  "redeemScript": "522103fcc8546e8feca858b6b41861962c5f22bcde8e4e63af2ac2368de59c5bfeb584210322c3d0ff973d84460dc8f182e05a16c78c53786c113dfd26c55fbd7edc93adff2102719cf88e506ac458fbfffa7c820fb3223837fecbff7083b5f40f81860126c6dd53ae",
  "descriptor": "wsh(multi(2,03fcc8546e8feca858b6b41861962c5f22bcde8e4e63af2ac2368de59c5bfeb584,0322c3d0ff973d84460dc8f182e05a16c78c53786c113dfd26c55fbd7edc93adff,02719cf88e506ac458fbfffa7c820fb3223837fecbff7083b5f40f81860126c6dd))#tee4lf5x"
}

'''

# P2PKHのトランザクション
'''
legacyアドレス
miYzxaQwQFfXdfxARr6JjUAiESk4PpsGuD


createrawtransaction  '[{"txid":"008e3e0e73344656752212cdbf132b8d5444cff6480e2271b7ed9098da470221","vout":1}]'  '[{"miYzxaQwQFfXdfxARr6JjUAiESk4PpsGuD":0.0198}]'

0200000001210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000100000000ffffffff0160361e00000000001976a914214b6ee7f165dcd25437d732cd5f5b8a11e1d5c488ac00000000


signrawtransactionwithwallet 0200000001210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000100000000ffffffff0160361e00000000001976a914214b6ee7f165dcd25437d732cd5f5b8a11e1d5c488ac00000000

{
  "hex": "02000000000101210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000100000000ffffffff0160361e00000000001976a914214b6ee7f165dcd25437d732cd5f5b8a11e1d5c488ac024730440220595d461905040e2f7bf4581984fdbb7f32224f4ab80659420bd973afb2541206022077e719e61df0f5eed9268e87fe04d7d3939672b3cda8c74e09f8f91a5b3d157d01210322c3d0ff973d84460dc8f182e05a16c78c53786c113dfd26c55fbd7edc93adff00000000",
  "complete": true
}

できたものの確認
decoderawtransaction 02000000000101210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000100000000ffffffff0160361e00000000001976a914214b6ee7f165dcd25437d732cd5f5b8a11e1d5c488ac024730440220595d461905040e2f7bf4581984fdbb7f32224f4ab80659420bd973afb2541206022077e719e61df0f5eed9268e87fe04d7d3939672b3cda8c74e09f8f91a5b3d157d01210322c3d0ff973d84460dc8f182e05a16c78c53786c113dfd26c55fbd7edc93adff00000000



￼
{
  "txid": "7b94a5d04d9bb6aad7295190ef5d279078dea673e625b47fc122703e8b4eb70d",
  "hash": "99362b74257040b6cc56f112ce3d1668d35f78a47f80e84f7ad9c8a85bacf121",
  "version": 2,
  "size": 194,
  "vsize": 113,
  "weight": 449,
  "locktime": 0,
  "vin": [
    {
      "txid": "008e3e0e73344656752212cdbf132b8d5444cff6480e2271b7ed9098da470221",
      "vout": 1,
      "scriptSig": {
        "asm": "",
        "hex": ""
      },
      "txinwitness": [
        "30440220595d461905040e2f7bf4581984fdbb7f32224f4ab80659420bd973afb2541206022077e719e61df0f5eed9268e87fe04d7d3939672b3cda8c74e09f8f91a5b3d157d01",
        "0322c3d0ff973d84460dc8f182e05a16c78c53786c113dfd26c55fbd7edc93adff"
      ],
      "sequence": 4294967295
    }
  ],
  "vout": [
    {
      "value": 0.01980000,
      "n": 0,
      "scriptPubKey": {
        "asm": "OP_DUP OP_HASH160 214b6ee7f165dcd25437d732cd5f5b8a11e1d5c4 OP_EQUALVERIFY OP_CHECKSIG",
        "hex": "76a914214b6ee7f165dcd25437d732cd5f5b8a11e1d5c488ac",
        "address": "miYzxaQwQFfXdfxARr6JjUAiESk4PpsGuD",
        "type": "pubkeyhash"
      }
    }
  ]
}

'''

# P2SHのトランザクション

'''
送金先のアドレス
2MyWtb4FqPy47EHvT9tVs4yH44pBc7CtM1j

createrawtransaction  '[{"txid":"008e3e0e73344656752212cdbf132b8d5444cff6480e2271b7ed9098da470221","vout":2}]'  '[{"2MyWtb4FqPy47EHvT9tVs4yH44pBc7CtM1j":0.0198}]'
0200000001210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000200000000ffffffff0160361e000000000017a91444c73724565d0965be127d338ee5a4c3025fa4618700000000

signrawtransactionwithwallet 0200000001210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000200000000ffffffff0160361e000000000017a91444c73724565d0965be127d338ee5a4c3025fa4618700000000

{
  "hex": "02000000000101210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000200000000ffffffff0160361e000000000017a91444c73724565d0965be127d338ee5a4c3025fa4618702473044022042505c930383b9368bfd75c03f586bdbdb0acadeefc796909a71d6e1a5f643e0022048edbb26bb5fc913620ae42f1b31d30b8d6ecb4b65608412c47e5c6cc48fe22f012102719cf88e506ac458fbfffa7c820fb3223837fecbff7083b5f40f81860126c6dd00000000",
  "complete": true
}


decoderawtransaction 02000000000101210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000200000000ffffffff0160361e000000000017a91444c73724565d0965be127d338ee5a4c3025fa4618702473044022042505c930383b9368bfd75c03f586bdbdb0acadeefc796909a71d6e1a5f643e0022048edbb26bb5fc913620ae42f1b31d30b8d6ecb4b65608412c47e5c6cc48fe22f012102719cf88e506ac458fbfffa7c820fb3223837fecbff7083b5f40f81860126c6dd00000000

{
  "txid": "d94b078fea471e2a9fab266cd4d101a8076039775c3e01eba0fa1c14db356f13",
  "hash": "971fce94d3bf035e00ceaf6eb5dfd772e7ee1018ad238645108ae4dcd414e61b",
  "version": 2,
  "size": 192,
  "vsize": 111,
  "weight": 441,
  "locktime": 0,
  "vin": [
    {
      "txid": "008e3e0e73344656752212cdbf132b8d5444cff6480e2271b7ed9098da470221",
      "vout": 2,
      "scriptSig": {
        "asm": "",
        "hex": ""
      },
      "txinwitness": [
        "3044022042505c930383b9368bfd75c03f586bdbdb0acadeefc796909a71d6e1a5f643e0022048edbb26bb5fc913620ae42f1b31d30b8d6ecb4b65608412c47e5c6cc48fe22f01",
        "02719cf88e506ac458fbfffa7c820fb3223837fecbff7083b5f40f81860126c6dd"
      ],
      "sequence": 4294967295
    }
  ],
  "vout": [
    {
      "value": 0.01980000,
      "n": 0,
      "scriptPubKey": {
        "asm": "OP_HASH160 44c73724565d0965be127d338ee5a4c3025fa461 OP_EQUAL",
        "hex": "a91444c73724565d0965be127d338ee5a4c3025fa46187",
        "address": "2MyWtb4FqPy47EHvT9tVs4yH44pBc7CtM1j",
        "type": "scripthash"
      }
    }
  ]
}

'''

# P2WPKHのトランザクション
'''
送金先のアドレス
tb1qdptzkgec9qvfr7ydj9fl2xd0exy5fn5rdrf272

createrawtransaction  '[{"txid":"008e3e0e73344656752212cdbf132b8d5444cff6480e2271b7ed9098da470221","vout":3}]'  '[{"tb1qdptzkgec9qvfr7ydj9fl2xd0exy5fn5rdrf272":0.0198}]'

0200000001210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000300000000ffffffff0160361e000000000016001468562b2338281891f88d9153f519afc98944ce8300000000

signrawtransactionwithwallet 0200000001210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000300000000ffffffff0160361e000000000016001468562b2338281891f88d9153f519afc98944ce8300000000

{
  "hex": "02000000000101210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000300000000ffffffff0160361e000000000016001468562b2338281891f88d9153f519afc98944ce8302473044022038de23b36abb63f154c10f554ec55523ca9d32c9c8fae5cee1ef4b50ce4b631602202cbe0a2159ab4adaea840f13a8f009538924e4f40f7d690e9e17d19fe96d80950121027419777d0385d51d313236204632fbe750a3574c1ad225cf461e1117fdc227d000000000",
  "complete": true
}

確認
decoderawtransaction 02000000000101210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000300000000ffffffff0160361e000000000016001468562b2338281891f88d9153f519afc98944ce8302473044022038de23b36abb63f154c10f554ec55523ca9d32c9c8fae5cee1ef4b50ce4b631602202cbe0a2159ab4adaea840f13a8f009538924e4f40f7d690e9e17d19fe96d80950121027419777d0385d51d313236204632fbe750a3574c1ad225cf461e1117fdc227d000000000


{
  "txid": "cc77d1352bc375499ebb342beb13ce9243168ef751b0e09ee27c4407003e1899",
  "hash": "14dfc48525ce643a5b5af8dff059151dc9b55fa2a931f7d284878e0bd4e6b106",
  "version": 2,
  "size": 191,
  "vsize": 110,
  "weight": 437,
  "locktime": 0,
  "vin": [
    {
      "txid": "008e3e0e73344656752212cdbf132b8d5444cff6480e2271b7ed9098da470221",
      "vout": 3,
      "scriptSig": {
        "asm": "",
        "hex": ""
      },
      "txinwitness": [
        "3044022038de23b36abb63f154c10f554ec55523ca9d32c9c8fae5cee1ef4b50ce4b631602202cbe0a2159ab4adaea840f13a8f009538924e4f40f7d690e9e17d19fe96d809501",
        "027419777d0385d51d313236204632fbe750a3574c1ad225cf461e1117fdc227d0"
      ],
      "sequence": 4294967295
    }
  ],
  "vout": [
    {
      "value": 0.01980000,
      "n": 0,
      "scriptPubKey": {
        "asm": "0 68562b2338281891f88d9153f519afc98944ce83",
        "hex": "001468562b2338281891f88d9153f519afc98944ce83",
        "address": "tb1qdptzkgec9qvfr7ydj9fl2xd0exy5fn5rdrf272",
        "type": "witness_v0_keyhash"
      }
    }
  ]
}

'''
# P2WSH
'''
アドレス
tb1q87q20jrh9f9cek7dmge0sjddxrf70ncappskfpxqm468zlpcuccs68udu8

createrawtransaction  '[{"txid":"008e3e0e73344656752212cdbf132b8d5444cff6480e2271b7ed9098da470221","vout":4}]' '[{"tb1q87q20jrh9f9cek7dmge0sjddxrf70ncappskfpxqm468zlpcuccs68udu8":0.0198}]'

15:00:38
￼
createrawtransaction  '[{"txid":"008e3e0e73344656752212cdbf132b8d5444cff6480e2271b7ed9098da470221","vout":4}]' '[{"tb1q87q20jrh9f9cek7dmge0sjddxrf70ncappskfpxqm468zlpcuccs68udu8":0.0198}]'

0200000001210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000400000000ffffffff0160361e00000000002200203f80a7c8772a4b8cdbcdda32f849ad30d3e7cf1d08616484c0dd74717c38e63100000000

signrawtransactionwithwallet 0200000001210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000400000000ffffffff0160361e00000000002200203f80a7c8772a4b8cdbcdda32f849ad30d3e7cf1d08616484c0dd74717c38e63100000000

{
  "hex": "02000000000101210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000400000000ffffffff0160361e00000000002200203f80a7c8772a4b8cdbcdda32f849ad30d3e7cf1d08616484c0dd74717c38e63102473044022040b9907010220eaeb2b2a42bf1bc23e555fb535d659f215c8023ff0f0ee2579f02205522fc13458b9c8730e64794e8f1ece2101e661438b6b454874e14ccedf17f220121021dfcdb8c9c2ca894efc4b705622efb23fb2f1c5edc856787ac4a9518fa27b57100000000",
  "complete": true
}

decoderawtransaction 02000000000101210247da9890edb771220e48f6cf44548d2b13bfcd122275564634730e3e8e000400000000ffffffff0160361e00000000002200203f80a7c8772a4b8cdbcdda32f849ad30d3e7cf1d08616484c0dd74717c38e63102473044022040b9907010220eaeb2b2a42bf1bc23e555fb535d659f215c8023ff0f0ee2579f02205522fc13458b9c8730e64794e8f1ece2101e661438b6b454874e14ccedf17f220121021dfcdb8c9c2ca894efc4b705622efb23fb2f1c5edc856787ac4a9518fa27b57100000000


{
  "txid": "c39c9dadad0dc95e3dea6c7aa8b68ab7e4f1d098d23b6b06c319cf822e71c613",
  "hash": "cda1eb8e93ebcd01df2b72436b69130ddab36bfaace84c01ba021ff767ca6912",
  "version": 2,
  "size": 203,
  "vsize": 122,
  "weight": 485,
  "locktime": 0,
  "vin": [
    {
      "txid": "008e3e0e73344656752212cdbf132b8d5444cff6480e2271b7ed9098da470221",
      "vout": 4,
      "scriptSig": {
        "asm": "",
        "hex": ""
      },
      "txinwitness": [
        "3044022040b9907010220eaeb2b2a42bf1bc23e555fb535d659f215c8023ff0f0ee2579f02205522fc13458b9c8730e64794e8f1ece2101e661438b6b454874e14ccedf17f2201",
        "021dfcdb8c9c2ca894efc4b705622efb23fb2f1c5edc856787ac4a9518fa27b571"
      ],
      "sequence": 4294967295
    }
  ],
  "vout": [
    {
      "value": 0.01980000,
      "n": 0,
      "scriptPubKey": {
        "asm": "0 3f80a7c8772a4b8cdbcdda32f849ad30d3e7cf1d08616484c0dd74717c38e631",
        "hex": "00203f80a7c8772a4b8cdbcdda32f849ad30d3e7cf1d08616484c0dd74717c38e631",
        "address": "tb1q87q20jrh9f9cek7dmge0sjddxrf70ncappskfpxqm468zlpcuccs68udu8",
        "type": "witness_v0_scripthash"
      }
    }
  ]
}

'''


# P2PKのトランザクション

'''


'''
