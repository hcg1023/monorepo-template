# monorepo project

## 使用这个模板
1. 点击Use this template
2. 修改package.json的repository信息
3. 如果需要使用github actions，需要在仓库的设置`Settings/Actions/General/Workflow permissions`中选择`Read and write permissions`和`Allow GitHub Actions to create and approve pull requests`

4. 非特殊情况不要在main分支开发，而是通过feature分支pull request合并到main分支
5. 在github apps仓库中安装changeset-bot，并使它对当前仓库生效


## package.json命令详解
### preinstall
必须使用pnpm进行安装，否则会报错
### prepare
初始化husky
### test
单元测试
### lint
eslint代码校验
### lint:style
stylelint代码校验
### prettier
prettier代码格式化
### lint-staged
提供给husky配置的pre-commit hook
### commitlint
提供给husky配置的commit-msg hook
### pack-version
在github action ci中使用changesets构建版本号
### release
使用pnpm发布npm包，并且使用changesets构建tag和release版本号
### publish-success
发布npm包成功之后的hook
