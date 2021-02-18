---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cf65e93f1dc2026c0fc973d694fe1f44718df12e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240851"
---
# <span data-ttu-id="b88c5-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b88c5-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="b88c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b88c5-102">SYNOPSIS</span></span>
<span data-ttu-id="b88c5-103">Tworzy tablicę mapowań ścieżek adresu URL na pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b88c5-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="b88c5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b88c5-104">SYNTAX</span></span>

### <span data-ttu-id="b88c5-105">BackendSetByResource (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b88c5-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b88c5-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b88c5-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b88c5-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="b88c5-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b88c5-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b88c5-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b88c5-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b88c5-109">DESCRIPTION</span></span>
<span data-ttu-id="b88c5-110">Polecenie **cmdlet New-AzApplicationGatewayUrlPathMapConfig** tworzy tablicę mapowań ścieżek adresu URL na pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b88c5-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="b88c5-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b88c5-111">EXAMPLES</span></span>

### <span data-ttu-id="b88c5-112">Przykład 1. Tworzenie tablicy mapowań ścieżek adresu URL na pulę serwerów zaplecza</span><span class="sxs-lookup"><span data-stu-id="b88c5-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="b88c5-113">To polecenie tworzy tablicę mapowań ścieżek adresu URL na pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b88c5-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="b88c5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b88c5-114">PARAMETERS</span></span>

### <span data-ttu-id="b88c5-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b88c5-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="b88c5-116">Określa domyślną pulę adresów zaplecza do rozsyłania na wypadek, gdy żadne z reguł określonych w parametrze *pathRules* nie jest zgodne.</span><span class="sxs-lookup"><span data-stu-id="b88c5-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b88c5-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="b88c5-118">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b88c5-118">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b88c5-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="b88c5-120">Określa domyślne ustawienia protokołu HTTP zaplecza w przypadku, gdy żadne z reguł określonych w parametrze *pathRules* nie są zgodne.</span><span class="sxs-lookup"><span data-stu-id="b88c5-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="b88c5-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="b88c5-122">Określa domyślny identyfikator ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b88c5-122">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b88c5-123">-DefaultProfile</span></span>
<span data-ttu-id="b88c5-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b88c5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b88c5-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b88c5-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="b88c5-126">Domyślna konfiguracja RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b88c5-126">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b88c5-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="b88c5-128">Identyfikator domyślnej konfiguracji przekierowywania (RedirectConfiguration) bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b88c5-128">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b88c5-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="b88c5-130">Domyślny zestaw reguł ponownego ustawienia bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b88c5-130">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="b88c5-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="b88c5-132">Identyfikator domyślnego zestawu reguł ponownego ustawienia reguły dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="b88c5-132">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b88c5-133">-Name</span></span>
<span data-ttu-id="b88c5-134">Określa nazwę mapy ścieżki adresu URL, którą tworzy to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b88c5-134">Specifies the URL path map name that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-135">- PathRules</span><span class="sxs-lookup"><span data-stu-id="b88c5-135">-PathRules</span></span>
<span data-ttu-id="b88c5-136">Określa listę reguł ścieżki.</span><span class="sxs-lookup"><span data-stu-id="b88c5-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="b88c5-137">Zwróć uwagę, że reguły ścieżki mają porządek i są stosowane w określonej kolejności.</span><span class="sxs-lookup"><span data-stu-id="b88c5-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b88c5-138">CommonParameters</span></span>
<span data-ttu-id="b88c5-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b88c5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b88c5-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b88c5-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b88c5-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b88c5-141">INPUTS</span></span>

### <span data-ttu-id="b88c5-142">Brak</span><span class="sxs-lookup"><span data-stu-id="b88c5-142">None</span></span>

## <span data-ttu-id="b88c5-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b88c5-143">OUTPUTS</span></span>

### <span data-ttu-id="b88c5-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="b88c5-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="b88c5-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b88c5-145">NOTES</span></span>

## <span data-ttu-id="b88c5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b88c5-146">RELATED LINKS</span></span>

[<span data-ttu-id="b88c5-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b88c5-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b88c5-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b88c5-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b88c5-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b88c5-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b88c5-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b88c5-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


