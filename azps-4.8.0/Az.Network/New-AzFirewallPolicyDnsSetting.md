---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 2e4179019f74a8fd85b5f0ea3471bc586864172a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223803"
---
# <span data-ttu-id="126a2-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="126a2-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="126a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="126a2-102">SYNOPSIS</span></span>
<span data-ttu-id="126a2-103">Tworzy nowe ustawienie DNS dla zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="126a2-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="126a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="126a2-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-ProxyNotRequiredForNetworkRule] [-Server <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="126a2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="126a2-105">DESCRIPTION</span></span>
<span data-ttu-id="126a2-106">Polecenie cmdlet **New-AzFirewallPolicyDnsSetting** tworzy obiekt ustawień DNS dla zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="126a2-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="126a2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="126a2-107">EXAMPLES</span></span>

### <span data-ttu-id="126a2-108">1. tworzenie pustych zasad</span><span class="sxs-lookup"><span data-stu-id="126a2-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="126a2-109">W tym przykładzie jest tworzony obiekt ustawień DNS z ustawieniem włączania serwera proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="126a2-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="126a2-110">2. tworzenie pustych zasad z trybem ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="126a2-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```
<span data-ttu-id="126a2-111">W tym przykładzie pokazano, jak utworzyć obiekt ustawienia DNS z ustawieniem włączania serwera proxy DNS i ustawianiu niestandardowych serwerów DNS.</span><span class="sxs-lookup"><span data-stu-id="126a2-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="126a2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="126a2-112">PARAMETERS</span></span>

### <span data-ttu-id="126a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="126a2-113">-DefaultProfile</span></span>
<span data-ttu-id="126a2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="126a2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="126a2-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="126a2-115">-EnableProxy</span></span>
<span data-ttu-id="126a2-116">Włącz serwer proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="126a2-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="126a2-117">Domyślnie jest on wyłączony.</span><span class="sxs-lookup"><span data-stu-id="126a2-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="126a2-118">-ProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="126a2-118">-ProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="126a2-119">Wymaga funkcji proxy DNS dla nazw FQDN w regułach sieciowych.</span><span class="sxs-lookup"><span data-stu-id="126a2-119">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>
<span data-ttu-id="126a2-120">Domyślnie jest to prawdą.</span><span class="sxs-lookup"><span data-stu-id="126a2-120">By default it is true.</span></span>

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

### <span data-ttu-id="126a2-121">-Server</span><span class="sxs-lookup"><span data-stu-id="126a2-121">-Server</span></span>
<span data-ttu-id="126a2-122">Lista serwerów DNS</span><span class="sxs-lookup"><span data-stu-id="126a2-122">The list of DNS Servers</span></span>

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

### <span data-ttu-id="126a2-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="126a2-123">-Confirm</span></span>
<span data-ttu-id="126a2-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="126a2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="126a2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="126a2-125">-WhatIf</span></span>
<span data-ttu-id="126a2-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="126a2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="126a2-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="126a2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="126a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="126a2-128">CommonParameters</span></span>
<span data-ttu-id="126a2-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="126a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="126a2-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="126a2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="126a2-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="126a2-131">INPUTS</span></span>

### <span data-ttu-id="126a2-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="126a2-132">None</span></span>

## <span data-ttu-id="126a2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="126a2-133">OUTPUTS</span></span>

### <span data-ttu-id="126a2-134">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="126a2-134">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="126a2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="126a2-135">NOTES</span></span>

## <span data-ttu-id="126a2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="126a2-136">RELATED LINKS</span></span>
