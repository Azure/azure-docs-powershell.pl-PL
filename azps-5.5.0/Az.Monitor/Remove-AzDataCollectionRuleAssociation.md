---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 798bb97b9e84121894341dd807bbaa9b3658a039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203405"
---
# <span data-ttu-id="65fdd-101">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="65fdd-101">Remove-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="65fdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="65fdd-103">Usuwanie skojarzenia reguł zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="65fdd-103">Delete a data collection rule association.</span></span>

## <span data-ttu-id="65fdd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="65fdd-104">SYNTAX</span></span>

### <span data-ttu-id="65fdd-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="65fdd-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -TargetResourceId <string> 
      -AssociationName <string> 
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="65fdd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="65fdd-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="65fdd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65fdd-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="65fdd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="65fdd-108">DESCRIPTION</span></span>
<span data-ttu-id="65fdd-109">Polecenie **cmdlet Remove-AzDataCollectionRuleAssociation** usuń skojarzenie reguł zbierania danych (DCRA).</span><span class="sxs-lookup"><span data-stu-id="65fdd-109">The **Remove-AzDataCollectionRuleAssociation** cmdlet delete a data collection rule association (DCRA).</span></span>

<span data-ttu-id="65fdd-110">Aby zastosować dcr do maszyny wirtualnej, należy utworzyć skojarzenie dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="65fdd-110">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="65fdd-111">Maszynę wirtualną może mieć skojarzenie z wieloma kontrolerami domeny i może być z nią skojarzona wiele maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="65fdd-111">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="65fdd-112">Dzięki temu można zdefiniować zestaw wymagań katalogowych (DCR) spełniających określone wymagania i zastosować je tylko do maszyn wirtualnych, do których mają zastosowanie.</span><span class="sxs-lookup"><span data-stu-id="65fdd-112">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="65fdd-113">Oto artykuł ["Konfigurowanie zbierania](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) danych dla agenta monitora Azure" przy użyciu narzędzia DCRA.</span><span class="sxs-lookup"><span data-stu-id="65fdd-113">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="65fdd-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="65fdd-114">EXAMPLES</span></span>

### <span data-ttu-id="65fdd-115">Przykład 1. Usuwanie skojarzenia reguły zbierania danych z parametrami nazwa i identyfikator zasobu docelowego (skojarzona maszyna wirtualna)</span><span class="sxs-lookup"><span data-stu-id="65fdd-115">Example 1: Delete data collection rule association with name and target resource ID (associated virtual machine) parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### <span data-ttu-id="65fdd-116">Przykład 2. Usuwanie reguły zbierania danych przy użyciu obiektu Input Object</span><span class="sxs-lookup"><span data-stu-id="65fdd-116">Example 2: Delete data collection rule with Input Object</span></span>
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### <span data-ttu-id="65fdd-117">Przykład 3. Usuwanie reguły zbierania danych przy użyciu właściwości identyfikatorów zasobów skojarzenia</span><span class="sxs-lookup"><span data-stu-id="65fdd-117">Example 3: Delete data collection rule with the association resource ID property</span></span>
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## <span data-ttu-id="65fdd-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65fdd-118">PARAMETERS</span></span>

### <span data-ttu-id="65fdd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65fdd-119">-DefaultProfile</span></span>
<span data-ttu-id="65fdd-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="65fdd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65fdd-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="65fdd-121">-TargetResourceId</span></span>
<span data-ttu-id="65fdd-122">Skojarzony identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="65fdd-122">The associated resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65fdd-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="65fdd-123">-AssociationName</span></span>
<span data-ttu-id="65fdd-124">Nazwa zasobu skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="65fdd-124">The name of the association resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName (Default)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65fdd-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65fdd-125">-InputObject</span></span>
<span data-ttu-id="65fdd-126">Obiekt PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="65fdd-126">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="65fdd-127">-AssociationId</span><span class="sxs-lookup"><span data-stu-id="65fdd-127">-AssociationId</span></span>
<span data-ttu-id="65fdd-128">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="65fdd-128">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65fdd-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65fdd-129">-Confirm</span></span>
<span data-ttu-id="65fdd-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="65fdd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65fdd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65fdd-131">-WhatIf</span></span>
<span data-ttu-id="65fdd-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65fdd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65fdd-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="65fdd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65fdd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65fdd-134">CommonParameters</span></span>
<span data-ttu-id="65fdd-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65fdd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65fdd-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65fdd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65fdd-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65fdd-137">INPUTS</span></span>

### <span data-ttu-id="65fdd-138">System.String</span><span class="sxs-lookup"><span data-stu-id="65fdd-138">System.String</span></span>
###<span data-ttu-id="65fdd-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="65fdd-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="65fdd-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65fdd-140">OUTPUTS</span></span>

### <span data-ttu-id="65fdd-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65fdd-141">System.Boolean</span></span>

## <span data-ttu-id="65fdd-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="65fdd-142">NOTES</span></span>

## <span data-ttu-id="65fdd-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65fdd-143">RELATED LINKS</span></span>

<span data-ttu-id="65fdd-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="65fdd-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span></span>
