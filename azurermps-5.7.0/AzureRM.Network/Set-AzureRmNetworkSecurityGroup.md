---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: ab009608100bc4cbb4915f6bc3e82d44d9e08cd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718638"
---
# <span data-ttu-id="f7008-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f7008-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="f7008-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7008-102">SYNOPSIS</span></span>
<span data-ttu-id="f7008-103">Ustawia stan celu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="f7008-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7008-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7008-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7008-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7008-105">DESCRIPTION</span></span>
<span data-ttu-id="f7008-106">Polecenie cmdlet **Set-AzureRmNetworkSecurityGroup** ustawia stan celu dla grupy zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="f7008-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="f7008-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7008-107">EXAMPLES</span></span>

### <span data-ttu-id="f7008-108">Przykład 1: Ustawianie stanu celu dla grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="f7008-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="f7008-109">To polecenie pobiera grupę zabezpieczeń sieci Azure o nazwie Nsg1 i dodaje regułę zabezpieczeń sieciowych o nazwie Rdp-Rule, aby zezwolić na ruch internetowy na porcie 3389 do pobranego obiektu grupy zabezpieczeń sieci przy użyciu polecenia Add-AzureRmNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="f7008-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="f7008-110">Polecenie pozostanie w niezmienionej grupie zabezpieczeń sieci Azure przy użyciu polecenia **Set-AzureRmNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="f7008-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="f7008-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7008-111">PARAMETERS</span></span>

### <span data-ttu-id="f7008-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7008-112">-AsJob</span></span>
<span data-ttu-id="f7008-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f7008-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7008-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7008-114">-DefaultProfile</span></span>
<span data-ttu-id="f7008-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7008-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7008-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f7008-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="f7008-117">Obiekt grupy zabezpieczeń sieci reprezentujący stan celu, w którym polecenie cmdlet ustawia grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="f7008-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="f7008-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7008-118">CommonParameters</span></span>
<span data-ttu-id="f7008-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7008-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7008-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7008-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7008-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7008-121">INPUTS</span></span>

### <span data-ttu-id="f7008-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f7008-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="f7008-123">Parametr "NetworkSecurityGroup" akceptuje wartość typu "PSNetworkSecurityGroup" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="f7008-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="f7008-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7008-124">OUTPUTS</span></span>

### <span data-ttu-id="f7008-125">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f7008-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="f7008-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7008-126">NOTES</span></span>

## <span data-ttu-id="f7008-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7008-127">RELATED LINKS</span></span>

[<span data-ttu-id="f7008-128">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f7008-128">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="f7008-129">Nowe — AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f7008-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="f7008-130">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f7008-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


