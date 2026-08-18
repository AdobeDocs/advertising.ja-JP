---
title: Creative StudioのC2PA メタデータ
description: Creative Studioの生成AIで生成または編集されたコンテンツに、C2PA メタデータが自動的に添付される方法をご確認ください。
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d335c890ccc3ff8b2d391881660a71d10fcba53a
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 2%

---

# [!UICONTROL Creative Studio]のC2PA メタデータ

[!UICONTROL Creative Studio]は、生成AIで生成または編集されたコンテンツにC2PA メタデータを自動的に添付するので、広告コンテンツの出所は、耐久性のある目に見えないメタデータとして記録されます。 メタデータは、コンテンツの出所と信頼性に関する[連合](https://c2pa.org/) （C2PA）の標準に従っています。

## コンテンツの種類とその範囲 {#cc-content-types}

| コンテンツタイプ | サポート対象？ | コンテンツを生成するAI サービス | 資格情報を生成するモデル |
| --- | --- | --- | --- |
| 画像 | はい。 生成AIを利用して画像を生成または編集する際に、C2PA メタデータが付加され、AI アシスタントが実行するトリミングやサイズ変更の操作を通じて保存されます。 | [!DNL Adobe Firefly C2PA] | [!DNL Gemini Flash] |

## C2PA メタデータを添付するアクション

次の表は、[!UICONTROL Creative Studio] AI アシスタントで実行された画像アクションに基づいて、C2PA メタデータが添付されるタイミングをまとめたものです。

| アクション | 説明 | C2PA メタデータが添付されていますか？ | 使用例 |
| --- | --- | --- | --- |
| **画像を生成** | テキストプロンプトを使用した新しい画像の作成 | 画像は生成AIによって生成されたからです。 | テキストプロンプトを使用して、広告テンプレート用の新しい背景画像またはロゴを生成します。<br><br> テキストプロンプトを使用して、広告コンセプトのデフォルト画像を、ライブラリからアップロードされたアセットに置き換えます。<br><br> テキストプロンプトを使用して、広告テンプレートの背景画像のバリエーションを生成します。 |

## コンテンツが移動するとどうなりますか？ {#cc-content-moves}

来歴チェーン全体は、ユーザーが画像ファイルをダウンロードするか、広告で配信するために送信されるときに保持されます。

## C2PA メタデータには何が含まれますか？

生成AIの生成や変更ごとに、以下がC2PA メタデータに含まれます。 アセットが複数回変更された場合、各操作はC2PA メタデータに表示されます。

* 使用されているAI システムの名前とバージョン情報（[!DNL Adobe Firefly C2PA]）
* 使用されているAI モデル （[!DNL Gemini Flash]）
* 使用状況：生成AIを使用して生成または編集されたかどうか
* 生成AI ツールによるコンテンツの制作や修正の日時
* 一意のID （生成AIの各用途を区別するために使用できます）

## 画像のC2PA メタデータを表示するにはどうすればよいですか？

画像のアセット履歴を包括的に確認するには，

* https://contentauthenticity.adobe.com/inspectやhttps://verify.contentauthenticity.org/などのコンテンツ認証検査ツールで画像ファイルを開きます。

* 画像メタデータを表示します。

* ブラウザーのコード検査ツール（[!DNL Inspect]とも呼ばれます）を使用して画像コードを表示します。

![画像のC2PA メタデータの例](/help/creative/assets/cs-content-credentials-example.png "画像のC2PA メタデータ ")

## 関連資料

* [生成AI ユーザーガイドラインが[!DNL Adobe]件](https://www.adobe.com/jp/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

>[!MORELIKETHIS]
>
>* [Creative Studioについて](/help/creative/creative-studio/creative-studio-about.md)
