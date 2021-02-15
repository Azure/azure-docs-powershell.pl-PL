---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 03e03de70f61672d1246ffeb8469efe0c04b3ea4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187091"
---
# <span data-ttu-id="d3d00-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d3d00-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="d3d00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3d00-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d00-103">Tworzy zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d3d00-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="d3d00-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3d00-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3d00-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3d00-105">DESCRIPTION</span></span>
<span data-ttu-id="d3d00-106">Polecenie **cmdlet New-AzApplicationGatewayFirewallPolicy** tworzy zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d3d00-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="d3d00-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3d00-107">EXAMPLES</span></span>

### <span data-ttu-id="d3d00-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d3d00-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="d3d00-109">To polecenie tworzy nowe zasady zapory bramy aplikacji platformy Azure o nazwie "wafResource1" w grupie zasobów "rg1" w lokalizacji "westus" z regułami niestandardowymi zdefiniowanymi w $customRule sieci web</span><span class="sxs-lookup"><span data-stu-id="d3d00-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="d3d00-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3d00-110">PARAMETERS</span></span>

### <span data-ttu-id="d3d00-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d3d00-111">-AsJob</span></span>
<span data-ttu-id="d3d00-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d3d00-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3d00-113">- CustomRule</span><span class="sxs-lookup"><span data-stu-id="d3d00-113">-CustomRule</span></span>
<span data-ttu-id="d3d00-114">Lista elementów CustomRules</span><span class="sxs-lookup"><span data-stu-id="d3d00-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="d3d00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d00-115">-DefaultProfile</span></span>
<span data-ttu-id="d3d00-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d00-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3d00-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d3d00-117">-Force</span></span>
<span data-ttu-id="d3d00-118">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="d3d00-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d3d00-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d3d00-119">-Location</span></span>
<span data-ttu-id="d3d00-120">.</span><span class="sxs-lookup"><span data-stu-id="d3d00-120">location.</span></span>

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

### <span data-ttu-id="d3d00-121">- ManagedRule</span><span class="sxs-lookup"><span data-stu-id="d3d00-121">-ManagedRule</span></span>
<span data-ttu-id="d3d00-122">Ustawienie reguły zarządzanej</span><span class="sxs-lookup"><span data-stu-id="d3d00-122">Managed Rule Setting</span></span>

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

### <span data-ttu-id="d3d00-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d3d00-123">-Name</span></span>
<span data-ttu-id="d3d00-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="d3d00-124">The resource name.</span></span>

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

### <span data-ttu-id="d3d00-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="d3d00-125">-PolicySetting</span></span>
<span data-ttu-id="d3d00-126">Ustawienia zasad zapory aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="d3d00-126">Policy Settings for Web Application Firewall</span></span>

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

### <span data-ttu-id="d3d00-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3d00-127">-ResourceGroupName</span></span>
<span data-ttu-id="d3d00-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3d00-128">The resource group name.</span></span>

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

### <span data-ttu-id="d3d00-129">— Tag</span><span class="sxs-lookup"><span data-stu-id="d3d00-129">-Tag</span></span>
<span data-ttu-id="d3d00-130">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3d00-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d3d00-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3d00-131">-Confirm</span></span>
<span data-ttu-id="d3d00-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d3d00-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3d00-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3d00-133">-WhatIf</span></span>
<span data-ttu-id="d3d00-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3d00-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3d00-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d3d00-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3d00-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d00-136">CommonParameters</span></span>
<span data-ttu-id="d3d00-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d00-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d00-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3d00-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d00-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3d00-139">INPUTS</span></span>

### <span data-ttu-id="d3d00-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d3d00-140">System.String</span></span>

### <span data-ttu-id="d3d00-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span><span class="sxs-lookup"><span data-stu-id="d3d00-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="d3d00-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="d3d00-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="d3d00-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="d3d00-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="d3d00-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d3d00-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d3d00-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3d00-145">OUTPUTS</span></span>

### <span data-ttu-id="d3d00-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d3d00-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="d3d00-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3d00-147">NOTES</span></span>

## <span data-ttu-id="d3d00-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3d00-148">RELATED LINKS</span></span>
