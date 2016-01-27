Summary
=======

-	[Introduction](README.md)
-	[基本概念介紹](basic/README.md)
	-	[豐田式生產](basic/lean.md)
	-	[敏捷式開發](basic/agile.md)
	-	[持續整合](basic/continuous-integration.md)
	-	[安裝 Jenkins](basic/install.md)
-	設定
	-	[環境變數](setup/env.md)
	-	[ssh](setup/ssh.md)
	-	[security](setup/security.md)
	-	[timezone](setup/timezone.md)
	-	[master/slave](setup/master-slave.md)
-	Jenkins CI 常用功能
	-	[build archive](common/build-archive.md)
	-	[執行 Shell Script](common/shell.md)
	-	[Jenkins API 使用簡介](common/api.md)
	-	[Plugin 安裝](common/plugin.md)
	-	[Subversion 整合](common/subversion.md)
	-	[JUnit 報表](common/test-report.md)
	-	[Script Console](common/script-console.md)
-	[常用 plugin 介紹](plugin/README.md)

	-	[publish over ssh](plugin/publish-over-ssh.md)
	-	[Config File Provider](plugin/config-file-provider.md)
	-	[GitHub pull request builder](plugin/github_pull_request_builder.md)
	-	[Bitbucket](plugin/bitbucket.md)
	-	[Cobertura](plugin/cobertura.md)
	-	[Jira](plugin/jira.md)
	-	[使用指令安裝常用套件](plugin/install_use_command.md)

-	[CI flow 簡介](task/flow.md)

-	[Task 實作以 Node.js 為例](task/nodejs/README.md)

	-	[build](task/nodejs/build.md)
	-	[test](task/nodejs/test.md)
	-	[preview](task/nodejs/preview.md)
	-	[release](task/nodejs/release.md)

-	[Task 實作以 Java 為例](task/java/README.md)

	-	[專案組成](task/java/project.md)
	-	[初始資料](task/java/inital.md)
	-	[build](task/java/build.md)
	-	[test](task/java/test.md)
	-	[preview](task/java/preview.md)
	-	[release](task/java/release.md)

-	Task 實作進階

	-	[cron jobs test](task/cron_test.md)
	-	[pull request test](task/pr_test.md)
	-	[branch/fork preview](task/branch_fork_preview.md)
	-	[if test ok then preview](task/if_test_ok_then_preview.md)

-	[搭配 docker 使用 Jenkins 協助測試](withDocker/README.md)

	-	[install](withDocker/install.md)
	-	[build](withDocker/build.md)
	-	[test](withDocker/test.md)
	-	[preview](withDocker/preview.md)
	-	[release](withDocker/release.md)

-	Q & A

	-	[一般問題](QA/general.md)
	-	[JAVA](QA/java.md)
