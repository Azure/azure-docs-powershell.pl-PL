---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339922"
---
# <span data-ttu-id="e1bf0-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e1bf0-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="e1bf0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bf0-103">Zapisuje zmodyfikowane zasady zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e1bf0-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="e1bf0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1bf0-104">SYNTAX</span></span>

### <span data-ttu-id="e1bf0-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e1bf0-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1bf0-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1bf0-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1bf0-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1bf0-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1bf0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e1bf0-108">DESCRIPTION</span></span>
<span data-ttu-id="e1bf0-109">Polecenie cmdlet **Set-AzFirewallPolicy** aktualizuje zasady zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="e1bf0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1bf0-110">EXAMPLES</span></span>

### <span data-ttu-id="e1bf0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e1bf0-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="e1bf0-112">W tym przykładzie ustawiono zasadę zapory z nową wartością zasad zapory</span><span class="sxs-lookup"><span data-stu-id="e1bf0-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="e1bf0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e1bf0-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="e1bf0-114">W tym przykładzie ustawiono zasady zapory przy użyciu nowego trybu zagrożenia dla procesorów firmy Intel</span><span class="sxs-lookup"><span data-stu-id="e1bf0-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="e1bf0-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e1bf0-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="e1bf0-116">W tym przykładzie ustawiono zasady zapory przy użyciu nowego zagrożenia Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="e1bf0-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="e1bf0-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1bf0-117">PARAMETERS</span></span>

### <span data-ttu-id="e1bf0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1bf0-118">-AsJob</span></span>
<span data-ttu-id="e1bf0-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e1bf0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1bf0-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="e1bf0-120">-BasePolicy</span></span>
<span data-ttu-id="e1bf0-121">Zasady bazowe, których dziedziczenie</span><span class="sxs-lookup"><span data-stu-id="e1bf0-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="e1bf0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bf0-122">-DefaultProfile</span></span>
<span data-ttu-id="e1bf0-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1bf0-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="e1bf0-124">-DnsSetting</span></span>
<span data-ttu-id="e1bf0-125">Ustawienie DNS</span><span class="sxs-lookup"><span data-stu-id="e1bf0-125">The DNS Setting</span></span>

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

### <span data-ttu-id="e1bf0-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e1bf0-126">-InputObject</span></span>
<span data-ttu-id="e1bf0-127">Zasady AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e1bf0-127">The AzureFirewall Policy</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bf0-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e1bf0-128">-Location</span></span>
<span data-ttu-id="e1bf0-129">pozycję.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-129">location.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bf0-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1bf0-130">-Name</span></span>
<span data-ttu-id="e1bf0-131">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-131">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bf0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1bf0-132">-ResourceGroupName</span></span>
<span data-ttu-id="e1bf0-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-133">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bf0-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1bf0-134">-ResourceId</span></span>
<span data-ttu-id="e1bf0-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-135">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bf0-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="e1bf0-136">-Tag</span></span>
<span data-ttu-id="e1bf0-137">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e1bf0-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="e1bf0-138">-ThreatIntelMode</span></span>
<span data-ttu-id="e1bf0-139">Tryb pracy dla analizy zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="e1bf0-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="e1bf0-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="e1bf0-141">Whitelist dla analizy zagrożeń</span><span class="sxs-lookup"><span data-stu-id="e1bf0-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="e1bf0-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1bf0-142">-Confirm</span></span>
<span data-ttu-id="e1bf0-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1bf0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1bf0-144">-WhatIf</span></span>
<span data-ttu-id="e1bf0-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1bf0-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1bf0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bf0-147">CommonParameters</span></span>
<span data-ttu-id="e1bf0-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1bf0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bf0-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1bf0-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bf0-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1bf0-150">INPUTS</span></span>

### <span data-ttu-id="e1bf0-151">System. String</span><span class="sxs-lookup"><span data-stu-id="e1bf0-151">System.String</span></span>

### <span data-ttu-id="e1bf0-152">Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e1bf0-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="e1bf0-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e1bf0-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e1bf0-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1bf0-154">OUTPUTS</span></span>

### <span data-ttu-id="e1bf0-155">Microsoft. Azure. Commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e1bf0-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="e1bf0-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1bf0-156">NOTES</span></span>

## <span data-ttu-id="e1bf0-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1bf0-157">RELATED LINKS</span></span>
