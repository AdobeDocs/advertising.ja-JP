---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---
# 階層 2 - ショッピング広告テンプレートの階層 8 フィールド

**[!UICONTROL Tier  2 - Tier 8]:** （製品グループの階層を追加する場合）製品をターゲットにする製品属性タイプと、選択した属性タイプの選定条件（例：「Brand=Acme」または「条件=新規」）。 値は階層的に適用され、適格な製品が決定されます。 属性タイプを選択し、選定条件を入力します。 次の文字は使用できません。`[ ] < > >>` （2 つの連続する「大なり」記号）は、テンプレートの列名、テンプレートのモディファイヤ名、バルクシートの [!UICONTROL Parent Product Grouping] 列の階層区切り文字を指定するために使用されます。

製品グループには、「[!UICONTROL All Products]」（階層 1）を含む最大 8 つの階層（レベル）を含めることができます。 各層には複数の製品グループを含めることができますが、同じ属性タイプ（「条件」など）に関連している必要があります。

>[!NOTE]
>
>* （[!DNL Google Ads] のみ） [!UICONTROL Channel] の可能な値は「[!UICONTROL Local]」または「[!UICONTROL Online]」で、[!UICONTROL ChannelExclusivity] の可能な値は「[!UICONTROL SingleChannel]」および「[!UICONTROL MultiChannel]」です。
>* [!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns] 表示の「[!UICONTROL Product Groups]」タブで広告グループの 2 番目の階層（子）製品グループを作成すると、デフォルトの広告グループ入札を使用して、「[!UICONTROL Everything Else]」という別の製品グループが自動的に作成されます。 ただし、在庫フィードテンプレートの使用からは、「[!UICONTROL Everything Else]」製品グループは除外されます。
>* 複数の層を含め、最後の（最も大きい番号の）層に値を使用できない場合は、次に大きい層が入札可能な製品グループとして使用されます。 例えば、5 層を含み、Tier 5 に使用できる値がない場合、Tier 4 が入札可能な製品グループ（ユニット）として使用されます。 ただし、中間層に使用可能な値がない場合、その行は無視されます。 例えば、5 つの層を含め、層 5 に値があるが層 4 には値がない場合、行 4 は無視されます。
