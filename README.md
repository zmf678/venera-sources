# Venera 漫画源整合仓库

汇总 5 个公开的 Venera 漫画源仓库，按 `key` 去重、合并同名/同站点的备用与精简版，共 **148** 个源。所有脚本均通过 JavaScript 语法与 `ComicSource` 结构静态校验。

> 本仓库只存放源脚本与索引，不托管、不内置任何漫画内容。

## 订阅地址

- GitHub Raw：`https://raw.githubusercontent.com/zmf678/venera-sources/main/index.json`
- jsDelivr（国内较快）：`https://cdn.jsdelivr.net/gh/zmf678/venera-sources@main/index.json`

在 Venera / VeneraNext / Venera Prime / VeneraX 中打开「漫画源 → 添加来源 / 源仓库」，粘贴上面的 `index.json` 地址，识别预览后勾选需要的源安装。

## 统计

| 项目 | 数量 |
|---|---|
| 上游原始条目 | 382 |
| 去重后唯一 key | 176 |
| 同名精简版合并后 | 155 |
| 同站点备用/重复版再合并后 | 148 |
| 静态校验失败 | 0 |

来源分布：Junkrat9527/venera-sources 59、weihanlong267-spec/Venera-Next-sources 48、handahao666-boop/venera_comic_source 29、venera-app/venera-configs 12。

## 去重规则

- 同一 `key`：保留版本号最高的一份，版本相同则优先来源更新、文件更完整的。
- 同名或同站点：只保留主实现，去掉“备用”“X版”“W版”等重复入口和 5KB 左右的精简模板版。
- 保留 `拷贝漫画M`（多账号版）这类功能确实不同的变体。
- 未做联网可用性测试：源站是否可访问、是否需要登录/代理、是否被 Cloudflare 拦截，需在 App 内实际验证。

## 说明

- 部分源为成人向内容，请确认你已成年，并遵守所在地法律与目标站点条款。
- 脚本版权归原作者，许可证以原仓库为准；本仓库仅做索引整理、去重与镜像，未对脚本重新授权。
- 若原作者不希望被收录，请开 Issue，我会删除对应文件。
- 源站改版会导致脚本失效；建议同时保留上游仓库作为更新来源。

## 文件

- `index.json`：源索引，供 App 订阅
- `*.js`：源脚本
- `SOURCES.md`：每个源的名称、版本、来源仓库与上游文件
