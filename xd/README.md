# 24XD（下单）工作区

- **参考 XPP 包**（只读来源）：[`../soucre/24XD/24XD.xpp`](../soucre/24XD/24XD.xpp)
- **开发计划与任务表**：[`../docs/jd-xxtouch-24XD-development-plan.md`](../docs/jd-xxtouch-24XD-development-plan.md)
- **实施进度日志**：[`../implementation-plan.mdc`](../implementation-plan.mdc)（文中「24XD 功能实施进度」一节）
- **逐步核对指南（IDE 校准、状态机、封装/`res` 表、合规闸门、回归清单）**：[`../docs/24XD-implementation-guide.md`](../docs/24XD-implementation-guide.md)

建议在 **XXTouch IDE** 中直接打开上述 `.xpp` 目录进行编辑与调试；本目录用于存放你从 IDE 导出或整理的笔记、配置样例（按需添加文件）。Git 内通常只保留 [`Info.lua`](../soucre/24XD/24XD.xpp/Info.lua) 等元数据，业务脚本以本地完整包为准。

**合规**：支付、扫码、代付相关自动化边界须遵守 [`../docs/jd-xxtouch-24XD-development-plan.md`](../docs/jd-xxtouch-24XD-development-plan.md) §3。

**双包纪律**：修改与 24SC **同名**顶层脚本或共享资源前，必读 [`../docs/shared-modules-manifest.md`](../docs/shared-modules-manifest.md)，并在两包各跑一次冒烟。

**推荐顺序**：入口与 XUI（XD-1）→ `下单主函数` 状态机（XD-2）→ `下单_APP下单` 最小闭环（XD-3）→ 封装与 `res/`（XD-4～5）→ 与 SC 同源界面与地址（XD-6～7、XD-16）→ 优惠券与返首页（XD-8～9）→ 扫码与代付合规闸门后再联动（XD-10～11）→ 复登与 TouchIOS（XD-12～13）→ 下载与备用代码（XD-14～15）→ 文档 §4 整体验证；细则见实施指南。
