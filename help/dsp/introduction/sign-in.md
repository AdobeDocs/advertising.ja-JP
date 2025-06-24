---
title: DSPへのログイン
description: DSPへのログイン方法を説明します。
feature: DSP Introduction
exl-id: 1704cd75-81f8-4715-a177-69a03093ba1d
source-git-commit: 143c7bfc38baca48abde323cbca7f582de234bc1
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# Adobe Advertising DSPへのログイン

Adobe Advertising DSPは、ログイン認証のためにAdobe Identity Management サービス（IMS）に移行しています。 IMS を使用すると、Real-Time Customer Data Platform、Customer Journey Analytics、Target、Analytics など、IMS をサポートするすべての [!DNL Adobe] 製品にシングルサインオン（SSO）でアクセスできます。 （変更に伴う）

* 1 つの [!DNL Adobe ID] を使用して、Experience Cloudのログインページまたは従来のDSPのログインページから、[!DNL Adobe] つの製品間でログインできます。 [!DNL Adobe ID] はユーザープロファイル管理を提供します。 今後のリリースでは、トップメニューからDSP アカウント、IMS 組織アカウント、[!DNL Adobe] 商品を変更できるようになります。

* エンタープライズ認証がサポートされています。

* 1 時間ごとにログインする代わりに、24 時間ログインしたままにすることができます。

現在のDSP資格情報は 2025 年 7 月 15 日（PT）まで有効なので、変更に備えることができます。

## 従来のDSP ログインを認証に使用

* [advertising.adobe.com](https://advertising.adobe.com) に移動し、従来のDSP資格情報を使用してログインします。

## 認証に [!DNL Adobe ID] を使用

1. 次のいずれかのログイン画面を開きます。

   * [advertising.adobe.com](https://advertising.adobe.com) に移動します。 「[!UICONTROL Sign in with the Adobe Experience Cloud account]」の下の「**[!UICONTROL Continue]**」をクリックします。

   * [experience.adobe.com](https://experience.adobe.com) に移動します。

1. 資格情報を入力：

   * 既に [!DNL Adobe] アカウントを使用している場合は、既存の資格情報を使用してログインします。

   * [!DNL Adobe] アカウントがない場合は、[!DNL Adobe] アカウントの作成を招待するメールを探します。 DSP アカウントごとに 1 件の招待状が届きます。 メールに記載されたリンクをたどって資格情報を設定します。 複数のDSP アカウントがある場合は、手順に従ってそれらをリンクします。

1. 組織を選択します。

   * プロンプトが表示されたら、「個人用アカウント**または **会社または学校用アカウント** を選択します。

   * 複数の IMS 組織にアクセスできる場合は、正しい組織を選択します。

ユーザープロファイルの管理など、Experience Cloud インターフェイスの詳細については、「[Experience Cloud インターフェイスと管理 ](https://experienceleague.adobe.com/en/docs/core-services/interface/experience-cloud)」を参照してください。

### トラブルシューティング

一般的なログインの問題については、「[Adobe アカウントのログインの問題の解決 ](https://helpx.adobe.com/manage-account/kb/account-password-sign-help.linkfree.html)」も参照してください。

#### 新しい [!DNL Adobe] IMS ログインを有効にするための前提条件はありますか？

新しいログインアカウントを追加するには、メールアドレスをAdobe アカウントチームに伝えます。 サポートチームが、DSPのプロビジョニング先である IMS 組織のユーザーリストにユーザーのアドレスを追加します。

その間、ユーザーは従来のDSP資格情報を引き続き使用できます。

#### Adobe IMSアカウントを使用してログインすると、adobe.advertising.comのログインページにリダイレクトされます。

使用しているメールが IMS 組織に追加されたことを IMS 組織の管理者に確認します。 IMS 組織に追加されたことを管理者が確認した場合は、Adobe アカウントチームに依頼して、DSPを使用するためにアカウントをプロビジョニングします。

その間、従来のDSP資格情報を引き続き使用できます。

#### 誤ったメールアドレスでログインしましたが、[!DNL Adobe] にログインしましたが、DSPへのアクセスが提供されません。

1. [experience.adobe.com](https://experience.adobe.com) に移動してログアウトします。

1. [advertising.adobe.com](https://advertising.adobe.com) に移動し、正しいメール ID でログインします。

#### [!DNL Adobe] の IMS アカウントとDSP アカウントは、別のメールに登録されています。 [!DNL Adobe] IMS アカウントを使用してログインするにはどうすればよいですか？

Adobeを使用するために、既存の [!DNL Adobe] IMS アカウントのプロビジョニングをDSP アカウントチームにお問い合わせください。
