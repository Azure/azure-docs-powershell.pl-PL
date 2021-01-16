---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351829"
---
# <span data-ttu-id="dcd36-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd36-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="dcd36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcd36-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd36-103">Aktualizuje zasady zapory bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dcd36-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="dcd36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcd36-104">SYNTAX</span></span>

### <span data-ttu-id="dcd36-105">ByFactoryObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dcd36-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd36-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="dcd36-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd36-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd36-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcd36-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dcd36-108">DESCRIPTION</span></span>
<span data-ttu-id="dcd36-109">Polecenie cmdlet **Set-AzApplicationGatewayFirewallPolicy** aktualizuje zasady zapory Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="dcd36-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="dcd36-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcd36-110">EXAMPLES</span></span>

### <span data-ttu-id="dcd36-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dcd36-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="dcd36-112">To polecenie aktualizuje zasady zapory bramy aplikacji za pomocą ustawień w zmiennej $AppGwFirewallPolicy i przechowuje zaktualizowaną bramę w zmiennej $UpdatedAppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="dcd36-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="dcd36-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcd36-113">PARAMETERS</span></span>

### <span data-ttu-id="dcd36-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcd36-114">-AsJob</span></span>
<span data-ttu-id="dcd36-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="dcd36-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcd36-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="dcd36-116">-CustomRule</span></span>
<span data-ttu-id="dcd36-117">Lista CustomRules</span><span class="sxs-lookup"><span data-stu-id="dcd36-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="dcd36-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd36-118">-DefaultProfile</span></span>
<span data-ttu-id="dcd36-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd36-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcd36-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dcd36-120">-InputObject</span></span>
<span data-ttu-id="dcd36-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd36-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="dcd36-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="dcd36-122">-ManagedRule</span></span>
<span data-ttu-id="dcd36-123">ManagedRules zasad zapory</span><span class="sxs-lookup"><span data-stu-id="dcd36-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="dcd36-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dcd36-124">-Name</span></span>
<span data-ttu-id="dcd36-125">Nazwa zasad zapory.</span><span class="sxs-lookup"><span data-stu-id="dcd36-125">The Firewall Policy Name.</span></span>

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

### <span data-ttu-id="dcd36-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="dcd36-126">-PolicySetting</span></span>
<span data-ttu-id="dcd36-127">Policysettings zasad zapory</span><span class="sxs-lookup"><span data-stu-id="dcd36-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="dcd36-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcd36-128">-ResourceGroupName</span></span>
<span data-ttu-id="dcd36-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dcd36-129">The resource group name.</span></span>

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

### <span data-ttu-id="dcd36-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd36-130">-ResourceId</span></span>
<span data-ttu-id="dcd36-131">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd36-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="dcd36-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dcd36-132">-Confirm</span></span>
<span data-ttu-id="dcd36-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcd36-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcd36-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcd36-134">-WhatIf</span></span>
<span data-ttu-id="dcd36-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcd36-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcd36-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dcd36-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcd36-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd36-137">CommonParameters</span></span>
<span data-ttu-id="dcd36-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcd36-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd36-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcd36-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd36-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcd36-140">INPUTS</span></span>

### <span data-ttu-id="dcd36-141">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd36-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="dcd36-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcd36-142">OUTPUTS</span></span>

### <span data-ttu-id="dcd36-143">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd36-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="dcd36-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcd36-144">NOTES</span></span>

## <span data-ttu-id="dcd36-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcd36-145">RELATED LINKS</span></span>
