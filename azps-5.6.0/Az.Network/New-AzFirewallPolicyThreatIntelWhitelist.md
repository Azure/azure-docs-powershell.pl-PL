---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: eed81fbd222220225a67378c67aa1d32d440577a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960394"
---
# <span data-ttu-id="2d6d9-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="2d6d9-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="2d6d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d6d9-102">SYNOPSIS</span></span>
<span data-ttu-id="2d6d9-103">Tworzenie nowej listy białej analizy zagrożeń dla zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2d6d9-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="2d6d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2d6d9-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d6d9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2d6d9-105">DESCRIPTION</span></span>
<span data-ttu-id="2d6d9-106">Polecenie cmdlet **New-AzFirewallPolicyThreatIntelWhitelist** tworzy obiekt whitelist threat firmy Intel, którego można używać podczas tworzenia lub ustawiania zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2d6d9-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="2d6d9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2d6d9-107">EXAMPLES</span></span>

### <span data-ttu-id="2d6d9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d6d9-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="2d6d9-109">W tym przykładzie jest białą listę zagrożeń, która zawiera listę białą FQDN zawierającą jeden wpis i białą listę adresów IP zawierającą dwa wpisy.</span><span class="sxs-lookup"><span data-stu-id="2d6d9-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="2d6d9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d6d9-110">PARAMETERS</span></span>

### <span data-ttu-id="2d6d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d6d9-111">-DefaultProfile</span></span>
<span data-ttu-id="2d6d9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d6d9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6d9-113">— FQDN</span><span class="sxs-lookup"><span data-stu-id="2d6d9-113">-FQDN</span></span>
<span data-ttu-id="2d6d9-114">The FQDNs of the Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="2d6d9-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6d9-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="2d6d9-115">-IpAddress</span></span>
<span data-ttu-id="2d6d9-116">Adresy IP listy zagrożeń" (Threat Intel Whitelist)</span><span class="sxs-lookup"><span data-stu-id="2d6d9-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6d9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d6d9-117">CommonParameters</span></span>
<span data-ttu-id="2d6d9-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d6d9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d6d9-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d6d9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d6d9-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d6d9-120">INPUTS</span></span>

### <span data-ttu-id="2d6d9-121">Brak</span><span class="sxs-lookup"><span data-stu-id="2d6d9-121">None</span></span>

## <span data-ttu-id="2d6d9-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d6d9-122">OUTPUTS</span></span>

### <span data-ttu-id="2d6d9-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="2d6d9-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="2d6d9-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2d6d9-124">NOTES</span></span>

## <span data-ttu-id="2d6d9-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d6d9-125">RELATED LINKS</span></span>
