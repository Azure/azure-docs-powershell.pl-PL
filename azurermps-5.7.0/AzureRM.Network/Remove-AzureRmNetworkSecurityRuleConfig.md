---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: fa75146ef26fc19108b918211a83289f73bfe4cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526745"
---
# <span data-ttu-id="ceacc-101">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ceacc-101">Remove-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="ceacc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ceacc-102">SYNOPSIS</span></span>
<span data-ttu-id="ceacc-103">Usuwa regułę zabezpieczeń sieci z grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="ceacc-103">Removes a network security rule from a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceacc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ceacc-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceacc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ceacc-105">DESCRIPTION</span></span>
<span data-ttu-id="ceacc-106">Polecenie cmdlet **Remove-AzureRmNetworkSecurityRuleConfig** usuwa konfigurację reguły zabezpieczeń sieci z grupy zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="ceacc-106">The **Remove-AzureRmNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="ceacc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ceacc-107">EXAMPLES</span></span>

### <span data-ttu-id="ceacc-108">Przykład 1: Usuwanie konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="ceacc-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="ceacc-109">Pierwsze polecenie powoduje utworzenie konfiguracji reguł zabezpieczeń sieci o nazwie RDP — reguły, a następnie zapisanie jej w zmiennej $rule 1.</span><span class="sxs-lookup"><span data-stu-id="ceacc-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>

<span data-ttu-id="ceacc-110">Drugie polecenie tworzy grupę zabezpieczeń sieci przy użyciu reguły w $rule 1, a następnie zapisuje grupę zabezpieczeń sieci w zmiennej $nsg.</span><span class="sxs-lookup"><span data-stu-id="ceacc-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>

<span data-ttu-id="ceacc-111">Trzecie polecenie usuwa konfigurację reguł zabezpieczeń sieci o nazwie RDP-Rule z grupy zabezpieczenia sieci w $nsg.</span><span class="sxs-lookup"><span data-stu-id="ceacc-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="ceacc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ceacc-112">PARAMETERS</span></span>

### <span data-ttu-id="ceacc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceacc-113">-DefaultProfile</span></span>
<span data-ttu-id="ceacc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ceacc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceacc-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ceacc-115">-Name</span></span>
<span data-ttu-id="ceacc-116">Określa nazwę konfiguracji reguł zabezpieczeń sieci, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceacc-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceacc-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ceacc-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ceacc-118">Określa obiekt **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="ceacc-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="ceacc-119">Ten obiekt zawiera konfigurację reguły zabezpieczeń sieci do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ceacc-119">This object contains the network security rule configuration to remove.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ceacc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceacc-120">CommonParameters</span></span>
<span data-ttu-id="ceacc-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceacc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceacc-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceacc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceacc-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ceacc-123">INPUTS</span></span>

### <span data-ttu-id="ceacc-124">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ceacc-124">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="ceacc-125">Parametr "NetworkSecurityGroup" akceptuje wartość typu "PSNetworkSecurityGroup" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ceacc-125">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="ceacc-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ceacc-126">OUTPUTS</span></span>

### <span data-ttu-id="ceacc-127">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ceacc-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ceacc-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ceacc-128">NOTES</span></span>

## <span data-ttu-id="ceacc-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ceacc-129">RELATED LINKS</span></span>

[<span data-ttu-id="ceacc-130">Dodaj-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ceacc-130">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ceacc-131">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ceacc-131">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ceacc-132">Nowe — AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ceacc-132">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="ceacc-133">Nowe — AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ceacc-133">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ceacc-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ceacc-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


