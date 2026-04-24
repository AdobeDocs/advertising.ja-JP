---
title: DSPにログイン
description: DSPへのログイン方法を説明します。
feature: DSP Introduction
exl-id: 1704cd75-81f8-4715-a177-69a03093ba1d
TQID: https://experienceleague.adobe.com/KjBIag8qcpMONcX6pS2IJot3IA4Q-KOq0Av-1VzAot4
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: 535
ht-degree: 0%

---

# Adobe Advertising DSPにログイン

Adobe Advertising DSPは、ログイン認証のためにAdobe Identity Management サービス（IMS）に移行中です。 IMSは、Real-Time Customer Data Platform、Customer Journey Analytics、[!DNL Target]、[!DNL Analytics]など、IMSをサポートするすべての[!DNL Adobe]製品に対して、フェデレーション IDを使用したシングルサインオン（SSO）アクセスを提供します。 変更内容：

* 1つの[!DNL Adobe ID]を使用して、Adobe CX Enterprise（旧Adobe Experience Cloud）のログインページまたは従来のDSPのログインページから[!DNL Adobe]製品間でログインできます。 お客様の[!DNL Adobe ID]はユーザープロファイル管理を提供しています。 今後のリリースでは、上部メニューからDSP アカウント、IMS組織アカウント、および[!DNL Adobe]製品を変更できるようになります。

* エンタープライズ認証がサポートされています。

* 1時間ごとにログインするのではなく、24時間ログインし続けることができます。

現在のDSP資格情報は、変更に備えることができるように、短期間アクティブのままになります。

## 認証に従来のDSP ログインを使用する

* [advertising.adobe.com](https://advertising.adobe.com)に移動し、従来のDSP資格情報を使用してログインします。

## 認証に[!DNL Adobe ID]を使用

1. 次のいずれかのログイン画面を開きます。

   * [advertising.adobe.com](https://advertising.adobe.com)に移動します。 「[!UICONTROL Sign in with the Adobe Experience Cloud account]」で、「**[!UICONTROL Continue]**」をクリックします。

   * [experience.adobe.com](https://experience.adobe.com)に移動します。

1. 資格情報を入力してください：

   * 既に[!DNL Adobe] アカウントを使用している場合は、既存の資格情報でログインします。

   * [!DNL Adobe] アカウントをお持ちでない場合は、[!DNL Adobe] アカウントの作成を促す電子メールを探します。 DSP アカウントごとに1件の招待状が届きます。 電子メールのリンクに従って、資格情報を設定します。 複数のDSP アカウントがある場合は、手順に従ってリンクします。

1. 組織の選択：

   * プロンプトが表示されたら、「[!UICONTROL Personal Account]」または「**[!UICONTROL Company or School Account]**」**選択します。

   * 複数のIMS組織にアクセスできる場合は、正しいものを選択します。

ユーザープロファイルの管理など、CX Enterprise インターフェイスについて詳しくは、「[CX Enterprise インターフェイスと管理](https://experienceleague.adobe.com/en/docs/core-services/interface/experience-cloud)」を参照してください。

### トラブルシューティング

一般的なログインの問題については、「[Adobe アカウントのログインの問題を解決](https://helpx.adobe.com/manage-account/kb/account-password-sign-help.linkfree.html)」も参照してください。

#### 新しい[!DNL Adobe] IMS ログインを有効にするための前提条件はありますか？

新しいログインアカウントを追加するには、メールアドレスをAdobe アカウントチームと共有します。 DSPのプロビジョニング先のIMS組織のユーザーリストに、お客様のアドレスが追加されます。

その間、ユーザーは引き続き従来のDSP資格情報を使用できます。

#### Adobe IMSアカウントを使用してログインした後、adobe.advertising.com ログインページにリダイレクトされます。

使用している電子メールがIMS組織に追加されたことをIMS組織の管理者に確認します。 IMS組織に追加されたことを管理者が確認した場合は、Adobe アカウントチームに対して、DSPを使用するようにアカウントをプロビジョニングするように依頼します。

その間、従来のDSP資格情報を引き続き使用できます。

#### 間違った電子メールアドレスでサインインし、[!DNL Adobe]にサインインしましたが、DSP アクセスを提供していません。

1. [experience.adobe.com](https://experience.adobe.com)に移動してログアウトします。

1. [advertising.adobe.com](https://advertising.adobe.com)に移動し、正しい電子メール IDでログインします。

#### 自分の[!DNL Adobe] IMS アカウントとDSP アカウントは、別の電子メールで登録されています。 [!DNL Adobe] IMS アカウントを使用してログインするにはどうすればよいですか？

DSPを使用するために、既存の[!DNL Adobe] IMS アカウントをプロビジョニングするようにAdobe アカウントチームに依頼します。
