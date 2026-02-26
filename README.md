# 🚜 Terminal-Farm-Business | 终端农场商业版

<div align="center">

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Node.js](https://img.shields.io/badge/node-%3E%3D20-green.svg)
![Bun](https://img.shields.io/badge/bun-%3E%3D1.2-orange.svg)
![TypeScript](https://img.shields.io/badge/typescript-%3E%3D5.0-blue.svg)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=flat&logo=react&logoColor=%2361DAFB)

**下一代全自动 QQ 农场经典版云托管系统**

*稳定、高效、极客，不仅是工具，更是一套完整的商业化解决方案。*

</div>

---

### 🌐 在线体验

* **演示站点**：[http://112.124.43.11:8888/](http://112.124.43.11:8888/)
* STAR STAR STAR STAR STAR 麻烦给下star
> **💡 提示**：为方便开发者与用户测试，系统提供了以下演示卡密，可直接在登录界面使用。2026/2/25 14:50 更新了新一批测试月卡 烦请点下右上角star⭐。
#### 🔑 演示测试卡密

```text
FARM-MM1OCPSM-98FE3B86
FARM-MM1OCPSM-133D8301
FARM-MM1OCPSM-618376D7
FARM-MM1OCPSM-912FB822
FARM-MM1OCPSM-EA355400
FARM-MM1OCPSM-779D5A2C
FARM-MM1OCPSM-D2CF7C63
FARM-MM1OCPSM-864622A8
FARM-MM1OCPSM-26E5BEA5
FARM-MM1OCPSM-80BEDE78
```

<br/>

<img src="./QQ20260221-135818.png" alt="Terminal-Farm-Business卡密登录" style="max-width: 100%; border-radius: 8px; margin-bottom: 10px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);" />
<img src="./1234.png" alt="Terminal-Farm-Business用户端" style="max-width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);" />
<img src="./5678.png" alt="Terminal-Farm-Business管理端" style="max-width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);" />
<br/>

> [!NOTE]
> **项目背景与来源**
> 本项目是基于开源项目 [StringKe/terminal-farm](https://github.com/StringKe/terminal-farm) 进行的深度重构与二次开发。
> **核心改进点：**
> 1. **Web 化迁移**：将原有的终端交互全面迁移至现代化 Web 端，提供极速的网页管理体验。
> 2. **全面商业化**：内置完善的卡密授权、分销商（代理）管理体系，支持规模化运营。
> 3. **工业级分流机制**：引入独家的多租户代理分流引擎，实现一号一 IP，彻底解决大规模封号难题。
> 4. **智能异常提醒**：深度集成 AstrBot 机器人，实现账号状态、异常告警的即时通知。

> [!IMPORTANT]
> **🚀 独家深度特性：多租户代理池分流系统 (Proxy Traffic Splitting)**
>
> 区别于市面上大多数“单机直连”或“单一全局代理”的开源项目，本项目内置了**工业级代理隔离分流引擎**。每个挂机账号都可以被智能调度到不同的代理节点上，实现真正的**一号一放、多路分流**。这是规避大规模封号、保障账号安全的基石级功能。

[English Brief](#guide-en) | **[中文详细深度指南](#guide-zh)**

---

<a name="guide-zh"></a>

## 📖 项目深度背景

**Terminal Farm** 诞生于对极致自动化的追求。它不仅仅是一个简单的挂机脚本，而是一个集成了 **逆向协议处理**、**高并发 WebSocket 调度**、**现代化 Web 管理界面** 以及 **完善的分销授权体系** 的全栈式系统。

在面临服务器关停和网络攻击的背景下，我们将这套历经数次生产环境迭代的版本完全开源，旨在为开发者提供一个研究 **高并发 Node.js/Bun 应用**、**Protobuf 通讯协议** 及 **自动化运维** 的绝佳案例。

---

## ✨ 核心功能全景图 (Feature Matrix)

### 🖥️ 1. 用户端：极致的挂机体验 (Web User Terminal)
-   **无感登录**：集成 `QRLib` 登录引擎，支持 QQ扫码直登/QQ 微信 CODE登录，彻底告别繁琐的密码输入与风险。
-   **实时仪表盘**：采用 Framer Motion 打造的流畅动效，实时滚动展示金币、经验、等级、点券增长曲线。
-   **全能自动化逻辑**：
    -   **智能种植**：支持“等级优先”、“收益优先”或“自定义序列”种植策略。
    -   **精细化养护**：毫秒级监控土地状态，自动完成浇水、除草、杀虫、复活。
    -   **精准收获**：全自动收获成熟作物，确保土地无缝轮转。
    -   **智能邮件处理**：全自动读取并领取游戏内邮件奖励，不再错过任何活动补偿。
    -   **天气状态自适应**：系统实时同步游戏内天气（晴、雨、雪），并根据天气自动调整养护逻辑。
    -   **VIP 特权激活**：自动应用 QQ/微信 VIP 带来的额外加成与特殊权限。
-   **社交互动引擎**：
    -   **自动互助**：自动帮助好友除草/巡逻，获取额外经验奖励。
    -   **自动驱赶**：保护自身利益的同时，协助好友驱赶破坏者。
    -   **智能偷取**：自动扫描好友列表，发现成熟作物即刻出手。
    -   **自动邀请**：支持自动处理好友申请与邀请。
-   **资产管理**：
    -   **背包系统**：实时查看种子、化肥、特殊物品。
    -   **智能仓库**：根据预设策略，自动出售产物，换取金币。
    -   **图鉴系统**：自动整理并展示已收集的作物图鉴，方便进阶玩家查漏补缺。
-   **任务与计算**：
    -   **任务系统**：全天候自动完成每日农场挑战，领取丰厚奖励。
    -   **经验预报**：集成精准模型，计算当前土地配置下的升级预计时间。

### 🛡️ 2. 管理端：掌握全局的中心 (Web Admin Terminal)
-   **上帝视角监控**：实时查看服务器总会话数、当前在线人数、总卡密激活统计。
-   **代理池心脏**：全局管理 `.proxies.txt`，支持一键健康检查、失效节点高亮。
-   **卡密生命周期管理**：
    -   **批量制卡**：支持定义天卡、周卡、月卡、年卡、甚至永久卡。
    -   **状态控制**：一键封号、强制下线、修改有效期、解除设备绑定。
-   **分销商(代理)体系**：
    -   创建下级代理账号，分配独立点数。
    -   为不同代理定制独立的制卡成本，实现多级分销。
-   **系统动态调整**：无需重启即可修改全局公告、背景音乐、甚至是页面主题色。

### 🤖 3. 机器人端：身边的智能助手 (AstrBot Integration)
-   **即时触达**：当账号掉线、密码过期、需要额外人工验证时，机器人第一时间通过 QQ/微信 @用户。
-   **快捷查询**：
    -   `/rank`：实时查看全平台金币/等级排行榜。
    -   `/status`：查看系统负载、在线人数、延迟。
    -   `/buy`：获取定制化的购买链接和资费信息。
    -   `/功能`：获取精美的功能海报介绍。

---

## 🏗️ 项目架构深度解析 (Architecture)

系统采用典型的 **微服务+单边核心** 架构，确保了高度的灵活性：

```mermaid
graph TD
    A[用户浏览器] <-->|HTTP/WS| B[Nginx 反向代理]
    B <-->|Port 80| C[React 前端静态资源]
    B <-->|Port 2222| D[Bun 核心 API / Admin Server]
    D <-->|WebSocket| E[游戏服务器]
    D <-->|Port 11451| F[QRLib 扫码微服务]
    D <-->|HTTP| G[AstrBot 机器人]
    D --- H[(Local JSON DB / .proxies.txt)]
```

-   **Bun Runtime**: 核心引擎运行在 Bun 之上，相比 Node.js，在处理高负载的 Protobuf 序列化时效率提升约 40%。
-   **QRLib**: 独立出登录服务，解决了 Puppeteer/Playwright 资源占用高的问题，实现了纯协议/扫码的高效登录。
-   **Protobuf Engine**: 项目内置了全套逆向封装的游戏通讯协议，直接与底层服务器通讯，非模拟点击，速度极快。

---

#### 🚀 独家：工业级代理分流引擎 (Traffic Splitting Engine)
代理池是规避 IP 封禁的唯一防线。本项目实现了极其严谨的代理调度逻辑，这是本项目的核心优势：

-   **智能分流隔离**：基于 **Least Connections (最小连接数)** 算法。系统会自动计算每个代理节点的负载情况，将新登录的账号分配到负载最轻的节点。
-   **负载强力限制**：支持设置每个代理的最大承载数（如一个代理下只允许挂 5 个号），超出后自动熔断。
-   **自动健康探测 (Active Probing)**：系统定时对代理池进行“体检”，自动剔除失效节点，并计算响应延迟，优先使用低延迟节点。
-   **故障转移与冷却 (Auto Failover)**：当某个代理在登录过程中报错（如被拦截、403、或者连接超时），系统会立即将其标记为“风险节点”，进入 5 分钟的**冷却期**。在此期间，系统会自动通过其他健康的代理尝试重连。
-   **深度流量均衡**：通过清洗与重新构造代理层流量，确保护航游戏协议的稳定性。

---

## 🌐 代理池深度指南 (Proxy Pool)

代理池是规避 IP 封禁的唯一防线。本项目实现了极其严谨的代理调度逻辑。

### 1. 配置 `proxies.txt`
在根目录下新建或修改 `.proxies.txt`，支持以下格式：
```text
# 格式 A: 地址形式（默认识别为 SOCKS5）
1.2.3.4:1080
# 注意：1080 常用作 Tailscale 或其他内网穿透端口

# 格式 B: 完整认证形式 (推荐)
socks5://user:pass@5.6.7.8:1080
```

### 2. 调度逻辑
-   **健康测试 (Probe)**：系统会对每个代理进行 ICMP 和 HTTP 连通性测试。
-   **负载指数 (L.C.)**：系统优先选择当前分配账号最少的代理，确保 IP 干净度。
-   **熔断机制 (Circuit Breaker)**：一旦代理节点被标记为“被拦截/失效”，系统会进入 5 分钟的冷却期，在此期间不会分配该代理账号给新用户。

---

## 🚀 极致部署教程 (避坑版生产环境)

本教程适用于干净的 Ubuntu 服务器（推荐 22.04 LTS 及以上），已修复原版依赖遗漏问题。

### 1. 基础环境配置 (Node.js, Bun, Nginx)
请先更新系统，并安装必要的运行环境与 Web 服务器：
```bash
# 更新系统并安装基础工具与 Nginx
sudo apt update && sudo apt upgrade -y
sudo apt install -y curl git nginx

# 安装 Node.js (20.x)
curl -fsSL [https://deb.nodesource.com/setup_20.x](https://deb.nodesource.com/setup_20.x) | sudo -E bash -
sudo apt-get install -y nodejs

# 安装 Bun 引擎并重载环境变量
curl -fsSL [https://bun.sh/install](https://bun.sh/install) | bash
source ~/.bashrc 
```

### 2. 克隆项目与基础配置
```bash
git clone [https://github.com/RoseKhlifa/Terminal-Farm-Business.git](https://github.com/RoseKhlifa/Terminal-Farm-Business.git)
cd Terminal-Farm-Business

# 复制环境变量配置文件并根据需要修改
cp .env.example .env

# 【重要】创建缺失的版本信息文件，防止后端启动崩溃
echo '{"version": "1.0.0"}' > .version.json
```

### 3. 执行核心服务一键部署
赋予脚本执行权限并运行，此过程将安装后端依赖并构建前端：
```bash
chmod +x deploy.sh
sudo ./deploy.sh
```

### 4. 配置 Nginx 反向代理
`deploy.sh` 运行完后需手动链接配置并覆盖默认页面：
```bash
# 复制配置文件
sudo cp /root/Terminal-Farm-Business/nginx.conf /etc/nginx/sites-available/farm.conf

# 将配置文件中的 YOUR_DOMAIN.com 替换为 _（代表允许所有 IP 访问）
sudo sed -i 's/YOUR_[DOMAIN.com/_/g](https://DOMAIN.com/_/g)' /etc/nginx/sites-available/farm.conf

# 移除 Nginx 默认页面，并启用农场项目路由
sudo rm -f /etc/nginx/sites-enabled/default
sudo ln -s /etc/nginx/sites-available/farm.conf /etc/nginx/sites-enabled/

# 检查语法并重启 Nginx
sudo nginx -t
sudo systemctl restart nginx
```

### 5. 启动 QRLib 扫码微服务 (关键)
必须单独启动该服务，否则面板登录时会提示 `500 QRLib 服务未启动`：
```bash
# 进入微服务目录并安装 Node 依赖
cd /root/Terminal-Farm-Business/QRLib-main
npm install

# 将服务文件复制到系统并设置开机自启
sudo cp /root/Terminal-Farm-Business/qrlib.service /etc/systemd/system/
sudo systemctl daemon-reload
sudo systemctl enable --now qrlib

# 确认服务状态 (需显示 active running)
sudo systemctl status qrlib
```

### 6. 端口放行与访问
请确保你的云服务器**安全组（防火墙）**中放行了以下端口：
* **80** 端口 (TCP)：用于前端 Web 面板访问。
* **2222** 端口 (TCP)：用于管理后台访问。

-   **前端页面**：`http://你的服务器IP`
-   **管理后台**：`http://你的服务器IP:2222`
    -   **初始密码**：请参考 `.env` 文件中的设置 (请第一时间修改)。

---

## 🛠️ 运维与二次开发

### 文件结构导航
- `/src/core`: 包含农场所有自动化逻辑、代理池、会话管理。
- `/src/admin`: 后台管理系统服务器源码。
- `/web-terminal`: 基于 React 的前端源码。
- `/main.py`: AstrBot 机器人插件代码。
- `/proto`: 游戏原始及解密后的 Protobuf 定义。
- `/QRLib-main`: 独立的 QQ 扫码/登录鉴权微服务。

### 后期更新命令
如果您拉取了新的代码，只需再次运行：
```bash
git pull && sudo ./deploy.sh
```

---

## 🔐 内部授权与卡密逻辑 (Licensing Logic)

本项目内置了一套严谨的授权校验体系，确保商业化运营的安全性：

### 1. 卡密生成原理
卡密（License Key）由管理员后台生成，其核心结构包含：
- **批次号 (Batch ID)**：用于追踪具体的生成任务。
- **权限掩码 (Permission Mask)**：定义该卡密是否具备“多绑”、“加速”、“高级自动化”等权限。
- **有效期时间戳 (Expiry Timestamp)**：定义卡密的截止日期。

### 2. 多级代理授权
系统支持“核心管理员 -> 大代理 -> 小代理”的三级分馏模式：
- **点数扣除机制**：代理在生成卡密时，会从其账户扣除相应的“点数”。
- **独立管理域**：代理只能查看和管理自己生成的卡密及关联的游戏账号。

---

## 📡 核心协议处理 (Protocol Deep Dive)

由于游戏后端采用 Protobuf 协议通讯，本项目实现了一套高性能的编解码引擎：

### 1. 会话握手机制 (Handshake)
1. **HTTP Auth**: 用户通过账户密码或扫码获取 `SKEY`。
2. **WebSocket Upgrade**: 建立加密的长连接。
3. **Session Binding**: 将游戏账号与当前 WebSocket 会话绑定。

### 2. 自动化执行 pipeline
每一个农场动作（如收获）都遵循以下链路：
`逻辑触发 (src/core) -> 构造 Proto Message -> PB 序列化 (Bun Engine) -> WebSocket 发送 -> 接收回包 -> 逻辑反馈 (EventEmitter)`。

---

## 🔧 常见安装问题排查 (Troubleshooting)

如果在部署过程中遇到困难，请参考下表：

| 现象 | 可能原因 | 解决方案 |
| :--- | :--- | :--- |
| `Bun not found` | 环境变量未生效 | 运行 `source ~/.bashrc` 或手动添加 Bun 路径 |
| `Nginx 502` / `80 端口无法访问` | API / Web 服务未就绪 | `systemctl status farm-api` 及 `systemctl status nginx` 检查 |
| `500 QRLib 服务未启动` | QRLib 微服务宕机 | 检查 11451 端口及 `systemctl status qrlib` 运行状态 |
| `Port 2222 busy` | 端口被占用 | `lsof -i :2222` 查进程并杀掉，或修改 `.env` 端口 |
| `Permission denied` | 执行权限不足 | 为脚本添加权限：`chmod +x deploy.sh` |
| `Build failed` | 内存不足 (OOM) | 建议开启 Swap 或升级到至少 2GB RAM 的服务器 |
| `Login Timeout` | 代理池连通性差 | 暂注 `.proxies.txt` 所有内容，测试直连是否成功 |

---

## 🔒 安全最佳实践 (Security Best Practices)

作为一套生产级别的托管系统，我们强烈建议您：
1. **强制开启 HTTPS**：通过 Nginx 和 Certbot 部署 SSL 证书。
2. **修改默认凭据**：
   - 建议在安全组中仅对您的个人 IP 开放 `2222` 管理端口。
3. **定期清理日志**：
   - 虽然系统会自动轮转日志，但定期手动运行 `rm -rf logs/*.log` 可释放磁盘空间。
4. **代理隔离**：
   - 每个代理账户挂机上限尽量控制在 5-10 个，且尽量选择高匿 SOCKS5 代理。

---

## 📈 项目路线图 (Roadmap)

我们计划在未来的版本中引入以下功能（欢迎提交 Pull Request）：
- [ ] **多平台支持**：支持除了 QQ/微信之外的更多农场版本。
- [ ] **智能异常重试**：基于 AI 的验证码自动绕过机制。
- [ ] **移动端 APP**：基于 React Native 的安卓/iOS 管理端。
- [ ] **大数据看板**：更详细的个人资产增长曲线分析。

---

## 🤝 参与贡献 (Contribution)

如果你想参与本项目开发，请遵循以下规范：
- **代码风格**：本项目使用 `Biome` 进行格式化，提交前请运行 `bun run lint`。
- **协议修改**：所有通讯协议定义在 `/proto` 目录下，修改后需重新生成对应的 TypeScript 定义。
- **分支管理**：所有的功能维护请在 `feature/` 分支进行，修复请在 `hotfix/` 分支进行。

---

## ⭐ Star History

感谢所有支持本项目的朋友！

[![Star History Chart](https://api.star-history.com/svg?repos=RoseKhlifa/Terminal-Farm-Business&type=Date)](https://star-history.com/#RoseKhlifa/terminal-farm&Date)

---

## ⚠️ 免责声明 (Disclaimer)

本项目仅供学术交流与技术研究之用。

1.  **禁止商业化**：严禁利用本项目进行任何形式的营利行为。
2.  **账号风险**：作者不对使用本项目导致的账号封号、经济损失负责。
3.  **合法合规**：请在遵守相关法律法规及游戏官方服务条款的前提下使用。

## 📄 许可证

本项目基于 [MIT License](LICENSE) 开源，请在二次分发时保留作者署名及原项目地址。
