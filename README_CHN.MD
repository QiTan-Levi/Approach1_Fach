# 全栈FastAPI模板

<a href="https://github.com/fastapi/full-stack-fastapi-template/actions?query=workflow%3A%22Test+Docker+Compose%22" target="_blank"><img src="https://github.com/fastapi/full-stack-fastapi-template/workflows/Test%20Docker%20Compose/badge.svg" alt="测试Docker Compose"></a>
<a href="https://github.com/fastapi/full-stack-fastapi-template/actions?query=workflow%3A%22Test+Backend%22" target="_blank"><img src="https://github.com/fastapi/full-stack-fastapi-template/workflows/Test%20Backend/badge.svg" alt="测试后端"></a>
<a href="https://coverage-badge.samuelcolvin.workers.dev/redirect/fastapi/full-stack-fastapi-template" target="_blank"><img src="https://coverage-badge.samuelcolvin.workers.dev/fastapi/full-stack-fastapi-template.svg" alt="覆盖率"></a>

## 技术栈与特性

- ⚡ **FastAPI** (https://fastapi.tiangolo.com) 用于Python后端API。

- 🧰 [SQLModel](https://sqlmodel.tiangolo.com) 用于 Python SQL 数据库交互（对象关系映射，ORM）。

- 🔍 [Pydantic](https://docs.pydantic.dev)，FastAPI 所使用的，用于数据验证和设置管理。

- 💾 [PostgreSQL](https://www.postgresql.org) 作为SQL数据库。

- 🚀 前端使用[React](https://react.dev)。

- 💃 使用TypeScript、hooks、[Vite](https://vitejs.dev)以及现代前端技术栈的其他部分。

- 🎨 前端组件使用 [Tailwind CSS](https://tailwindcss.com) 和 [shadcn/ui](https://ui.shadcn.com)。
  🤖 一个自动生成的前端客户端。

- 🧪 [Playwright](https://playwright.dev) 用于端到端测试。

- 🦇 支持深色模式。

- 🐋 [Docker Compose](https://www.docker.com) 用于开发和生产环境。

- 🔒 默认情况下，采用安全密码哈希。

- 🔑 JWT（JSON Web Token）身份验证。

- 📫 基于电子邮件的密码恢复。

- 📬 [Mailcatcher](https://mailcatcher.me)：用于开发过程中的本地邮件测试。
  ✅ 使用[Pytest](https://pytest.org)进行测试。

- 📞 [Traefik](https://traefik.io) 作为反向代理/负载均衡器。
  🚢 使用Docker Compose的部署说明，包括如何设置前端Traefik代理以处理自动HTTPS证书。

- 基于GitHub Actions的持续集成（CI）和持续部署（CD）。
  
  ### 控制面板登录
  
  [![API文档](img/login.png)](https://github.com/fastapi/full-stack-fastapi-template)
  
  ### 控制面板 - 管理员
  
  [![API文档](img/dashboard.png)](https://github.com/fastapi/full-stack-fastapi-template)
  
  ### 控制面板 - 项目
  
  [![API文档](img/dashboard-items.png)](https://github.com/fastapi/full-stack-fastapi-template)
  
  ### 控制面板 - 暗色模式
  
  [![API文档](img/dashboard-dark.png)](https://github.com/fastapi/full-stack-fastapi-template)
  
  ### 交互式API文档
  
  [![API文档](img/docs.png)](https://github.com/fastapi/full-stack-fastapi-template)
  
  ## 如何使用
  
  你可以直接**fork或clone**这个仓库，然后按原样使用。
  ✨ 就是这么好用。 ✨
  
  ### 如何使用私有仓库
  
  如果你想要一个私有仓库，GitHub不允许你直接通过fork来创建，因为它不允许更改fork的可见性。
  但你可以采取以下措施：

- 创建一个新的GitHub仓库，例如`my-full-stack`。

- 手动克隆此仓库，并将其名称设置为你想要使用的项目名称，例如“my-full-stack”：
  
  ```bash
  使用以下命令克隆仓库：git clone git@github.com:fastapi/full-stack-fastapi-template.git my-full-stack
  ```

- 进入新目录：
  
  ```bash
  切换到 my-full-stack 目录
  ```

- 将新的origin设置为新的仓库，例如，从GitHub界面进行复制：
  
  ```bash
  将远程仓库的URL设置为`git@github.com:octocat/my-full-stack.git`
  ```

- 将此仓库添加为另一个“远程仓库”，以便您后续获取更新：
  
  ```bash
  git 远程添加上游仓库 git@github.com:fastapi/full-stack-fastapi-template.git
  ```

- 将代码推送到你的新仓库：
  
  ```bash
  git 推送 -u origin master
  ```
  
  ### 更新自原始模板
  
  克隆存储库并进行更改后，您可能希望从原始模板获取最新更改。

- 确保已将原始仓库添加为远程仓库，你可以通过以下命令进行检查：
  
  ```bash
  git remote -v
  原始仓库 git@github.com:octocat/my-full-stack.git (获取中)
  来源 git@github.com:octocat/my-full-stack.git (推送)
  上游仓库    git@github.com:fastapi/full-stack-fastapi-template.git（获取）
  上游仓库    git@github.com:fastapi/full-stack-fastapi-template.git (推送)
  ```

- 拉取最新更改而不进行合并：
  
  ```bash
  git pull --no-commit upstream master
  ```
  
  这将从该模板下载最新更改，而不会进行提交，这样你就可以在提交之前检查所有内容是否正确。

- 如果存在冲突，请在编辑器中解决。

- 完成后，提交更改：
  
  ```bash
  git 合并 --继续
  ```
  
  ### 配置
  
  然后，你可以更新 `.env` 文件中的配置来定制你的配置。
  在部署之前，请确保至少更改以下值：

- `SECRET_KEY`

- `FIRST_SUPERUSER_PASSWORD`

- `POSTGRES_PASSWORD`
  你可以（并且应该）将这些信息作为环境变量从secrets中传递。
  更多详情，请参阅[deployment.md](./deployment.md)文档。
  
  ### 生成密钥
  
  `.env`文件中的一些环境变量的默认值为`changethis`。
  你必须使用一个秘密密钥来更改它们，要生成秘密密钥，你可以运行以下命令：
  
  ```bash
  python -c "import secrets; print(secrets.token_urlsafe(32))"
  ```
  
  复制内容并将其作为密码/密钥使用。再次运行以生成另一个安全密钥。
  
  ## 如何使用 - 替代复印机
  
  此仓库还支持使用[Copier](https://copier.readthedocs.io)来生成新项目。
  它会复制所有文件，询问你一些配置问题，并根据你的回答更新 `.env` 文件。
  
  ### 安装复印机
  
  你可以通过以下方式安装Copier：
  
  ```bash
  使用pip安装copier
  ```
  
  或者更好的是，如果你有[`pipx`](https://pipx.pypa.io/)，你可以使用以下命令运行它：
  
  ```bash
  使用pipx安装copier
  ```
  
  **注意**：如果你已安装`pipx`，则安装copier是可选的，你可以直接运行它。
  
  ### 使用Copier生成项目
  
  为你的新项目目录起一个名字，你将在下面使用它。例如，“my-awesome-project”。
  转到将成为项目父目录的目录，并使用项目名称运行命令：
  
  ```bash
  使用复制命令复制 https://github.com/fastapi/full-stack-fastapi-template 到 my-awesome-project 目录中，并信任该仓库
  ```
  
  如果你已安装`pipx`但未安装`copier`，则可以直接运行它：
  
  ```bash
  使用pipx运行`copier`命令，将`https://github.com/fastapi/full-stack-fastapi-template`复制到`my-awesome-project`目录中，并启用信任选项
  ```
  
  **注意**：为了能够执行[创建后脚本](https://github.com/fastapi/full-stack-fastapi-template/blob/master/.copier/update_dotenv.py)来更新您的`.env`文件，`--trust`选项是必需的。
  
  ### 输入变量
  
  在生成项目之前，复印机可能会要求你提供一些数据，你可能需要提前准备好这些数据。
  但别担心，之后你可以在`.env`文件中更新任何内容。
  输入变量及其默认值（部分为自动生成）如下：

- `project_name`：（默认值：`"FastAPI Project"`）项目的名称，显示给API用户（在.env文件中）。

- `stack_name`：（默认值：`"fastapi-project"`）用于Docker Compose标签的堆栈名称和项目名称（无空格，无句点）（在.env文件中）。

- `secret_key`：（默认值：`"changethis"`）项目的秘密密钥，用于安全目的，存储在.env文件中，您可以使用上述方法生成一个。

- `first_superuser`：（默认值：`"admin@example.com"`）第一个超级用户的电子邮件（在.env文件中）。

- `first_superuser_password`：（默认值：`"changethis"`）第一个超级用户的密码（位于.env文件中）。

- `smtp_host`：（默认值：""）用于发送电子邮件的SMTP服务器主机，您可以在后续的.env文件中进行设置。

- `smtp_user`：（默认值：""）用于发送电子邮件的SMTP服务器用户，您可以在后续的.env文件中进行设置。

- `smtp_password`：（默认值：""）用于发送电子邮件的SMTP服务器密码，您可以在后续的.env文件中进行设置。

- `emails_from_email`：（默认值：`"info@example.com"`）用于发送电子邮件的邮箱地址，您可以在后续的.env文件中进行设置。

- `postgres_password`：（默认值：`"changethis"`）PostgreSQL数据库的密码，存储在.env文件中，您可以使用上述方法生成一个。

- `sentry_dsn`：（默认值：""）如果您正在使用Sentry，则可以在.env文件中稍后设置其DSN。
  
  ## 后端开发
  
  后端文档：[backend/README.md](./backend/README.md)。
  
  ## 前端开发
  
  前端文档：[frontend/README.md](./frontend/README.md)。
  
  ## 部署
  
  部署文档：[deployment.md](./deployment.md)。
  
  ## 开发
  
  通用开发文档：[development.md](./development.md)。
  这包括使用Docker Compose、自定义本地域名、`.env`配置等。
  
  ## 发布说明
  
  请查看文件[release-notes.md](./release-notes.md)。
  
  ## 许可证
  
  全栈FastAPI模板遵循MIT许可证条款。
