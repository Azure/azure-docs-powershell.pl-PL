---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 5f63ee4d1c55211b13eb525a76547064e61cba48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001281"
---
# <span data-ttu-id="5352f-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="5352f-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="5352f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5352f-102">SYNOPSIS</span></span>
<span data-ttu-id="5352f-103">Utwórz obiekt reprezentujący ustawienia reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="5352f-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="5352f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5352f-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5352f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5352f-105">DESCRIPTION</span></span>
<span data-ttu-id="5352f-106">Utwórz obiekt reprezentujący ustawienia reguły sieciowej, których można używać podczas tworzenia magazynu.</span><span class="sxs-lookup"><span data-stu-id="5352f-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="5352f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5352f-107">EXAMPLES</span></span>

### <span data-ttu-id="5352f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5352f-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="5352f-109">Tworzenie nowego magazynu i określa reguły sieciowe umożliwiające dostęp do określonego adresu IP z sieci wirtualnej wskazanej przez $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="5352f-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="5352f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5352f-110">PARAMETERS</span></span>

### <span data-ttu-id="5352f-111">— Obejście</span><span class="sxs-lookup"><span data-stu-id="5352f-111">-Bypass</span></span>
<span data-ttu-id="5352f-112">Określa obejście reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="5352f-112">Specifies bypass of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5352f-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="5352f-113">-DefaultAction</span></span>
<span data-ttu-id="5352f-114">Określa domyślną akcję reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="5352f-114">Specifies default action of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5352f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5352f-115">-DefaultProfile</span></span>
<span data-ttu-id="5352f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5352f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5352f-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="5352f-117">-IpAddressRange</span></span>
<span data-ttu-id="5352f-118">Określa dozwolony zakres adresów IP sieci reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="5352f-118">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5352f-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5352f-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="5352f-120">Określa dozwolony identyfikator zasobu sieci wirtualnej reguły sieciowej.</span><span class="sxs-lookup"><span data-stu-id="5352f-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5352f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5352f-121">CommonParameters</span></span>
<span data-ttu-id="5352f-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5352f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5352f-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5352f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5352f-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5352f-124">INPUTS</span></span>

### <span data-ttu-id="5352f-125">Brak</span><span class="sxs-lookup"><span data-stu-id="5352f-125">None</span></span>

## <span data-ttu-id="5352f-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5352f-126">OUTPUTS</span></span>

### <span data-ttu-id="5352f-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5352f-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="5352f-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5352f-128">NOTES</span></span>

## <span data-ttu-id="5352f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5352f-129">RELATED LINKS</span></span>
