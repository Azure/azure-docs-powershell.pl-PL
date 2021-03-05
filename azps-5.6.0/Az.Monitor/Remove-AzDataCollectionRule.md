---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
ms.openlocfilehash: 4dfa9417b2bce7473b3d2986f503c163cb6bf42f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974801"
---
# <span data-ttu-id="5d6a1-101">Remove-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="5d6a1-101">Remove-AzDataCollectionRule</span></span>

## <span data-ttu-id="5d6a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="5d6a1-103">Usuwanie reguły zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-103">Delete a data collection rule.</span></span>

## <span data-ttu-id="5d6a1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5d6a1-104">SYNTAX</span></span>

### <span data-ttu-id="5d6a1-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="5d6a1-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRule
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="5d6a1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5d6a1-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRule
   -InputObject <PSDataCollectionRuleResource>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="5d6a1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d6a1-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRule
   -RuleId <string>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="5d6a1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5d6a1-108">DESCRIPTION</span></span>
<span data-ttu-id="5d6a1-109">Polecenie **cmdlet Remove-AzDataCollectionRule** usuń regułę zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-109">The **Remove-AzDataCollectionRule** cmdlet delete a data collection rule.</span></span>

<span data-ttu-id="5d6a1-110">Reguły zbierania danych (DCR, Data Collection Rules) definiują dane trafiace do usługi Azure Monitor i określają, gdzie te dane mają być wysyłane lub przechowywane.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="5d6a1-111">Oto pełny artykuł [z omówieniem funkcji DCR.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="5d6a1-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="5d6a1-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5d6a1-112">EXAMPLES</span></span>

### <span data-ttu-id="5d6a1-113">Przykład 1. Usuwanie reguły zbierania danych przy użyciu parametrów nazwy i grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5d6a1-113">Example 1: Delete data collection rule with name and resource group parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr"             
```

### <span data-ttu-id="5d6a1-114">Przykład 2. Usuwanie reguły zbierania danych przy użyciu reguły zwracania nazwy i grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5d6a1-114">Example 2: Delete data collection rule with name and resource group return bool</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr" -PassThru

True
```

### <span data-ttu-id="5d6a1-115">Przykład 3. Usuwanie reguły zbierania danych z inputObject</span><span class="sxs-lookup"><span data-stu-id="5d6a1-115">Example 3: Delete data collection rule from InputObject</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroupName "testdcr" -RuleName "dcrFromPipe95" | Remove-AzDataCollectionRule
```

### <span data-ttu-id="5d6a1-116">Przykład 4. Usuwanie reguły zbierania danych ze identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="5d6a1-116">Example 4: Delete data collection rule from resource id</span></span>
```
PS C:\>Remove-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/{dcrName}"
```

## <span data-ttu-id="5d6a1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d6a1-117">PARAMETERS</span></span>

### <span data-ttu-id="5d6a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d6a1-118">-DefaultProfile</span></span>
<span data-ttu-id="5d6a1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5d6a1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d6a1-120">-ResourceGroupName</span></span>
<span data-ttu-id="5d6a1-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5d6a1-121">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d6a1-122">-RuleName</span><span class="sxs-lookup"><span data-stu-id="5d6a1-122">-RuleName</span></span>
<span data-ttu-id="5d6a1-123">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d6a1-124">-RuleId</span><span class="sxs-lookup"><span data-stu-id="5d6a1-124">-RuleId</span></span>
<span data-ttu-id="5d6a1-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-125">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d6a1-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d6a1-126">-Confirm</span></span>
<span data-ttu-id="5d6a1-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6a1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d6a1-128">-WhatIf</span></span>
<span data-ttu-id="5d6a1-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d6a1-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d6a1-131">CommonParameters</span></span>
<span data-ttu-id="5d6a1-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d6a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d6a1-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d6a1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d6a1-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d6a1-134">INPUTS</span></span>

### <span data-ttu-id="5d6a1-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5d6a1-135">System.String</span></span>

## <span data-ttu-id="5d6a1-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d6a1-136">OUTPUTS</span></span>

### <span data-ttu-id="5d6a1-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="5d6a1-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="5d6a1-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5d6a1-138">NOTES</span></span>

## <span data-ttu-id="5d6a1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d6a1-139">RELATED LINKS</span></span>

<span data-ttu-id="5d6a1-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="5d6a1-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>