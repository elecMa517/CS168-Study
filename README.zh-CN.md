[English](./README.md) | [中文](./README.zh-CN.md)

# CS168 学习仓库

这是我用于学习 **Berkeley CS168 — 互联网架构与协议**（2025 Spring）的个人学习仓库，采用 Claude Code 作为 AI 辅导工具，基于苏格拉底式教学法（Socratic Method）进行引导式学习。

**GitHub**: [github.com/elecMa517](https://github.com/elecMa517)

---

## 这个仓库是做什么的

Claude Code 作为交互式 CS168 辅导老师：

- 先问你已经知道什么，再在此基础上解释（不直接给答案）
- 每次解释后出题检验理解，根据回答调整教学方式
- 自动记录每次学习的内容、掌握的知识点和薄弱环节
- 结合 `reference/` 里的 disc 题目一起练习

---

## 仓库结构

```
/reference/                       # 在本地放入 disc PDF（已 git-ignore，链接见下方）

/sessions/                        # 每日学习记录
  /YYYY-MM-DD/
    session-notes.md
  SESSION-TEMPLATE.md             # 记录模板

/progress/
  cs168-study-tracker.md          # 唯一进度文件：48 个知识点全覆盖

CLAUDE.md                         # AI 辅导老师的行为指令
README.md                         # 英文版说明
README.zh-CN.md                   # 本文件（中文）
```

---

## 讨论课题目（官方链接）

所有 PDF 均托管在 CS168 SP25 官方课程网站，下载后放入本地 `reference/` 文件夹即可使用。

| Disc | 主题 | 题目 | 解答 |
|------|------|------|------|
| 01 | 网络分层架构、封装、Traceroute | [disc01](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc01.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc01-sols.pdf) |
| 02 | 分组交换、延迟类型、统计复用 | [disc02](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc02.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc02-sols.pdf) |
| 03 | 距离矢量路由（Bellman-Ford） | [disc03](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc03.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc03-sols.pdf) |
| 04 | 链路状态路由（Dijkstra / OSPF） | [disc04](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc04.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc04-sols.pdf) |
| 05 | BGP — 域间路由 | [disc05](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc05.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc05-sols.pdf) |
| 06 | TCP — 可靠传输 | [disc06](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc06.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc06-sols.pdf) |
| 07 | 拥塞控制（AIMD、慢启动） | [disc07](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc07.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc07-sols.pdf) |
| 08 | DNS、HTTP、以太网 | [disc08](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc08.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc08-sols.pdf) |
| 09 | ARP、DHCP、NAT | [disc09](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc09.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc09-sols.pdf) |
| 10 | 数据中心网络与 SDN | [disc10](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc10.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc10-sols.pdf) |
| 11 | 主机网络栈（内核、RDMA） | [disc11](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc11.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc11-sols.pdf) |
| 12 | 组播与集体通信 | [disc12](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc12.pdf) | [sols](https://sp25.cs168.io/assets/discussions/cs168-sp25-disc12-sols.pdf) |

---

## 如何使用

### 第一步：环境准备

```bash
git clone https://github.com/elecMa517/Network-Study.git
cd Network-Study
```

安装 [Claude Code](https://claude.ai/code)，然后在仓库目录下运行：

```bash
claude
```

### 第二步：开始学习

直接提问，像和辅导老师聊天一样：

```
"我想学 disc03 的 distance-vector routing"
"TCP 的 sliding window 是怎么工作的？"
"帮我做 disc06 的第一道题"
```

Claude 会先问你的已有理解，再解释，最后出题确认你真的掌握了。

### 第三步：做 disc 题目

```
"我们来做 disc04 的题"
"我卡在 disc05 的 BGP 题上了"
```

Claude 会读取 `reference/` 里的 PDF，用提示引导你逐步解题，而不是直接给答案。

### 第四步：查看进度 & 复习薄弱点

```
"我哪些地方还没掌握？"
"帮我复习上次没弄懂的知识点"
```

Claude 会读取 `progress/cs168-study-tracker.md` 和近期学习记录，给出针对性复习建议。

### 学习结束后

无需手动操作——Claude 会自动：
1. 在 `sessions/YYYY-MM-DD/session-notes.md` 记录本次学习详情
2. 更新 `progress/cs168-study-tracker.md` 里的进度和知识漏洞

---

## 推荐学习顺序

`disc01 → disc02 → disc03+04 → disc05 → disc06+07 → disc08+09 → disc10 → disc11+12`

disc01 建立分层模型的基础，后续所有内容都依赖于此。

---

## 使用的权威参考资料

- **Kurose & Ross** 《Computer Networking: A Top-Down Approach》
- **Tanenbaum & Wetherall** 《Computer Networks》
- **RFC 文档**：RFC 793（TCP）、RFC 791（IP）、RFC 4271（BGP）等
- [sp25.cs168.io](https://sp25.cs168.io/) 提供的 disc PDF（课程一手练习材料）

---

## 致谢

- **CS168 — UC Berkeley**：本仓库使用的所有讨论课题目均来自 [CS168 Spring 2025](https://sp25.cs168.io/) 课程。本仓库是独立学习工具，与 UC Berkeley 及 CS168 课程团队无任何隶属关系。

- **[chenran818/CFP-Study](https://github.com/chenran818/CFP-Study)**：本仓库的文件结构、学习记录协议以及 `CLAUDE.md` 中的苏格拉底式教学方法，均改编自该项目。原项目使用相同的 AI 引导式学习方法成功通过了 CFP 考试。
