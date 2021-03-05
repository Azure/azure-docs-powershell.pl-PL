---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 18946b74ea72ac3d5db2dd683657eda60b8eeec5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964154"
---
# <span data-ttu-id="d43b9-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="d43b9-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="d43b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d43b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d43b9-103">Tworzenie nowej listy białej analizy zagrożeń dla zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d43b9-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="d43b9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d43b9-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d43b9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d43b9-105">DESCRIPTION</span></span>
<span data-ttu-id="d43b9-106">Polecenie **cmdlet New-AzFirewallThreatIntelWhitelist** tworzy obiekt analizy zagrożeń, którego można używać podczas tworzenia lub ustawiania zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d43b9-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="d43b9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d43b9-107">EXAMPLES</span></span>

### <span data-ttu-id="d43b9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d43b9-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="d43b9-109">W tym przykładzie jest białą listę zagrożeń firmy Intel zawierającą białą listę FQDN zawierającą dwa wpisy oraz białą listę adresów IP zawierającą dwa wpisy.</span><span class="sxs-lookup"><span data-stu-id="d43b9-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="d43b9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d43b9-110">PARAMETERS</span></span>

### <span data-ttu-id="d43b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d43b9-111">-DefaultProfile</span></span>
<span data-ttu-id="d43b9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d43b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d43b9-113">— FQDN</span><span class="sxs-lookup"><span data-stu-id="d43b9-113">-FQDN</span></span>
<span data-ttu-id="d43b9-114">The FQDNs of the Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="d43b9-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43b9-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="d43b9-115">-IpAddress</span></span>
<span data-ttu-id="d43b9-116">Adresy IP listy zagrożeń" (Threat Intel Whitelist)</span><span class="sxs-lookup"><span data-stu-id="d43b9-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43b9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43b9-117">CommonParameters</span></span>
<span data-ttu-id="d43b9-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d43b9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43b9-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d43b9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43b9-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d43b9-120">INPUTS</span></span>

### <span data-ttu-id="d43b9-121">Brak</span><span class="sxs-lookup"><span data-stu-id="d43b9-121">None</span></span>

## <span data-ttu-id="d43b9-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d43b9-122">OUTPUTS</span></span>

### <span data-ttu-id="d43b9-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="d43b9-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="d43b9-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d43b9-124">NOTES</span></span>

## <span data-ttu-id="d43b9-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d43b9-125">RELATED LINKS</span></span>

[<span data-ttu-id="d43b9-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d43b9-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="d43b9-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d43b9-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="d43b9-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d43b9-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)