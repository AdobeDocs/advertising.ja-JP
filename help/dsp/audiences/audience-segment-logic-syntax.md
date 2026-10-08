---
title: オーディエンスセグメントロジックの構文
description: オーディエンスセグメントのロジックを定義するために使用できる構文を参照します。
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
TQID: 'https://experienceleague.adobe.com/FPci9npdKrFxwge6tw41Fhx4XAC9VqYFc-RZhLhILLo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: b4dc2b3d-fdb5-55cd-9190-f1076d8563e4
    internal-label: DSP Audiences
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%
---
# オーディエンスセグメントロジックの構文

再利用可能なオーディエンスを作成する場合、英数字のセグメント ID （キー）と次の構文を使用して、セグメントロジックを手動で定義できます。

* （）グループを示す
* [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->の`||`
* [!DNL AND]の&amp;&amp;
* ! [!DNL NOT]の場合（除外）

>[!NOTE]
>
>* 指定したすべてのセグメントグループは、先頭にが付いていない限り含まれます。 （除外されます）。
>* オーディエンス [&#128279;](reusable-audience-clipboard.md)のセグメント IDは、[!UICONTROL Audiences] > [!UICONTROL All audiences]から検索できます。

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
