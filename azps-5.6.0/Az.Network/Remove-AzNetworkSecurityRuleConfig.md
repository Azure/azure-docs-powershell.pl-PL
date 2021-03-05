---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a60fa0e305d05ae5d944a69705c3cb3f392b28f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993616"
---
# <span data-ttu-id="ad2b2-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad2b2-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="ad2b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad2b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2b2-103">Usuwa regułę zabezpieczeń sieci z grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="ad2b2-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="ad2b2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad2b2-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad2b2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad2b2-105">DESCRIPTION</span></span>
<span data-ttu-id="ad2b2-106">Polecenie **cmdlet Remove-AzNetworkSecurityRuleConfig** usuwa konfigurację reguły zabezpieczeń sieci z grupy zabezpieczeń sieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ad2b2-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="ad2b2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad2b2-107">EXAMPLES</span></span>

### <span data-ttu-id="ad2b2-108">Przykład 1. Usuwanie konfiguracji reguły zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="ad2b2-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="ad2b2-109">Pierwsze polecenie tworzy konfigurację reguły zabezpieczeń sieciowych o nazwie reguła rdp, a następnie zapisuje ją w zmiennej $rule 1.</span><span class="sxs-lookup"><span data-stu-id="ad2b2-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="ad2b2-110">Drugie polecenie tworzy grupę zabezpieczeń sieciowych przy użyciu reguły w programie $rule 1, a następnie zapisuje grupę zabezpieczeń sieciowych w $nsg sieci.</span><span class="sxs-lookup"><span data-stu-id="ad2b2-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="ad2b2-111">Trzecie polecenie usuwa konfigurację reguły zabezpieczeń sieciowych o nazwie reguła rdp z grupy zabezpieczeń sieciowych w programie $nsg.</span><span class="sxs-lookup"><span data-stu-id="ad2b2-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="ad2b2-112">Polecenie Z powrotem zapisuje zmianę.</span><span class="sxs-lookup"><span data-stu-id="ad2b2-112">The forth command saves the change.</span></span>

## <span data-ttu-id="ad2b2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad2b2-113">PARAMETERS</span></span>

### <span data-ttu-id="ad2b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2b2-114">-DefaultProfile</span></span>
<span data-ttu-id="ad2b2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad2b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad2b2-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ad2b2-116">-Name</span></span>
<span data-ttu-id="ad2b2-117">Określa nazwę konfiguracji reguły zabezpieczeń sieciowych, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad2b2-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ad2b2-118">- NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ad2b2-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ad2b2-119">Określa obiekt **NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="ad2b2-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="ad2b2-120">Ten obiekt zawiera konfigurację reguły zabezpieczeń sieci do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ad2b2-120">This object contains the network security rule configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad2b2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2b2-121">CommonParameters</span></span>
<span data-ttu-id="ad2b2-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad2b2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2b2-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad2b2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2b2-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad2b2-124">INPUTS</span></span>

### <span data-ttu-id="ad2b2-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ad2b2-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ad2b2-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad2b2-126">OUTPUTS</span></span>

### <span data-ttu-id="ad2b2-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ad2b2-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ad2b2-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad2b2-128">NOTES</span></span>

## <span data-ttu-id="ad2b2-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad2b2-129">RELATED LINKS</span></span>

[<span data-ttu-id="ad2b2-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad2b2-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ad2b2-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad2b2-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ad2b2-132">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ad2b2-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="ad2b2-133">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad2b2-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ad2b2-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ad2b2-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


