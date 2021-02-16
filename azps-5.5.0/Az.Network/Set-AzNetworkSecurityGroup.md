---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: d7a13c27550b206bc1c8d8fa909cb5135df0db55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191642"
---
# <span data-ttu-id="bcf73-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bcf73-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="bcf73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcf73-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf73-103">Aktualizuje grupę zabezpieczeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="bcf73-103">Updates a network security group.</span></span>

## <span data-ttu-id="bcf73-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bcf73-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcf73-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bcf73-105">DESCRIPTION</span></span>
<span data-ttu-id="bcf73-106">Polecenie **cmdlet Set-AzNetworkSecurityGroup** aktualizuje grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="bcf73-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="bcf73-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bcf73-107">EXAMPLES</span></span>

### <span data-ttu-id="bcf73-108">Przykład 1. Aktualizowanie istniejącej grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="bcf73-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="bcf73-109">To polecenie pobiera grupę zabezpieczeń sieci platformy Azure o nazwie Nsg1 i dodaje regułę zabezpieczeń sieciowych o nazwie Rdp-Rule, aby zezwolić na ruch internetowy na porcie 3389 do pobranego obiektu grupy zabezpieczeń sieci przy użyciu dodatku Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="bcf73-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="bcf73-110">Polecenie będzie zachowywać zmodyfikowaną grupę zabezpieczeń sieci platformy Azure przy użyciu **polecenia Set-AzNetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="bcf73-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="bcf73-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcf73-111">PARAMETERS</span></span>

### <span data-ttu-id="bcf73-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bcf73-112">-AsJob</span></span>
<span data-ttu-id="bcf73-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bcf73-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcf73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf73-114">-DefaultProfile</span></span>
<span data-ttu-id="bcf73-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bcf73-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcf73-116">- NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bcf73-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="bcf73-117">Określa obiekt grupy zabezpieczeń sieci reprezentujący stan, dla którego grupa zabezpieczeń sieci powinna zostać ustawiona.</span><span class="sxs-lookup"><span data-stu-id="bcf73-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="bcf73-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bcf73-118">-Confirm</span></span>
<span data-ttu-id="bcf73-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bcf73-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcf73-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcf73-120">-WhatIf</span></span>
<span data-ttu-id="bcf73-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcf73-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bcf73-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bcf73-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcf73-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf73-123">CommonParameters</span></span>
<span data-ttu-id="bcf73-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcf73-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf73-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcf73-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf73-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcf73-126">INPUTS</span></span>

### <span data-ttu-id="bcf73-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bcf73-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="bcf73-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcf73-128">OUTPUTS</span></span>

### <span data-ttu-id="bcf73-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bcf73-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="bcf73-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bcf73-130">NOTES</span></span>

## <span data-ttu-id="bcf73-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bcf73-131">RELATED LINKS</span></span>

[<span data-ttu-id="bcf73-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bcf73-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="bcf73-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bcf73-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="bcf73-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bcf73-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


