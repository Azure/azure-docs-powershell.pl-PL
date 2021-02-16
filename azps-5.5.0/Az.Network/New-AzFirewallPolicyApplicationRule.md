---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 25a81344d9d8d5b8af8eed907bce7977408515ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184499"
---
# <span data-ttu-id="c88d7-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="c88d7-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="c88d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c88d7-102">SYNOPSIS</span></span>
<span data-ttu-id="c88d7-103">Tworzenie nowej reguły aplikacji zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="c88d7-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="c88d7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c88d7-104">SYNTAX</span></span>

### <span data-ttu-id="c88d7-105">SourceAddressAndTargetFqdn (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c88d7-105">SourceAddressAndTargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c88d7-106">SourceAddressAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="c88d7-106">SourceAddressAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c88d7-107">SourceAddressAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="c88d7-107">SourceAddressAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c88d7-108">SourceAddressAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="c88d7-108">SourceAddressAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c88d7-109">SourceIpGroupAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="c88d7-109">SourceIpGroupAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c88d7-110">SourceIpGroupAndTargetFqdn</span><span class="sxs-lookup"><span data-stu-id="c88d7-110">SourceIpGroupAndTargetFqdn</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c88d7-111">SourceIpGroupAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="c88d7-111">SourceIpGroupAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c88d7-112">SourceIpGroupAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="c88d7-112">SourceIpGroupAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c88d7-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="c88d7-113">DESCRIPTION</span></span>
<span data-ttu-id="c88d7-114">Polecenie **cmdlet New-AzFirewallPolicyApplicationRule** tworzy regułę aplikacji dla zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c88d7-114">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="c88d7-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c88d7-115">EXAMPLES</span></span>

### <span data-ttu-id="c88d7-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c88d7-116">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="c88d7-117">W tym przykładzie jest utworzenie reguły aplikacji z adresem źródłowym, protokołem i docelowymi domenami fqdn.</span><span class="sxs-lookup"><span data-stu-id="c88d7-117">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="c88d7-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c88d7-118">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -WebCategory "DatingAndPersonals", "Tasteless"
```

<span data-ttu-id="c88d7-119">W tym przykładzie jest tworzyna reguła aplikacji z adresem źródłowym, protokołem i kategoriami sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c88d7-119">This example creates an application rule with the source address, protocol and web categories.</span></span>

## <span data-ttu-id="c88d7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c88d7-120">PARAMETERS</span></span>

### <span data-ttu-id="c88d7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c88d7-121">-DefaultProfile</span></span>
<span data-ttu-id="c88d7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c88d7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c88d7-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="c88d7-123">-Description</span></span>
<span data-ttu-id="c88d7-124">Opis reguły</span><span class="sxs-lookup"><span data-stu-id="c88d7-124">The description of the rule</span></span>

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

### <span data-ttu-id="c88d7-125">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="c88d7-125">-FqdnTag</span></span>
<span data-ttu-id="c88d7-126">Tagi FQDN reguły</span><span class="sxs-lookup"><span data-stu-id="c88d7-126">The FQDN Tags of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndFqdnTag, SourceIpGroupAndFqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88d7-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c88d7-127">-Name</span></span>
<span data-ttu-id="c88d7-128">Nazwa reguły aplikacji</span><span class="sxs-lookup"><span data-stu-id="c88d7-128">The name of the Application Rule</span></span>

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

### <span data-ttu-id="c88d7-129">— Protokół</span><span class="sxs-lookup"><span data-stu-id="c88d7-129">-Protocol</span></span>
<span data-ttu-id="c88d7-130">Protokoły reguły</span><span class="sxs-lookup"><span data-stu-id="c88d7-130">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndWebCategory, SourceIpGroupAndTargetFqdn, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88d7-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="c88d7-131">-SourceAddress</span></span>
<span data-ttu-id="c88d7-132">Adresy źródłowe reguły</span><span class="sxs-lookup"><span data-stu-id="c88d7-132">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndFqdnTag, SourceAddressAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88d7-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="c88d7-133">-SourceIpGroup</span></span>
<span data-ttu-id="c88d7-134">Źródłowe grupy ipgroup reguły</span><span class="sxs-lookup"><span data-stu-id="c88d7-134">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTargetFqdn, SourceIpGroupAndFqdnTag, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88d7-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="c88d7-135">-TargetFqdn</span></span>
<span data-ttu-id="c88d7-136">Docelowe wartości FQN reguły</span><span class="sxs-lookup"><span data-stu-id="c88d7-136">The target FQDNs of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceIpGroupAndTargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88d7-137">- WebCategory</span><span class="sxs-lookup"><span data-stu-id="c88d7-137">-WebCategory</span></span>
<span data-ttu-id="c88d7-138">Kategorie sieci Web reguły</span><span class="sxs-lookup"><span data-stu-id="c88d7-138">The Web Categories of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndWebCategory, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88d7-139">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="c88d7-139">-TargetUrl</span></span>
<span data-ttu-id="c88d7-140">Docelowy adres URL reguły</span><span class="sxs-lookup"><span data-stu-id="c88d7-140">The Target Url of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetUrl, SourceIpGroupAndTargetUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88d7-141">- TerminateTLS</span><span class="sxs-lookup"><span data-stu-id="c88d7-141">-TerminateTLS</span></span>
<span data-ttu-id="c88d7-142">Oznacza zakończenie TLS</span><span class="sxs-lookup"><span data-stu-id="c88d7-142">Indicates terminating TLS</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88d7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c88d7-143">CommonParameters</span></span>
<span data-ttu-id="c88d7-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c88d7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c88d7-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c88d7-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c88d7-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c88d7-146">INPUTS</span></span>

### <span data-ttu-id="c88d7-147">Brak</span><span class="sxs-lookup"><span data-stu-id="c88d7-147">None</span></span>

## <span data-ttu-id="c88d7-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c88d7-148">OUTPUTS</span></span>

### <span data-ttu-id="c88d7-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="c88d7-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="c88d7-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c88d7-150">NOTES</span></span>

## <span data-ttu-id="c88d7-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c88d7-151">RELATED LINKS</span></span>
