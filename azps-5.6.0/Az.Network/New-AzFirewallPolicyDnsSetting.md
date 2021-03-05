---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 35b56e6aafe73c09343fb17d385dd7ab4c705c5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985769"
---
# <span data-ttu-id="c1227-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="c1227-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="c1227-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1227-102">SYNOPSIS</span></span>
<span data-ttu-id="c1227-103">Tworzy nowe ustawienie DNS dla zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c1227-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="c1227-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c1227-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1227-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c1227-105">DESCRIPTION</span></span>
<span data-ttu-id="c1227-106">Polecenie **cmdlet New-AzFirewallPolicyDnsSetting** tworzy obiekt ustawień DNS dla zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c1227-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="c1227-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c1227-107">EXAMPLES</span></span>

### <span data-ttu-id="c1227-108">1. Tworzenie pustych zasad</span><span class="sxs-lookup"><span data-stu-id="c1227-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="c1227-109">W tym przykładzie jest obiektu ustawień dns z ustawieniem włączania serwera proxy dns.</span><span class="sxs-lookup"><span data-stu-id="c1227-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="c1227-110">2. Tworzenie pustych zasad przy użyciu trybu ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="c1227-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="c1227-111">W tym przykładzie jest tworzyć obiekty dns Setting z ustawieniem włączania serwera proxy DNS i ustawiania niestandardowych serwerów dns.</span><span class="sxs-lookup"><span data-stu-id="c1227-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="c1227-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1227-112">PARAMETERS</span></span>

### <span data-ttu-id="c1227-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1227-113">-DefaultProfile</span></span>
<span data-ttu-id="c1227-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1227-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1227-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="c1227-115">-EnableProxy</span></span>
<span data-ttu-id="c1227-116">Włącz serwer proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="c1227-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="c1227-117">Domyślnie jest ona wyłączona.</span><span class="sxs-lookup"><span data-stu-id="c1227-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="c1227-118">— Serwer</span><span class="sxs-lookup"><span data-stu-id="c1227-118">-Server</span></span>
<span data-ttu-id="c1227-119">Lista serwerów DNS</span><span class="sxs-lookup"><span data-stu-id="c1227-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="c1227-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1227-120">-Confirm</span></span>
<span data-ttu-id="c1227-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c1227-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1227-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1227-122">-WhatIf</span></span>
<span data-ttu-id="c1227-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1227-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1227-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c1227-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1227-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1227-125">CommonParameters</span></span>
<span data-ttu-id="c1227-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1227-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1227-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1227-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1227-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1227-128">INPUTS</span></span>

### <span data-ttu-id="c1227-129">Brak</span><span class="sxs-lookup"><span data-stu-id="c1227-129">None</span></span>

## <span data-ttu-id="c1227-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1227-130">OUTPUTS</span></span>

### <span data-ttu-id="c1227-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="c1227-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="c1227-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c1227-132">NOTES</span></span>

## <span data-ttu-id="c1227-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1227-133">RELATED LINKS</span></span>
