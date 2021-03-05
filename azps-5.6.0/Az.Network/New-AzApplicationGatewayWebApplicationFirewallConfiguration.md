---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 7d13febefe06ed1c290a0f95cbfda39dea353426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977921"
---
# <span data-ttu-id="8e823-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e823-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="8e823-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e823-102">SYNOPSIS</span></span>
<span data-ttu-id="8e823-103">Tworzy konfigurację aplikacji WAF dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8e823-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="8e823-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8e823-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e823-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8e823-105">DESCRIPTION</span></span>
<span data-ttu-id="8e823-106">Polecenie **cmdlet New-AzApplicationGatewayWebApplicationFirewallConfiguration** tworzy konfigurację zapory aplikacji sieci Web (WAF) dla bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="8e823-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="8e823-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8e823-107">EXAMPLES</span></span>

### <span data-ttu-id="8e823-108">Przykład 1. Tworzenie konfiguracji zapory aplikacji sieci Web dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="8e823-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="8e823-109">Pierwsze polecenie tworzy nową konfigurację wyłączonej grupy reguł dla grupy reguł o nazwie "REQUEST-942-APPLICATION-ATTACK-SQLI" z regułą 942130 i regułą 942140, która jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="8e823-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="8e823-110">Drugie polecenie tworzy kolejną wyłączono konfigurację grupy reguł dla grupy reguł o nazwie "REQUEST-921-PROTOCOL-ATTACK".</span><span class="sxs-lookup"><span data-stu-id="8e823-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="8e823-111">Nie są przekazywane żadne reguły, dlatego wszystkie reguły grupy reguł zostaną wyłączone.</span><span class="sxs-lookup"><span data-stu-id="8e823-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="8e823-112">Ostatnie polecenie utworzy konfigurację aplikacji WAF z wyłączonymi regułami zapory skonfigurowanymi w $disabledRuleGroup 1 i $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="8e823-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="8e823-113">Nowa konfiguracja aplikacji SAF jest przechowywana w $firewallConfig sieci.</span><span class="sxs-lookup"><span data-stu-id="8e823-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="8e823-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e823-114">PARAMETERS</span></span>

### <span data-ttu-id="8e823-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e823-115">-DefaultProfile</span></span>
<span data-ttu-id="8e823-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e823-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e823-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="8e823-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="8e823-118">Wyłączone grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="8e823-118">The disabled rule groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup[]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e823-119">— włączone</span><span class="sxs-lookup"><span data-stu-id="8e823-119">-Enabled</span></span>
<span data-ttu-id="8e823-120">Wskazuje, czy sieć WAF jest włączona.</span><span class="sxs-lookup"><span data-stu-id="8e823-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e823-121">— Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="8e823-121">-Exclusion</span></span>
<span data-ttu-id="8e823-122">Listy wykluczeń.</span><span class="sxs-lookup"><span data-stu-id="8e823-122">The exclusion lists.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e823-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="8e823-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="8e823-124">Maksymalny limit przekazywania plików w MB.</span><span class="sxs-lookup"><span data-stu-id="8e823-124">Max file upload limit in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e823-125">- FirewallMode</span><span class="sxs-lookup"><span data-stu-id="8e823-125">-FirewallMode</span></span>
<span data-ttu-id="8e823-126">Określa tryb zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="8e823-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="8e823-127">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8e823-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e823-128">Wykrywanie</span><span class="sxs-lookup"><span data-stu-id="8e823-128">Detection</span></span>
- <span data-ttu-id="8e823-129">Zapobieganie</span><span class="sxs-lookup"><span data-stu-id="8e823-129">Prevention</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e823-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="8e823-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="8e823-131">Maksymalny rozmiar treści żądania w KB.</span><span class="sxs-lookup"><span data-stu-id="8e823-131">Max request body size in KB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e823-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="8e823-132">-RequestBodyCheck</span></span>
<span data-ttu-id="8e823-133">Czy zaznaczono treść żądania, czy nie.</span><span class="sxs-lookup"><span data-stu-id="8e823-133">Whether request body is checked or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e823-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="8e823-134">-RuleSetType</span></span>
<span data-ttu-id="8e823-135">Typ zestawu reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="8e823-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="8e823-136">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8e823-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="8e823-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="8e823-137">OWASP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e823-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="8e823-138">-RuleSetVersion</span></span>
<span data-ttu-id="8e823-139">Wersja typu zestawu reguł.</span><span class="sxs-lookup"><span data-stu-id="8e823-139">The version of the rule set type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e823-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e823-140">-Confirm</span></span>
<span data-ttu-id="8e823-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8e823-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e823-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e823-142">-WhatIf</span></span>
<span data-ttu-id="8e823-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e823-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e823-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8e823-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e823-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e823-145">CommonParameters</span></span>
<span data-ttu-id="8e823-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e823-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e823-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e823-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e823-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e823-148">INPUTS</span></span>

### <span data-ttu-id="8e823-149">Brak</span><span class="sxs-lookup"><span data-stu-id="8e823-149">None</span></span>

## <span data-ttu-id="8e823-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e823-150">OUTPUTS</span></span>

### <span data-ttu-id="8e823-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e823-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="8e823-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8e823-152">NOTES</span></span>

## <span data-ttu-id="8e823-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e823-153">RELATED LINKS</span></span>

[<span data-ttu-id="8e823-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e823-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="8e823-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e823-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


