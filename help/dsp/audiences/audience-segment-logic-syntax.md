---
title: オーディエンスセグメントロジックの構文
description: オーディエンスセグメントのロジックを定義するために使用できる構文を参照します。
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
TQID: https://experienceleague.adobe.com/FPci9npdKrFxwge6tw41Fhx4XAC9VqYFc-RZhLhILLo
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 0%

---

# オーディエンスセグメントロジックの構文

再利用可能なオーディエンスを作成する場合、英数字のセグメント ID （キー）と次の構文を使用して、セグメントロジックを手動で定義できます。

* （）グループを示す
* `||` [!DNL OR]の<!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* [!DNL AND]の&amp;&amp;
* ! [!DNL NOT]の場合（除外）

>[!NOTE]
>
>* 指定したすべてのセグメントグループは、先頭にが付いていない限り含まれます。 （除外されます）。
>* オーディエンス [のセグメント IDは、](reusable-audience-clipboard.md) > [!UICONTROL Audiences]から[!UICONTROL All audiences]検索できます。

例えば、次のロジックを使用します。

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

意味（平易な英語）

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>プレースメント設定では、保存したオーディエンスを明示的にターゲティングするオーディエンスとして使用したり、ターゲティングから除外する個別のオーディエンスとして使用したりできます。 セグメントロジックに、オーディエンスを使用する目的が反映されていることを確認します。

>[!MORELIKETHIS]
>
>* [再利用可能なオーディエンスのセグメントキーをクリップボードにコピー](reusable-audience-clipboard.md)
>* [&#x200B; オーディエンス管理について](audience-about.md)
>* [再利用可能なオーディエンスを作成](reusable-audience-create.md)
>* [&#x200B; オーディエンス設定](audience-settings.md)
>* [使用可能なサードパーティのデータプロバイダー](third-party-data-providers.md)
