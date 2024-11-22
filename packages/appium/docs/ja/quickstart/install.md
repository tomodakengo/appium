---
hide:
  - toc

title: Appiumをインストールする
---

<!--
!!! info

    Before installing, make sure to check the [System Requirements](./requirements.md).
-->

!!! info

    インストールする前に、[システム要件](./requirements.md)を確認してください。

<!--
Appium can be installed globally using `npm`:
-->

Appiumは `npm`を使ってグローバルにインストールできます：

```bash
npm install -g appium
```

<!--
!!! note

    Other package managers are not currently supported.
-->

!!! note

    その他のパッケージマネージャーは現在サポートされていません。


## Appiumを始めよう

<!--
Appium can be started [using the command line](../cli/index.md):
-->

Appiumは[コマンドラインを使って](../cli/index.md)起動できます:

```
appium
```

<!--
This launches the Appium server process, which loads all the installed Appium drivers, and
begins waiting for new session requests from client connections (such as test automation scripts).
Since the server process is independent from its clients, it must be explicitly launched before
attempting to start a new session.
-->

これによりAppiumのサーバープロセスが起動し、インストールされているすべてのAppiumドライバーをロードし、
クライアント(テスト自動化スクリプトなど)からの新しいセッションの要求を待ちます。
サーバープロセスはクライアントから独立しているため、新しいセッションを開始する前に明示的に起動する必要があります。

<!--
When the server is launched, the console log will list all the valid URLs that clients can use to
connect to this server:
-->

サーバーが起動すると、クライアントがこのサーバーに接続するために使用できる有効なURLの一覧がコンソールログに表示されます:

```
[Appium] You can provide the following URLs in your client code to connect to this server:
[Appium] 	http://127.0.0.1:4723/ (only accessible from the same host)
(... any other URLs ...)
```

<!--
Once a client requests a new session, the Appium server process will start logging all details about
this session until its termination. Keep this in mind - if you ever encounter issues with Appium
tests, you can always check the server log for more details.
-->

一度クライアントが新しいセッションを要求すると、Appiumのサーバープロセスはセッションが終了するまで、このセッションに関するすべての詳細を記録します。
このことを覚えておいてください - Appiumのテストで問題が発生した場合は、いつでもサーバーログで詳細を確認することができます。

<!--
So what's next? Even though Appium is installed and running, it does not come bundled with any
drivers, which means it cannot automate anything yet. We will therefore set up automation for
Android - continue to [Installing the UiAutomator2 Driver](./uiauto2-driver.md).
-->

それでは次は何をしましょうか？
Appiumはインストールされ実行されていますが、まだドライバーはバンドルされていません。
そのため、Android用の自動化を設定していきます。
[UiAutomator2ドライバーをインストールする](./uiauto2-driver.md)に続きます。
