---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: bf4a87ebae55329e4594d11559fda0aee9047cbc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892806"
---
# <span data-ttu-id="ae5bb-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae5bb-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="ae5bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae5bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5bb-103">Modyfikuje konfigurację WAF bramy Application.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="ae5bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae5bb-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae5bb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae5bb-105">DESCRIPTION</span></span>
<span data-ttu-id="ae5bb-106">Polecenie cmdlet **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** modyfikuje konfigurację zapory aplikacji sieci Web (WAF) bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="ae5bb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae5bb-107">EXAMPLES</span></span>

### <span data-ttu-id="ae5bb-108">Przykład 1: aktualizowanie konfiguracji zapory aplikacji sieci Web bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="ae5bb-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="ae5bb-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01, a następnie zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="ae5bb-110">Drugie polecenie włącza konfigurację zapory dla bramy aplikacji przechowywaną w $AppGw i ustawia tryb zapory na "wykrywanie", zestaw reguł na wartość "OWASP" i RuleSetVersion na "3,0".</span><span class="sxs-lookup"><span data-stu-id="ae5bb-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="ae5bb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae5bb-111">PARAMETERS</span></span>

### <span data-ttu-id="ae5bb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae5bb-112">-ApplicationGateway</span></span>
<span data-ttu-id="ae5bb-113">Określa obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="ae5bb-114">Możesz użyć polecenia cmdlet Get-AzApplicationGateway, aby uzyskać obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae5bb-115">-DefaultProfile</span></span>
<span data-ttu-id="ae5bb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae5bb-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="ae5bb-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="ae5bb-118">Wyłączone grupy reguł.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="ae5bb-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="ae5bb-119">-Enabled</span></span>
<span data-ttu-id="ae5bb-120">Wskazuje, czy jest włączona Zapora aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="ae5bb-121">-Firewallmode</span><span class="sxs-lookup"><span data-stu-id="ae5bb-121">-FirewallMode</span></span>
<span data-ttu-id="ae5bb-122">Określa tryb zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="ae5bb-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ae5bb-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae5bb-124">Wykrywanie</span><span class="sxs-lookup"><span data-stu-id="ae5bb-124">Detection</span></span>
- <span data-ttu-id="ae5bb-125">Ochrona przed</span><span class="sxs-lookup"><span data-stu-id="ae5bb-125">Prevention</span></span>

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

### <span data-ttu-id="ae5bb-126">-Zestaw reguł</span><span class="sxs-lookup"><span data-stu-id="ae5bb-126">-RuleSetType</span></span>
<span data-ttu-id="ae5bb-127">Typ zestawu reguł zapory aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="ae5bb-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ae5bb-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="ae5bb-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="ae5bb-129">OWASP</span></span>

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

### <span data-ttu-id="ae5bb-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="ae5bb-130">-RuleSetVersion</span></span>
<span data-ttu-id="ae5bb-131">Wersja typu zestawu reguł.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-131">The version of the rule set type.</span></span>
<span data-ttu-id="ae5bb-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ae5bb-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="ae5bb-133">3,0</span><span class="sxs-lookup"><span data-stu-id="ae5bb-133">3.0</span></span>
- <span data-ttu-id="ae5bb-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="ae5bb-134">2.2.9</span></span>

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

### <span data-ttu-id="ae5bb-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae5bb-135">-Confirm</span></span>
<span data-ttu-id="ae5bb-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae5bb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae5bb-137">-WhatIf</span></span>
<span data-ttu-id="ae5bb-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae5bb-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae5bb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5bb-140">CommonParameters</span></span>
<span data-ttu-id="ae5bb-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae5bb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae5bb-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae5bb-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5bb-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae5bb-143">INPUTS</span></span>

### <span data-ttu-id="ae5bb-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae5bb-144">PSApplicationGateway</span></span>
<span data-ttu-id="ae5bb-145">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ae5bb-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="ae5bb-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae5bb-146">OUTPUTS</span></span>

### <span data-ttu-id="ae5bb-147">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae5bb-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ae5bb-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae5bb-148">NOTES</span></span>

## <span data-ttu-id="ae5bb-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae5bb-149">RELATED LINKS</span></span>

[<span data-ttu-id="ae5bb-150">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ae5bb-150">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="ae5bb-151">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae5bb-151">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="ae5bb-152">Nowe — AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae5bb-152">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


