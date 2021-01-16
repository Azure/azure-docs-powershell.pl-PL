---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 318d5915e07ac55430dbe8e1788d862673dc5998
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336982"
---
# <span data-ttu-id="af306-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="af306-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="af306-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af306-102">SYNOPSIS</span></span>
<span data-ttu-id="af306-103">Utwórz obiekt reprezentujący ustawienia reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="af306-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="af306-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af306-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af306-105">Opis</span><span class="sxs-lookup"><span data-stu-id="af306-105">DESCRIPTION</span></span>
<span data-ttu-id="af306-106">Utwórz obiekt reprezentujący ustawienia reguły sieci, których można użyć podczas tworzenia magazynu.</span><span class="sxs-lookup"><span data-stu-id="af306-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="af306-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af306-107">EXAMPLES</span></span>

### <span data-ttu-id="af306-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="af306-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="af306-109">Utworzenie nowego magazynu i określenie reguł sieciowych umożliwiających dostęp do określonego adresu IP z sieci wirtualnej określonej przez $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="af306-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="af306-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af306-110">PARAMETERS</span></span>

### <span data-ttu-id="af306-111">-Bypass</span><span class="sxs-lookup"><span data-stu-id="af306-111">-Bypass</span></span>
<span data-ttu-id="af306-112">Określa ominięcie reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="af306-112">Specifies bypass of network rule.</span></span>

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

### <span data-ttu-id="af306-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="af306-113">-DefaultAction</span></span>
<span data-ttu-id="af306-114">Określa domyślną akcję reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="af306-114">Specifies default action of network rule.</span></span>

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

### <span data-ttu-id="af306-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af306-115">-DefaultProfile</span></span>
<span data-ttu-id="af306-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af306-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af306-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="af306-117">-IpAddressRange</span></span>
<span data-ttu-id="af306-118">Określa dozwolony zakres adresów IP sieci w regule sieci.</span><span class="sxs-lookup"><span data-stu-id="af306-118">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="af306-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="af306-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="af306-120">Określa dozwolony identyfikator zasobu sieci wirtualnej reguły sieci.</span><span class="sxs-lookup"><span data-stu-id="af306-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="af306-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af306-121">CommonParameters</span></span>
<span data-ttu-id="af306-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af306-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af306-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af306-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af306-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af306-124">INPUTS</span></span>

### <span data-ttu-id="af306-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="af306-125">None</span></span>

## <span data-ttu-id="af306-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af306-126">OUTPUTS</span></span>

### <span data-ttu-id="af306-127">Microsoft. Azure. Commands. platforming. models. PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="af306-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="af306-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af306-128">NOTES</span></span>

## <span data-ttu-id="af306-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af306-129">RELATED LINKS</span></span>
