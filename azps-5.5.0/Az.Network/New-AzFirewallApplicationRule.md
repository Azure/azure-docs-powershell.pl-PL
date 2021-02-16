---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: d5c3a560f0afcfb28224cf4681af78d6bd5249ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189683"
---
# <span data-ttu-id="986aa-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="986aa-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="986aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="986aa-102">SYNOPSIS</span></span>
<span data-ttu-id="986aa-103">Tworzy regułę aplikacji zapory.</span><span class="sxs-lookup"><span data-stu-id="986aa-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="986aa-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="986aa-104">SYNTAX</span></span>

### <span data-ttu-id="986aa-105">TargetFqdn (domyślna)</span><span class="sxs-lookup"><span data-stu-id="986aa-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="986aa-106">Tag Fqdn</span><span class="sxs-lookup"><span data-stu-id="986aa-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="986aa-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="986aa-107">DESCRIPTION</span></span>
<span data-ttu-id="986aa-108">Polecenie **cmdlet New-AzFirewallApplicationRule** tworzy regułę aplikacji dla Zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="986aa-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="986aa-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="986aa-109">EXAMPLES</span></span>

### <span data-ttu-id="986aa-110">Przykład 1. Tworzenie reguły zezwalania na cały ruch HTTPS z 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="986aa-110">Example 1: Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="986aa-111">W tym przykładzie jest organizacji tworzącej regułę, która zezwala na cały ruch HTTPS na porcie 443 z portu 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="986aa-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="986aa-112">Przykład 2. Tworzenie reguły zezwalania na program WindowsUpdate dla podsieci 10.0.0.0/24</span><span class="sxs-lookup"><span data-stu-id="986aa-112">Example 2: Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="986aa-113">W tym przykładzie jest organizacji tworzącej regułę, która zezwala na ruch dla domeny 10.0.0.0/24 dla systemu Windows Updates.</span><span class="sxs-lookup"><span data-stu-id="986aa-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="986aa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="986aa-114">PARAMETERS</span></span>

### <span data-ttu-id="986aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="986aa-115">-DefaultProfile</span></span>
<span data-ttu-id="986aa-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="986aa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="986aa-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="986aa-117">-Description</span></span>
<span data-ttu-id="986aa-118">Określa opcjonalny opis tej reguły.</span><span class="sxs-lookup"><span data-stu-id="986aa-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="986aa-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="986aa-119">-FqdnTag</span></span>
<span data-ttu-id="986aa-120">Określa listę tagów FQDN dla tej reguły.</span><span class="sxs-lookup"><span data-stu-id="986aa-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="986aa-121">Dostępne tagi można pobrać za pomocą polecenia cmdlet [Get-AzFirewallFqdnTag.](./Get-AzFirewallFqdnTag.md)</span><span class="sxs-lookup"><span data-stu-id="986aa-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

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

### <span data-ttu-id="986aa-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="986aa-122">-Name</span></span>
<span data-ttu-id="986aa-123">Określa nazwę tej reguły aplikacji.</span><span class="sxs-lookup"><span data-stu-id="986aa-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="986aa-124">Nazwa musi być unikatowa w zbiorze reguł.</span><span class="sxs-lookup"><span data-stu-id="986aa-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="986aa-125">— Protokół</span><span class="sxs-lookup"><span data-stu-id="986aa-125">-Protocol</span></span>
<span data-ttu-id="986aa-126">Określa typ ruchu, który ma być filtrowany przez tę regułę.</span><span class="sxs-lookup"><span data-stu-id="986aa-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="986aa-127">Format: <protocol type> <port> .</span><span class="sxs-lookup"><span data-stu-id="986aa-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="986aa-128">Na przykład : "http:80" lub "https:443".</span><span class="sxs-lookup"><span data-stu-id="986aa-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="986aa-129">Protokół jest obowiązkowy w przypadku korzystania z domeny TargetFqdn, ale nie można go używać z tagiem FqdnTag.</span><span class="sxs-lookup"><span data-stu-id="986aa-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="986aa-130">Obsługiwane protokoły to HTTP i HTTPS.</span><span class="sxs-lookup"><span data-stu-id="986aa-130">The supported protocols are HTTP and HTTPS.</span></span>

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

### <span data-ttu-id="986aa-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="986aa-131">-SourceAddress</span></span>
<span data-ttu-id="986aa-132">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="986aa-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="986aa-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="986aa-133">-SourceIpGroup</span></span>
<span data-ttu-id="986aa-134">Źródłowa grupa ipgroup reguły</span><span class="sxs-lookup"><span data-stu-id="986aa-134">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="986aa-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="986aa-135">-TargetFqdn</span></span>
<span data-ttu-id="986aa-136">Określa listę nazw domen filtrowanych według tej reguły.</span><span class="sxs-lookup"><span data-stu-id="986aa-136">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="986aa-137">Znak gwiazdki ' ', jest akceptowany tylko jako *pierwszy znak FQDN na liście. W przypadku korzystania gwiazdka odpowiada dowolnej liczbie znaków. (np. ' msn.com'* będzie zgodne msn.com i wszystkich jej poddomen)</span><span class="sxs-lookup"><span data-stu-id="986aa-137">The asterisk character, '*', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

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

### <span data-ttu-id="986aa-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="986aa-138">-Confirm</span></span>
<span data-ttu-id="986aa-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="986aa-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="986aa-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="986aa-140">-WhatIf</span></span>
<span data-ttu-id="986aa-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="986aa-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="986aa-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="986aa-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="986aa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="986aa-143">CommonParameters</span></span>
<span data-ttu-id="986aa-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="986aa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="986aa-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="986aa-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="986aa-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="986aa-146">INPUTS</span></span>

### <span data-ttu-id="986aa-147">Brak</span><span class="sxs-lookup"><span data-stu-id="986aa-147">None</span></span>

## <span data-ttu-id="986aa-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="986aa-148">OUTPUTS</span></span>

### <span data-ttu-id="986aa-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="986aa-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="986aa-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="986aa-150">NOTES</span></span>

## <span data-ttu-id="986aa-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="986aa-151">RELATED LINKS</span></span>

[<span data-ttu-id="986aa-152">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="986aa-152">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="986aa-153">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="986aa-153">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="986aa-154">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="986aa-154">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="986aa-155">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="986aa-155">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
