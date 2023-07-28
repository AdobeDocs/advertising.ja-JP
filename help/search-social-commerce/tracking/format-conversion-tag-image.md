---
title: 画像コンバージョントラッキングタグの形式
description: 画像コンバージョントラッキングタグの形式を参照します。
exl-id: 019981cd-37b6-4b80-bb48-26e0d7ac7665
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# 画像コンバージョントラッキングタグの形式

>[!NOTE]
>
>画像タグと JavaScript タグを使用するタイミングについて詳しくは、 [トラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* HTTP を使用するサイトの非セキュアタグ：

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* HTTPS を使用するサイトのセキュアタグ：

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

場所：

* `<ef-userid>` は、Search、Social および Commerce が広告主に割り当てる一意の数値ユーザー ID です。

* `<propertyname>` は、追跡されるコンバージョンです。 例えば、「登録」と呼ばれるコンバージョンを追跡している場合、タグにはパラメーターが含まれます `ev_registration=<registration>`を渡す場合は、各トランザクションの実際の売上高 ( `ev_registration=1`) をクリックします。 複数のプロパティを追跡する場合、それらのプロパティはアンパサンド (`&`など ) `ev_registration=<registration>&ev_sale=<sale>` ( 例： `ev_registration=1&ev_sale=12.99`) をクリックします。 **注意：**  プロパティ名に特殊文字を含めることはできません。

* `<transid>` は、トランザクションを識別するために広告主が生成して渡す一意のトランザクション ID（実際の注文 ID など）です。 これは、「[!UICONTROL Include unique transaction IDs]」オプションが選択されています。

  検索、ソーシャル、コマースでは、トランザクション ID を使用して、同じトランザクション ID とプロパティ値を持つ重複トランザクションを排除します。 トランザクション ID は [!UICONTROL Transaction Report]：広告主のデータとのAdobe Advertising内でデータを検証するために使用できます。 **注意：** 広告主のデータにトランザクションごとの一意の ID が含まれていない場合、検索、ソーシャル、コマースは引き続きトランザクション時間に基づいて ID を生成します。

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Adobe Advertisingのコンバージョントラッキングタグについて](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Advertisingコンバージョンタグの生成](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [コンバージョンおよびページビューのトラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript コンバージョントラッキングタグバージョン 2 の形式](format-conversion-tag-jsv2.md)
>* [JavaScript コンバージョントラッキングタグバージョン 3 の形式](format-conversion-tag-jsv3.md)
