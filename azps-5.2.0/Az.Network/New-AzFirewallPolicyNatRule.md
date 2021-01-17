---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 05b89c164b8a6cd3f91880edac1536d22817ea57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329490"
---
# <span data-ttu-id="d2112-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="d2112-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="d2112-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2112-102">SYNOPSIS</span></span>
<span data-ttu-id="d2112-103">Tworzenie nowej reguły NAT zasad usługi Zapora Azure</span><span class="sxs-lookup"><span data-stu-id="d2112-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="d2112-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2112-104">SYNTAX</span></span>

### <span data-ttu-id="d2112-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="d2112-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2112-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="d2112-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2112-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="d2112-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2112-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="d2112-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2112-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d2112-109">DESCRIPTION</span></span>
<span data-ttu-id="d2112-110">Polecenie cmdlet **New-AzFirewallPolicyNatRule** tworzy regułę NAT dla zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d2112-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="d2112-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2112-111">EXAMPLES</span></span>

### <span data-ttu-id="d2112-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d2112-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="d2112-113">W tym przykładzie przedstawiono tworzenie reguły NAT z adresem źródłowym, protokołem, adresem docelowym, portem docelowym, adresem przetłumaczonym i przetłumaczonym portem.</span><span class="sxs-lookup"><span data-stu-id="d2112-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="d2112-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d2112-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="d2112-115">W tym przykładzie przedstawiono tworzenie reguły NAT z adresem źródłowym, protokołem, adresem docelowym, portem docelowym, przetłumaczoną nazwą FQDN i przetłumaczonym portem.</span><span class="sxs-lookup"><span data-stu-id="d2112-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="d2112-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2112-116">PARAMETERS</span></span>

### <span data-ttu-id="d2112-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2112-117">-DefaultProfile</span></span>
<span data-ttu-id="d2112-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2112-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2112-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="d2112-119">-Description</span></span>
<span data-ttu-id="d2112-120">Opis reguły</span><span class="sxs-lookup"><span data-stu-id="d2112-120">The description of the rule</span></span>

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

### <span data-ttu-id="d2112-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d2112-121">-DestinationAddress</span></span>
<span data-ttu-id="d2112-122">Adresy docelowe reguły.</span><span class="sxs-lookup"><span data-stu-id="d2112-122">The destination addresses of the rule.</span></span> <span data-ttu-id="d2112-123">Ten adres musi być publicznym adresem IP zapory.</span><span class="sxs-lookup"><span data-stu-id="d2112-123">This has to be Public IP of the Firewall.</span></span>

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

### <span data-ttu-id="d2112-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d2112-124">-DestinationPort</span></span>
<span data-ttu-id="d2112-125">Porty docelowe reguły</span><span class="sxs-lookup"><span data-stu-id="d2112-125">The destination ports of the rule</span></span>

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

### <span data-ttu-id="d2112-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d2112-126">-Name</span></span>
<span data-ttu-id="d2112-127">Nazwa kolekcji reguł NAT</span><span class="sxs-lookup"><span data-stu-id="d2112-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="d2112-128">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="d2112-128">-Protocol</span></span>
<span data-ttu-id="d2112-129">Protokoły reguły</span><span class="sxs-lookup"><span data-stu-id="d2112-129">The protocols of the rule</span></span>

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

### <span data-ttu-id="d2112-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="d2112-130">-SourceAddress</span></span>
<span data-ttu-id="d2112-131">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="d2112-131">The source addresses of the rule</span></span>

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

### <span data-ttu-id="d2112-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="d2112-132">-SourceIpGroup</span></span>
<span data-ttu-id="d2112-133">Ipgroups źródłowa reguły</span><span class="sxs-lookup"><span data-stu-id="d2112-133">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="d2112-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="d2112-134">-TranslatedAddress</span></span>
<span data-ttu-id="d2112-135">Adres przetłumaczony tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="d2112-135">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="d2112-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="d2112-136">-TranslatedFqdn</span></span>
<span data-ttu-id="d2112-137">Przetłumaczona nazwa FQDN dla tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="d2112-137">The translated FQDN for this NAT rule</span></span>

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

### <span data-ttu-id="d2112-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="d2112-138">-TranslatedPort</span></span>
<span data-ttu-id="d2112-139">Przetłumaczony port dla tej reguły NAT</span><span class="sxs-lookup"><span data-stu-id="d2112-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="d2112-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2112-140">CommonParameters</span></span>
<span data-ttu-id="d2112-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2112-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2112-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2112-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2112-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2112-143">INPUTS</span></span>

### <span data-ttu-id="d2112-144">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d2112-144">None</span></span>

## <span data-ttu-id="d2112-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2112-145">OUTPUTS</span></span>

### <span data-ttu-id="d2112-146">Microsoft. Azure. Commands. Network. models. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="d2112-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="d2112-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2112-147">NOTES</span></span>

## <span data-ttu-id="d2112-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2112-148">RELATED LINKS</span></span>
