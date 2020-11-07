---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: bdfd9cb100b43f58326b9b94c4e15bb24561eadd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890529"
---
# <span data-ttu-id="d0106-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0106-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="d0106-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0106-102">SYNOPSIS</span></span>
<span data-ttu-id="d0106-103">Tworzy konfigurację WAF dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d0106-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="d0106-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0106-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0106-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0106-105">DESCRIPTION</span></span>
<span data-ttu-id="d0106-106">Polecenie cmdlet **New-AzApplicationGatewayWebApplicationFirewallConfiguration** umożliwia utworzenie konfiguracji zapory aplikacji sieci Web (WAF) dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0106-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="d0106-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0106-107">EXAMPLES</span></span>

### <span data-ttu-id="d0106-108">Przykład 1: Tworzenie konfiguracji zapory aplikacji sieci Web dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="d0106-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="d0106-109">Pierwsze polecenie powoduje utworzenie nowej konfiguracji grupy reguł z wyłączonym dla grupy reguł o nazwie "REQUEST-942-APPLICATION-ataki-SQLI" z regułą 942130 oraz wyłączanie reguły 942140.</span><span class="sxs-lookup"><span data-stu-id="d0106-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="d0106-110">Drugie polecenie tworzy inną konfigurację grupy reguł z wyłączonymi dla grupy reguł o nazwie "REQUEST-921-PROTOCOL-ataki".</span><span class="sxs-lookup"><span data-stu-id="d0106-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="d0106-111">Żadne reguły nie są ściśle przekazywane, a więc wszystkie reguły grupy reguł zostaną wyłączone.</span><span class="sxs-lookup"><span data-stu-id="d0106-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="d0106-112">Następnie ostatnie polecenie tworzy konfigurację WAF z regułami zapory wyłączonymi zgodnie z konfiguracją w $disabledRuleGroup 1 i $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="d0106-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="d0106-113">Nowa konfiguracja WAF jest przechowywana w zmiennej $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="d0106-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="d0106-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0106-114">PARAMETERS</span></span>

### <span data-ttu-id="d0106-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0106-115">-DefaultProfile</span></span>
<span data-ttu-id="d0106-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0106-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0106-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="d0106-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="d0106-118">Wyłączone grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="d0106-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="d0106-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="d0106-119">-Enabled</span></span>
<span data-ttu-id="d0106-120">Wskazuje, czy WAF jest włączony.</span><span class="sxs-lookup"><span data-stu-id="d0106-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0106-121">-Firewallmode</span><span class="sxs-lookup"><span data-stu-id="d0106-121">-FirewallMode</span></span>
<span data-ttu-id="d0106-122">Określa tryb zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d0106-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="d0106-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d0106-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d0106-124">Wykrywanie</span><span class="sxs-lookup"><span data-stu-id="d0106-124">Detection</span></span>
- <span data-ttu-id="d0106-125">Ochrona przed</span><span class="sxs-lookup"><span data-stu-id="d0106-125">Prevention</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0106-126">-Zestaw reguł</span><span class="sxs-lookup"><span data-stu-id="d0106-126">-RuleSetType</span></span>
<span data-ttu-id="d0106-127">Typ zestawu reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d0106-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="d0106-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d0106-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="d0106-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="d0106-129">OWASP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0106-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="d0106-130">-RuleSetVersion</span></span>
<span data-ttu-id="d0106-131">Wersja typu zestawu reguł.</span><span class="sxs-lookup"><span data-stu-id="d0106-131">The version of the rule set type.</span></span>
<span data-ttu-id="d0106-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d0106-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="d0106-133">3,0</span><span class="sxs-lookup"><span data-stu-id="d0106-133">3.0</span></span>
- <span data-ttu-id="d0106-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="d0106-134">2.2.9</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0106-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0106-135">-Confirm</span></span>
<span data-ttu-id="d0106-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0106-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0106-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0106-137">-WhatIf</span></span>
<span data-ttu-id="d0106-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0106-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0106-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d0106-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0106-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0106-140">CommonParameters</span></span>
<span data-ttu-id="d0106-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0106-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0106-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0106-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0106-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0106-143">INPUTS</span></span>

## <span data-ttu-id="d0106-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0106-144">OUTPUTS</span></span>

### <span data-ttu-id="d0106-145">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0106-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="d0106-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0106-146">NOTES</span></span>

## <span data-ttu-id="d0106-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0106-147">RELATED LINKS</span></span>

[<span data-ttu-id="d0106-148">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0106-148">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="d0106-149">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0106-149">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


