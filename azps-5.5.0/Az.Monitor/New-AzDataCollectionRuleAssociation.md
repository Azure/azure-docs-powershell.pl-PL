---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: bdfc576c64b56d11ecf30f32e34f80b0ef6de866
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203425"
---
# <span data-ttu-id="05f76-101">New-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="05f76-101">New-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="05f76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05f76-102">SYNOPSIS</span></span>
<span data-ttu-id="05f76-103">Tworzenie skojarzenia reguł zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="05f76-103">Create data collection rule association.</span></span>

## <span data-ttu-id="05f76-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="05f76-104">SYNTAX</span></span>

### <span data-ttu-id="05f76-105">ByDataCollectionRuleId (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="05f76-105">ByDataCollectionRuleId (Default)</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -RuleId <string>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="05f76-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="05f76-106">ByInputObject</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -InputObject <PSDataCollectionRuleResource>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]  
   [-WhatIf]   
   [-Confirm]   
   [<CommonParameters>]
```


## <span data-ttu-id="05f76-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="05f76-107">DESCRIPTION</span></span>
<span data-ttu-id="05f76-108">Polecenie **cmdlet New-AzDataCollectionRuleAssociation** tworzy skojarzenie reguł zbierania danych (DCRA).</span><span class="sxs-lookup"><span data-stu-id="05f76-108">The **New-AzDataCollectionRuleAssociation** cmdlet creates a data collection rules association (DCRA).</span></span>

<span data-ttu-id="05f76-109">Aby zastosować dcr do maszyny wirtualnej, należy utworzyć skojarzenie dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="05f76-109">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="05f76-110">Maszynę wirtualną może mieć skojarzenie z wieloma kontrolerami domeny i może być z nią skojarzona wiele maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="05f76-110">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="05f76-111">Umożliwia to zdefiniowanie zestawu wymagań katalogowych (DCR) spełniających określone wymagania i zastosowanie ich tylko do maszyn wirtualnych, do których mają zastosowanie.</span><span class="sxs-lookup"><span data-stu-id="05f76-111">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="05f76-112">Oto artykuł ["Konfigurowanie zbierania](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) danych dla agenta monitora Azure" przy użyciu narzędzia DCRA.</span><span class="sxs-lookup"><span data-stu-id="05f76-112">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="05f76-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="05f76-113">EXAMPLES</span></span>

### <span data-ttu-id="05f76-114">Przykład 1. Tworzenie skojarzenia reguł zbierania danych</span><span class="sxs-lookup"><span data-stu-id="05f76-114">Example 1: Create data collection rule association</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssoc" -RuleId $dcr.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssoc
Name                 : dcrAssoc
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="05f76-115">To polecenie tworzy skojarzenie reguły zbierania danych dla danej reguły i identyfikatora zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="05f76-115">This command creates a data collection rule association for given rule and target resource ID.</span></span>

### <span data-ttu-id="05f76-116">Przykład 2. Tworzenie skojarzenia reguł zbierania danych z obiektu DCR</span><span class="sxs-lookup"><span data-stu-id="05f76-116">Example 2: Create data collection rule association from a DCR object</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>$dcr | New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssocInput"

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssocInput
Name                 : dcrAssocInput
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="05f76-117">To polecenie tworzy skojarzenie reguły zbierania danych dla danej reguły i identyfikatora zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="05f76-117">This command creates a data collection rule association for given rule and target resource ID.</span></span>

## <span data-ttu-id="05f76-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05f76-118">PARAMETERS</span></span>

### <span data-ttu-id="05f76-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05f76-119">-DefaultProfile</span></span>
<span data-ttu-id="05f76-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="05f76-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05f76-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="05f76-121">-TargetResourceId</span></span>
<span data-ttu-id="05f76-122">Identyfikator zasobu do skojarzenia</span><span class="sxs-lookup"><span data-stu-id="05f76-122">The resource ID to associate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f76-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="05f76-123">-AssociationName</span></span>
<span data-ttu-id="05f76-124">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="05f76-124">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f76-125">-RuleId</span><span class="sxs-lookup"><span data-stu-id="05f76-125">-RuleId</span></span>
<span data-ttu-id="05f76-126">Identyfikator reguły zbierania danych</span><span class="sxs-lookup"><span data-stu-id="05f76-126">The data collection rule ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByDataCollectionRuleId
Aliases: DataCollectionRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f76-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05f76-127">-InputObject</span></span>
<span data-ttu-id="05f76-128">Obiekt PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="05f76-128">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="05f76-129">— Opis</span><span class="sxs-lookup"><span data-stu-id="05f76-129">-Description</span></span>
<span data-ttu-id="05f76-130">Opis zasobu</span><span class="sxs-lookup"><span data-stu-id="05f76-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f76-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05f76-131">-Confirm</span></span>
<span data-ttu-id="05f76-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="05f76-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05f76-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05f76-133">-WhatIf</span></span>
<span data-ttu-id="05f76-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05f76-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05f76-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="05f76-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05f76-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f76-136">CommonParameters</span></span>
<span data-ttu-id="05f76-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05f76-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05f76-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05f76-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f76-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05f76-139">INPUTS</span></span>

### <span data-ttu-id="05f76-140">System.String</span><span class="sxs-lookup"><span data-stu-id="05f76-140">System.String</span></span>

## <span data-ttu-id="05f76-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05f76-141">OUTPUTS</span></span>

### <span data-ttu-id="05f76-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="05f76-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="05f76-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="05f76-143">NOTES</span></span>

## <span data-ttu-id="05f76-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05f76-144">RELATED LINKS</span></span>

<span data-ttu-id="05f76-145">[Set-AzDataCollectionRuleAssociation](./Set-AzDataCollectionRuleAssociation.md) 
 [Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="05f76-145">[Set-AzDataCollectionRuleAssociation](./Set-AzDataCollectionRuleAssociation.md)
[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span></span>
