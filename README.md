1. 中央仓库 (github-actions-templates) 设置
创建仓库：创建一个名为 github-actions-templates 的私有仓库。
添加文件：将 universal-pipeline.yml, registry-config.yml 和 setup-language action 添加到仓库中。
配置 Secrets：
REGISTRY_USERNAME: 镜像仓库的通用用户名。
REGISTRY_TOKEN: 镜像仓库的通用Token或密码。
配置 Environments：
在 Settings > Environments 中创建 production 环境。
添加保护规则和审批人（team-leads）。
2. 项目仓库 (any-project) 设置
创建调用文件：在项目仓库的 .github/workflows/ 目录下创建 ci.yml 文件，内容如上。
配置 Secrets：
KUBECONFIG: Kubernetes集群的访问配置。
NOTIFICATION_EMAIL: (可选) 通知邮箱。
SLACK_WEBHOOK: (可选) Slack Webhook URL。