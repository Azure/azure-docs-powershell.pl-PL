---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: 8fadba097b602bd84c8eb36d75f5b7a331e2280b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972545"
---
# <span data-ttu-id="80609-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="80609-101">Set-AzSearchService</span></span>

## <span data-ttu-id="80609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80609-102">SYNOPSIS</span></span>
<span data-ttu-id="80609-103">Zaktualizuj usługę Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="80609-103">Update an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="80609-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="80609-104">SYNTAX</span></span>

### <span data-ttu-id="80609-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="80609-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>]
 [-IPRuleList <PSIpRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80609-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80609-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80609-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80609-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80609-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="80609-108">DESCRIPTION</span></span>
<span data-ttu-id="80609-109">Polecenie **cmdlet Set-AzSearchService** modyfikuje usługę Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="80609-109">The **Set-AzSearchService** cmdlet modifies an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="80609-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="80609-110">EXAMPLES</span></span>

### <span data-ttu-id="80609-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="80609-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="80609-112">Przykład zmienia liczbę partycji i liczbę replik usługi Azure Cognitive Search na 2.</span><span class="sxs-lookup"><span data-stu-id="80609-112">The example changes partition count and replica count of the Azure Cognitive Search service to 2.</span></span>

## <span data-ttu-id="80609-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80609-113">PARAMETERS</span></span>

### <span data-ttu-id="80609-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80609-114">-DefaultProfile</span></span>
<span data-ttu-id="80609-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="80609-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80609-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="80609-116">-IdentityType</span></span>
<span data-ttu-id="80609-117">(Opcjonalnie) Azure Cognitive Search Service Identity (None/SystemAssigned)</span><span class="sxs-lookup"><span data-stu-id="80609-117">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSIdentityType]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80609-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80609-118">-InputObject</span></span>
<span data-ttu-id="80609-119">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="80609-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80609-120">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="80609-120">-IPRuleList</span></span>
<span data-ttu-id="80609-121">(Opcjonalnie) Reguły IP usługi Azure Cognitive Search Service</span><span class="sxs-lookup"><span data-stu-id="80609-121">(Optional) Azure Cognitive Search Service IP rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80609-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="80609-122">-Name</span></span>
<span data-ttu-id="80609-123">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="80609-123">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80609-124">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="80609-124">-PartitionCount</span></span>
<span data-ttu-id="80609-125">Liczba partycji usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="80609-125">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80609-126">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="80609-126">-PublicNetworkAccess</span></span>
<span data-ttu-id="80609-127">(Opcjonalnie) Dostęp do publicznej sieci usługi Azure Cognitive Search (włączony/wyłączony)</span><span class="sxs-lookup"><span data-stu-id="80609-127">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSPublicNetworkAccess]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80609-128">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="80609-128">-ReplicaCount</span></span>
<span data-ttu-id="80609-129">Liczba replik usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="80609-129">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80609-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80609-130">-ResourceGroupName</span></span>
<span data-ttu-id="80609-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="80609-131">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80609-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80609-132">-ResourceId</span></span>
<span data-ttu-id="80609-133">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="80609-133">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80609-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80609-134">-Confirm</span></span>
<span data-ttu-id="80609-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="80609-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80609-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80609-136">-WhatIf</span></span>
<span data-ttu-id="80609-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80609-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80609-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="80609-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80609-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80609-139">CommonParameters</span></span>
<span data-ttu-id="80609-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80609-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80609-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80609-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80609-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80609-142">INPUTS</span></span>

### <span data-ttu-id="80609-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="80609-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="80609-144">System.String</span><span class="sxs-lookup"><span data-stu-id="80609-144">System.String</span></span>

## <span data-ttu-id="80609-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80609-145">OUTPUTS</span></span>

### <span data-ttu-id="80609-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="80609-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="80609-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="80609-147">NOTES</span></span>

## <span data-ttu-id="80609-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80609-148">RELATED LINKS</span></span>

[<span data-ttu-id="80609-149">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="80609-149">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="80609-150">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="80609-150">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="80609-151">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="80609-151">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)