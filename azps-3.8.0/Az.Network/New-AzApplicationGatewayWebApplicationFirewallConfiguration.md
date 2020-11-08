---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 0f186de1ad548be0c566c6fac2b8d1505885bfe0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053727"
---
# <span data-ttu-id="a3af9-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3af9-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="a3af9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3af9-102">SYNOPSIS</span></span>
<span data-ttu-id="a3af9-103">Tworzy konfigurację WAF dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a3af9-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="a3af9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3af9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3af9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a3af9-105">DESCRIPTION</span></span>
<span data-ttu-id="a3af9-106">Polecenie cmdlet **New-AzApplicationGatewayWebApplicationFirewallConfiguration** umożliwia utworzenie konfiguracji zapory aplikacji sieci Web (WAF) dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a3af9-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="a3af9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3af9-107">EXAMPLES</span></span>

### <span data-ttu-id="a3af9-108">Przykład 1: Tworzenie konfiguracji zapory aplikacji sieci Web dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a3af9-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="a3af9-109">Pierwsze polecenie powoduje utworzenie nowej konfiguracji grupy reguł z wyłączonym dla grupy reguł o nazwie "REQUEST-942-APPLICATION-ataki-SQLI" z regułą 942130 oraz wyłączanie reguły 942140.</span><span class="sxs-lookup"><span data-stu-id="a3af9-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="a3af9-110">Drugie polecenie tworzy inną konfigurację grupy reguł z wyłączonymi dla grupy reguł o nazwie "REQUEST-921-PROTOCOL-ataki".</span><span class="sxs-lookup"><span data-stu-id="a3af9-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="a3af9-111">Żadne reguły nie są ściśle przekazywane, a więc wszystkie reguły grupy reguł zostaną wyłączone.</span><span class="sxs-lookup"><span data-stu-id="a3af9-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="a3af9-112">Następnie ostatnie polecenie tworzy konfigurację WAF z regułami zapory wyłączonymi zgodnie z konfiguracją w $disabledRuleGroup 1 i $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="a3af9-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="a3af9-113">Nowa konfiguracja WAF jest przechowywana w zmiennej $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="a3af9-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="a3af9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3af9-114">PARAMETERS</span></span>

### <span data-ttu-id="a3af9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3af9-115">-DefaultProfile</span></span>
<span data-ttu-id="a3af9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3af9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3af9-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="a3af9-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="a3af9-118">Wyłączone grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="a3af9-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="a3af9-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="a3af9-119">-Enabled</span></span>
<span data-ttu-id="a3af9-120">Wskazuje, czy WAF jest włączony.</span><span class="sxs-lookup"><span data-stu-id="a3af9-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="a3af9-121">-Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="a3af9-121">-Exclusion</span></span>
<span data-ttu-id="a3af9-122">Listy wykluczeń.</span><span class="sxs-lookup"><span data-stu-id="a3af9-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="a3af9-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="a3af9-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="a3af9-124">Maksymalny limit przekazywania plików w MB.</span><span class="sxs-lookup"><span data-stu-id="a3af9-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="a3af9-125">-Firewallmode</span><span class="sxs-lookup"><span data-stu-id="a3af9-125">-FirewallMode</span></span>
<span data-ttu-id="a3af9-126">Określa tryb zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a3af9-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="a3af9-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a3af9-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3af9-128">Wykrywanie</span><span class="sxs-lookup"><span data-stu-id="a3af9-128">Detection</span></span>
- <span data-ttu-id="a3af9-129">Ochrona przed</span><span class="sxs-lookup"><span data-stu-id="a3af9-129">Prevention</span></span>

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

### <span data-ttu-id="a3af9-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="a3af9-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="a3af9-131">Maksymalny rozmiar treści żądania w KB.</span><span class="sxs-lookup"><span data-stu-id="a3af9-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="a3af9-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="a3af9-132">-RequestBodyCheck</span></span>
<span data-ttu-id="a3af9-133">Czy treść żądania jest zaznaczona, czy nie.</span><span class="sxs-lookup"><span data-stu-id="a3af9-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="a3af9-134">-Zestaw reguł</span><span class="sxs-lookup"><span data-stu-id="a3af9-134">-RuleSetType</span></span>
<span data-ttu-id="a3af9-135">Typ zestawu reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a3af9-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="a3af9-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a3af9-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="a3af9-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="a3af9-137">OWASP</span></span>

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

### <span data-ttu-id="a3af9-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="a3af9-138">-RuleSetVersion</span></span>
<span data-ttu-id="a3af9-139">Wersja typu zestawu reguł.</span><span class="sxs-lookup"><span data-stu-id="a3af9-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="a3af9-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3af9-140">-Confirm</span></span>
<span data-ttu-id="a3af9-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3af9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3af9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3af9-142">-WhatIf</span></span>
<span data-ttu-id="a3af9-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3af9-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3af9-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3af9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3af9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3af9-145">CommonParameters</span></span>
<span data-ttu-id="a3af9-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3af9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3af9-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3af9-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3af9-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3af9-148">INPUTS</span></span>

### <span data-ttu-id="a3af9-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a3af9-149">None</span></span>

## <span data-ttu-id="a3af9-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3af9-150">OUTPUTS</span></span>

### <span data-ttu-id="a3af9-151">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3af9-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="a3af9-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3af9-152">NOTES</span></span>

## <span data-ttu-id="a3af9-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3af9-153">RELATED LINKS</span></span>

[<span data-ttu-id="a3af9-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3af9-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="a3af9-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3af9-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


