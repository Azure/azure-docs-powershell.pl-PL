---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342754"
---
# <span data-ttu-id="1b6d3-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="1b6d3-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="1b6d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b6d3-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6d3-103">Tworzenie nowego whitelist analizy zagrożeń dla zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="1b6d3-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="1b6d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b6d3-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b6d3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1b6d3-105">DESCRIPTION</span></span>
<span data-ttu-id="1b6d3-106">Polecenie cmdlet **New-AzFirewallThreatIntelWhitelist** powoduje utworzenie zagrożenia dla obiektu Intel whitelist, którego można użyć podczas tworzenia lub konfigurowania zapory systemu Azure.</span><span class="sxs-lookup"><span data-stu-id="1b6d3-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="1b6d3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b6d3-107">EXAMPLES</span></span>

### <span data-ttu-id="1b6d3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1b6d3-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="1b6d3-109">W tym przykładzie jest tworzone zagrożenie, które Intel whitelist zawiera nazwę FQDN whitelist dwóch wpisów oraz adres IP whitelist z dwóch wpisów.</span><span class="sxs-lookup"><span data-stu-id="1b6d3-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="1b6d3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b6d3-110">PARAMETERS</span></span>

### <span data-ttu-id="1b6d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6d3-111">-DefaultProfile</span></span>
<span data-ttu-id="1b6d3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b6d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b6d3-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="1b6d3-113">-FQDN</span></span>
<span data-ttu-id="1b6d3-114">Nazwy FQDN zagrożenia Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="1b6d3-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="1b6d3-115">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="1b6d3-115">-IpAddress</span></span>
<span data-ttu-id="1b6d3-116">Adresy IP zagrożenia dla procesorów Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="1b6d3-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="1b6d3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6d3-117">CommonParameters</span></span>
<span data-ttu-id="1b6d3-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b6d3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6d3-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b6d3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6d3-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b6d3-120">INPUTS</span></span>

### <span data-ttu-id="1b6d3-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1b6d3-121">None</span></span>

## <span data-ttu-id="1b6d3-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b6d3-122">OUTPUTS</span></span>

### <span data-ttu-id="1b6d3-123">Microsoft. Azure. Commands. Network. models. PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="1b6d3-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="1b6d3-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b6d3-124">NOTES</span></span>

## <span data-ttu-id="1b6d3-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b6d3-125">RELATED LINKS</span></span>

[<span data-ttu-id="1b6d3-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1b6d3-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="1b6d3-127">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1b6d3-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="1b6d3-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1b6d3-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)