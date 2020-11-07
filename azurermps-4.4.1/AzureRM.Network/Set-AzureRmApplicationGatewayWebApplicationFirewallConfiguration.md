---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 03acee0ee1e15ffe0be605753d166ff4a956c274
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718733"
---
# <span data-ttu-id="e4f21-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4f21-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="e4f21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4f21-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f21-103">Modyfikuje konfigurację WAF bramy Application.</span><span class="sxs-lookup"><span data-stu-id="e4f21-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4f21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4f21-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4f21-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4f21-105">DESCRIPTION</span></span>
<span data-ttu-id="e4f21-106">Polecenie cmdlet **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** modyfikuje konfigurację zapory aplikacji sieci Web (WAF) bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e4f21-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="e4f21-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4f21-107">EXAMPLES</span></span>

### <span data-ttu-id="e4f21-108">Przykład 1: aktualizowanie konfiguracji zapory aplikacji sieci Web bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e4f21-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="e4f21-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01, a następnie zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e4f21-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e4f21-110">Drugie polecenie włącza konfigurację zapory dla bramy aplikacji przechowywaną w $AppGw i ustawia tryb zapory na "wykrywanie", zestaw reguł na wartość "OWASP" i RuleSetVersion na "3,0".</span><span class="sxs-lookup"><span data-stu-id="e4f21-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="e4f21-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4f21-111">PARAMETERS</span></span>

### <span data-ttu-id="e4f21-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4f21-112">-ApplicationGateway</span></span>
<span data-ttu-id="e4f21-113">Określa obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e4f21-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="e4f21-114">Możesz użyć polecenia cmdlet Get-AzureRmApplicationGateway, aby uzyskać obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e4f21-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f21-115">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="e4f21-115">-DisabledRuleGroups</span></span>
<span data-ttu-id="e4f21-116">Wyłączone grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="e4f21-116">The disabled rule groups.</span></span>

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

### <span data-ttu-id="e4f21-117">-Enabled</span><span class="sxs-lookup"><span data-stu-id="e4f21-117">-Enabled</span></span>
<span data-ttu-id="e4f21-118">Wskazuje, czy jest włączona Zapora aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e4f21-118">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="e4f21-119">-Firewallmode</span><span class="sxs-lookup"><span data-stu-id="e4f21-119">-FirewallMode</span></span>
<span data-ttu-id="e4f21-120">Określa tryb zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e4f21-120">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="e4f21-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e4f21-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e4f21-122">Wykrywanie</span><span class="sxs-lookup"><span data-stu-id="e4f21-122">Detection</span></span>
- <span data-ttu-id="e4f21-123">Ochrona przed</span><span class="sxs-lookup"><span data-stu-id="e4f21-123">Prevention</span></span>

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

### <span data-ttu-id="e4f21-124">-Zestaw reguł</span><span class="sxs-lookup"><span data-stu-id="e4f21-124">-RuleSetType</span></span>
<span data-ttu-id="e4f21-125">Typ zestawu reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e4f21-125">The type of the web application firewall rule set.</span></span> <span data-ttu-id="e4f21-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e4f21-126">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="e4f21-127">OWASP</span><span class="sxs-lookup"><span data-stu-id="e4f21-127">OWASP</span></span>

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

### <span data-ttu-id="e4f21-128">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="e4f21-128">-RuleSetVersion</span></span>
<span data-ttu-id="e4f21-129">Wersja typu zestawu reguł.</span><span class="sxs-lookup"><span data-stu-id="e4f21-129">The version of the rule set type.</span></span>
<span data-ttu-id="e4f21-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e4f21-130">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="e4f21-131">3,0</span><span class="sxs-lookup"><span data-stu-id="e4f21-131">3.0</span></span>
- <span data-ttu-id="e4f21-132">2.2.9</span><span class="sxs-lookup"><span data-stu-id="e4f21-132">2.2.9</span></span>

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

### <span data-ttu-id="e4f21-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4f21-133">-Confirm</span></span>
<span data-ttu-id="e4f21-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4f21-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4f21-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4f21-135">-WhatIf</span></span>
<span data-ttu-id="e4f21-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4f21-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4f21-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4f21-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4f21-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f21-138">-DefaultProfile</span></span>
<span data-ttu-id="e4f21-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4f21-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4f21-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f21-140">CommonParameters</span></span>
<span data-ttu-id="e4f21-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4f21-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f21-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4f21-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f21-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4f21-143">INPUTS</span></span>

### <span data-ttu-id="e4f21-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4f21-144">PSApplicationGateway</span></span>
<span data-ttu-id="e4f21-145">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="e4f21-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="e4f21-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4f21-146">OUTPUTS</span></span>

### <span data-ttu-id="e4f21-147">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4f21-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e4f21-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4f21-148">NOTES</span></span>

## <span data-ttu-id="e4f21-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4f21-149">RELATED LINKS</span></span>

[<span data-ttu-id="e4f21-150">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4f21-150">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="e4f21-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4f21-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="e4f21-152">Nowe — AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4f21-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


