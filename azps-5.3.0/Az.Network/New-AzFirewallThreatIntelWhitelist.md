---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501265"
---
# <span data-ttu-id="ce9ab-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="ce9ab-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="ce9ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce9ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ce9ab-103">Tworzenie nowego whitelist analizy zagrożeń dla zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ce9ab-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="ce9ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce9ab-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce9ab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ce9ab-105">DESCRIPTION</span></span>
<span data-ttu-id="ce9ab-106">Polecenie cmdlet **New-AzFirewallThreatIntelWhitelist** powoduje utworzenie zagrożenia dla obiektu Intel whitelist, którego można użyć podczas tworzenia lub konfigurowania zapory systemu Azure.</span><span class="sxs-lookup"><span data-stu-id="ce9ab-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="ce9ab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce9ab-107">EXAMPLES</span></span>

### <span data-ttu-id="ce9ab-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ce9ab-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="ce9ab-109">W tym przykładzie jest tworzone zagrożenie, które Intel whitelist zawiera nazwę FQDN whitelist dwóch wpisów oraz adres IP whitelist z dwóch wpisów.</span><span class="sxs-lookup"><span data-stu-id="ce9ab-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="ce9ab-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce9ab-110">PARAMETERS</span></span>

### <span data-ttu-id="ce9ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce9ab-111">-DefaultProfile</span></span>
<span data-ttu-id="ce9ab-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce9ab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce9ab-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="ce9ab-113">-FQDN</span></span>
<span data-ttu-id="ce9ab-114">Nazwy FQDN zagrożenia Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="ce9ab-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="ce9ab-115">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="ce9ab-115">-IpAddress</span></span>
<span data-ttu-id="ce9ab-116">Adresy IP zagrożenia dla procesorów Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="ce9ab-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="ce9ab-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce9ab-117">CommonParameters</span></span>
<span data-ttu-id="ce9ab-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce9ab-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce9ab-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce9ab-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce9ab-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce9ab-120">INPUTS</span></span>

### <span data-ttu-id="ce9ab-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ce9ab-121">None</span></span>

## <span data-ttu-id="ce9ab-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce9ab-122">OUTPUTS</span></span>

### <span data-ttu-id="ce9ab-123">Microsoft. Azure. Commands. Network. models. PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="ce9ab-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="ce9ab-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce9ab-124">NOTES</span></span>

## <span data-ttu-id="ce9ab-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce9ab-125">RELATED LINKS</span></span>

[<span data-ttu-id="ce9ab-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ce9ab-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="ce9ab-127">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ce9ab-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="ce9ab-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ce9ab-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)