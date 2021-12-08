'''

"txid": "a8731e3213cc651e96247d8c6b6fe9743af63df2bd12127db0d10af5a259b297",
    "vout": 0,
    "address": "tb1q38qqa0lgxve0uekezt84lgjqhv8nekq8tjwpuq",
    "label": "",
    "scriptPubKey": "001489c00ebfe83332fe66d912cf5fa240bb0f3cd807",
    "amount": 0.10000000,
gettransaction
020000000001019bc917ef29b51eed7f021c5080a040564438052af90d2a8c7a36115c3e3474ac0100000000feffffff02809698000000000016001489c00ebfe83332fe66d912cf5fa240bb0f3cd807ca797a1f5d06000016001490c9ed0c7c60faa9486f5cc1e61cd79bdbc1d79a0247304402206d84bd251318b685650be14b1830972d616b077d810888d59ebcb73d4f05c95c022052ba637f95d6a5094b0d725f4b597b1343527330bdd42fa293e922b35f89e4a40121030abbf8cbd1a39d2dda27a6898802a40178cd0e782c8018daa44e97ac8957005458dd0000

Aliceのアドレス
tb1q38qqa0lgxve0uekezt84lgjqhv8nekq8tjwpuq

Bobのアドレス
tb1qk70ukq6qud409kl2fxys8p0u9p964z26hmf85w

Aliceの秘密鍵
cTbgUy1n6kWiuCRBnSENSikQzLBcvMhv1diHq7kcMEfLJo6mMo6w

Bobの秘密鍵
cW3Dk8KrQc5ScqcAw2Tax8ESVSDE9ZKusiCiZZ6CNVFqq7E4N7s1


Aliceの公開鍵
"pubkey": "02ace577cb332aedbbf83f4c79c5edb065b19ec07fbff15e662ed415711d7f5715"

Bobの公開鍵
"pubkey": "03602a06dc26ba20ddf8fe1106f9d81536b02d46bf48a69e90b40850d7f70bcb82"









 require 'bitcoin'
=> true
>> require 'net/http'
=> true
>> require 'json'
=> false
>> Bitcoin.chain_params = :signet
>> HOST="localhost"
=> "localhost"
>> PORT=38332
=> 38332
>> RPCUSER="hoge"
=> "hoge"
>> RPCPASSWORD="hogehoge"
=> "hogehoge"
'''