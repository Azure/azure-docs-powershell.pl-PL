---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: ff5dee9a4e072cea7f1ee5bd46898857233ed0d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956945"
---
# <span data-ttu-id="f0613-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="f0613-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="f0613-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0613-102">SYNOPSIS</span></span>
<span data-ttu-id="f0613-103">Pobiera dostępne tagi Fqdn zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f0613-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="f0613-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f0613-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0613-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f0613-105">DESCRIPTION</span></span>
<span data-ttu-id="f0613-106">Polecenie **cmdlet Get-AzFirewallFqdnTag** pobiera listę tagów FQDN, których można używać w regułach aplikacji zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f0613-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="f0613-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f0613-107">EXAMPLES</span></span>

### <span data-ttu-id="f0613-108">1. Pobieranie wszystkich dostępnych tagów FQDN</span><span class="sxs-lookup"><span data-stu-id="f0613-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="f0613-109">W tym przykładzie są pobierane wszystkie dostępne tagi FQDN.</span><span class="sxs-lookup"><span data-stu-id="f0613-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="f0613-110">2. Używanie pierwszego dostępnego tagu FQDN w witrynie application Rule</span><span class="sxs-lookup"><span data-stu-id="f0613-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="f0613-111">W tym przykładzie jest tworzenie reguły aplikacji zapory przy użyciu pierwszego dostępnego tagu FQDN</span><span class="sxs-lookup"><span data-stu-id="f0613-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="f0613-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0613-112">PARAMETERS</span></span>

### <span data-ttu-id="f0613-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0613-113">-DefaultProfile</span></span>
<span data-ttu-id="f0613-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0613-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0613-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0613-115">CommonParameters</span></span>
<span data-ttu-id="f0613-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0613-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0613-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0613-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0613-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0613-118">INPUTS</span></span>

### <span data-ttu-id="f0613-119">Brak</span><span class="sxs-lookup"><span data-stu-id="f0613-119">None</span></span>

## <span data-ttu-id="f0613-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0613-120">OUTPUTS</span></span>

### <span data-ttu-id="f0613-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="f0613-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="f0613-122">System.Collections.generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlet.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f0613-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f0613-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f0613-123">NOTES</span></span>

## <span data-ttu-id="f0613-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0613-124">RELATED LINKS</span></span>

[<span data-ttu-id="f0613-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="f0613-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="f0613-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f0613-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
