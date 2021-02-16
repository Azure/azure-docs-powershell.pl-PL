---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 05b89c164b8a6cd3f91880edac1536d22817ea57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191859"
---
# <span data-ttu-id="e222e-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="e222e-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="e222e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e222e-102">SYNOPSIS</span></span>
<span data-ttu-id="e222e-103">Tworzenie nowej reguły nat zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e222e-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="e222e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e222e-104">SYNTAX</span></span>

### <span data-ttu-id="e222e-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="e222e-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e222e-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="e222e-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e222e-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="e222e-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e222e-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="e222e-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e222e-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e222e-109">DESCRIPTION</span></span>
<span data-ttu-id="e222e-110">Polecenie **cmdlet New-AzFirewallPolicyNatRule** tworzy regułę NAT dla zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e222e-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="e222e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e222e-111">EXAMPLES</span></span>

### <span data-ttu-id="e222e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e222e-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="e222e-113">W tym przykładzie jest owana reguła NAT z adresem źródłowym, protokołem, adresem docelowym, portem docelowym, przetłumaczonym adresem i przetłumaczonym portem.</span><span class="sxs-lookup"><span data-stu-id="e222e-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="e222e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e222e-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="e222e-115">W tym przykładzie jest owana reguła NAT z adresem źródłowym, protokołem, adresem docelowym, portem docelowym, przetłumaczoną witrynie fqdn i przetłumaczonym portem.</span><span class="sxs-lookup"><span data-stu-id="e222e-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="e222e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e222e-116">PARAMETERS</span></span>

### <span data-ttu-id="e222e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e222e-117">-DefaultProfile</span></span>
<span data-ttu-id="e222e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e222e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e222e-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="e222e-119">-Description</span></span>
<span data-ttu-id="e222e-120">Opis reguły</span><span class="sxs-lookup"><span data-stu-id="e222e-120">The description of the rule</span></span>

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

### <span data-ttu-id="e222e-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e222e-121">-DestinationAddress</span></span>
<span data-ttu-id="e222e-122">Adresy docelowe reguły.</span><span class="sxs-lookup"><span data-stu-id="e222e-122">The destination addresses of the rule.</span></span> <span data-ttu-id="e222e-123">Musi to być publiczny adres IP Zapory.</span><span class="sxs-lookup"><span data-stu-id="e222e-123">This has to be Public IP of the Firewall.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e222e-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e222e-124">-DestinationPort</span></span>
<span data-ttu-id="e222e-125">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="e222e-125">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e222e-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e222e-126">-Name</span></span>
<span data-ttu-id="e222e-127">Nazwa zbioru reguł NAT</span><span class="sxs-lookup"><span data-stu-id="e222e-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="e222e-128">— Protokół</span><span class="sxs-lookup"><span data-stu-id="e222e-128">-Protocol</span></span>
<span data-ttu-id="e222e-129">Protokoły reguły</span><span class="sxs-lookup"><span data-stu-id="e222e-129">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e222e-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e222e-130">-SourceAddress</span></span>
<span data-ttu-id="e222e-131">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="e222e-131">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTranslatedAddress, SourceAddressAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e222e-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="e222e-132">-SourceIpGroup</span></span>
<span data-ttu-id="e222e-133">Źródłowe grupy ipgroup reguły</span><span class="sxs-lookup"><span data-stu-id="e222e-133">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTranslatedAddress, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e222e-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="e222e-134">-TranslatedAddress</span></span>
<span data-ttu-id="e222e-135">Przetłumaczony adres tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="e222e-135">The translated address for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedAddress, SourceIpGroupAndTranslatedAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e222e-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="e222e-136">-TranslatedFqdn</span></span>
<span data-ttu-id="e222e-137">Przetłumaczona fqdn tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="e222e-137">The translated FQDN for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedFqdn, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e222e-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="e222e-138">-TranslatedPort</span></span>
<span data-ttu-id="e222e-139">Przetłumaczony port tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="e222e-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="e222e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e222e-140">CommonParameters</span></span>
<span data-ttu-id="e222e-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e222e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e222e-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e222e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e222e-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e222e-143">INPUTS</span></span>

### <span data-ttu-id="e222e-144">Brak</span><span class="sxs-lookup"><span data-stu-id="e222e-144">None</span></span>

## <span data-ttu-id="e222e-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e222e-145">OUTPUTS</span></span>

### <span data-ttu-id="e222e-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="e222e-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="e222e-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e222e-147">NOTES</span></span>

## <span data-ttu-id="e222e-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e222e-148">RELATED LINKS</span></span>
