---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: d6ca2ac1e091e3576af51ba8f1a2f50676994ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552680"
---
# <span data-ttu-id="b6762-101">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6762-101">Remove-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="b6762-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6762-102">SYNOPSIS</span></span>
<span data-ttu-id="b6762-103">Usuwa regułę zabezpieczeń sieci z grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="b6762-103">Removes a network security rule from a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6762-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6762-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6762-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6762-105">DESCRIPTION</span></span>
<span data-ttu-id="b6762-106">Polecenie cmdlet **Remove-AzureRmNetworkSecurityRuleConfig** usuwa konfigurację reguły zabezpieczeń sieci z grupy zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="b6762-106">The **Remove-AzureRmNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="b6762-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6762-107">EXAMPLES</span></span>

### <span data-ttu-id="b6762-108">Przykład 1: Usuwanie konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="b6762-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="b6762-109">Pierwsze polecenie powoduje utworzenie konfiguracji reguł zabezpieczeń sieci o nazwie RDP — reguły, a następnie zapisanie jej w zmiennej $rule 1.</span><span class="sxs-lookup"><span data-stu-id="b6762-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="b6762-110">Drugie polecenie tworzy grupę zabezpieczeń sieci przy użyciu reguły w $rule 1, a następnie zapisuje grupę zabezpieczeń sieci w zmiennej $nsg.</span><span class="sxs-lookup"><span data-stu-id="b6762-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="b6762-111">Trzecie polecenie usuwa konfigurację reguł zabezpieczeń sieci o nazwie RDP-Rule z grupy zabezpieczenia sieci w $nsg.</span><span class="sxs-lookup"><span data-stu-id="b6762-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="b6762-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6762-112">PARAMETERS</span></span>

### <span data-ttu-id="b6762-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6762-113">-DefaultProfile</span></span>
<span data-ttu-id="b6762-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6762-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6762-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6762-115">-Name</span></span>
<span data-ttu-id="b6762-116">Określa nazwę konfiguracji reguł zabezpieczeń sieci, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6762-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b6762-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b6762-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b6762-118">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="b6762-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="b6762-119">Ten obiekt zawiera konfigurację reguły zabezpieczeń sieci do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b6762-119">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="b6762-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6762-120">CommonParameters</span></span>
<span data-ttu-id="b6762-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6762-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6762-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6762-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6762-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6762-123">INPUTS</span></span>

### <span data-ttu-id="b6762-124">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b6762-124">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="b6762-125">Parametry: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b6762-125">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="b6762-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6762-126">OUTPUTS</span></span>

### <span data-ttu-id="b6762-127">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b6762-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="b6762-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6762-128">NOTES</span></span>

## <span data-ttu-id="b6762-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6762-129">RELATED LINKS</span></span>

[<span data-ttu-id="b6762-130">Dodaj-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6762-130">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b6762-131">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6762-131">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b6762-132">Nowe — AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b6762-132">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="b6762-133">Nowe — AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6762-133">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b6762-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b6762-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


