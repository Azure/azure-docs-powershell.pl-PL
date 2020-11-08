---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: d5c3a560f0afcfb28224cf4681af78d6bd5249ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232797"
---
# <span data-ttu-id="b5bda-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="b5bda-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="b5bda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5bda-102">SYNOPSIS</span></span>
<span data-ttu-id="b5bda-103">Tworzy regułę aplikacji zapory.</span><span class="sxs-lookup"><span data-stu-id="b5bda-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="b5bda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5bda-104">SYNTAX</span></span>

### <span data-ttu-id="b5bda-105">TargetFqdn (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b5bda-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5bda-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="b5bda-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5bda-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b5bda-107">DESCRIPTION</span></span>
<span data-ttu-id="b5bda-108">Polecenie cmdlet **New-AzFirewallApplicationRule** umożliwia utworzenie reguły aplikacji dla zapory systemu Azure.</span><span class="sxs-lookup"><span data-stu-id="b5bda-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="b5bda-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5bda-109">EXAMPLES</span></span>

### <span data-ttu-id="b5bda-110">Przykład 1. Tworzenie reguły zezwalającej na cały ruch HTTPS od 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="b5bda-110">Example 1: Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="b5bda-111">W tym przykładzie jest tworzona reguła zezwalająca na cały ruch HTTPS na porcie 443 od 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="b5bda-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="b5bda-112">Przykład 2: Tworzenie reguły zezwalającej na obsługę usługi WindowsUpdate dla podsieci 10.0.0.0/24</span><span class="sxs-lookup"><span data-stu-id="b5bda-112">Example 2: Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="b5bda-113">W tym przykładzie jest tworzona reguła zezwalająca na ruch w usłudze Windows updates dla domeny 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="b5bda-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="b5bda-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5bda-114">PARAMETERS</span></span>

### <span data-ttu-id="b5bda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5bda-115">-DefaultProfile</span></span>
<span data-ttu-id="b5bda-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5bda-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5bda-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="b5bda-117">-Description</span></span>
<span data-ttu-id="b5bda-118">Umożliwia określenie opcjonalnego opisu tej reguły.</span><span class="sxs-lookup"><span data-stu-id="b5bda-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="b5bda-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="b5bda-119">-FqdnTag</span></span>
<span data-ttu-id="b5bda-120">Określa listę tagów FQDN dla tej reguły.</span><span class="sxs-lookup"><span data-stu-id="b5bda-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="b5bda-121">Dostępne Tagi można pobrać przy użyciu polecenia cmdlet [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) .</span><span class="sxs-lookup"><span data-stu-id="b5bda-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5bda-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5bda-122">-Name</span></span>
<span data-ttu-id="b5bda-123">Określa nazwę tej reguły aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b5bda-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="b5bda-124">Nazwa musi być unikatowa w kolekcji reguł.</span><span class="sxs-lookup"><span data-stu-id="b5bda-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="b5bda-125">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="b5bda-125">-Protocol</span></span>
<span data-ttu-id="b5bda-126">Określa typ ruchu, który ma być filtrowany przez tę regułę.</span><span class="sxs-lookup"><span data-stu-id="b5bda-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="b5bda-127">Format <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="b5bda-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="b5bda-128">Na przykład "http: 80" lub "https: 443".</span><span class="sxs-lookup"><span data-stu-id="b5bda-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="b5bda-129">Protokół jest obowiązkowy, gdy jest używana TargetFqdn, ale nie można go użyć z FqdnTag.</span><span class="sxs-lookup"><span data-stu-id="b5bda-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="b5bda-130">Obsługiwane protokoły to HTTP i HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b5bda-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5bda-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="b5bda-131">-SourceAddress</span></span>
<span data-ttu-id="b5bda-132">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="b5bda-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="b5bda-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="b5bda-133">-SourceIpGroup</span></span>
<span data-ttu-id="b5bda-134">Ipgroup źródłowa reguły</span><span class="sxs-lookup"><span data-stu-id="b5bda-134">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="b5bda-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="b5bda-135">-TargetFqdn</span></span>
<span data-ttu-id="b5bda-136">Określa listę nazw domen filtrowanych według tej reguły.</span><span class="sxs-lookup"><span data-stu-id="b5bda-136">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="b5bda-137">Znak gwiazdki " *" jest akceptowany tylko jako pierwszy znak nazwy FQDN na liście. W przypadku użycia gwiazdka pasuje do dowolnej liczby znaków. (na przykład "* MSN.com" będzie pasować MSN.com i wszystkie jej poddomeny)</span><span class="sxs-lookup"><span data-stu-id="b5bda-137">The asterisk character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5bda-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5bda-138">-Confirm</span></span>
<span data-ttu-id="b5bda-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5bda-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5bda-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5bda-140">-WhatIf</span></span>
<span data-ttu-id="b5bda-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5bda-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5bda-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5bda-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5bda-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5bda-143">CommonParameters</span></span>
<span data-ttu-id="b5bda-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5bda-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5bda-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5bda-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5bda-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5bda-146">INPUTS</span></span>

### <span data-ttu-id="b5bda-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b5bda-147">None</span></span>

## <span data-ttu-id="b5bda-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5bda-148">OUTPUTS</span></span>

### <span data-ttu-id="b5bda-149">Microsoft. Azure. Commands. Network. models. PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="b5bda-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="b5bda-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5bda-150">NOTES</span></span>

## <span data-ttu-id="b5bda-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5bda-151">RELATED LINKS</span></span>

[<span data-ttu-id="b5bda-152">Nowe — AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="b5bda-152">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="b5bda-153">Nowe — AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b5bda-153">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="b5bda-154">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="b5bda-154">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="b5bda-155">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="b5bda-155">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
