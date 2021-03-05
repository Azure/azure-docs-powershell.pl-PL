---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 91144275806c5e3a6913d39990ad68644c71b244
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003306"
---
# <span data-ttu-id="7d23a-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7d23a-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="7d23a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d23a-102">SYNOPSIS</span></span>
<span data-ttu-id="7d23a-103">Aktualizuje grupę zabezpieczeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="7d23a-103">Updates a network security group.</span></span>

## <span data-ttu-id="7d23a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7d23a-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d23a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7d23a-105">DESCRIPTION</span></span>
<span data-ttu-id="7d23a-106">Polecenie **cmdlet Set-AzNetworkSecurityGroup** aktualizuje grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="7d23a-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="7d23a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7d23a-107">EXAMPLES</span></span>

### <span data-ttu-id="7d23a-108">Przykład 1. Aktualizowanie istniejącej grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="7d23a-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="7d23a-109">To polecenie pobiera grupę zabezpieczeń sieci platformy Azure o nazwie Nsg1 i dodaje regułę zabezpieczeń sieci o nazwie Rdp-Rule, aby zezwolić na ruch internetowy na porcie 3389 do pobranego obiektu grupy zabezpieczeń sieci przy użyciu dodatku Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7d23a-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="7d23a-110">To polecenie będzie zachowywać zmodyfikowaną grupę zabezpieczeń sieci platformy Azure przy użyciu **polecenia Set-AzNetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="7d23a-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="7d23a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d23a-111">PARAMETERS</span></span>

### <span data-ttu-id="7d23a-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="7d23a-112">-AsJob</span></span>
<span data-ttu-id="7d23a-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7d23a-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d23a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d23a-114">-DefaultProfile</span></span>
<span data-ttu-id="7d23a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d23a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d23a-116">- NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7d23a-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7d23a-117">Określa obiekt grupy zabezpieczeń sieci reprezentujący stan, dla którego ma zostać ustawiona grupa zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="7d23a-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="7d23a-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7d23a-118">-Confirm</span></span>
<span data-ttu-id="7d23a-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7d23a-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d23a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d23a-120">-WhatIf</span></span>
<span data-ttu-id="7d23a-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d23a-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d23a-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7d23a-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d23a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d23a-123">CommonParameters</span></span>
<span data-ttu-id="7d23a-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d23a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d23a-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d23a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d23a-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d23a-126">INPUTS</span></span>

### <span data-ttu-id="7d23a-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7d23a-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="7d23a-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d23a-128">OUTPUTS</span></span>

### <span data-ttu-id="7d23a-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7d23a-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="7d23a-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7d23a-130">NOTES</span></span>

## <span data-ttu-id="7d23a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d23a-131">RELATED LINKS</span></span>

[<span data-ttu-id="7d23a-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7d23a-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="7d23a-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7d23a-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="7d23a-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7d23a-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


