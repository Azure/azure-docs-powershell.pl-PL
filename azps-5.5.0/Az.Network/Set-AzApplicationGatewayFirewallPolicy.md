---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202482"
---
# <span data-ttu-id="c43c3-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c43c3-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="c43c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c43c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c43c3-103">Aktualizuje zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c43c3-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="c43c3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c43c3-104">SYNTAX</span></span>

### <span data-ttu-id="c43c3-105">ByFactoryObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c43c3-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c43c3-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="c43c3-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c43c3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c43c3-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c43c3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c43c3-108">DESCRIPTION</span></span>
<span data-ttu-id="c43c3-109">Polecenie **cmdlet Set-AzApplicationGatewayFirewallPolicy** aktualizuje zasady zapory bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="c43c3-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="c43c3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c43c3-110">EXAMPLES</span></span>

### <span data-ttu-id="c43c3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c43c3-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="c43c3-112">To polecenie aktualizuje zasady zapory bramy aplikacji przy użyciu ustawień $AppGwFirewallPolicy zmiennej sieciowej i zapisuje zaktualizowaną bramę w $UpdatedAppGwFirewallPolicy sieciowej.</span><span class="sxs-lookup"><span data-stu-id="c43c3-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="c43c3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c43c3-113">PARAMETERS</span></span>

### <span data-ttu-id="c43c3-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c43c3-114">-AsJob</span></span>
<span data-ttu-id="c43c3-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c43c3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c43c3-116">- CustomRule</span><span class="sxs-lookup"><span data-stu-id="c43c3-116">-CustomRule</span></span>
<span data-ttu-id="c43c3-117">Lista elementów CustomRules</span><span class="sxs-lookup"><span data-stu-id="c43c3-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="c43c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c43c3-118">-DefaultProfile</span></span>
<span data-ttu-id="c43c3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c43c3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c43c3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c43c3-120">-InputObject</span></span>
<span data-ttu-id="c43c3-121">The applicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c43c3-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c43c3-122">- ManagedRule</span><span class="sxs-lookup"><span data-stu-id="c43c3-122">-ManagedRule</span></span>
<span data-ttu-id="c43c3-123">ManagedRules zasad zapory</span><span class="sxs-lookup"><span data-stu-id="c43c3-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="c43c3-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c43c3-124">-Name</span></span>
<span data-ttu-id="c43c3-125">Nazwa zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="c43c3-125">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c43c3-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="c43c3-126">-PolicySetting</span></span>
<span data-ttu-id="c43c3-127">Ustawienia zasad zapory</span><span class="sxs-lookup"><span data-stu-id="c43c3-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="c43c3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c43c3-128">-ResourceGroupName</span></span>
<span data-ttu-id="c43c3-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c43c3-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c43c3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c43c3-130">-ResourceId</span></span>
<span data-ttu-id="c43c3-131">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="c43c3-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c43c3-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c43c3-132">-Confirm</span></span>
<span data-ttu-id="c43c3-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c43c3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c43c3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c43c3-134">-WhatIf</span></span>
<span data-ttu-id="c43c3-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c43c3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c43c3-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c43c3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c43c3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c43c3-137">CommonParameters</span></span>
<span data-ttu-id="c43c3-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c43c3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c43c3-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c43c3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c43c3-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c43c3-140">INPUTS</span></span>

### <span data-ttu-id="c43c3-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c43c3-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="c43c3-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c43c3-142">OUTPUTS</span></span>

### <span data-ttu-id="c43c3-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c43c3-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="c43c3-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c43c3-144">NOTES</span></span>

## <span data-ttu-id="c43c3-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c43c3-145">RELATED LINKS</span></span>
