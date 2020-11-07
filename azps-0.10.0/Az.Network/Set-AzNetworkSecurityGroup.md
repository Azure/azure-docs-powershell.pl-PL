---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 1c61af223b97ac60dd74f55504ce623b26b5233e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892766"
---
# <span data-ttu-id="8fb59-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8fb59-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="8fb59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8fb59-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb59-103">Ustawia stan celu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="8fb59-103">Sets the goal state for a network security group.</span></span>

## <span data-ttu-id="8fb59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8fb59-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fb59-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8fb59-105">DESCRIPTION</span></span>
<span data-ttu-id="8fb59-106">Polecenie cmdlet **Set-AzNetworkSecurityGroup** ustawia stan celu dla grupy zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="8fb59-106">The **Set-AzNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="8fb59-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8fb59-107">EXAMPLES</span></span>

### <span data-ttu-id="8fb59-108">Przykład 1: Ustawianie stanu celu dla grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="8fb59-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="8fb59-109">To polecenie pobiera grupę zabezpieczeń sieci Azure o nazwie Nsg1 i dodaje regułę zabezpieczeń sieciowych o nazwie Rdp-Rule, aby zezwolić na ruch internetowy na porcie 3389 do pobranego obiektu grupy zabezpieczeń sieci przy użyciu polecenia Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="8fb59-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="8fb59-110">Polecenie pozostanie w niezmienionej grupie zabezpieczeń sieci Azure przy użyciu polecenia **Set-AzNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="8fb59-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="8fb59-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8fb59-111">PARAMETERS</span></span>

### <span data-ttu-id="8fb59-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8fb59-112">-AsJob</span></span>
<span data-ttu-id="8fb59-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8fb59-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8fb59-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fb59-114">-DefaultProfile</span></span>
<span data-ttu-id="8fb59-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8fb59-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fb59-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8fb59-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="8fb59-117">Obiekt grupy zabezpieczeń sieci reprezentujący stan celu, w którym polecenie cmdlet ustawia grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="8fb59-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="8fb59-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb59-118">CommonParameters</span></span>
<span data-ttu-id="8fb59-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fb59-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fb59-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fb59-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb59-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fb59-121">INPUTS</span></span>

### <span data-ttu-id="8fb59-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8fb59-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="8fb59-123">Parametr "NetworkSecurityGroup" akceptuje wartość typu "PSNetworkSecurityGroup" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="8fb59-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="8fb59-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8fb59-124">OUTPUTS</span></span>

### <span data-ttu-id="8fb59-125">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8fb59-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8fb59-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8fb59-126">NOTES</span></span>

## <span data-ttu-id="8fb59-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8fb59-127">RELATED LINKS</span></span>

[<span data-ttu-id="8fb59-128">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8fb59-128">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="8fb59-129">Nowe — AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8fb59-129">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="8fb59-130">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8fb59-130">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


