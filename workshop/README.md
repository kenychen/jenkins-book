# Jenkins Workshop

歡迎 ;- )

## AgileWorks

AgileWorks 是由創科資訊獨家開發的 DevOps 教學平台，使用瀏覽器即可進行練習。

請先取得 `AgileWorksJenkins-20160307.ova` 檔案，匯入至 VirtualBox 並啟動。

並且檢查以下功能是否正常？

* 終端機
* 操作練習

在終端機下切換執行身份：

jenkins

```
sudo su - jenkins
```

root

```
sudo su -
```

檢查 Jenkins 狀態

```
sudo service jenkins status
```

重新啟動 Jenkins 伺服器

```
sudo service jenkins restart
```

重新啟動 Linux 系統（VM）

```
sudo reboot
```

## Hello! Jenkins!

難度：
簡易

目標：
認識 Jenkins Job 基礎操作。

專案：
https://github.com/agileworks-tw/java-hello-world

練習：

1. 新增作業（Jenkins Job）名稱：`HelloWorld`
2. 使用 Shell 指令檢查 JDK 版本
3. 使用 Git SCM，設定 Git Repository URL
4. 使用 `javac` 指令進行編譯、`java` 指令執行
5. 使用 curl 指令操作 Remote API：`curl http://localhost:8080/job/HelloWorld/build`
6. 自訂字串參數：`WHO`，並帶入 Shell 指令
7. 設定 Git 分支（branch）
8. 使用 curl 指令操作參數化建置 Remote API：`http://localhost:8080/job/HelloWorld/buildWithParameters?WHO=Mary`
9. 使用 Git Parameter 參數化建置切換分支：`BRANCH_NAME`，並帶入 Git SCM 設定
10. 利用 Remote API 回傳 XML 或 JSON 格式的 Jenkins Job 定義資料
11. 使用 Jenkins CLI 刪除 Job

Remote API 範例

```
curl http://localhost:8080/job/HelloWorld/api/json | python -m json.tool
```

```
curl http://localhost:8080/job/HelloWorld/api/json | xmllint --format -
```

Jenkins CLI 範例

```
java -jar jenkins-cli.jar -s http://localhost:8080/ delete-job HelloWorld
```

## Test Report: JUnit v.s. TAP

難度：
簡易

目標：
瞭解 Jenkins 的測試報表（Reporting）功能。

使用 YSlow for PhantomJS。

PhantomJS is a headless WebKit with JavaScript API. YSlow for PhantomJS is a command line script that allows page performance analysis from live URLs, unlike YSlow for Command Line (HAR) where a pre-generated HAR file is needed in order to analyze page performance.

http://yslow.org/phantomjs/

練習：

1. 新建 Free-Style Jenkins Job：`YSlow`
2. 執行 Shell 指令檢查 `phantomjs` 版本
3. 下載並解壓縮：`http://yslow.org/yslow-phantomjs-3.1.8.zip`
4. 執行 `phantomjs` 產生 JUnit 格式的測試報告 yslow.xml
5. 使用 Post-build actions 發佈 JUnit 測試結果報告
6. 改用 TAP Test Results 輸出測試結果

PhantomJS + YSlow 指令範例：

```
# junit
phantomjs yslow.js -i grade -threshold "B" -f junit http://localhost:8080/ > yslow.xml

# tap
phantomjs yslow.js -i grade -threshold "B" -f tap http://localhost:8080/ > yslow.tap
```

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

