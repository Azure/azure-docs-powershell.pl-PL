---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 281a4a0d935d73777f7fdd693f3d32982b2da47a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544687"
---
# <span data-ttu-id="da951-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="da951-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="da951-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da951-102">SYNOPSIS</span></span>
<span data-ttu-id="da951-103">Tworzy konfigurację WAF dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="da951-103">Creates a WAF configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da951-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da951-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da951-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da951-105">DESCRIPTION</span></span>
<span data-ttu-id="da951-106">Polecenie cmdlet **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** umożliwia utworzenie konfiguracji zapory aplikacji sieci Web (WAF) dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="da951-106">The **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="da951-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da951-107">EXAMPLES</span></span>

### <span data-ttu-id="da951-108">Przykład 1: Tworzenie konfiguracji zapory aplikacji sieci Web dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="da951-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="da951-109">Pierwsze polecenie powoduje utworzenie nowej konfiguracji grupy reguł z wyłączonym dla grupy reguł o nazwie "REQUEST-942-APPLICATION-ataki-SQLI" z regułą 942130 oraz wyłączanie reguły 942140.</span><span class="sxs-lookup"><span data-stu-id="da951-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="da951-110">Drugie polecenie tworzy inną konfigurację grupy reguł z wyłączonymi dla grupy reguł o nazwie "REQUEST-921-PROTOCOL-ataki".</span><span class="sxs-lookup"><span data-stu-id="da951-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="da951-111">Żadne reguły nie są ściśle przekazywane, a więc wszystkie reguły grupy reguł zostaną wyłączone.</span><span class="sxs-lookup"><span data-stu-id="da951-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="da951-112">Następnie ostatnie polecenie tworzy konfigurację WAF z regułami zapory wyłączonymi zgodnie z konfiguracją w $disabledRuleGroup 1 i $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="da951-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="da951-113">Nowa konfiguracja WAF jest przechowywana w zmiennej $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="da951-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="da951-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da951-114">PARAMETERS</span></span>

### <span data-ttu-id="da951-115">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="da951-115">-DisabledRuleGroups</span></span>
<span data-ttu-id="da951-116">Wyłączone grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="da951-116">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da951-117">-Enabled</span><span class="sxs-lookup"><span data-stu-id="da951-117">-Enabled</span></span>
<span data-ttu-id="da951-118">Wskazuje, czy WAF jest włączony.</span><span class="sxs-lookup"><span data-stu-id="da951-118">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="da951-119">-Firewallmode</span><span class="sxs-lookup"><span data-stu-id="da951-119">-FirewallMode</span></span>
<span data-ttu-id="da951-120">Określa tryb zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="da951-120">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="da951-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="da951-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="da951-122">Wykrywanie</span><span class="sxs-lookup"><span data-stu-id="da951-122">Detection</span></span>
- <span data-ttu-id="da951-123">Ochrona przed</span><span class="sxs-lookup"><span data-stu-id="da951-123">Prevention</span></span>

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

### <span data-ttu-id="da951-124">-Zestaw reguł</span><span class="sxs-lookup"><span data-stu-id="da951-124">-RuleSetType</span></span>
<span data-ttu-id="da951-125">Typ zestawu reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="da951-125">The type of the web application firewall rule set.</span></span> <span data-ttu-id="da951-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="da951-126">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="da951-127">OWASP</span><span class="sxs-lookup"><span data-stu-id="da951-127">OWASP</span></span>

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

### <span data-ttu-id="da951-128">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="da951-128">-RuleSetVersion</span></span>
<span data-ttu-id="da951-129">Wersja typu zestawu reguł.</span><span class="sxs-lookup"><span data-stu-id="da951-129">The version of the rule set type.</span></span>
<span data-ttu-id="da951-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="da951-130">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="da951-131">3,0</span><span class="sxs-lookup"><span data-stu-id="da951-131">3.0</span></span>
- <span data-ttu-id="da951-132">2.2.9</span><span class="sxs-lookup"><span data-stu-id="da951-132">2.2.9</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da951-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da951-133">-Confirm</span></span>
<span data-ttu-id="da951-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da951-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da951-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da951-135">-WhatIf</span></span>
<span data-ttu-id="da951-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da951-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da951-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da951-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da951-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da951-138">-DefaultProfile</span></span>
<span data-ttu-id="da951-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da951-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da951-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da951-140">CommonParameters</span></span>
<span data-ttu-id="da951-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da951-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da951-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da951-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da951-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da951-143">INPUTS</span></span>

## <span data-ttu-id="da951-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da951-144">OUTPUTS</span></span>

### <span data-ttu-id="da951-145">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="da951-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="da951-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da951-146">NOTES</span></span>

## <span data-ttu-id="da951-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da951-147">RELATED LINKS</span></span>

[<span data-ttu-id="da951-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="da951-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="da951-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="da951-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


