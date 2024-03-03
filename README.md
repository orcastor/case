<p align="center">
  <a href="https://orcastor.github.io/doc/">
    <img src="https://orcastor.github.io/doc/logo.svg">
  </a>
</p>

<h1 align="center"><strong>OrcaS 3D打印外壳</strong></h1>

# BOM表

## 打印件

> 衍生自[@汪汪队射手](https://space.bilibili.com/300702869)的[QNAS Mini](https://github.com/thunder439/QNASMINI)，增加了自制背板

|类型|数量|材料|1.75mm用量|100mm/s耗时|精度|配置|注意事项|
|-|-|-|-|-|-|-|-|
|外壳|1|PETG/PLA/ABS|244g 103.89m|31h8min|0.2mm|2层墙，2层顶底，20%锯齿填充||
|内框|1|PETG/PLA/ABS|||0.2mm|2层墙，0层顶底，30%锯齿填充||
|硬盘笼|1|PETG/PLA/ABS|151g 50.55m|33h23min|0.2mm|2层墙，0层顶底，40%锯齿填充||
|硬盘支架|6|PETG/ABS|11g 3.54m|1h51min|0.2mm|3层墙，0层顶底，30%锯齿填充||
|背板|1|PETG/ABS|22g|5h12min|0.12mm/0.16mm|2层墙，1层顶底，60%锯齿填充|注意凹槽向下，可能要反过来打|
|背盖|6|PETG/ABS|1g 0.39m|17min|0.12mm/0.16mm|2层墙，0层顶底，50%锯齿填充||

## 采购件

|类型|数量|价格|配置|
|-|-|-|-|
|Orange Pi 5（4G）主板|1|￥500|
|裸板易驱线（送数据线）|6|￥10|主控JMS577泰国产
|Type-C -> USB3.0×4 Hub|1|￥20|
|5V4A Type-C电源|1|￥20|
|Type-C两焊点母座|1|￥2.5|
|Type-C公头带软排线|1|￥7|
|热缩管|3|￥3|164根|
|4010风扇|2|￥7|
|JST-2P 母头|1|￥2.5|5根|
|20×35mm过线防尘橡胶圈|1|￥2|4个|
|40×20×3mm硅胶脚垫|4|￥10|6个|
|M3带螺母14mm（风扇）|8|￥3|20套|
|M1.7×6自攻螺丝（背盖）|24|￥4|200颗|
|M3×4.8（硬盘）|24|￥5|100颗|
|M3×7沉头内六角（内框）|4|￥2|5颗|

<h2 align="center">自制背板成本低至23%</h2>

### 使用裸板易驱线替换6盘位背板

原方案：

|类型|数量|价格|
|-|-|-|
|6盘位背板|1|￥150|
|M.2转6口SATA|1|￥115|
|SATA线|6|￥13|
|总计||￥343|

新方案：

|类型|数量|价格|
|-|-|-|
|裸板易驱线（送数据线）|6|￥10|
|Type-C -> USB3.0×4 Hub|1|￥20|
|总计||￥80|

### 效果（严丝合缝）

<a href="https://raw.githubusercontent.com/orcastor/case/master/assets/inner.jpg">
  <img src="./assets/inner.jpg" width="20%" />
</a><a href="https://raw.githubusercontent.com/orcastor/case/master/assets/outter.jpg">
  <img src="./assets/outter.jpg" width="29.3%" />
</a><a href="https://raw.githubusercontent.com/orcastor/case/master/assets/match.jpg">
  <img src="./assets/match.jpg" width="22%" />
</a>

### 优势：

- 只有USB 3.1 Type-C接口的情况下（比如Orange Pi 5主板）
- PCIe 2.0 ×1的接口（500 MB/s）没有USB 3.1 Type-C（1280 MB/s）的速度快，该方案更合适

<h2 align="center">为什么选择Rockchip而不是Intel？</h2>

- 性能对比 [J4125 vs RK3588S](https://gadgetversus.com/processor/intel-celeron-j4125-vs-rockchip-rk3588s/)

|核心|优势|
|-|-|
|Intel Celeron J4125|x86架构，应用支持广泛；PCIe通道多|
|Rockchip RK3588S|CPU Mark高了一倍；AI算力6T ops；内存上限32GB；核心数多一倍（8核）；GPU FLOPS4倍多|
