---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 03e03de70f61672d1246ffeb8469efe0c04b3ea4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233045"
---
# <span data-ttu-id="02ff8-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="02ff8-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="02ff8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="02ff8-103">Tworzy zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="02ff8-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="02ff8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02ff8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02ff8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="02ff8-106">Polecenie cmdlet **New-AzApplicationGatewayFirewallPolicy** tworzy zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="02ff8-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="02ff8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02ff8-107">EXAMPLES</span></span>

### <span data-ttu-id="02ff8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="02ff8-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="02ff8-109">To polecenie tworzy nową zasadę zapory dla bramy aplikacji platformy Azure o nazwie "wafResource1" w grupie zasobów "RG1" w lokalizacji "zachód" z regułami niestandardowymi zdefiniowanymi w zmiennej $customRule</span><span class="sxs-lookup"><span data-stu-id="02ff8-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="02ff8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02ff8-110">PARAMETERS</span></span>

### <span data-ttu-id="02ff8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02ff8-111">-AsJob</span></span>
<span data-ttu-id="02ff8-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="02ff8-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ff8-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="02ff8-113">-CustomRule</span></span>
<span data-ttu-id="02ff8-114">Lista CustomRules</span><span class="sxs-lookup"><span data-stu-id="02ff8-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ff8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ff8-115">-DefaultProfile</span></span>
<span data-ttu-id="02ff8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02ff8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02ff8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="02ff8-117">-Force</span></span>
<span data-ttu-id="02ff8-118">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="02ff8-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ff8-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="02ff8-119">-Location</span></span>
<span data-ttu-id="02ff8-120">pozycję.</span><span class="sxs-lookup"><span data-stu-id="02ff8-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ff8-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="02ff8-121">-ManagedRule</span></span>
<span data-ttu-id="02ff8-122">Ustawienie reguły zarządzanej</span><span class="sxs-lookup"><span data-stu-id="02ff8-122">Managed Rule Setting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ff8-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02ff8-123">-Name</span></span>
<span data-ttu-id="02ff8-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="02ff8-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ff8-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="02ff8-125">-PolicySetting</span></span>
<span data-ttu-id="02ff8-126">Ustawienia zasad dotyczące zapory aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="02ff8-126">Policy Settings for Web Application Firewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ff8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ff8-127">-ResourceGroupName</span></span>
<span data-ttu-id="02ff8-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="02ff8-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ff8-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="02ff8-129">-Tag</span></span>
<span data-ttu-id="02ff8-130">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="02ff8-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ff8-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02ff8-131">-Confirm</span></span>
<span data-ttu-id="02ff8-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02ff8-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ff8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02ff8-133">-WhatIf</span></span>
<span data-ttu-id="02ff8-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02ff8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02ff8-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02ff8-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ff8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ff8-136">CommonParameters</span></span>
<span data-ttu-id="02ff8-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02ff8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ff8-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02ff8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ff8-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02ff8-139">INPUTS</span></span>

### <span data-ttu-id="02ff8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="02ff8-140">System.String</span></span>

### <span data-ttu-id="02ff8-141">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="02ff8-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="02ff8-142">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="02ff8-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="02ff8-143">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="02ff8-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="02ff8-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="02ff8-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="02ff8-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02ff8-145">OUTPUTS</span></span>

### <span data-ttu-id="02ff8-146">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="02ff8-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="02ff8-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02ff8-147">NOTES</span></span>

## <span data-ttu-id="02ff8-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02ff8-148">RELATED LINKS</span></span>
