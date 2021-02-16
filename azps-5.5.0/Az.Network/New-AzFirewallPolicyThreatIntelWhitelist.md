---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189666"
---
# <span data-ttu-id="e0879-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="e0879-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="e0879-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0879-102">SYNOPSIS</span></span>
<span data-ttu-id="e0879-103">Tworzenie nowej listy analiz zagrożeń dla zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e0879-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="e0879-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0879-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0879-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0879-105">DESCRIPTION</span></span>
<span data-ttu-id="e0879-106">Polecenie cmdlet **New-AzFirewallPolicyThreatIntelWhitelist** tworzy obiekt whitelist threat firmy Intel, którego można używać podczas tworzenia lub ustawiania zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0879-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="e0879-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0879-107">EXAMPLES</span></span>

### <span data-ttu-id="e0879-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e0879-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="e0879-109">W tym przykładzie jest białą listę zagrożeń firmy Intel zawierającą białą listę FQDN zawierającą jeden wpis i białą listę adresów IP zawierającą dwa wpisy.</span><span class="sxs-lookup"><span data-stu-id="e0879-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="e0879-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0879-110">PARAMETERS</span></span>

### <span data-ttu-id="e0879-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0879-111">-DefaultProfile</span></span>
<span data-ttu-id="e0879-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0879-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0879-113">— FQDN</span><span class="sxs-lookup"><span data-stu-id="e0879-113">-FQDN</span></span>
<span data-ttu-id="e0879-114">The FQDNs of the Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="e0879-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="e0879-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="e0879-115">-IpAddress</span></span>
<span data-ttu-id="e0879-116">Adresy IP listy zagrożeń" (Threat Intel Whitelist)</span><span class="sxs-lookup"><span data-stu-id="e0879-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="e0879-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0879-117">CommonParameters</span></span>
<span data-ttu-id="e0879-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0879-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0879-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0879-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0879-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0879-120">INPUTS</span></span>

### <span data-ttu-id="e0879-121">Brak</span><span class="sxs-lookup"><span data-stu-id="e0879-121">None</span></span>

## <span data-ttu-id="e0879-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0879-122">OUTPUTS</span></span>

### <span data-ttu-id="e0879-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="e0879-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="e0879-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0879-124">NOTES</span></span>

## <span data-ttu-id="e0879-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0879-125">RELATED LINKS</span></span>
