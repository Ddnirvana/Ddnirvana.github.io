# Publication verification, 2026-11-04

This update covers the eight missing entries in the IPADS publications index and the independently verified Bes-Mode journal paper. ACM/IEEE entries use publisher-registered Crossref metadata; USENIX entries use official presentation-page BibTeX. DeltaBox is provisional.

## Verified sources and decisions

### MeldKernel / SOSP 2026

Title: Taming Dynamism on GPUs: Cross-SM Kernel Fusion via SM Cooperation and Just-in-Time Reduction.
Authors: Jingkai He; Guangda Sun; TianJian Li; Dong Du; Yubin Xia; Haibo Chen.
DOI: 10.1145/3830418.3843857. ACM. Proceedings of the ACM SIGOPS 32nd Symposium on Operating Systems Principles. Pages 1070--1090. Year 2026. Publisher spells TianJian with a capital J; retained.

- https://sigops.org/s/conferences/sosp/2026/schedule.html (official program links this DOI)
- https://api.crossref.org/works/10.1145/3830418.3843857 (ACM-registered metadata)
- https://api.crossref.org/works/10.1145/3830418.3843857/transform/application/x-bibtex
- ACM DL page returned 403 to this tool; no claim of downloading an ACM DL export.

### CHIME / ISCA 2026

Title: CHIME: A Case for Efficient Long-Context Attention-FC Disaggregated Inference with DIMM-PIM.
Authors: Qingyuan Liu; Liyan Chen; Haocheng Wang; Yanning Yang; Dong Du; Zhigang Mao; Naifeng Jing; Yubin Xia; Haibo Chen.
DOI: 10.1109/ISCA66397.2026.00056. Publisher IEEE; conference 2026 ACM/IEEE 53rd Annual International Symposium on Computer Architecture (ISCA). Year 2026. Pages 1--17 in IEEE-registered Crossref record.

- https://api.crossref.org/works/10.1109/ISCA66397.2026.00056
- https://api.crossref.org/works/10.1109/ISCA66397.2026.00056/transform/application/x-bibtex
- https://iscaconf.org/isca2026/program/
- Third-party EurekaMag lists 620--636, whereas publisher-registered Crossref gives 1--17. Use publisher record, keep discrepancy documented, do not silently merge values.

### Three OSDI 2026 papers

Exact USENIX BibTeX was extracted from official presentation pages. Publisher is USENIX Association, not ACM. DOI absent in official BibTeX; do not invent one.

1. Virtualizing eBPF with Late-Binding. Jing Zhang; Xiaguannan Song; Dong Du; Yubin Xia; Binyu Zang; Haibo Chen. Pages 2127--2148. https://www.usenix.org/conference/osdi26/presentation/zhang-jing
2. Disentangling Graph Dependencies for Efficient Billion-Scale GPU Vector Search. Haoru Zhao; Jingkai He; Jingyao Zeng; Mingkai Dong; Dong Du. Pages 1563--1584. https://www.usenix.org/conference/osdi26/presentation/zhao
3. Stop Pretending to Be Busy: A Case for Serverless Paradigms in Co-Located Batch Workloads (Operational Systems). Xiaohu Chai; Jianfeng Tan; Congsi Yuan; Bowen Yang; Hao Dai; Tongkai Yang; Chao Huang; Dong Du; Yu Chen. Pages 1967--1988. https://www.usenix.org/conference/osdi26/presentation/chai

All use 20th USENIX Symposium on Operating Systems Design and Implementation (OSDI 26); 2026; July; Seattle, WA; ISBN 978-1-939133-55-7. Quark's official BibTeX includes '(Operational Systems)' in title; retain unless intentionally presenting a shortened display title.

### DeltaBox / ATC 2026

The final official schedule and artifact results title: DeltaBox: Millisecond-Scale Sandbox Checkpoint and Rollback for Stateful AI Agents.
Authors: Yunpeng Dong; Jingkai He; Shiqi Liu; Yuze Hou; Dong Du; Zhonghu Xu; Si Yu; Baochuan Yang; Yubin Xia; Haibo Chen.
Conference: 2026 ACM SIGOPS Annual Technical Conference; November 15--18, 2026, Shatin, Hong Kong. This is future relative to verification date, so use accepted/forthcoming, not presented.

- https://sigops.org/s/conferences/atc/2026/schedule.html (final program, Session 21)
- https://sigops.org/s/conferences/atc/2026/accepted.html (older title deltaSandbox, rendered Greek delta)
- https://sysartifacts.github.io/atc2026/results (DeltaBox title; available/functional/reproduced badges)
- https://ipads.sjtu.edu.cn/zh/news/ (2026-09-22 announcement of ATC acceptance)
- Crossref queries by full title, DeltaBox, deltaSandbox, and first author found no matching paper. No paper DOI, ISBN, or page range verified. Artifact DOI 10.5281/zenodo.23202153 is NOT a paper DOI and must not be put in the paper's doi field.
- IPADS publications currently omits 'Sandbox' in the title. Prefer final conference schedule title for the bibliographic record; note the source discrepancy to the owner.

### Bes-Mode / TOCS 2026

Making Hardware Features Bespoke: Operating System Support for Bes-Mode Processes.
Authors: Bicheng Yang; Yuanpei Wu; Rongchuan Liu; Dong Du; Yubin Xia; Binyu Zang; Haibo Chen.
DOI 10.1145/3802921. ACM Transactions on Computer Systems, 44(3), August 2026, pages 1--29 in Crossref. Crossref does not give article number; do not add number from a third party as if publisher-verified.

- https://api.crossref.org/works/10.1145/3802921
- https://api.crossref.org/works/10.1145/3802921/transform/application/x-bibtex
- https://ipads.sjtu.edu.cn/zh/pub/members/bicheng_yang/
- https://sigops.org/s/conferences/sosp/2026/schedule.html lists invited TOCS talk (do not relabel this as a second SOSP paper).

### Existing records

- RhymeRL: ACM-registered final title is 'History Doesn't Repeat Itself but Rollouts Rhyme: Accelerating Reinforcement Learning with RhymeRL'; DOI10.1145/3779212.3790172; ASPLOS 2026 volume2, pages929--945. HistoRL on IPADS is an older naming variant. https://api.crossref.org/works/10.1145/3779212.3790172
- SYSSPEC: official FAST26 page explicitly says 'Awarded Best Paper!' and 'Distinguished Artifact Award Winner'. FAST2026 is correct, FAST2025 in old news is a typo. https://www.usenix.org/conference/fast26/presentation/liu-qingyuan

## Potential further gaps (not added or fully verified here)

IPADS Bicheng Yang page also lists 2026 TACO 'Semantics-aware Software Cache Coherence with Coherence Lock' and 2025 Chinese Journal of Computers SegTEE. DBLP Dong Du0003 lists 2026 TOCS 'Resource-Efficient Orchestration for Heterogeneous Serverless Computing with Harmonized Effectiveness and Practicability' and 2026 TCAD LayerTEE. These are leads for a future update, not verified entries included in this bibliography.

## Additional ACM records

- miniK8s: A Pedagogical Cloud-Native System. Dong Du, Mingyu Wu, Haibo Chen, Binyu Zang. Proceedings of the 57th ACM Technical Symposium on Computer Science Education V.1, 2026, pages 295–301. DOI https://doi.org/10.1145/3770762.3772592. Metadata/BibTeX: https://api.crossref.org/works/10.1145/3770762.3772592/transform/application/x-bibtex. Conference program: https://sigcse2026.sigcse.org/details/sigcse-ts-2026-Papers/109/miniK8s-A-Pedagogical-Cloud-Native-System.
- Offloading Cloud-Native Infrastructure with XpuPod. Bicheng Yang, Jingkai He, Dong Du, Yubin Xia, Haibo Chen. Proceedings of the 2025 ACM Symposium on Cloud Computing, pages 45–58. DOI https://doi.org/10.1145/3772052.3772211. Metadata/BibTeX: https://api.crossref.org/works/10.1145/3772052.3772211/transform/application/x-bibtex. Use the published proceedings year 2025 despite a conference schedule URL containing 2026.

## News dates and corrections

- DeltaBox: 2026-09-22; MeldKernel: 2026-07-08. Both are dated IPADS announcements at https://ipads.sjtu.edu.cn/zh/news/.
- miniK8s: 2025-09-24, the SJTU acceptance announcement at https://news.sjtu.edu.cn/jdzh/20250924/214607.html.
- The 2026-11-04 editorial publication-list update was withdrawn from public news at the owner’s request.
- FAST award news year corrected from 2025 to 2026. ASPLOS HistoRL name changed to final RhymeRL. ISCA CHIME title and OSDI FlowANN title match final proceedings. Existing news dates remain unchanged.
- The SOSP2025 Copier Best Paper award is supported by the dated IPADS award announcement (2025-10-14) at https://ipads.sjtu.edu.cn/zh/news/; the user's existing news date is preserved.

## Legacy bibliography repairs

- Removed a duplicate `and` in the 2025 Fork in the Road author field.
- Normalized malformed LaTeX braces in the 2025 OS Rendering title.
- Changed SplitPass's comma-separated author list to BibTeX's `and`-separated names without changing the names/order.
- Preserved Dong Du in the OS Rendering author list: the official page header and PDF include him, while the USENIX downloadable BibTeX omits him. The header/PDF and existing site take precedence for this field: https://www.usenix.org/conference/osdi25/presentation/wu-yuanpei and https://www.usenix.org/system/files/osdi25-wu-yuanpei.pdf.
- Preserved the previous site's 12 corresponding-author assignments and rendered them through the supported `additional_info` field. No corresponding-author assignments were inferred for new publications.

## DeltaBox Lite and homepage revision

The owner requested the October 16, 2026 open-source announcement and the exact congratulations to Jingkai He, Shiqi Liu, Puxi, and the team. The project's README independently records this release date and describes its filesystem sandbox, diff/commit/abort operations, and agent adapters: https://github.com/delta-box/deltabox-lite. The linked introduction is https://mp.weixin.qq.com/s/uFswgOfOJK-yrYwZslTDaA; direct retrieval returned a verification page, so the project description is grounded in the official README rather than an unread article. The introduction link is retained for readers.

The HPCA 2027 TPC service, first/second Agentic OS Workshop affiliations (ASPLOS 2026 / SOSP 2026), and revised AI/Agentic Operating Systems research directions were supplied by the owner. No specific workshop chair title was inferred.
