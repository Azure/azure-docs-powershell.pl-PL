---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: e643bf488073f6da685265cea4a2a0c6cb7cebf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970513"
---
# <span data-ttu-id="60d8b-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="60d8b-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="60d8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="60d8b-103">Tworzy zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="60d8b-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="60d8b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="60d8b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60d8b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="60d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="60d8b-106">Polecenie **cmdlet New-AzApplicationGatewayFirewallPolicy** tworzy zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="60d8b-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="60d8b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="60d8b-107">EXAMPLES</span></span>

### <span data-ttu-id="60d8b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60d8b-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="60d8b-109">To polecenie tworzy nowe zasady zapory bramy aplikacji platformy Azure o nazwie "wafResource1" w grupie zasobów "rg1" w lokalizacji "westus" z regułami niestandardowymi zdefiniowanymi w $customRule sieci web</span><span class="sxs-lookup"><span data-stu-id="60d8b-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="60d8b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60d8b-110">PARAMETERS</span></span>

### <span data-ttu-id="60d8b-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="60d8b-111">-AsJob</span></span>
<span data-ttu-id="60d8b-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="60d8b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60d8b-113">- CustomRule</span><span class="sxs-lookup"><span data-stu-id="60d8b-113">-CustomRule</span></span>
<span data-ttu-id="60d8b-114">Lista list CustomRules</span><span class="sxs-lookup"><span data-stu-id="60d8b-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="60d8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d8b-115">-DefaultProfile</span></span>
<span data-ttu-id="60d8b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="60d8b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60d8b-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="60d8b-117">-Force</span></span>
<span data-ttu-id="60d8b-118">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="60d8b-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="60d8b-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="60d8b-119">-Location</span></span>
<span data-ttu-id="60d8b-120">.</span><span class="sxs-lookup"><span data-stu-id="60d8b-120">location.</span></span>

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

### <span data-ttu-id="60d8b-121">- ManagedRule</span><span class="sxs-lookup"><span data-stu-id="60d8b-121">-ManagedRule</span></span>
<span data-ttu-id="60d8b-122">Ustawienie reguły zarządzanej</span><span class="sxs-lookup"><span data-stu-id="60d8b-122">Managed Rule Setting</span></span>

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

### <span data-ttu-id="60d8b-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="60d8b-123">-Name</span></span>
<span data-ttu-id="60d8b-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="60d8b-124">The resource name.</span></span>

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

### <span data-ttu-id="60d8b-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="60d8b-125">-PolicySetting</span></span>
<span data-ttu-id="60d8b-126">Ustawienia zasad zapory aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="60d8b-126">Policy Settings for Web Application Firewall</span></span>

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

### <span data-ttu-id="60d8b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60d8b-127">-ResourceGroupName</span></span>
<span data-ttu-id="60d8b-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="60d8b-128">The resource group name.</span></span>

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

### <span data-ttu-id="60d8b-129">— Tag</span><span class="sxs-lookup"><span data-stu-id="60d8b-129">-Tag</span></span>
<span data-ttu-id="60d8b-130">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="60d8b-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="60d8b-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60d8b-131">-Confirm</span></span>
<span data-ttu-id="60d8b-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="60d8b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60d8b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60d8b-133">-WhatIf</span></span>
<span data-ttu-id="60d8b-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60d8b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60d8b-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="60d8b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60d8b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d8b-136">CommonParameters</span></span>
<span data-ttu-id="60d8b-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60d8b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d8b-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60d8b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d8b-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60d8b-139">INPUTS</span></span>

### <span data-ttu-id="60d8b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="60d8b-140">System.String</span></span>

### <span data-ttu-id="60d8b-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span><span class="sxs-lookup"><span data-stu-id="60d8b-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="60d8b-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="60d8b-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="60d8b-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="60d8b-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="60d8b-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="60d8b-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="60d8b-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60d8b-145">OUTPUTS</span></span>

### <span data-ttu-id="60d8b-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="60d8b-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="60d8b-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="60d8b-147">NOTES</span></span>

## <span data-ttu-id="60d8b-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60d8b-148">RELATED LINKS</span></span>
