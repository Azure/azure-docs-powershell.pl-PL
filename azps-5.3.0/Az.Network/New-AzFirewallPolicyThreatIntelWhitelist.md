---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500353"
---
# <span data-ttu-id="60fa4-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="60fa4-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="60fa4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="60fa4-103">Utwórz nowe whitelist analizy zagrożeń dla zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="60fa4-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="60fa4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60fa4-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60fa4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="60fa4-105">DESCRIPTION</span></span>
<span data-ttu-id="60fa4-106">Polecenie cmdlet **New-AzFirewallPolicyThreatIntelWhitelist** powoduje utworzenie zagrożenia dla obiektu Intel whitelist, którego można użyć podczas tworzenia lub ustawiania zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="60fa4-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="60fa4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60fa4-107">EXAMPLES</span></span>

### <span data-ttu-id="60fa4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60fa4-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="60fa4-109">W tym przykładzie jest tworzone zagrożenie, które Intel whitelist zawiera nazwę FQDN whitelist jednego wpisu i adres IP whitelist z dwóch wpisów.</span><span class="sxs-lookup"><span data-stu-id="60fa4-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="60fa4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60fa4-110">PARAMETERS</span></span>

### <span data-ttu-id="60fa4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60fa4-111">-DefaultProfile</span></span>
<span data-ttu-id="60fa4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60fa4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60fa4-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="60fa4-113">-FQDN</span></span>
<span data-ttu-id="60fa4-114">Nazwy FQDN zagrożenia Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="60fa4-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="60fa4-115">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="60fa4-115">-IpAddress</span></span>
<span data-ttu-id="60fa4-116">Adresy IP zagrożenia dla procesorów Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="60fa4-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="60fa4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60fa4-117">CommonParameters</span></span>
<span data-ttu-id="60fa4-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60fa4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60fa4-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60fa4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60fa4-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60fa4-120">INPUTS</span></span>

### <span data-ttu-id="60fa4-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="60fa4-121">None</span></span>

## <span data-ttu-id="60fa4-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60fa4-122">OUTPUTS</span></span>

### <span data-ttu-id="60fa4-123">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="60fa4-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="60fa4-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60fa4-124">NOTES</span></span>

## <span data-ttu-id="60fa4-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60fa4-125">RELATED LINKS</span></span>
