---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 144e67a2e58aeaa7fe7aa424ddc79bfca4aaa538
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180187"
---
# <span data-ttu-id="06a28-101">Get-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="06a28-101">Get-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="06a28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06a28-102">SYNOPSIS</span></span>
<span data-ttu-id="06a28-103">Pobiera skojarzenia reguł zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="06a28-103">Gets data collection rule association(s).</span></span>

## <span data-ttu-id="06a28-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06a28-104">SYNTAX</span></span>

### <span data-ttu-id="06a28-105">ByAssociatedResource (Default)</span><span class="sxs-lookup"><span data-stu-id="06a28-105">ByAssociatedResource (Default)</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="06a28-106">ByName</span><span class="sxs-lookup"><span data-stu-id="06a28-106">ByName</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   -AssociationName <string> 
   [-DefaultProfile <IAzureContextContainer>] 
   [<CommonParameters>]
```

### <span data-ttu-id="06a28-107">ByRule</span><span class="sxs-lookup"><span data-stu-id="06a28-107">ByRule</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="06a28-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="06a28-108">ByInputObject</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="06a28-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="06a28-109">DESCRIPTION</span></span>
<span data-ttu-id="06a28-110">Polecenie **cmdlet Get-AzDataCollectionRuleAssociation** pobiera jedno lub więcej skojarzeń reguł zbierania danych (DCRA).</span><span class="sxs-lookup"><span data-stu-id="06a28-110">The **Get-AzDataCollectionRuleAssociation** cmdlet gets one or more data collection rules associations (DCRA).</span></span>

<span data-ttu-id="06a28-111">Aby zastosować dcr do maszyny wirtualnej, należy utworzyć skojarzenie dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="06a28-111">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="06a28-112">Maszynę wirtualną może mieć skojarzenie z wieloma kontrolerami domeny i może być z nią skojarzona wiele maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="06a28-112">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="06a28-113">Dzięki temu można zdefiniować zestaw wymagań katalogowych (DCR) spełniających określone wymagania i zastosować je tylko do maszyn wirtualnych, do których mają zastosowanie.</span><span class="sxs-lookup"><span data-stu-id="06a28-113">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="06a28-114">Oto artykuł ["Konfigurowanie zbierania](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) danych dla agenta monitora Azure" przy użyciu narzędzia DCRA.</span><span class="sxs-lookup"><span data-stu-id="06a28-114">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="06a28-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06a28-115">EXAMPLES</span></span>

### <span data-ttu-id="06a28-116">Przykład 1. Uzyskiwanie skojarzeń reguł zbierania danych według identyfikatora zasobu docelowego (skojarzonej maszyny wirtualnej)</span><span class="sxs-lookup"><span data-stu-id="06a28-116">Example 1: Get data collection rules associations by target resource ID (associated virtual machine)</span></span>
```
PS C:\>$vm = Get-AzVM -ResourceGroupName $rg -Name $vmName
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="06a28-117">To polecenie zawiera listę wszystkich reguł zbierania danych dla danego identyfikatora zasobu docelowego (maszyny wirtualnej).</span><span class="sxs-lookup"><span data-stu-id="06a28-117">This command lists all the data collection rules for the given target resource ID (virtual machine).</span></span>

### <span data-ttu-id="06a28-118">Przykład 2. Pobieranie skojarzeń reguł zbierania danych według reguły (DCR)</span><span class="sxs-lookup"><span data-stu-id="06a28-118">Example 2: Get data collection rules associations by rule (DCR)</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -ResourceGroup $rg -RuleName $dcrName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="06a28-119">To polecenie zawiera listę skojarzeń reguł zbierania danych dla danej grupy zasobów i reguły (DCR).</span><span class="sxs-lookup"><span data-stu-id="06a28-119">This command lists data collection rules associations for the given resource group and rule (DCR).</span></span>

### <span data-ttu-id="06a28-120">Przykład 3. Uzyskiwanie skojarzeń reguł zbierania danych według obiektu wejściowego (PSDataCollectionRuleResource)</span><span class="sxs-lookup"><span data-stu-id="06a28-120">Example 3: Get data collection rule associations by input object (PSDataCollectionRuleResource)</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$dcr | Get-AzDataCollectionRuleAssociation

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="06a28-121">To polecenie zawiera listę skojarzeń reguł zbierania danych dla danego obiektu wejściowego.</span><span class="sxs-lookup"><span data-stu-id="06a28-121">This command lists data collection rules associations for the given input object.</span></span>

### <span data-ttu-id="06a28-122">Przykład 4. Uzyskiwanie skojarzenia reguł zbierania danych według identyfikatora zasobu docelowego (skojarzonej maszyny wirtualnej) i nazwy skojarzenia</span><span class="sxs-lookup"><span data-stu-id="06a28-122">Example 4: Get a data collection rule association by target resource ID (associated virtual machine) and association name</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="06a28-123">To polecenie wyświetla jedno (listę z jednym elementem) skojarzenia reguł zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="06a28-123">This command lists one (a list with a single element) data collection rule association.</span></span>

## <span data-ttu-id="06a28-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06a28-124">PARAMETERS</span></span>

### <span data-ttu-id="06a28-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a28-125">-DefaultProfile</span></span>
<span data-ttu-id="06a28-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="06a28-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06a28-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="06a28-127">-TargetResourceId</span></span>
<span data-ttu-id="06a28-128">Skojarzony identyfikator zasobu</span><span class="sxs-lookup"><span data-stu-id="06a28-128">The associated resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByAssociatedResource (Default)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="06a28-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a28-129">-ResourceGroupName</span></span>
<span data-ttu-id="06a28-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="06a28-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a28-131">-RuleName</span><span class="sxs-lookup"><span data-stu-id="06a28-131">-RuleName</span></span>
<span data-ttu-id="06a28-132">Nazwa reguły zbierania danych</span><span class="sxs-lookup"><span data-stu-id="06a28-132">The data collection rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases: DataCollectionRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a28-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06a28-133">-InputObject</span></span>
<span data-ttu-id="06a28-134">Obiekt PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="06a28-134">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="06a28-135">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="06a28-135">-AssociationName</span></span>
<span data-ttu-id="06a28-136">Nazwa skojarzenia.</span><span class="sxs-lookup"><span data-stu-id="06a28-136">The name of the association.</span></span>

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

### <span data-ttu-id="06a28-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a28-137">CommonParameters</span></span>
<span data-ttu-id="06a28-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06a28-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a28-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06a28-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a28-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06a28-140">INPUTS</span></span>

### <span data-ttu-id="06a28-141">System.String</span><span class="sxs-lookup"><span data-stu-id="06a28-141">System.String</span></span>
### <span data-ttu-id="06a28-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="06a28-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="06a28-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="06a28-143">OUTPUTS</span></span>

### <span data-ttu-id="06a28-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="06a28-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="06a28-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06a28-145">NOTES</span></span>

## <span data-ttu-id="06a28-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06a28-146">RELATED LINKS</span></span>

<span data-ttu-id="06a28-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="06a28-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span></span>
