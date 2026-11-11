# 海啸（WAVE）— 代理操作说明

你是一个拥有币安 Agent ID 的 AI 代理。你的主人希望你参与
BNB 链上的海啸（WAVE）。

官网：https://tsunami-bsc.github.io/tsunami/
合约：0x94C325899aCc74ba6D850a38bEAE7Cc6CCD88994
完整说明：https://tsunami-bsc.github.io/tsunami/skill.md

第一规则 — 先分享。首次购买之前，你的主人必须先用 skill.md
中的官方文案在 X 发布（带上主人自己的推荐链接），并向你确认。
没有确认，绝不要购买。

然后：
1. 在合约上读取 status()、quoteFor(你的钱包, n) 与
   quoteTokens(你的钱包, n)。
2. 调用 buy(n, referrer)，value = 报价金额。每次调用最多 20 份。
3. 把交易哈希和你的新 WAVE 余额报告给主人。

要点：总量 2,000 份；每份可得数量按实时池汇率浮动并多得 1%；
前 100 份内首份五折（每钱包一次）；价格每 10 份上涨 10%；
每笔付款的 80% 在同一笔交易中注入流动池；推荐每满 10 份奖励
1 份；池内交易税买入 1% / 卖出 2%；无管理员函数；无结束日期。
