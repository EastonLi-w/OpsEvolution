# 🚀 运维演进实战项目 - OpsEvolution

## 📋 项目概述

本项目通过模拟真实业务场景，从单体架构开始，通过发现和解决性能瓶颈，逐步演进为分布式、高可用的系统架构。每个技术栈的引入都有明确的问题驱动和性能数据支撑。

## 🎯 学习目标

1. 复习和整合常用运维技术栈
2. 培养问题发现和解决的能力
3. 建立SRE（站点可靠性工程）思维方式
4. 构建完整的GitHub项目成长记录

## 🗺️ 演进路线图

### 阶段一：单体应用基础

### 阶段二：监控与可观测性

### 阶段三：应用层扩展

### 阶段四：数据层优化

### 阶段五：容器化转型

### 阶段六：自动化运维

### 阶段七：微服务与高级特性

## 📁 项目结构

```text
OpsEvolution/
├── 01-baseline/                    # 阶段1：基础部署和基准测试
│   ├── deployment/                 # 部署脚本和配置
│   ├── load-tests/                 # 压力测试脚本
│   └── results/                    # 基准测试结果
│
├── 02-monitoring/                  # 阶段2：监控体系
│   ├── prometheus-setup/           # Prometheus配置
│   ├── zabbix-setup/               # Zabbix配置（对比）
│   └── dashboards/                 # Grafana仪表盘
│
├── 03-ha-application/              # 阶段3：应用高可用
│   ├── nginx-lb/                   # Nginx负载均衡
│   ├── session-sharing/            # 会话共享方案
│   └── performance-comparison/     # 性能对比
│
├── 04-ha-database/                 # 阶段4：数据库高可用
│   ├── mysql-replication/          # MySQL主从复制
│   ├── mycat-setup/                # Mycat读写分离
│   ├── mha-config/                 # MHA高可用
│   ├── redis-ha/                   # Redis高可用方案
│   └── benchmark-results/          # 性能基准
│
├── 05-containerization/            # 阶段5：容器化
│   ├── dockerfiles/                # Dockerfile
│   ├── docker-compose/             # Docker Compose编排
│   ├── harbor-setup/               # Harbor私有仓库
│   └── k8s-manifests/              # Kubernetes配置文件
│
├── 06-automation/                  # 阶段6：自动化运维
│   ├── jenkins-pipelines/          # Jenkins流水线
│   ├── ansible-playbooks/          # Ansible剧本
│   ├── gitlab-ci/                  # GitLab CI配置
│   └── jumpserver-config/          # JumpServer配置
│
├── 07-microservices/               # 阶段7：微服务
│   ├── service-split/              # 服务拆分方案
│   ├── message-queues/             # 消息队列配置
│   ├── service-mesh/               # 服务网格
│   ├── distributed-storage/        # 分布式存储
│   └── logging-system/             # 日志系统
│
├── tools/                          # 实用工具
│   ├── bottleneck-detector/        # 瓶颈检测脚本
│   ├── chaos-experiments/          # 混沌工程实验
│   ├── performance-analyzer/       # 性能分析工具
│   └── health-check/               # 健康检查脚本
│
├── docs/                           # 项目文档
│   ├── decision-log.md             # 技术决策记录
│   ├── problem-solutions.md        # 问题与解决方案
│   ├── performance-reports/        # 性能报告
│   └── architecture-diagrams/      # 架构图
│
└── scripts/                        # 全局脚本
    ├── setup.sh                    # 环境搭建脚本
    ├── benchmark.sh                # 基准测试脚本
    └── deploy.sh                   # 部署脚本
```

## 🔧 技术栈对应关系

| 技术组件           | 引入阶段      | 解决的问题             | 验证指标         |
| :----------------- | :------------ | :--------------------- | :--------------- |
| **Nginx**          | 阶段1         | 静态资源处理、反向代理 | 静态资源响应时间 |
| **Prometheus**     | 阶段2         | 系统监控和告警         | 指标采集成功率   |
| **Zabbix**         | 阶段2（对比） | 企业级监控             | 监控覆盖率       |
| **Keepalived**     | 阶段3         | Nginx高可用            | VIP切换时间      |
| **Mycat**          | 阶段4         | 数据库读写分离         | 查询性能提升比   |
| **MHA**            | 阶段4         | MySQL高可用            | 故障切换时间     |
| **Redis Cluster**  | 阶段4         | 缓存高可用             | 缓存命中率       |
| **Docker**         | 阶段5         | 环境标准化             | 部署时间缩短     |
| **Kubernetes**     | 阶段5         | 容器编排               | 资源利用率       |
| **Jenkins**        | 阶段6         | CI/CD流水线            | 构建部署时间     |
| **Ansible**        | 阶段6         | 配置管理               | 配置同步时间     |
| **RabbitMQ/Kafka** | 阶段7         | 服务解耦               | 消息处理延迟     |
| **Istio**          | 阶段7         | 服务网格               | 服务调用成功率   |
| **Ceph**           | 阶段7         | 分布式存储             | IOPS性能         |
| **ELK/EFK**        | 阶段7         | 集中日志               | 日志查询时间     |

## 🚦 开始使用

### 环境要求

- 虚拟机或云服务器（建议4核8G+）
- CentOS 7.9 / Ubuntu 20.04+
- 至少50GB可用磁盘空间

### 快速开始

```bash
# 1. 克隆项目
git clone https://github.com/yourusername/OpsEvolution.git
cd OpsEvolution

# 2. 初始化环境
./scripts/setup.sh --stage 1

# 3. 部署基础应用
cd 01-baseline/deployment
./deploy.sh

# 4. 运行基准测试
cd ../load-tests
./run-baseline-test.sh
```

## 📊 性能指标定义

每个阶段都会跟踪以下核心指标：

- **响应时间**：P50、P95、P99
- **吞吐量**：QPS（每秒查询数）
- **资源利用率**：CPU、内存、磁盘IO、网络
- **可用性**：服务可用率
- **故障恢复时间**：MTTR（平均恢复时间）

## 🔍 问题发现方法

### 1. 渐进式压力测试

```bash
# 逐步增加并发用户
./tools/bottleneck-detector/step-load-test.sh \
  --start 100 \
  --end 5000 \
  --step 500 \
  --duration 300
```

### 2. 监控告警触发

- CPU使用率 > 80%持续5分钟
- 内存使用率 > 85%
- 慢查询比例 > 5%
- 错误率 > 1%

### 3. 混沌工程实验

```bash
# 模拟网络延迟
./tools/chaos-experiments/network-delay.sh

# 模拟服务故障
./tools/chaos-experiments/service-failure.sh
```

## 📈 演进记录要求

每个阶段完成后需要记录：

1. **问题分析报告**：发现什么瓶颈，如何发现的
2. **解决方案设计**：有哪些可选方案，为什么选择当前方案
3. **实施过程**：具体的配置和部署步骤
4. **效果验证**：性能对比数据
5. **经验总结**：学到了什么，有什么坑

## 🤝 贡献指南

欢迎提交：

- 新的瓶颈发现方法和测试脚本
- 替代技术方案的实现
- 性能优化建议
- 文档改进

## 📚 学习资源

- [每个阶段的详细实施指南](https://./docs/stage-guides/)
- [技术选型对比分析](https://./docs/tech-comparison/)
- [常见问题解决记录](https://./docs/troubleshooting/)
- [性能调优最佳实践](https://./docs/performance-tuning/)

## 🏆 完成目标

完成所有阶段后，你将：

- ✅ 掌握从单体到微服务的完整演进路径
- ✅ 理解每个技术组件解决的实际问题
- ✅ 具备通过数据驱动决策的能力
- ✅ 拥有完整的GitHub项目作为技术证明
- ✅ 为SRE岗位做好充分准备

------

**开始你的演进之旅吧！每个问题都是成长的机会，每次瓶颈都是技术提升的契机。**

> 提示：建议按阶段顺序进行，每个阶段完成后提交代码并更新文档。遇到问题时，先查看对应阶段的troubleshooting文档。

------

*最后更新: 2025年*
*作者:*
*许可证: MIT*
