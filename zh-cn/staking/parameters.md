# 星系共识中术语和参数释义

有关星系共识的技术黄皮书，可点击这里获取。

下面我们列出了关键的术语和参数值。

**WAN：** WAN是验证节点进行质押的指定代币，节点通过质押参与确定Wanchain网络运行的安全和稳定。通过提高质押WAN代币数量和质押时间，验证节点可以赚取更多的权益能量（Staking Power），从而提高奖励概率。在一个Epoch时间段内，如果一个验证节点被选为RNP（Random Number Proposer）或EL（Epoch Leader），则这个验证节点和委托给此节点的委托人都将获得WAN代币奖励。由于WAN代币同样作为Wanchain生态应用的交易手续费和跨链交易手续费，所以在一个Epoch内，验证节点和委托人也享有交易手续费的奖励。
 
**验证节点（Validator）：** 验证节点可被选中成为RNP或EL的角色，参与星系共识过程，进行区块的提出、验证和最终确认，从而保证网络安全稳定的运行。验证节点有两种类型，可接受委托的受托验证节点和不可接受委托的普通验证节点。一个Epoch大约持续一天，因此每个月约有30个Epoch。运行受托验证节点所需要的WAN代币数量门槛（50,000 WAN）要高于普通验证节点的WAN代币门槛（10,000 WAN）。
 
**普通验证节点（Non-delegate Node）：** 普通验证节点的质押门槛不高，只需10,000WAN起。但普通验证节点不具有接受委托的权利。除此之外，普通验证节点和受托验证节点在星系共识过程中享有的权利和应尽的义务完全相同。如果希望能够吸引大量的WAN代币委托，建议用户运营受托验证节点。

**受托验证节点（Delegate Node）：** 受托验证节点和普通验证节点的权利和义务相同，除此之外，受托验证节点额外享有接受委托的权利。受托节点的最低质押门槛是50,000 WAN ，上限为1050万WAN。受托节点质押WAN的数量和可接受委托的WAN数量比值为1:10（详细说明参见释义“委托比率”）。受托节点可自由设置委托费率。

**委托人（Delegator）：** 委托人可将WAN代币委托给任意受托验证节点。委托人最低委托数量为100 WAN。
 
**委托比率（Delegate Ratio）：** 单个受托验证节点和其上的委托人之间的代币质押比率，目前为1：10。如果委托额达到该比率，为接受更多的委托，受托节点需要质押更多的WAN。例如：某受托节点质押了100,000 WAN，则该节点最多可接受1,000,000 WAN的委托。如果该受托节点达到了1,000,000 WAN委托量但仍希望能够接受更多委托，则该节点需要通过质押更多WAN来提高其委托额。
  
**Epoch：** 1个Epoch代表一轮共识协议周期。1个Epoch大约为1天。在1Epoch周期内，约产生17,280个区块，被选中成为RNP或EL的验证节点将得到WAN代币奖励。
 
**RNP（Random Number Proposer）：** 在每轮Epoch时间段内，根据验证节点的WAN代币质押量和质押时间等因子，从所有验证节点中选取25个验证节点组成RNP组。RNP组内成员（即被选中的验证节点）负责生成随机数以供协议进行随机选择时使用。RNP组产生的随机数将用于下一轮RNP组、EL组选择和出块者选择等工作。
 
**EL（Epoch Leader）：** 在每轮Epoch时间段内，根据验证节点的WAN代币质押量和质押时间等因子，从所有验证节点中选取24个验证节点组成EL组（EL组总共有验证节点50个，其中基金会暂时自持26个但不享有收益，对外开放24个）。EL组内成员（即被选中的验证节点）负责收集交易、打包出块。EL组需要完成两个周期的工作，第一个周期通过完成秘密信息序列（secret message array）的协商来完成EL组内部秘密数据的共享，第二个周期通过秘密信息序列和链上随机数确定出块权归属，并在自身负责出块的时间段内打包区块并广播，完成链的生长发展。
 
**验证节点选中概率：** 验证节点选中概率由该验证节点的质押WAN代币数量、质押时长以及节点活性相关（活性大小受该节点在共识过程中的发交易行为和出块行为影响）。质押的WAN数量越多，质押时间越长，节点活性越高，则该节点被选为EL或者RNP组员并获得出块权的概率越大，从而获得的奖励越多。
 
**到账延迟（Withdraw Delay）：** 验证节点参与质押到期后的到账时间会有1天延迟。委托人如果跟随验证节点到期后退出，则同样是1天延迟；但如果委托人中途退出，会有3-4天延迟。

**委托费率（Commission Rate）：** 受托验证节点可自由设置委托费率，委托人委托WAN代币给受托节点，会被收取委托费用。委托费率的精度为万分之一，即0.01%。目前市场上合理的委托费率为10%-20%。

**参数汇总**
- **受托验证节点最低质押门槛：** 50,000 WAN
- **委托比率：** 1:10
- **普通验证节点最低质押门槛：** 10,000 WAN，不可接受委托
- **委托人最低门槛：** 100 WAN
- **验证节点数量：** 75个，其中对外公开49个，基金会暂时自持26个（基金会自持节点只运营但无收益，且未来会逐渐全部开放）
- **单个验证节点质押总量上限：** 1050万WAN。该值为该验证节点自身的质押量和该验证节点接收的委托量之和的上限。
- **无增发：** 预留21,000,000 WAN作为奖励，首年2,500,000 WAN，此后逐年递减12%
- **验证节点质押锁定时间：** 7天至90天，自主选择。质押到期后，质押的WAN币在1天内到账。
- **委托人委托质押锁定时间：** 随时参与，随时退出（如到期退出，质押的WAN币在1天内到账；如中途退出，质押WAN币3-4天内到账）。 


