# Jenkins Quick Start

## Markdown Converter

難度：
簡易

目標：
使用 Jenkins 處理轉檔任務並保存結果。

專案：
https://github.com/agileworks-tw/markdown-example

練習：

1. 建立 Free-Style Jenkins Job：`Markdown`
2. 執行 Shell 指令檢查 `pandoc` 版本
3. 設定 Git Repository URL
4. 將 `README.md` 轉成 html 文件格式
5. 保存 `README.html` 文件

```
pandoc -s README.md -o README.html
```

## Using Gradle

難度：
普通

目標：
使用 Gradle 自動化建置與測試 Java 專案。

專案：
https://github.com/agileworks-tw/gradle-example

練習：

* 建立 Free-Style Jenkins Job：`gradle-example`
* 執行 Shell 指令檢查 `gradle` 版本
* 設定 Git Repository URL
* 執行 `gradle build` 指令
* 封存產生的 .jar 檔案
* 建立並封存 JUnit Report
* 建立並封存 JavaDoc Report

## Getting Started with Java Projects

https://github.com/TrunkWorkshop/jhipster-sample-app.git

https://github.com/agileworks-tw/spring-boot-sample.git




## 延伸閱讀

* [Jenkins The Definitive Guide](http://www.bogotobogo.com/DevOps/Jenkins/images/Intro_install/jenkins-the-definitive-guide.pdf)

