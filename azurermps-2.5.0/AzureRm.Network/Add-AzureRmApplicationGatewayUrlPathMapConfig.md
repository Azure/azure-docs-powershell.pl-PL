---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 1b6e5c2c2a28333e51c74d9621a3fd607f6a652d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898418"
---
# <span data-ttu-id="de2cb-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="de2cb-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="de2cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="de2cb-103">Dodaje tablicę mapowań ścieżek adresów URL do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="de2cb-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de2cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de2cb-104">SYNTAX</span></span>

### <span data-ttu-id="de2cb-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="de2cb-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de2cb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="de2cb-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de2cb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="de2cb-107">DESCRIPTION</span></span>
<span data-ttu-id="de2cb-108">Polecenie cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** umożliwia dodanie tablicy mapowań ścieżek adresów URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="de2cb-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="de2cb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de2cb-109">EXAMPLES</span></span>

### <span data-ttu-id="de2cb-110">1:1</span><span class="sxs-lookup"><span data-stu-id="de2cb-110">1:</span></span>
```

```

## <span data-ttu-id="de2cb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de2cb-111">PARAMETERS</span></span>

### <span data-ttu-id="de2cb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de2cb-112">-ApplicationGateway</span></span>
<span data-ttu-id="de2cb-113">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje konfigurację mapowania ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="de2cb-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="de2cb-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="de2cb-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="de2cb-115">Określa domyślną pulę adresów zaplecza, która ma być przekierowywana na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="de2cb-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de2cb-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="de2cb-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="de2cb-117">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="de2cb-117">Specifies the default backend address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de2cb-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="de2cb-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="de2cb-119">Określa domyślne ustawienia protokołu HTTP zaplecza, których należy użyć na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="de2cb-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de2cb-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="de2cb-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="de2cb-121">Określa identyfikator domyślnych ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="de2cb-121">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de2cb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de2cb-122">-DefaultProfile</span></span>
<span data-ttu-id="de2cb-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de2cb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de2cb-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="de2cb-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="de2cb-125">Domyślny RedirectConfiguration bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="de2cb-125">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de2cb-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="de2cb-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="de2cb-127">Identyfikator domyślnej RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="de2cb-127">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de2cb-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de2cb-128">-Name</span></span>
<span data-ttu-id="de2cb-129">Określa nazwę mapy ścieżki URL, którą to polecenie cmdlet dodaje do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="de2cb-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de2cb-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="de2cb-130">-PathRules</span></span>
<span data-ttu-id="de2cb-131">Określa listę reguł ścieżek.</span><span class="sxs-lookup"><span data-stu-id="de2cb-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="de2cb-132">Reguły ścieżki są zależne od kolejności, są one stosowane w kolejności, w jakiej są określone.</span><span class="sxs-lookup"><span data-stu-id="de2cb-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="de2cb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de2cb-133">CommonParameters</span></span>
<span data-ttu-id="de2cb-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de2cb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de2cb-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de2cb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de2cb-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de2cb-136">INPUTS</span></span>

### <span data-ttu-id="de2cb-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de2cb-137">PSApplicationGateway</span></span>
<span data-ttu-id="de2cb-138">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="de2cb-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="de2cb-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de2cb-139">OUTPUTS</span></span>

### <span data-ttu-id="de2cb-140">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de2cb-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="de2cb-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de2cb-141">NOTES</span></span>

## <span data-ttu-id="de2cb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de2cb-142">RELATED LINKS</span></span>

[<span data-ttu-id="de2cb-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="de2cb-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="de2cb-144">Nowe — AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="de2cb-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="de2cb-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="de2cb-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="de2cb-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="de2cb-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


