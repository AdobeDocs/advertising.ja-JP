---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---
# Tier 2 - ショッピング広告テンプレートのTier 8 フィールド

**[!UICONTROL Tier  2 - Tier 8]:** （製品グループの階層を追加する場合）製品をターゲットにする製品属性タイプ、および選択した属性タイプの適格基準（Brand=AcmeまたはCondition=Newなど）。 値は階層的に適用され、適格な製品を決定します。 属性タイプを選択し、適格基準を入力します。 使用禁止文字には次のものが含まれます。`[ ] < > >>` （連続した2つの「大なり」記号）。テンプレート内の列名、テンプレート内の修飾子名、バルクシート内の[!UICONTROL Parent Product Grouping]列の階層区切り文字を指定するために使用されます。

「[!UICONTROL All Products]」（Tier 1）を含め、最大8つの階層（レベル）の製品グループを含めることができます。 各層には複数の製品グループを含めることができますが、同じ属性タイプ（「条件」など）に関連する必要があります。

>[!NOTE]
>
>* （[!DNL Google Ads]のみ） [!UICONTROL Channel]の指定可能な値は「[!UICONTROL Local]」または「[!UICONTROL Online]」であり、[!UICONTROL ChannelExclusivity]の指定可能な値は「[!UICONTROL SingleChannel]」および「[!UICONTROL MultiChannel]」です。
>* [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] ビューの[!UICONTROL Product Groups] タブから広告グループの2番目の階層（子）製品グループを作成すると、デフォルトの広告グループ入札を使用して、「[!UICONTROL Everything Else]」という別の製品グループが自動的に作成されます。 ただし、在庫フィード テンプレートを使用すると、「[!UICONTROL Everything Else]」製品グループは除外されます。
>* 複数の階層を含め、最終的な（最も番号の高い）階層に値が使用できない場合、次に高い階層が入札可能な製品グループとして使用されます。 例えば、5つの階層を含み、Tier 5に値が使用できない場合、Tier 4は入札可能な製品グループ（ユニット）として使用されます。 ただし、中間層に使用できる値がない場合、その行は無視されます。 例えば、5つの階層を含み、Tier 5に値があるがTier 4に値がない場合、行4は無視されます。
