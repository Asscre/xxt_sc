# 24SC / 24XD 顶层同名模块清单（共享层）

路径：`soucre/24SC/24SC.xpp` 与 `soucre/24XD/24XD.xpp` **顶层同名**文件（`ls` 对比生成）。

修改下列任一文件时，应假设 **两包行为均可受影响**，需在 XXTouch 中分别打开两个 `.xpp` 验证。

## 同名文件（共享）

- `Info.lua`（包元数据：版本号不同，合并时注意）
- `main.xxt`
- `interface.xuic`
- `xui-sub.xuic`
- `appicon.png`
- `LeiShe.xxt`
- `Xiadan.xxt`
- `nLog.xxt`
- `pjy.xxt`
- `pjy_jh.xxt`
- `static_view.xxt`
- `text_replacement.xxt`
- `ui_element.xxt`
- `下单_JD复登.xxt`
- `下单_公共界面.xxt`
- `下单_设置地址.xxt`
- `代付相关函数.xxt`
- `商品标题读取.xxt`
- `处理上次出现的界面.xxt`
- `复登相关函数.xxt`
- `序列号.xxt`
- `旋转轨迹.xxt`
- `滑块轨迹.xxt`
- `激活函数.xxt`
- `生成所需文件.xxt`
- `界面处理主函数.xxt`
- `脚本配置界面.xxt`
- `设置地址相关函数.xxt`
- `设置时间.xxt`
- `res`（目录名相同；内部 PNG 数量与内容可能不同，勿假设完全一致）

## 仅 24SC 顶层存在

- `收菜_删除订单.xxt`
- `收菜_永久删除.xxt`
- `收菜_确认收货.xxt`
- `收菜_确认收货返回.xxt`
- `收菜_评价.xxt`
- `收菜_评价返回.xxt`
- `收菜相关函数.xxt`
- `确认收货函数.xxt`
- `确认收货或评价主函数.xxt`
- `算法滑动.xxt`
- `设置地址主程序.xxt`
- `评价函数.xxt`

## 仅 24XD 顶层存在

- `TouchIOS.xxt`
- `下单_APP下单.xxt`
- `下单_扫码付款.xxt`
- `下单_返回到首页.xxt`
- `下单_领优惠券.xxt`
- `下单主函数.xxt`
- `下单相关函数.xxt`
- `下单相关截图函数.xxt`
- `下载图片函数.xxt`
- `备用代码.xxt`

## 后续「抽公共模块」建议流程

1. 在 XXTouch 中固定 **一份主副本**（建议以更新版本号更高的包为参考，当前 XD `BundleVersion` 为 1.0.861，SC 为 1.0.713）。
2. 对共享文件名做 **二进制或导出源码 diff**（若 IDE 支持导出 Lua）。
3. 合并差异后 **另一包替换同名文件** 并双端冒烟。
4. 将稳定后的共享层打成独立 **子 `.xpp` 或版本库**（按你团队规范）。
