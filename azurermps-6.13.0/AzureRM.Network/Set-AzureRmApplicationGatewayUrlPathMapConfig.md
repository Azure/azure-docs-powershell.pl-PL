---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: d0944ad15beeab3de380801480560bc216a7df16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710928"
---
# <span data-ttu-id="92b3e-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="92b3e-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="92b3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="92b3e-103">Ustawia konfigurację tablicy mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="92b3e-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92b3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92b3e-104">SYNTAX</span></span>

### <span data-ttu-id="92b3e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="92b3e-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92b3e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="92b3e-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92b3e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="92b3e-107">DESCRIPTION</span></span>
<span data-ttu-id="92b3e-108">Polecenie cmdlet **Set-AzureRmApplicationGatewayUrlPathMapConfig** ustawia konfigurację tablicy mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="92b3e-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="92b3e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92b3e-109">EXAMPLES</span></span>

## <span data-ttu-id="92b3e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92b3e-110">PARAMETERS</span></span>

### <span data-ttu-id="92b3e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92b3e-111">-ApplicationGateway</span></span>
<span data-ttu-id="92b3e-112">Określa bramę aplikacji, do której to polecenie cmdlet ustawia konfigurację mapowania ścieżki URL.</span><span class="sxs-lookup"><span data-stu-id="92b3e-112">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="92b3e-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="92b3e-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="92b3e-114">Określa domyślną pulę adresów zaplecza, która ma być przekierowywana na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="92b3e-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b3e-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="92b3e-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="92b3e-116">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="92b3e-116">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b3e-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="92b3e-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="92b3e-118">Określa domyślne ustawienia protokołu HTTP zaplecza, których należy użyć na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="92b3e-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b3e-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="92b3e-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="92b3e-120">Określa identyfikator domyślnych ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="92b3e-120">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b3e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b3e-121">-DefaultProfile</span></span>
<span data-ttu-id="92b3e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="92b3e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92b3e-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="92b3e-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="92b3e-124">Domyślny RedirectConfiguration bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="92b3e-124">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b3e-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="92b3e-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="92b3e-126">Identyfikator domyślnej RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="92b3e-126">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b3e-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="92b3e-127">-Name</span></span>
<span data-ttu-id="92b3e-128">Określa nazwę mapy ścieżki URL, w której to polecenie cmdlet ustawia konfigurację dla.</span><span class="sxs-lookup"><span data-stu-id="92b3e-128">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="92b3e-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="92b3e-129">-PathRules</span></span>
<span data-ttu-id="92b3e-130">Określa listę reguł ścieżek.</span><span class="sxs-lookup"><span data-stu-id="92b3e-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="92b3e-131">Pamiętaj, że reguły ścieżki są zależne od kolejności, są one stosowane w kolejności, w jakiej zostały określone.</span><span class="sxs-lookup"><span data-stu-id="92b3e-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b3e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b3e-132">CommonParameters</span></span>
<span data-ttu-id="92b3e-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92b3e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b3e-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92b3e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b3e-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92b3e-135">INPUTS</span></span>

### <span data-ttu-id="92b3e-136">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92b3e-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="92b3e-137">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="92b3e-137">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="92b3e-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92b3e-138">OUTPUTS</span></span>

### <span data-ttu-id="92b3e-139">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92b3e-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="92b3e-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92b3e-140">NOTES</span></span>

## <span data-ttu-id="92b3e-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92b3e-141">RELATED LINKS</span></span>

[<span data-ttu-id="92b3e-142">Dodaj-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="92b3e-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="92b3e-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="92b3e-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="92b3e-144">Nowe — AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="92b3e-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="92b3e-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="92b3e-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


