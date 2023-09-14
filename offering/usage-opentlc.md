---
sort: 5
---

# OPENTLC利用手順

本手順では、Red Hat Partner Training Portalに付随するラボ環境であるOPENTLCの利用手順を記載します。

## Tabele of Contents
- [OPENTLC利用手順](#opentlc利用手順)
  - [Tabele of Contents](#tabele-of-contents)
  - [ラボ環境デプロイ手順](#ラボ環境デプロイ手順)
  - [ラボ環境操作手順](#ラボ環境操作手順)

```note
Partner Training Portalのコンテンツ改訂に伴い、OpenTLCの新規ユーザ登録は終了いたしました。

Red Hat製品のハンズオンを実施されたい方は、Partner Training Portal内のDeliveryロールのコースにて利用できるラボ環境や、[Red Hat Developer](https://developers.redhat.com/learn)でご利用いただけるWebベースのラボ環境などをご利用ください。
```

<hr>

## ラボ環境デプロイ手順

本手順では、OPENTLCを使い実際にラボ環境をデプロイする手順を記載します。

1. [OPENTLC](https://labs.opentlc.com/)にログインします。

2. 画面左側の `サービス` に<b>マウスオーバー（クリックはしない）</b>することでメニューが表示されるため、表示されたメニューから `カタログ` をクリックします。

   ![picture](https://github.com/RH-OPEN/rh-open.github.io/blob/main/offering/images/opentlc/deploy-001.png?raw=true)

2. サービスカタログより、デプロイを行う環境の製品カテゴリを選択します（画像例では"OPENTLC OpenShift 4 Labs"を選択）。

   ![picture](https://github.com/RH-OPEN/rh-open.github.io/blob/main/offering/images/opentlc/deploy-002.png?raw=true)

3. 画面右側にデプロイ可能な環境の一覧が表示されるため、対象の環境の `オーダー` ボタンをクリックします（画像例では"Hands On with OpenShift 4.10"を選択）。

   ![picture](https://github.com/RH-OPEN/rh-open.github.io/blob/main/offering/images/opentlc/deploy-003.png?raw=true)

4. オーダーの申請画面が表示されるため、下記の項目を入力し `送信` をクリックします。
   
    - Accept T & C's : チェックボックスにチェック
    - Purpose : ラボ環境を使用する目的を選択（迷う場合は、"Training - As part of course"をご選択ください）。

   ![picture](https://github.com/RH-OPEN/rh-open.github.io/blob/main/offering/images/opentlc/deploy-004.png?raw=true)

5. "要求" 画面に遷移すれば、ラボ環境のリクエストは終了です。
   - "承認状態"のステータスが"承認待ち"と表示されますが、利用者側での操作や依頼は不要です

   ![picture](https://github.com/RH-OPEN/rh-open.github.io/blob/main/offering/images/opentlc/deploy-005.png?raw=true)

6. リクエスト後、デプロイ状況が複数回メールで送信され、最終的にリクエストから1時間程度で環境へのアクセス情報がメールで送付されます。メール記載の情報を使用し環境にアクセスください。 
 - メールの文言や停止・削除時間はリクエスト対象によって異なります

 - デプロイ開始時メール例

```
From：noreply@opentlc.com
Subject：Your Red Hat OPENTLC service provision request for OTLC-LAB-xxxxx-redhat.com-PROD_ELT_HANDS_ON_OPENSHIFT_410-xxxxxx has started.

Thank you for ordering Hands On with OpenShift 4.10.
Provisioning has started on your Red Hat OPENTLC OTLC-LAB-xxxxx-redhat.com-PROD_ELT_HANDS_ON_OPENSHIFT_410-xxxx environment.
You will receive more information via email during the build process within the next 30 minutes.

The new and improved UI for RHPDS is live. Please visit demo.redhat.com to easily provision your favorite demo today! *Currently open to Red Hat Associates only.
```

 - デプロイ進捗メール例

```
From：noreply@opentlc.com
Subject：Your Red Hat OPENTLC service provision request for OTLC-LAB-xxxxx-redhat.com-PROD_ELT_HANDS_ON_OPENSHIFT_410-xxxx has updated.

Thank you for ordering Hands On with OpenShift 4.10.
Provisioning is continuing for Red Hat OPENTLC service OTLC-LAB-xxxxx-redhat.com-PROD_ELT_HANDS_ON_OPENSHIFT_410-xxxx.
You will receive another email when the environment is available within the next 75 minutes.

Try the new RHPDS experience (beta) at https://demo.redhat.com *Currently open to Red Hat Associates only.
```

 - デプロイ完了メール例（下記例では環境情報・認証情報をマスクしています）

```
From：noreply@opentlc.com
Subject：Your Red Hat OPENTLC service provision request for OTLC-LAB-xxxxx-redhat.com-PROD_ELT_HANDS_ON_OPENSHIFT_410-xxxxx_COMPLETED has completed.

Thank you for ordering Hands On with OpenShift 4.10
Your environment for OTLC-LAB-xxxxx-redhat.com-PROD_ELT_HANDS_ON_OPENSHIFT_410-xxxxxx_COMPLETED has been provisioned.
Access to the environment will be granted as soon as the environment deployment is complete.

Please refer to the instructions for next steps and how to access your environment.

Troubleshooting and Access issues:

Always refer to the instructions to understand how to properly access and navigate your environment. If you need help using the SSH client on your computer you can consult http://www.opentlc.com/ssh.html.

NOTICE: Your environment will expire and be deleted in 2 day(s) at 2023-05-19 00:00:00 -0400.

In order to conserve resources, we cannot archive or restore any data in this environment. All data will be lost upon expiration.
Here is some important information about your environment:
aws_access_key_id: XXXXXXXXXXXXXXXXX
aws_default_region: us-east-2
aws_route53_domain: .sandboxXXXX.opentlc.com
aws_secret_access_key: XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
bastion_public_hostname: bastion.XXXXX.sandboxXXXX.opentlc.com
bastion_ssh_password: xxxxxxxx
bastion_ssh_user_name: xxxxx
guid: XXXXX
openshift_api_url: https://api.cluster-XXXXX.XXXXX.sandboxXXXX.opentlc.com:6443
openshift_client_download_url: http://XXXXXXXXXXXXXXX.cloudfront.net/pub/openshift-v4/clients/ocp/stable-4.10/openshift-client-linux.tar.gz
openshift_cluster_admin_password: XXXXXXXXXXXXXXXXX
openshift_cluster_admin_username: xxxxx
openshift_console_url: https://console-openshift-console.apps.cluster-XXXXX.XXXXX.sandboxXXXX.opentlc.com
users:
  user1: {console_url: 'https://console-openshift-console.apps.cluster-XXXXX.XXXXX.sandboxXXXX.opentlc.com',
    login_command: 'oc login -u xxxxx -p XXXXXXXXXXXXXXXXX https://api.cluster-XXXXX.XXXXX.sandboxXXXX.opentlc.com:6443',
    openshift_cluster_ingress_domain: apps.cluster-XXXXX.XXXXX.sandboxXXXX.opentlc.com,
    password: XXXXXXXXXXXXXXXXX

~~ 省略 ~~
```

```tip
メールにはハイパーリンクが含まれることから、お使いのメールシステムによっては迷惑メールへと振り分けられる場合がございます。メールが受信できない場合には迷惑メールボックスも合わせてご確認ください。
```

以上でラボ環境のデプロイ手順は終了です。<br>
なお、環境は数時間で自動的に停止状態となり、数日間で自動的に消去されますので、作業終了後、利用者側で環境の削除を行う必要はありません。
停止・削除予定の延伸や、停止してしまった環境の再起動については、次の[ラボ環境操作手順](#ラボ環境操作手順)をご参照ください。

<hr>

## ラボ環境操作手順

本手順では、デプロイした環境について、停止・削除予定の延伸や、停止してしまった環境の再起動を行う手順を記載します。

1. [OPENTLC](https://labs.opentlc.com/)にログインします。

2. トップページの"アクティブなサービス"から、操作対象のサービスを選択します。

   ![picture](https://github.com/RH-OPEN/rh-open.github.io/blob/main/offering/images/opentlc/control-001.png?raw=true)

3. 画面変更後、画面上部の `App Control` をクリックし、表示されたメニューから実行対象の操作を選択します。<br>
   選択できる操作は下記です（画像例では"Extend Rutime"を選択しています）。

   - 削除：ラボ環境を削除します
   - Extend Runtime ： 環境の自動停止までの時間を延伸します
   - Extend Lifetime :  環境の自動削除までの時間を延伸します
   - 状態：環境のステータス（停止・起動状態、停止・削除予定時刻等）を出力します
   - 停止：環境を電源停止状態にします
   - 開始：停止した環境を起動します
   - Resend Final Email：デプロイ時のアクセス情報が記載されたメールを再送します

   ![picture](https://github.com/RH-OPEN/rh-open.github.io/blob/main/offering/images/opentlc/control-002.png?raw=true)

4. 実行する処理の確認画面が表示されるため、 `送信` 選択します

   ![picture](https://github.com/RH-OPEN/rh-open.github.io/blob/main/offering/images/opentlc/control-003.png?raw=true)

5. 画面遷移し、下記の"オーダー要求が送信されました"画面が表示されれば操作終了です。
   
   ![picture](https://github.com/RH-OPEN/rh-open.github.io/blob/main/offering/images/opentlc/control-004.png?raw=true)
  
   実行結果はメールでも通知されます。

   - 実行結果の通知メール例（Extend Runtime実行時）

   ```
   From：noreply@opentlc.com
   Subject：Your Red Hat OPENTLC service OTLC-LAB-xxxxx-redhat.com-PROD_ELT_HANDS_ON_OPENSHIFT_410-xxxxxx_COMPLETED runtime extend request.

   Your Red Hat OPENTLC service OTLC-LAB-xxxxx-redhat.com-PROD_ELT_HANDS_ON_OPENSHIFT_410-XXXXX_COMPLETED runtime has been extended to 2023-05-18 10:53:46 UTC.
   Your environment runtime has been extended.
   See https://www.opentlc.com/lifecycle/ for more on application runtime and lifetime.

   Have a nice day! - Red Hat Red Hat OPENTLC team
   ```

以上でラボ環境操作手順は終了です。