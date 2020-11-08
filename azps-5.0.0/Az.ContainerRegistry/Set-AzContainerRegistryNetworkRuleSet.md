---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/set-azcontainerregistrynetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Set-AzContainerRegistryNetworkRuleSet.md
ms.openlocfilehash: 4a2292b0b573a5357466f3b240ba3b6df7cf0a1e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224544"
---
# <span data-ttu-id="c13ad-101">Set-AzContainerRegistryNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c13ad-101">Set-AzContainerRegistryNetworkRuleSet</span></span>

## <span data-ttu-id="c13ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c13ad-102">SYNOPSIS</span></span>
<span data-ttu-id="c13ad-103">Tworzenie lub aktualizowanie zestawu reguł sieci.</span><span class="sxs-lookup"><span data-stu-id="c13ad-103">Create or update a network rule set.</span></span> <span data-ttu-id="c13ad-104">Zestaw reguł można stosować tylko do rejestru "Premium".</span><span class="sxs-lookup"><span data-stu-id="c13ad-104">Rule set can only be applied to "Premium" registry.</span></span>

## <span data-ttu-id="c13ad-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c13ad-105">SYNTAX</span></span>

### <span data-ttu-id="c13ad-106">AddAddNetworkRuleWithoutInputObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c13ad-106">AddAddNetworkRuleWithoutInputObject (Default)</span></span>
```
Set-AzContainerRegistryNetworkRuleSet -DefaultAction <String> [-NetworkRule <IPSNetworkRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c13ad-107">AddNetworkRuleWithInputObject</span><span class="sxs-lookup"><span data-stu-id="c13ad-107">AddNetworkRuleWithInputObject</span></span>
```
Set-AzContainerRegistryNetworkRuleSet [-DefaultAction <String>] [-NetworkRule <IPSNetworkRule[]>]
 -InputObject <PSNetworkRuleSet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c13ad-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c13ad-108">DESCRIPTION</span></span>
<span data-ttu-id="c13ad-109">Tworzenie lub aktualizowanie zestawu reguł sieci</span><span class="sxs-lookup"><span data-stu-id="c13ad-109">Create or update a network rule set</span></span>

## <span data-ttu-id="c13ad-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c13ad-110">EXAMPLES</span></span>

### <span data-ttu-id="c13ad-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c13ad-111">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix "10.0.1.0/24" -ServiceEndpoint "Microsoft.ContainerRegistry"
PS C:\> $vnet = New-AzVirtualNetwork -Name $VnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix "10.0.0.0/16" -Subnet $subnet
PS C:\> $rule = New-AzContainerRegistryNetworkRule -VirtualNetworkRule -VirtualNetworkResourceId $vnet.Subnets[0].Id
PS C:\> $set = Set-AzContainerRegistryNetworkRuleSet -DefaultAction "Allow" -NetworkRule $rule
```

<span data-ttu-id="c13ad-112">Tworzenie nowego zestawu reguł sieci.</span><span class="sxs-lookup"><span data-stu-id="c13ad-112">Create a new network rule set.</span></span>

## <span data-ttu-id="c13ad-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c13ad-113">PARAMETERS</span></span>

### <span data-ttu-id="c13ad-114">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="c13ad-114">-DefaultAction</span></span>
<span data-ttu-id="c13ad-115">Akcja domyślna może mieć wartość "Zezwól" lub "Odmów"</span><span class="sxs-lookup"><span data-stu-id="c13ad-115">Default action, could be 'Allow' or 'Deny'</span></span>

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

### <span data-ttu-id="c13ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c13ad-116">-DefaultProfile</span></span>
<span data-ttu-id="c13ad-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c13ad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c13ad-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c13ad-118">-InputObject</span></span>
<span data-ttu-id="c13ad-119">Wprowadź PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c13ad-119">Input PSNetworkRuleSet</span></span>

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

### <span data-ttu-id="c13ad-120">-NetworkRule</span><span class="sxs-lookup"><span data-stu-id="c13ad-120">-NetworkRule</span></span>
<span data-ttu-id="c13ad-121">Lista reguł sieciowych</span><span class="sxs-lookup"><span data-stu-id="c13ad-121">List of Network rules</span></span>

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

### <span data-ttu-id="c13ad-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c13ad-122">CommonParameters</span></span>
<span data-ttu-id="c13ad-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c13ad-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c13ad-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c13ad-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c13ad-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c13ad-125">INPUTS</span></span>

### <span data-ttu-id="c13ad-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c13ad-126">System.String</span></span>

### <span data-ttu-id="c13ad-127">Microsoft. Azure. Commands. ContainerRegistry. models. IPSNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c13ad-127">Microsoft.Azure.Commands.ContainerRegistry.Models.IPSNetworkRule</span></span>

## <span data-ttu-id="c13ad-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c13ad-128">OUTPUTS</span></span>

### <span data-ttu-id="c13ad-129">Microsoft. Azure. Commands. ContainerRegistry. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c13ad-129">Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="c13ad-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c13ad-130">NOTES</span></span>

## <span data-ttu-id="c13ad-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c13ad-131">RELATED LINKS</span></span>
