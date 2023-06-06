---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---
# 階層 2 — ショッピング広告テンプレートの階層 8 フィールド

**[!UICONTROL Tier  2 - Tier 8]:** （製品グループの層を追加する場合）製品のターゲットにする製品属性タイプと、選択した属性タイプの適格な条件（例：Brand=Acme や Condition=New）。 値は階層的に適用され、対象となる製品が決定されます。 属性タイプを選択し、条件を入力します。 禁止される文字は次のとおりです。 `[ ] < > >>` （連続する「より大きい」記号）。テンプレート内の列名、テンプレート内の修飾子名、 [!UICONTROL Parent Product Grouping] 」列が表示されます。

最大 8 階層（レベル）の製品グループを含めることができます。[!UICONTROL All Products]「（第 1 層）。 各層には複数の製品グループを含めることができますが、同じ属性タイプ（「条件」など）に関係する必要があります。

>[!NOTE]
>
>* ([!DNL Google Ads] 唯一 ) [!UICONTROL Channel] 」[!UICONTROL Local]&quot;または&quot;[!UICONTROL Online]、」および [!UICONTROL ChannelExclusivity] 」[!UICONTROL SingleChannel]&quot;および&quot;[!UICONTROL MultiChannel].&quot;
>* 広告グループの 2 番目の層（子）製品グループを [!UICONTROL Product Groups] 」タブをクリックします。 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 表示、別の製品グループ (「 」)[!UICONTROL Everything Else]、」はデフォルトの広告グループ入札を使用して自動的に作成されます。 ただし、在庫フィードテンプレートを使用する場合は、「[!UICONTROL Everything Else]」個の製品グループが除外されます。
>* 複数の階層を含み、最終（最も大きい番号の）階層に値が提供されない場合、次に大きい層が入札可能な製品グループとして使用されます。 例えば、5 層を含み、Tier 5 に値がない場合、Tier 4 が入札可能な製品グループ（ユニット）として使用されます。 ただし、中間層に値がない場合、その行は無視されます。 例えば、5 つの階層を含み、Tier 5 の値が Tier 4 の値ではない場合、Row 4 は無視されます。

