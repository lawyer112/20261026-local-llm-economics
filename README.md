# 本地部署大模型，究竟用多少才划算？

How Much Must You Use a Local Language Model Before It Pays Off?

本地模型能运行，并不等于购买设备能够回本。本文将消费级硬件、推理引擎和低价在线方案放到同一框架中，比较真实负载下的吞吐、账单与回本条件。

**[中文全文 PDF](zh.pdf) · [English PDF](en.pdf) · [English introduction](#english) · [讨论与反馈](https://github.com/lawyer112/20261026-local-llm-economics/issues)**

作者：lawyer112 · 文章编号：20261026-local-llm-economics · 正文版本：0.3.1 · 本版日期：2026-10-28

## 论文简介

材料包括 2026 年 10 月 26—27 日核验的来源、在售硬件报价与一台 RTX 4090 上的测速和 613 个实际请求记录。情景使用同一 Token 结构和“引擎忙碌小时”口径，不启动付费调用。

- 短对话解码中位数为 102.4 Token/s，实际长上下文请求中位数约 32—34 Token/s，不能用峰值速度代替实际产能。
- 按历史截点与设定负载，每月 120 个忙碌小时的 DeepSeek 直连费用约 185—370 元；当时的 10 美元套餐在假定额度内可覆盖。
- 约 1.66 万元的 5070 主机，按本机吞吐、假定功耗和零残值计算，对比高峰直连需每月约 167 个忙碌小时才能三年回本，对比当时 GOAT 需约 329 小时。

这是历史截点的条件核算，不是当前报价或购买承诺。尚未评估回答质量、实测功耗或付费账户行为；其他设备吞吐、部分部件价格与残值为假设，挂单价格不是成交价。模型能否替代原有服务必须另测。

两份 PDF 均含完整正文、方法、限制与参考文献。计算复核与 AI 辅助自查的范围在正文说明，不等同于外部学术审稿。

## 讨论、协作与修订

欢迎通过 [Issues](https://github.com/lawyer112/20261026-local-llm-economics/issues) 提供反例、来源核对、计算复查或翻译建议。请注明**文章版本、语言、页码或段落、问题、建议及依据**。参与修改前，先在同一讨论中约定修改部分和版本基准，并明确资料核对、正文修订、英文校对与发布负责人。署名变化另行协商。

维护者将经讨论采用的修改整理进本地源稿，核对受影响的双语论断、数字、图表与引文。两种语言均核验后，将两份 PDF 和首页版本说明放在同一次提交中更新，并再次检查读者入口。只改首页说明或链接时，不增加正文版本；首页的小修也可提交 [Pull Request](https://github.com/lawyer112/20261026-local-llm-economics/pulls)。

本仓库是这篇文章的统一公开入口。其他获准渠道使用同一版本，并逐渠道核验；没有完成同步的渠道不标为新版本。公开文件只有本文介绍和两份全文 PDF，研究工作资料在本地保留。本篇未额外授予全文转载、改编或其他再利用许可；第三方资料保留其原有权利。

## 引用

lawyer112. (2026). *本地部署大模型，究竟用多少才划算？* (版本 0.3.1). https://github.com/lawyer112/20261026-local-llm-economics

引用请保留版本与链接，便于读者定位所用文本。

## English

### About the paper

Being able to run a model locally does not establish that buying hardware will pay off. This paper compares consumer hardware, inference engines, and low-cost online routes using actual workload throughput, bills, and break-even conditions.

**[Complete English PDF](en.pdf) · [Chinese PDF](zh.pdf) · [Discussion and feedback](https://github.com/lawyer112/20261026-local-llm-economics/issues)**

Author: lawyer112 · Paper ID: 20261026-local-llm-economics · Content version: 0.3.1 · Edition date: 28 October 2026

Materials include sources verified on 26–27 October 2026, listed hardware prices, a speed suite, and 613 real requests on one RTX 4090 machine. Scenarios share one token mix and an engine-busy-hour measure; no paid API calls are needed.

- Short-dialogue median decoding was 102.4 tokens/s, compared with roughly 32–34 tokens/s for real long-context requests. Peak speed should not substitute for workload throughput.
- At the historical cutoff and stipulated workload, 120 monthly busy hours cost about CNY 185–370 through the direct DeepSeek API; the then-current USD 10 plans could cover them within the assumed allowances.
- A roughly CNY 16,600 RTX 5070 PC needs about 167 monthly busy hours to recover cost in three years against peak direct-API pricing, or 329 against the historical GOAT plan, assuming the measured machine’s throughput, stipulated power, and zero residual value.

This is a conditional calculation at a historical cutoff, not a current quotation or purchasing promise. Answer quality, actual power, and paid-account behavior were not tested. Other devices’ throughput, some component prices, and residual values are assumptions; listed prices are not transaction prices. Replacement quality requires separate evaluation.

Both PDFs contain the complete text, methods, limitations, and references. The paper explains the scope of computational verification and AI-assisted self-checks; these are not external academic review.

### Discussion, collaboration, and revisions

Use [Issues](https://github.com/lawyer112/20261026-local-llm-economics/issues) for counterexamples, source checks, computational verification, or translation suggestions. Include the **version, language, page or passage, problem, proposed change, and supporting evidence**. Before editing, agree the scope and baseline version in the same discussion and identify responsibility for sources, substantive revision, English review, and release. Authorship changes are agreed separately.

The maintainer incorporates agreed changes into the local manuscripts and checks affected bilingual claims, numbers, figures, and references. Once both languages are verified, both PDFs and the README version information are updated in one commit and reader access is checked again. Changes confined to this introduction or its links leave the content version unchanged; small README corrections may also be proposed through a [Pull Request](https://github.com/lawyer112/20261026-local-llm-economics/pulls).

This repository is the canonical public entry for the paper. Any separately authorized channels use the same version and are individually verified; channels awaiting synchronization are not labeled as updated. The public files are this introduction and the two full-text PDFs; research working materials remain local. No additional license for full-text republication, adaptation, or other reuse is granted; third-party materials retain their existing rights.

### Citation

lawyer112. (2026). *How Much Must You Use a Local Language Model Before It Pays Off?* (Version 0.3.1). https://github.com/lawyer112/20261026-local-llm-economics

Retain the version and link when citing so readers can identify the text used.
