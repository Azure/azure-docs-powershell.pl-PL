---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
ms.openlocfilehash: 8a59f09184c7042b12abbd549398ca4690ace235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719086"
---
# <span data-ttu-id="e94bd-101">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="e94bd-101">New-AzureRmFirewallApplicationRule</span></span>

## <span data-ttu-id="e94bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e94bd-102">SYNOPSIS</span></span>
<span data-ttu-id="e94bd-103">Tworzy regułę aplikacji zapory.</span><span class="sxs-lookup"><span data-stu-id="e94bd-103">Creates a Firewall Application Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e94bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e94bd-104">SYNTAX</span></span>

### <span data-ttu-id="e94bd-105">TargetFqdn (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e94bd-105">TargetFqdn (Default)</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -TargetFqdn <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e94bd-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="e94bd-106">FqdnTag</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -FqdnTag <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e94bd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e94bd-107">DESCRIPTION</span></span>
<span data-ttu-id="e94bd-108">Polecenie cmdlet **New-AzureRmFirewallApplicationRule** umożliwia utworzenie reguły aplikacji dla zapory systemu Azure.</span><span class="sxs-lookup"><span data-stu-id="e94bd-108">The **New-AzureRmFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="e94bd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e94bd-109">EXAMPLES</span></span>

### <span data-ttu-id="e94bd-110">1: Tworzenie reguły zezwalającej na cały ruch HTTPS od 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="e94bd-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzureRmFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="e94bd-111">W tym przykładzie jest tworzona reguła zezwalająca na cały ruch HTTPS na porcie 443 od 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="e94bd-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="e94bd-112">2: Tworzenie reguły zezwalającej na obsługę usługi WindowsUpdate dla podsieci 10.0.0.0/24</span><span class="sxs-lookup"><span data-stu-id="e94bd-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzureRmFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="e94bd-113">W tym przykładzie jest tworzona reguła zezwalająca na ruch w usłudze Windows updates dla domeny 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="e94bd-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="e94bd-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e94bd-114">PARAMETERS</span></span>

### <span data-ttu-id="e94bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e94bd-115">-DefaultProfile</span></span>
<span data-ttu-id="e94bd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e94bd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94bd-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="e94bd-117">-Description</span></span>
<span data-ttu-id="e94bd-118">Umożliwia określenie opcjonalnego opisu tej reguły.</span><span class="sxs-lookup"><span data-stu-id="e94bd-118">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94bd-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="e94bd-119">-FqdnTag</span></span>
<span data-ttu-id="e94bd-120">Określa listę tagów FQDN dla tej reguły.</span><span class="sxs-lookup"><span data-stu-id="e94bd-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="e94bd-121">Dostępne Tagi można pobrać przy użyciu polecenia cmdlet [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) .</span><span class="sxs-lookup"><span data-stu-id="e94bd-121">The available tags can be retrieved using [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94bd-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e94bd-122">-Name</span></span>
<span data-ttu-id="e94bd-123">Określa nazwę tej reguły aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e94bd-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="e94bd-124">Nazwa musi być unikatowa w kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="e94bd-124">The name must be unique inside a rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94bd-125">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="e94bd-125">-Protocol</span></span>
<span data-ttu-id="e94bd-126">Określa typ ruchu, który ma być filtrowany przez tę regułę.</span><span class="sxs-lookup"><span data-stu-id="e94bd-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="e94bd-127">Format <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="e94bd-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="e94bd-128">Na przykład "http: 80" lub "https: 443".</span><span class="sxs-lookup"><span data-stu-id="e94bd-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="e94bd-129">Protokół jest obowiązkowy, gdy jest używana TargetFqdn, ale nie można go użyć z FqdnTag.</span><span class="sxs-lookup"><span data-stu-id="e94bd-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="e94bd-130">Obsługiwane protokoły to HTTP i HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e94bd-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94bd-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e94bd-131">-SourceAddress</span></span>
<span data-ttu-id="e94bd-132">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="e94bd-132">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94bd-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="e94bd-133">-TargetFqdn</span></span>
<span data-ttu-id="e94bd-134">Określa listę nazw domen filtrowanych według tej reguły.</span><span class="sxs-lookup"><span data-stu-id="e94bd-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="e94bd-135">Znak pomocą funkcji ' *' jest akceptowany tylko jako pierwszy znak nazwy FQDN na liście. W przypadku użycia pomocą funkcji uwzględnia dowolną liczbę znaków. (na przykład "* MSN.com" będzie pasować MSN.com i wszystkie jej poddomeny)</span><span class="sxs-lookup"><span data-stu-id="e94bd-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94bd-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e94bd-136">-Confirm</span></span>
<span data-ttu-id="e94bd-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e94bd-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94bd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e94bd-138">-WhatIf</span></span>
<span data-ttu-id="e94bd-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e94bd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e94bd-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e94bd-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94bd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94bd-141">CommonParameters</span></span>
<span data-ttu-id="e94bd-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e94bd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94bd-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e94bd-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94bd-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e94bd-144">INPUTS</span></span>

### <span data-ttu-id="e94bd-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e94bd-145">None</span></span>
<span data-ttu-id="e94bd-146">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e94bd-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e94bd-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e94bd-147">OUTPUTS</span></span>

### <span data-ttu-id="e94bd-148">Microsoft. Azure. Commands. Network. models. PSFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="e94bd-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRule</span></span>

## <span data-ttu-id="e94bd-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e94bd-149">NOTES</span></span>

## <span data-ttu-id="e94bd-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e94bd-150">RELATED LINKS</span></span>

[<span data-ttu-id="e94bd-151">Nowe — AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e94bd-151">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="e94bd-152">Nowe — AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e94bd-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="e94bd-153">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="e94bd-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="e94bd-154">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="e94bd-154">Get-AzureRmFirewallFqdnTag</span></span>](./Get-AzureRmFirewallFqdnTag.md)
