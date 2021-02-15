---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189507"
---
# <span data-ttu-id="3564a-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3564a-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="3564a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3564a-102">SYNOPSIS</span></span>
<span data-ttu-id="3564a-103">Zapisuje zmodyfikowane zasady zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3564a-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="3564a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3564a-104">SYNTAX</span></span>

### <span data-ttu-id="3564a-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="3564a-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3564a-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3564a-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3564a-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3564a-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3564a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="3564a-108">DESCRIPTION</span></span>
<span data-ttu-id="3564a-109">Polecenie **cmdlet Set-AzFirewallPolicy** aktualizuje zasady zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3564a-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="3564a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3564a-110">EXAMPLES</span></span>

### <span data-ttu-id="3564a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3564a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="3564a-112">W tym przykładzie dla zasad zapory jest ustawiana nowa wartość zasad zapory</span><span class="sxs-lookup"><span data-stu-id="3564a-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="3564a-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3564a-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="3564a-114">W tym przykładzie zasady zapory są ustawiane przy użyciu nowego trybu analizy zagrożeń</span><span class="sxs-lookup"><span data-stu-id="3564a-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="3564a-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3564a-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="3564a-116">W tym przykładzie zasady zapory są ustawiane przy użyciu nowej białej listy zagrożeń firmy Intel</span><span class="sxs-lookup"><span data-stu-id="3564a-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="3564a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3564a-117">PARAMETERS</span></span>

### <span data-ttu-id="3564a-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3564a-118">-AsJob</span></span>
<span data-ttu-id="3564a-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3564a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3564a-120">— BasePolicy</span><span class="sxs-lookup"><span data-stu-id="3564a-120">-BasePolicy</span></span>
<span data-ttu-id="3564a-121">Zasady podstawowe, po których mają być dziedziczone</span><span class="sxs-lookup"><span data-stu-id="3564a-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="3564a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3564a-122">-DefaultProfile</span></span>
<span data-ttu-id="3564a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3564a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3564a-124">- DnsSetting</span><span class="sxs-lookup"><span data-stu-id="3564a-124">-DnsSetting</span></span>
<span data-ttu-id="3564a-125">Ustawienie DNS</span><span class="sxs-lookup"><span data-stu-id="3564a-125">The DNS Setting</span></span>

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

### <span data-ttu-id="3564a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3564a-126">-InputObject</span></span>
<span data-ttu-id="3564a-127">Zasady AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3564a-127">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="3564a-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3564a-128">-Location</span></span>
<span data-ttu-id="3564a-129">.</span><span class="sxs-lookup"><span data-stu-id="3564a-129">location.</span></span>

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

### <span data-ttu-id="3564a-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3564a-130">-Name</span></span>
<span data-ttu-id="3564a-131">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="3564a-131">The resource name.</span></span>

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

### <span data-ttu-id="3564a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3564a-132">-ResourceGroupName</span></span>
<span data-ttu-id="3564a-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3564a-133">The resource group name.</span></span>

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

### <span data-ttu-id="3564a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3564a-134">-ResourceId</span></span>
<span data-ttu-id="3564a-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="3564a-135">The resource Id.</span></span>

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

### <span data-ttu-id="3564a-136">— Tag</span><span class="sxs-lookup"><span data-stu-id="3564a-136">-Tag</span></span>
<span data-ttu-id="3564a-137">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="3564a-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3564a-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="3564a-138">-ThreatIntelMode</span></span>
<span data-ttu-id="3564a-139">Tryb działania analizy zagrożeń.</span><span class="sxs-lookup"><span data-stu-id="3564a-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="3564a-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="3564a-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="3564a-141">Lista na liście na temat analizy zagrożeń</span><span class="sxs-lookup"><span data-stu-id="3564a-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="3564a-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3564a-142">-Confirm</span></span>
<span data-ttu-id="3564a-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3564a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3564a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3564a-144">-WhatIf</span></span>
<span data-ttu-id="3564a-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3564a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3564a-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3564a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3564a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3564a-147">CommonParameters</span></span>
<span data-ttu-id="3564a-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3564a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3564a-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3564a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3564a-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3564a-150">INPUTS</span></span>

### <span data-ttu-id="3564a-151">System.String</span><span class="sxs-lookup"><span data-stu-id="3564a-151">System.String</span></span>

### <span data-ttu-id="3564a-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3564a-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="3564a-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3564a-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3564a-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3564a-154">OUTPUTS</span></span>

### <span data-ttu-id="3564a-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3564a-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="3564a-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3564a-156">NOTES</span></span>

## <span data-ttu-id="3564a-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3564a-157">RELATED LINKS</span></span>
