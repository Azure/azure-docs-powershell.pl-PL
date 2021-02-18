---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: 4a2292b0b573a5357466f3b240ba3b6df7cf0a1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181451"
---
# <span data-ttu-id="46bdc-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="46bdc-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="46bdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="46bdc-103">Tworzenie lub aktualizowanie zestawu reguł sieciowych.</span><span class="sxs-lookup"><span data-stu-id="46bdc-103">Create or update a network rule set.</span></span> <span data-ttu-id="46bdc-104">Zestaw reguł można stosować tylko do rejestru "Premium".</span><span class="sxs-lookup"><span data-stu-id="46bdc-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="46bdc-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="46bdc-105">SYNTAX</span></span>

### <span data-ttu-id="46bdc-106">AddAddNetworkRuleWithoutInputObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="46bdc-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46bdc-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="46bdc-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46bdc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="46bdc-108">DESCRIPTION</span></span>
<span data-ttu-id="46bdc-109">Tworzenie lub aktualizowanie zestawu reguł sieciowych</span><span class="sxs-lookup"><span data-stu-id="46bdc-109">Create or update a network rule set</span></span>

## <span data-ttu-id="46bdc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="46bdc-110">EXAMPLES</span></span>

### <span data-ttu-id="46bdc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46bdc-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="46bdc-112">Utwórz nowy zestaw reguł sieciowych.</span><span class="sxs-lookup"><span data-stu-id="46bdc-112">Create a new network rule set.</span></span>

## <span data-ttu-id="46bdc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46bdc-113">PARAMETERS</span></span>

### <span data-ttu-id="46bdc-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="46bdc-114">-DefaultAction</span></span>
<span data-ttu-id="46bdc-115">Akcja domyślna, na przykład "Zezwalaj" lub "Odmów"</span><span class="sxs-lookup"><span data-stu-id="46bdc-115">Default action, could be 'Allow' or 'Deny'</span></span>

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

### <span data-ttu-id="46bdc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46bdc-116">-DefaultProfile</span></span>
<span data-ttu-id="46bdc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="46bdc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46bdc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46bdc-118">-InputObject</span></span>
<span data-ttu-id="46bdc-119">Input PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="46bdc-119">Input PSNetworkRuleSet</span></span>

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

### <span data-ttu-id="46bdc-120">— NetworkRule</span><span class="sxs-lookup"><span data-stu-id="46bdc-120">-NetworkRule</span></span>
<span data-ttu-id="46bdc-121">Lista reguł sieciowych</span><span class="sxs-lookup"><span data-stu-id="46bdc-121">List of Network rules</span></span>

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

### <span data-ttu-id="46bdc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46bdc-122">CommonParameters</span></span>
<span data-ttu-id="46bdc-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46bdc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46bdc-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46bdc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46bdc-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46bdc-125">INPUTS</span></span>

### <span data-ttu-id="46bdc-126">System.String</span><span class="sxs-lookup"><span data-stu-id="46bdc-126">System.String</span></span>

### <span data-ttu-id="46bdc-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="46bdc-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="46bdc-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46bdc-128">OUTPUTS</span></span>

### <span data-ttu-id="46bdc-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="46bdc-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="46bdc-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="46bdc-130">NOTES</span></span>

## <span data-ttu-id="46bdc-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46bdc-131">RELATED LINKS</span></span>
