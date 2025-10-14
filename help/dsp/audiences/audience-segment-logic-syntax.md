---
title: オーディエンスセグメントロジックの構文
description: オーディエンスセグメントのロジックの定義に使用できる構文を参照します。
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# オーディエンスセグメントロジックの構文

再利用可能なオーディエンスを作成する場合、英数字のセグメント ID （キー）と次の構文を使用して、セグメントロジックを手動で定義できます。

* （） グループを示す
* [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table --> の `||`
* [!DNL AND] の&amp;&amp;
* ! [!DNL NOT] の場合（除外）

>[!NOTE]
>
>* 先頭にが付いていない限り、指定したセグメントグループがすべて含まれます。 （これらのプロパティは除外されます）。
>* [!UICONTROL Audiences]/[!UICONTROL All audiences] から [&#x200B; オーディエンスのセグメント ID を検索 &#x200B;](reusable-audience-clipboard.md) できます。

例えば、次のようなロジックがあります。

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

平均（平易な英語で）

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>プレースメント設定では、保存されたオーディエンスを、明示的にターゲットにするオーディエンスとして、または個別のオーディエンスとして使用して、ターゲティングから除外できます。 セグメントロジックにオーディエンスを使用する目的が反映されていることを確認します。

>[!MORELIKETHIS]
>
>* [&#x200B; 再利用可能なオーディエンスのセグメントキーをクリップボードにコピー &#x200B;](reusable-audience-clipboard.md)
>* [Audience Management について &#x200B;](audience-about.md)
>* [&#x200B; 再利用可能なオーディエンスを作成 &#x200B;](reusable-audience-create.md)
>* [&#x200B; オーディエンス設定 &#x200B;](audience-settings.md)
>* [&#x200B; 利用可能なサードパーティデータプロバイダー &#x200B;](third-party-data-providers.md)
