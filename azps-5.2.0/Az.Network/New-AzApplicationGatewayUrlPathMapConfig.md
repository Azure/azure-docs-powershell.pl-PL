---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cf65e93f1dc2026c0fc973d694fe1f44718df12e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332638"
---
# <span data-ttu-id="a5807-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a5807-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="a5807-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5807-102">SYNOPSIS</span></span>
<span data-ttu-id="a5807-103">Tworzy tablicę mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a5807-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a5807-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5807-104">SYNTAX</span></span>

### <span data-ttu-id="a5807-105">BackendSetByResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a5807-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5807-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5807-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5807-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="a5807-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5807-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5807-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5807-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a5807-109">DESCRIPTION</span></span>
<span data-ttu-id="a5807-110">Polecenie cmdlet **New-AzApplicationGatewayUrlPathMapConfig** tworzy tablicę mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a5807-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a5807-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5807-111">EXAMPLES</span></span>

### <span data-ttu-id="a5807-112">Przykład 1. tworzenie tablicy mapowań ścieżek adresów URL do puli serwerów zaplecza</span><span class="sxs-lookup"><span data-stu-id="a5807-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="a5807-113">To polecenie tworzy tablicę mapowań ścieżki URL do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a5807-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a5807-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5807-114">PARAMETERS</span></span>

### <span data-ttu-id="a5807-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a5807-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="a5807-116">Określa domyślną pulę adresów zaplecza, która ma być przekierowywana na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="a5807-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="a5807-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a5807-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="a5807-118">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="a5807-118">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="a5807-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a5807-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="a5807-120">Określa domyślne ustawienia protokołu HTTP zaplecza, których należy użyć na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="a5807-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="a5807-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="a5807-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="a5807-122">Określa identyfikator domyślnych ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="a5807-122">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="a5807-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5807-123">-DefaultProfile</span></span>
<span data-ttu-id="a5807-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5807-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5807-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5807-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="a5807-126">Domyślny RedirectConfiguration bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a5807-126">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="a5807-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a5807-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="a5807-128">Identyfikator domyślnej RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a5807-128">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="a5807-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5807-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="a5807-130">Domyślny zestaw reguł ponownej edycji bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a5807-130">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="a5807-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="a5807-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="a5807-132">Identyfikator zestawu reguł domyślnego zapisu bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a5807-132">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="a5807-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5807-133">-Name</span></span>
<span data-ttu-id="a5807-134">Określa nazwę mapy ścieżki URL, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5807-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a5807-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="a5807-135">-PathRules</span></span>
<span data-ttu-id="a5807-136">Określa listę reguł ścieżek.</span><span class="sxs-lookup"><span data-stu-id="a5807-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="a5807-137">Pamiętaj, że reguły ścieżki są zależne od kolejności, są one stosowane w kolejności, w jakiej zostały określone.</span><span class="sxs-lookup"><span data-stu-id="a5807-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="a5807-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5807-138">CommonParameters</span></span>
<span data-ttu-id="a5807-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5807-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5807-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5807-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5807-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5807-141">INPUTS</span></span>

### <span data-ttu-id="a5807-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a5807-142">None</span></span>

## <span data-ttu-id="a5807-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5807-143">OUTPUTS</span></span>

### <span data-ttu-id="a5807-144">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="a5807-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="a5807-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5807-145">NOTES</span></span>

## <span data-ttu-id="a5807-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5807-146">RELATED LINKS</span></span>

[<span data-ttu-id="a5807-147">Dodaj-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a5807-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a5807-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a5807-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a5807-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a5807-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a5807-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a5807-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


