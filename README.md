# 曹操CCminerproxy 抽水 8.0极致稳定版<防DDos CC攻击>
最稳定的ETC/BTC/ETH中转托管软件！ 比例调整为0-95.纯中转及0.35%内 无开发费

Telegram群组:https://t.me/+kMd0E1sTVHMwNDFl

软件仅供学习参考，请勿用于其他目的，不承担任何责任

BTC目前鱼池和btc.com稳定测试通过，币印 和蚂蚁 也可使用。

注意：BTC钱包必须使用相对应矿池的用户名抽水 不能使用钱包地址

BTC由于存在大量的大政奉还和难度不一情况，你实际得到的托管费会显著低于你设定的值，开发费也一样，优先保证客户低拒绝率

# 开发费模型
``` javascript
//开发费百分比，taxPercent是你设置的抽水百分比
var devPercent = 0;
if (taxPercent <= 0.35) {
    //小于等于0.35的，无需开发费，感谢你为广大挖矿爱好者做出的贡献
    devPercent = 0;
} else if (taxPercent <= 1) {
    //大于0.35小于等于1的，开发费为你抽水比例的一半，以下所有开发费从客户那边算力收取，不影响你的收益
    devPercent = taxPercent / 2;
} else if (taxPercent <= 5) {
    //1到5的，固定开发费0.5%
    devPercent = 0.5;
} else if (taxPercent <= 10) {
    //5到10的，固定开发费1%
    devPercent = 1;
} else if (taxPercent <= 20) {
    //10到20的，固定开发费2%
    devPercent = 2;
} else {
    //20以上的，开发费线性增长，直到你的抽水比例为95%时，开发费为5%
    devPercent = 3 * (taxPercent - 20) / 75 + 2;
}
```

## 使用方法
[Windows](https://github.com/ccminerproxy/CC-MinerProxy/tree/master/windows/)

[Linux](https://github.com/ccminerproxy/CC-MinerProxy/tree/master/linux/)(支持一键脚本安装)

所有版本均包含一个网页版的监控平台，可配置是否启用

你可以同时添加两个抽水账户，并对每个账户分别设置抽水比例，两个账户抽数比例加起来不能超过95%

现在抽水比例可以设置为0，纯转发，同样不收取开发费

## 日你妈
我的忧伤,你是煞笔

GuoT,你也是煞笔



## 其他
请只设定足够平衡你支出的托管抽水比例，不要抽大动脉，做到可持续发展，托管时请一定告知客户存在托管费

ETH/ETC的归集功能由于跨池存在难度、协议不一致等原因，可能导致你抽到的算力过大/过小甚至于无法抽取等情况

4核心4G内存的搬瓦工，带机6000台，测试4天，机器稳定不掉线

如果你经常掉线：

①第一检查挖矿软件配置及内核配置，是否设置超过多少分钟没有成功提交重启内核

②查看你服务器的硬件配置及软件带宽，配置过低可能导致转发性能不足，导致TCP重发及超时

③检查你服务器的网络是否占用超过60%以上，是的话加带宽

④检查你的抽水情况，如果一直没抽到，你的配置可能存在问题，导致各种断连情况，特别是蚂蚁、币安、OK、HIVE等池子
