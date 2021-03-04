---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 61101242b100ca4b477910a0dfa339ef7f9ea81b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958001"
---
# <span data-ttu-id="06592-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="06592-101">New-AzSearchService</span></span>

## <span data-ttu-id="06592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06592-102">SYNOPSIS</span></span>
<span data-ttu-id="06592-103">Tworzy usługę Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="06592-103">Creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="06592-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06592-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06592-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="06592-105">DESCRIPTION</span></span>
<span data-ttu-id="06592-106">Polecenie **cmdlet New-AzSearchService** tworzy usługę Azure Cognitive Search z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="06592-106">The **New-AzSearchService** cmdlet creates an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="06592-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06592-107">EXAMPLES</span></span>

### <span data-ttu-id="06592-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="06592-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="06592-109">To polecenie tworzy usługę Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="06592-109">The command creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="06592-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06592-110">PARAMETERS</span></span>

### <span data-ttu-id="06592-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06592-111">-DefaultProfile</span></span>
<span data-ttu-id="06592-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06592-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06592-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="06592-113">-HostingMode</span></span>
<span data-ttu-id="06592-114">Tryb hostingu usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="06592-114">Azure Cognitive Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06592-115">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="06592-115">-IdentityType</span></span>
<span data-ttu-id="06592-116">(Opcjonalnie) Azure Cognitive Search Service Identity (None/SystemAssigned)</span><span class="sxs-lookup"><span data-stu-id="06592-116">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

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

### <span data-ttu-id="06592-117">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="06592-117">-IPRuleList</span></span>
<span data-ttu-id="06592-118">(Opcjonalnie) Reguły IP usługi Azure Cognitive Search Service</span><span class="sxs-lookup"><span data-stu-id="06592-118">(Optional) Azure Cognitive Search Service IP rules</span></span>

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

### <span data-ttu-id="06592-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="06592-119">-Location</span></span>
<span data-ttu-id="06592-120">Lokalizacja usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="06592-120">Azure Cognitive Search Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06592-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="06592-121">-Name</span></span>
<span data-ttu-id="06592-122">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="06592-122">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06592-123">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="06592-123">-PartitionCount</span></span>
<span data-ttu-id="06592-124">Liczba partycji usługi Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="06592-124">Azure Cognitive Search Service partition count.</span></span>

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

### <span data-ttu-id="06592-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="06592-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="06592-126">(Opcjonalnie) Dostęp do publicznej sieci usługi Azure Cognitive Search (włączony/wyłączony)</span><span class="sxs-lookup"><span data-stu-id="06592-126">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

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

### <span data-ttu-id="06592-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="06592-127">-ReplicaCount</span></span>
<span data-ttu-id="06592-128">Liczba replik usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="06592-128">Azure Cognitive Search Service replica count.</span></span>

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

### <span data-ttu-id="06592-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06592-129">-ResourceGroupName</span></span>
<span data-ttu-id="06592-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="06592-130">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06592-131">- SKU</span><span class="sxs-lookup"><span data-stu-id="06592-131">-Sku</span></span>
<span data-ttu-id="06592-132">SKU usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="06592-132">Azure Cognitive Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06592-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06592-133">-Confirm</span></span>
<span data-ttu-id="06592-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06592-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06592-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06592-135">-WhatIf</span></span>
<span data-ttu-id="06592-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06592-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06592-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="06592-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06592-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06592-138">CommonParameters</span></span>
<span data-ttu-id="06592-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06592-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06592-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06592-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06592-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06592-141">INPUTS</span></span>

### <span data-ttu-id="06592-142">Brak</span><span class="sxs-lookup"><span data-stu-id="06592-142">None</span></span>

## <span data-ttu-id="06592-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06592-143">OUTPUTS</span></span>

### <span data-ttu-id="06592-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="06592-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="06592-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06592-145">NOTES</span></span>

## <span data-ttu-id="06592-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06592-146">RELATED LINKS</span></span>

[<span data-ttu-id="06592-147">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="06592-147">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="06592-148">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="06592-148">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="06592-149">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="06592-149">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)