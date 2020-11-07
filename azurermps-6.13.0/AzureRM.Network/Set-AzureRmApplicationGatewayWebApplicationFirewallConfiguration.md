---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 3b2de5d139c8addb448ac76609e13becf2e0153c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710927"
---
# <span data-ttu-id="62a1e-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="62a1e-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="62a1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="62a1e-103">Modyfikuje konfigurację WAF bramy Application.</span><span class="sxs-lookup"><span data-stu-id="62a1e-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62a1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62a1e-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-RequestBodyCheck <Boolean>] [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62a1e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="62a1e-105">DESCRIPTION</span></span>
<span data-ttu-id="62a1e-106">Polecenie cmdlet **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** modyfikuje konfigurację zapory aplikacji sieci Web (WAF) bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="62a1e-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="62a1e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62a1e-107">EXAMPLES</span></span>

### <span data-ttu-id="62a1e-108">Przykład 1: aktualizowanie konfiguracji zapory aplikacji sieci Web bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="62a1e-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="62a1e-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01, a następnie zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="62a1e-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="62a1e-110">Drugie polecenie włącza konfigurację zapory dla bramy aplikacji przechowywaną w $AppGw i ustawia tryb zapory na "wykrywanie", zestaw reguł na wartość "OWASP" i RuleSetVersion na "3,0".</span><span class="sxs-lookup"><span data-stu-id="62a1e-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="62a1e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62a1e-111">PARAMETERS</span></span>

### <span data-ttu-id="62a1e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62a1e-112">-ApplicationGateway</span></span>
<span data-ttu-id="62a1e-113">Określa obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="62a1e-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="62a1e-114">Możesz użyć polecenia cmdlet Get-AzureRmApplicationGateway, aby uzyskać obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="62a1e-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="62a1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a1e-115">-DefaultProfile</span></span>
<span data-ttu-id="62a1e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="62a1e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62a1e-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="62a1e-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="62a1e-118">Wyłączone grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="62a1e-118">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a1e-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="62a1e-119">-Enabled</span></span>
<span data-ttu-id="62a1e-120">Wskazuje, czy jest włączona Zapora aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="62a1e-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="62a1e-121">-Wykluczenie</span><span class="sxs-lookup"><span data-stu-id="62a1e-121">-Exclusion</span></span>
<span data-ttu-id="62a1e-122">Listy wykluczeń.</span><span class="sxs-lookup"><span data-stu-id="62a1e-122">The exclusion lists.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a1e-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="62a1e-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="62a1e-124">Maksymalny limit przekazywania plików w MB.</span><span class="sxs-lookup"><span data-stu-id="62a1e-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="62a1e-125">-Firewallmode</span><span class="sxs-lookup"><span data-stu-id="62a1e-125">-FirewallMode</span></span>
<span data-ttu-id="62a1e-126">Określa tryb zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="62a1e-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="62a1e-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="62a1e-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62a1e-128">Wykrywanie</span><span class="sxs-lookup"><span data-stu-id="62a1e-128">Detection</span></span>
- <span data-ttu-id="62a1e-129">Ochrona przed</span><span class="sxs-lookup"><span data-stu-id="62a1e-129">Prevention</span></span>

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

### <span data-ttu-id="62a1e-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="62a1e-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="62a1e-131">Maksymalny rozmiar treści żądania w KB.</span><span class="sxs-lookup"><span data-stu-id="62a1e-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="62a1e-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="62a1e-132">-RequestBodyCheck</span></span>
<span data-ttu-id="62a1e-133">Czy treść żądania jest zaznaczona, czy nie.</span><span class="sxs-lookup"><span data-stu-id="62a1e-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="62a1e-134">-Zestaw reguł</span><span class="sxs-lookup"><span data-stu-id="62a1e-134">-RuleSetType</span></span>
<span data-ttu-id="62a1e-135">Typ zestawu reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="62a1e-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="62a1e-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="62a1e-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="62a1e-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="62a1e-137">OWASP</span></span>

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

### <span data-ttu-id="62a1e-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="62a1e-138">-RuleSetVersion</span></span>
<span data-ttu-id="62a1e-139">Wersja typu zestawu reguł.</span><span class="sxs-lookup"><span data-stu-id="62a1e-139">The version of the rule set type.</span></span>
<span data-ttu-id="62a1e-140">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="62a1e-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="62a1e-141">3,0</span><span class="sxs-lookup"><span data-stu-id="62a1e-141">3.0</span></span>
- <span data-ttu-id="62a1e-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="62a1e-142">2.2.9</span></span>

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

### <span data-ttu-id="62a1e-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62a1e-143">-Confirm</span></span>
<span data-ttu-id="62a1e-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62a1e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62a1e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62a1e-145">-WhatIf</span></span>
<span data-ttu-id="62a1e-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62a1e-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62a1e-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="62a1e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62a1e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a1e-148">CommonParameters</span></span>
<span data-ttu-id="62a1e-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62a1e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a1e-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62a1e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a1e-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62a1e-151">INPUTS</span></span>

### <span data-ttu-id="62a1e-152">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62a1e-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="62a1e-153">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="62a1e-153">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="62a1e-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62a1e-154">OUTPUTS</span></span>

### <span data-ttu-id="62a1e-155">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62a1e-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="62a1e-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62a1e-156">NOTES</span></span>

## <span data-ttu-id="62a1e-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62a1e-157">RELATED LINKS</span></span>

[<span data-ttu-id="62a1e-158">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="62a1e-158">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="62a1e-159">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="62a1e-159">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="62a1e-160">Nowe — AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="62a1e-160">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


