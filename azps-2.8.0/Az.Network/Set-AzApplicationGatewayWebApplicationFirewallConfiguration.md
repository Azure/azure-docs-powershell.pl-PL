---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9481580e482c709c17b3a1acf36be765ca45e444
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869583"
---
# <span data-ttu-id="e6a6b-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6a6b-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="e6a6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a6b-103">Modyfikuje konfigurację WAF bramy Application.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="e6a6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6a6b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6a6b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e6a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="e6a6b-106">Polecenie cmdlet **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** modyfikuje konfigurację zapory aplikacji sieci Web (WAF) bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="e6a6b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="e6a6b-108">Przykład 1: aktualizowanie konfiguracji zapory aplikacji sieci Web bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e6a6b-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="e6a6b-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01, a następnie zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e6a6b-110">Drugie polecenie włącza konfigurację zapory dla bramy aplikacji przechowywaną w $AppGw i ustawia tryb zapory na "wykrywanie", zestaw reguł na wartość "OWASP" i RuleSetVersion na "3,0".</span><span class="sxs-lookup"><span data-stu-id="e6a6b-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="e6a6b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6a6b-111">PARAMETERS</span></span>

### <span data-ttu-id="e6a6b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6a6b-112">-ApplicationGateway</span></span>
<span data-ttu-id="e6a6b-113">Określa obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="e6a6b-114">Możesz użyć polecenia cmdlet Get-AzApplicationGateway, aby uzyskać obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="e6a6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a6b-115">-DefaultProfile</span></span>
<span data-ttu-id="e6a6b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6a6b-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="e6a6b-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="e6a6b-118">Wyłączone grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="e6a6b-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="e6a6b-119">-Enabled</span></span>
<span data-ttu-id="e6a6b-120">Wskazuje, czy jest włączona Zapora aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="e6a6b-121">-Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="e6a6b-121">-Exclusion</span></span>
<span data-ttu-id="e6a6b-122">Listy wykluczeń.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="e6a6b-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="e6a6b-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="e6a6b-124">Maksymalny limit przekazywania plików w MB.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="e6a6b-125">-Firewallmode</span><span class="sxs-lookup"><span data-stu-id="e6a6b-125">-FirewallMode</span></span>
<span data-ttu-id="e6a6b-126">Określa tryb zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="e6a6b-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e6a6b-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e6a6b-128">Wykrywanie</span><span class="sxs-lookup"><span data-stu-id="e6a6b-128">Detection</span></span>
- <span data-ttu-id="e6a6b-129">Ochrona przed</span><span class="sxs-lookup"><span data-stu-id="e6a6b-129">Prevention</span></span>

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

### <span data-ttu-id="e6a6b-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="e6a6b-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="e6a6b-131">Maksymalny rozmiar treści żądania w KB.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="e6a6b-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="e6a6b-132">-RequestBodyCheck</span></span>
<span data-ttu-id="e6a6b-133">Czy treść żądania jest zaznaczona, czy nie.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="e6a6b-134">-Zestaw reguł</span><span class="sxs-lookup"><span data-stu-id="e6a6b-134">-RuleSetType</span></span>
<span data-ttu-id="e6a6b-135">Typ zestawu reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="e6a6b-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e6a6b-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="e6a6b-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="e6a6b-137">OWASP</span></span>

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

### <span data-ttu-id="e6a6b-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="e6a6b-138">-RuleSetVersion</span></span>
<span data-ttu-id="e6a6b-139">Wersja typu zestawu reguł.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="e6a6b-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6a6b-140">-Confirm</span></span>
<span data-ttu-id="e6a6b-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6a6b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6a6b-142">-WhatIf</span></span>
<span data-ttu-id="e6a6b-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6a6b-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6a6b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a6b-145">CommonParameters</span></span>
<span data-ttu-id="e6a6b-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a6b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a6b-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6a6b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a6b-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6a6b-148">INPUTS</span></span>

### <span data-ttu-id="e6a6b-149">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6a6b-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e6a6b-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6a6b-150">OUTPUTS</span></span>

### <span data-ttu-id="e6a6b-151">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6a6b-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e6a6b-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6a6b-152">NOTES</span></span>

## <span data-ttu-id="e6a6b-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6a6b-153">RELATED LINKS</span></span>

[<span data-ttu-id="e6a6b-154">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e6a6b-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="e6a6b-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6a6b-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="e6a6b-156">Nowe — AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6a6b-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


