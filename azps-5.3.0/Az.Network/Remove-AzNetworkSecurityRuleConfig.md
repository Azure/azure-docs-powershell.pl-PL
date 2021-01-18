---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 7f5d41774af2f5ee74c5d343fa9b143801c139f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500226"
---
# <span data-ttu-id="0a6c5-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a6c5-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="0a6c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6c5-103">Usuwa regułę zabezpieczeń sieci z grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="0a6c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a6c5-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a6c5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0a6c5-105">DESCRIPTION</span></span>
<span data-ttu-id="0a6c5-106">Polecenie cmdlet **Remove-AzNetworkSecurityRuleConfig** usuwa konfigurację reguły zabezpieczeń sieci z grupy zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="0a6c5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a6c5-107">EXAMPLES</span></span>

### <span data-ttu-id="0a6c5-108">Przykład 1: Usuwanie konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="0a6c5-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="0a6c5-109">Pierwsze polecenie powoduje utworzenie konfiguracji reguł zabezpieczeń sieci o nazwie RDP — reguły, a następnie zapisanie jej w zmiennej $rule 1.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="0a6c5-110">Drugie polecenie tworzy grupę zabezpieczeń sieci przy użyciu reguły w $rule 1, a następnie zapisuje grupę zabezpieczeń sieci w zmiennej $nsg.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="0a6c5-111">Trzecie polecenie usuwa konfigurację reguł zabezpieczeń sieci o nazwie RDP-Rule z grupy zabezpieczenia sieci w $nsg.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="0a6c5-112">W przypadku polecenia dalej jest zapisywana zmiana.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-112">The forth command saves the change.</span></span>

## <span data-ttu-id="0a6c5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a6c5-113">PARAMETERS</span></span>

### <span data-ttu-id="0a6c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6c5-114">-DefaultProfile</span></span>
<span data-ttu-id="0a6c5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a6c5-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0a6c5-116">-Name</span></span>
<span data-ttu-id="0a6c5-117">Określa nazwę konfiguracji reguł zabezpieczeń sieci, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0a6c5-118">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a6c5-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0a6c5-119">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="0a6c5-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="0a6c5-120">Ten obiekt zawiera konfigurację reguły zabezpieczeń sieci do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-120">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="0a6c5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6c5-121">CommonParameters</span></span>
<span data-ttu-id="0a6c5-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6c5-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a6c5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6c5-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a6c5-124">INPUTS</span></span>

### <span data-ttu-id="0a6c5-125">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a6c5-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0a6c5-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a6c5-126">OUTPUTS</span></span>

### <span data-ttu-id="0a6c5-127">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a6c5-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0a6c5-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a6c5-128">NOTES</span></span>

## <span data-ttu-id="0a6c5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a6c5-129">RELATED LINKS</span></span>

[<span data-ttu-id="0a6c5-130">Dodaj-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a6c5-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0a6c5-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a6c5-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0a6c5-132">Nowe — AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0a6c5-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="0a6c5-133">Nowe — AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a6c5-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0a6c5-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a6c5-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


