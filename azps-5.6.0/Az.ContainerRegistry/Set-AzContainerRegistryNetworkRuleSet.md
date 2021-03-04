---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: f0fc298ba92b7e9dc0f0bf5ed4f8cbdba5b8091f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956346"
---
# <span data-ttu-id="8370f-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8370f-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="8370f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8370f-102">SYNOPSIS</span></span>
<span data-ttu-id="8370f-103">Tworzenie lub aktualizowanie zestawu reguł sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8370f-103">Create or update a network rule set.</span></span> <span data-ttu-id="8370f-104">Zestaw reguł można stosować tylko do rejestru "Premium".</span><span class="sxs-lookup"><span data-stu-id="8370f-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="8370f-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8370f-105">SYNTAX</span></span>

### <span data-ttu-id="8370f-106">AddAddNetworkRuleWithoutInputObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="8370f-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8370f-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="8370f-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8370f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8370f-108">DESCRIPTION</span></span>
<span data-ttu-id="8370f-109">Tworzenie lub aktualizowanie zestawu reguł sieciowych</span><span class="sxs-lookup"><span data-stu-id="8370f-109">Create or update a network rule set</span></span>

## <span data-ttu-id="8370f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8370f-110">EXAMPLES</span></span>

### <span data-ttu-id="8370f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8370f-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="8370f-112">Utwórz nowy zestaw reguł sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8370f-112">Create a new network rule set.</span></span>

## <span data-ttu-id="8370f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8370f-113">PARAMETERS</span></span>

### <span data-ttu-id="8370f-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="8370f-114">-DefaultAction</span></span>
<span data-ttu-id="8370f-115">Akcja domyślna, na przykład "Zezwalaj" lub "Odmów"</span><span class="sxs-lookup"><span data-stu-id="8370f-115">Default action, could be 'Allow' or 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: AddAddNetworkRuleWithoutInputObject
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8370f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8370f-116">-DefaultProfile</span></span>
<span data-ttu-id="8370f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8370f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8370f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8370f-118">-InputObject</span></span>
<span data-ttu-id="8370f-119">Input PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8370f-119">Input PSNetworkRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: AddNetworkRuleWithInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8370f-120">— NetworkRule</span><span class="sxs-lookup"><span data-stu-id="8370f-120">-NetworkRule</span></span>
<span data-ttu-id="8370f-121">Lista reguł sieciowych</span><span class="sxs-lookup"><span data-stu-id="8370f-121">List of Network rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8370f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8370f-122">CommonParameters</span></span>
<span data-ttu-id="8370f-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8370f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8370f-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8370f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8370f-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8370f-125">INPUTS</span></span>

### <span data-ttu-id="8370f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8370f-126">System.String</span></span>

### <span data-ttu-id="8370f-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8370f-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="8370f-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8370f-128">OUTPUTS</span></span>

### <span data-ttu-id="8370f-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8370f-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="8370f-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8370f-130">NOTES</span></span>

## <span data-ttu-id="8370f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8370f-131">RELATED LINKS</span></span>
