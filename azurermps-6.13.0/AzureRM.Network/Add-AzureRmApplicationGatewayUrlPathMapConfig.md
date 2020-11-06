---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 321c7272c02b4e5555f731d3a9dbaa7d806c0727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545119"
---
# <span data-ttu-id="d3149-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d3149-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="d3149-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3149-102">SYNOPSIS</span></span>
<span data-ttu-id="d3149-103">Dodaje tablicę mapowań ścieżek adresów URL do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d3149-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3149-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3149-104">SYNTAX</span></span>

### <span data-ttu-id="d3149-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3149-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3149-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d3149-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3149-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d3149-107">DESCRIPTION</span></span>
<span data-ttu-id="d3149-108">Polecenie cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** umożliwia dodanie tablicy mapowań ścieżek adresów URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d3149-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="d3149-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3149-109">EXAMPLES</span></span>

## <span data-ttu-id="d3149-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3149-110">PARAMETERS</span></span>

### <span data-ttu-id="d3149-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3149-111">-ApplicationGateway</span></span>
<span data-ttu-id="d3149-112">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje konfigurację mapowania ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="d3149-112">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="d3149-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d3149-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="d3149-114">Określa domyślną pulę adresów zaplecza, która ma być przekierowywana na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="d3149-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d3149-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d3149-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="d3149-116">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d3149-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="d3149-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d3149-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="d3149-118">Określa domyślne ustawienia protokołu HTTP zaplecza, których należy użyć na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="d3149-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d3149-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d3149-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="d3149-120">Określa identyfikator domyślnych ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d3149-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="d3149-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3149-121">-DefaultProfile</span></span>
<span data-ttu-id="d3149-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3149-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3149-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3149-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="d3149-124">Domyślny RedirectConfiguration bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d3149-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d3149-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d3149-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="d3149-126">Identyfikator domyślnej RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="d3149-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d3149-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d3149-127">-Name</span></span>
<span data-ttu-id="d3149-128">Określa nazwę mapy ścieżki URL, którą to polecenie cmdlet dodaje do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d3149-128">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="d3149-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="d3149-129">-PathRules</span></span>
<span data-ttu-id="d3149-130">Określa listę reguł ścieżek.</span><span class="sxs-lookup"><span data-stu-id="d3149-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="d3149-131">Reguły ścieżki są zależne od kolejności, są one stosowane w kolejności, w jakiej są określone.</span><span class="sxs-lookup"><span data-stu-id="d3149-131">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="d3149-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3149-132">CommonParameters</span></span>
<span data-ttu-id="d3149-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3149-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3149-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3149-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3149-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3149-135">INPUTS</span></span>

### <span data-ttu-id="d3149-136">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3149-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="d3149-137">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d3149-137">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="d3149-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3149-138">OUTPUTS</span></span>

### <span data-ttu-id="d3149-139">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3149-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d3149-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3149-140">NOTES</span></span>

## <span data-ttu-id="d3149-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3149-141">RELATED LINKS</span></span>

[<span data-ttu-id="d3149-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d3149-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d3149-143">Nowe — AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d3149-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d3149-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d3149-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d3149-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d3149-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


