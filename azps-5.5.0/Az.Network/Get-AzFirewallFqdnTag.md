---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193867"
---
# <span data-ttu-id="6c7c8-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="6c7c8-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="6c7c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c7c8-102">SYNOPSIS</span></span>
<span data-ttu-id="6c7c8-103">Pobiera dostępne tagi Fqdn zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6c7c8-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="6c7c8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6c7c8-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c7c8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6c7c8-105">DESCRIPTION</span></span>
<span data-ttu-id="6c7c8-106">Polecenie **cmdlet Get-AzFirewallFqdnTag** pobiera listę tagów FQDN, których można używać w regułach aplikacji zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6c7c8-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="6c7c8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6c7c8-107">EXAMPLES</span></span>

### <span data-ttu-id="6c7c8-108">1. Pobieranie wszystkich dostępnych tagów FQDN</span><span class="sxs-lookup"><span data-stu-id="6c7c8-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="6c7c8-109">W tym przykładzie są pobierane wszystkie dostępne tagi FQDN.</span><span class="sxs-lookup"><span data-stu-id="6c7c8-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="6c7c8-110">2. Używanie pierwszego dostępnego tagu FQDN w witrynie application Rule</span><span class="sxs-lookup"><span data-stu-id="6c7c8-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="6c7c8-111">W tym przykładzie jest tworzenie reguły aplikacji zapory przy użyciu pierwszego dostępnego tagu FQDN</span><span class="sxs-lookup"><span data-stu-id="6c7c8-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="6c7c8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c7c8-112">PARAMETERS</span></span>

### <span data-ttu-id="6c7c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c7c8-113">-DefaultProfile</span></span>
<span data-ttu-id="6c7c8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c7c8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c7c8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c7c8-115">CommonParameters</span></span>
<span data-ttu-id="6c7c8-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c7c8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c7c8-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c7c8-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c7c8-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c7c8-118">INPUTS</span></span>

### <span data-ttu-id="6c7c8-119">Brak</span><span class="sxs-lookup"><span data-stu-id="6c7c8-119">None</span></span>

## <span data-ttu-id="6c7c8-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c7c8-120">OUTPUTS</span></span>

### <span data-ttu-id="6c7c8-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="6c7c8-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="6c7c8-122">System.Collections.generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlet.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="6c7c8-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6c7c8-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6c7c8-123">NOTES</span></span>

## <span data-ttu-id="6c7c8-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c7c8-124">RELATED LINKS</span></span>

[<span data-ttu-id="6c7c8-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="6c7c8-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="6c7c8-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6c7c8-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
