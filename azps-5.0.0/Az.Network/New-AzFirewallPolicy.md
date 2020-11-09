---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 17aea8ab38582373420107df87e2b6837a83a1a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317142"
---
# <span data-ttu-id="5f32f-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5f32f-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="5f32f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f32f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f32f-103">Tworzy nowe zasady zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5f32f-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="5f32f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f32f-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f32f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5f32f-105">DESCRIPTION</span></span>
<span data-ttu-id="5f32f-106">Polecenie cmdlet **New-AzFirewallPolicy** tworzy zasady zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f32f-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="5f32f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f32f-107">EXAMPLES</span></span>

### <span data-ttu-id="5f32f-108">Przykład 1:1.</span><span class="sxs-lookup"><span data-stu-id="5f32f-108">Example 1: 1.</span></span> <span data-ttu-id="5f32f-109">Tworzenie pustych zasad</span><span class="sxs-lookup"><span data-stu-id="5f32f-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="5f32f-110">W tym przykładzie przedstawiono tworzenie zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5f32f-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="5f32f-111">Przykład 2:2.</span><span class="sxs-lookup"><span data-stu-id="5f32f-111">Example 2: 2.</span></span> <span data-ttu-id="5f32f-112">Tworzenie pustych zasad z trybem ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="5f32f-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="5f32f-113">W tym przykładzie przedstawiono tworzenie zasad zapory platformy Azure z zagrożonym trybem Intel</span><span class="sxs-lookup"><span data-stu-id="5f32f-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="5f32f-114">Przykład 3:3.</span><span class="sxs-lookup"><span data-stu-id="5f32f-114">Example 3: 3.</span></span> <span data-ttu-id="5f32f-115">Tworzenie pustych zasad za pomocą programu ThreatIntel whitelist</span><span class="sxs-lookup"><span data-stu-id="5f32f-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="5f32f-116">W tym przykładzie przedstawiono tworzenie zasad zapory platformy Azure z zagrożeniem Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="5f32f-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

## <span data-ttu-id="5f32f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f32f-117">PARAMETERS</span></span>

### <span data-ttu-id="5f32f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f32f-118">-AsJob</span></span>
<span data-ttu-id="5f32f-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5f32f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f32f-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="5f32f-120">-BasePolicy</span></span>
<span data-ttu-id="5f32f-121">Zasady bazowe, których dziedziczenie</span><span class="sxs-lookup"><span data-stu-id="5f32f-121">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f32f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f32f-122">-DefaultProfile</span></span>
<span data-ttu-id="5f32f-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f32f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f32f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5f32f-124">-Force</span></span>
<span data-ttu-id="5f32f-125">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="5f32f-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5f32f-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5f32f-126">-Location</span></span>
<span data-ttu-id="5f32f-127">pozycję.</span><span class="sxs-lookup"><span data-stu-id="5f32f-127">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f32f-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5f32f-128">-Name</span></span>
<span data-ttu-id="5f32f-129">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5f32f-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f32f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f32f-130">-ResourceGroupName</span></span>
<span data-ttu-id="5f32f-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f32f-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f32f-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="5f32f-132">-Tag</span></span>
<span data-ttu-id="5f32f-133">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f32f-133">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f32f-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="5f32f-134">-ThreatIntelMode</span></span>
<span data-ttu-id="5f32f-135">Tryb pracy dla analizy zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="5f32f-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f32f-136">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="5f32f-136">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="5f32f-137">Whitelist dla analizy zagrożeń</span><span class="sxs-lookup"><span data-stu-id="5f32f-137">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f32f-138">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="5f32f-138">-DnsSetting</span></span>
<span data-ttu-id="5f32f-139">Ustawienie DNS</span><span class="sxs-lookup"><span data-stu-id="5f32f-139">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f32f-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f32f-140">-Confirm</span></span>
<span data-ttu-id="5f32f-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f32f-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f32f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f32f-142">-WhatIf</span></span>
<span data-ttu-id="5f32f-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f32f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f32f-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5f32f-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f32f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f32f-145">CommonParameters</span></span>
<span data-ttu-id="5f32f-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f32f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f32f-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f32f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f32f-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f32f-148">INPUTS</span></span>

### <span data-ttu-id="5f32f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5f32f-149">System.String</span></span>

### <span data-ttu-id="5f32f-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5f32f-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5f32f-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f32f-151">OUTPUTS</span></span>

### <span data-ttu-id="5f32f-152">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="5f32f-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="5f32f-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f32f-153">NOTES</span></span>

## <span data-ttu-id="5f32f-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f32f-154">RELATED LINKS</span></span>
