## 从上游同步已经Fork的仓库

1. 打开 [https://github.com/settings/tokens](https://github.com/settings/tokens) 生成 Fine-grained personal access tokens。
2. Repository access 选择全部仓库或指定仓库。
3. Permissions 的 Repository permissions 设置 **Contents** 为 `Read and write` 即可。
4. 生成 token 并复制。
5. 在你专门用于运行 GitHub Actions 来同步的 Repository 中点击 **Settings** → **Secrets and variables** → **Actions** → **New repository secrets**。
6. `Name` 填写 `PERSONAL_TOKEN`, `Secret` 粘贴刚才的 token。
7. 按照你的需要编辑 GitHub Actions [文件](.github/workflows/upstream_daily.yml)。

## 推送GitHub仓库到GitLab

1. 打开 [https://gitlab.com/-/user_settings/personal_access_tokens](https://gitlab.com/-/user_settings/personal_access_tokens) 生成个人访问令牌。
2. 注意: 选择范围勾选 `api`, `read_api`, `read_user`, `read_repository`, `write_repository`。
3. 生成 token 并复制。
4. 在你专门用于运行 GitHub Actions 来同步的 Repository 中点击 **Settings** → **Secrets and variables** → **Actions** → **New repository secrets**。
5. `Name` 填写 `GITLAB_PERSONAL_TOKEN`, `Secret` 粘贴刚才的 token。
6. 按照你的需要编辑 GitHub Actions [文件](.github/workflows/gitlab_3_days.yml)。
