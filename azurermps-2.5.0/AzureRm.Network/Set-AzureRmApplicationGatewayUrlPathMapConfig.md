---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 7ca1d4f8ee4ab3e83badecd7856fcee35f5b9a23
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898889"
---
# <span data-ttu-id="59e84-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="59e84-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="59e84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59e84-102">SYNOPSIS</span></span>
<span data-ttu-id="59e84-103">Ustawia konfigurację tablicy mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="59e84-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59e84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59e84-104">SYNTAX</span></span>

### <span data-ttu-id="59e84-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="59e84-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59e84-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="59e84-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59e84-107">Opis</span><span class="sxs-lookup"><span data-stu-id="59e84-107">DESCRIPTION</span></span>
<span data-ttu-id="59e84-108">Polecenie cmdlet **Set-AzureRmApplicationGatewayUrlPathMapConfig** ustawia konfigurację tablicy mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="59e84-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="59e84-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59e84-109">EXAMPLES</span></span>

### <span data-ttu-id="59e84-110">1:1</span><span class="sxs-lookup"><span data-stu-id="59e84-110">1:</span></span>
```

```

## <span data-ttu-id="59e84-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59e84-111">PARAMETERS</span></span>

### <span data-ttu-id="59e84-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59e84-112">-ApplicationGateway</span></span>
<span data-ttu-id="59e84-113">Określa bramę aplikacji, do której to polecenie cmdlet ustawia konfigurację mapowania ścieżki URL.</span><span class="sxs-lookup"><span data-stu-id="59e84-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="59e84-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="59e84-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="59e84-115">Określa domyślną pulę adresów zaplecza, która ma być przekierowywana na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="59e84-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="59e84-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="59e84-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="59e84-117">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="59e84-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="59e84-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="59e84-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="59e84-119">Określa domyślne ustawienia protokołu HTTP zaplecza, których należy użyć na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="59e84-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="59e84-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="59e84-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="59e84-121">Określa identyfikator domyślnych ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="59e84-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="59e84-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59e84-122">-DefaultProfile</span></span>
<span data-ttu-id="59e84-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="59e84-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59e84-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="59e84-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="59e84-125">Domyślny RedirectConfiguration bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="59e84-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="59e84-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="59e84-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="59e84-127">Identyfikator domyślnej RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="59e84-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="59e84-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="59e84-128">-Name</span></span>
<span data-ttu-id="59e84-129">Określa nazwę mapy ścieżki URL, w której to polecenie cmdlet ustawia konfigurację dla.</span><span class="sxs-lookup"><span data-stu-id="59e84-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="59e84-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="59e84-130">-PathRules</span></span>
<span data-ttu-id="59e84-131">Określa listę reguł ścieżek.</span><span class="sxs-lookup"><span data-stu-id="59e84-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="59e84-132">Pamiętaj, że reguły ścieżki są zależne od kolejności, są one stosowane w kolejności, w jakiej zostały określone.</span><span class="sxs-lookup"><span data-stu-id="59e84-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="59e84-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e84-133">CommonParameters</span></span>
<span data-ttu-id="59e84-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59e84-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e84-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59e84-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e84-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59e84-136">INPUTS</span></span>

### <span data-ttu-id="59e84-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59e84-137">PSApplicationGateway</span></span>
<span data-ttu-id="59e84-138">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="59e84-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="59e84-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59e84-139">OUTPUTS</span></span>

### <span data-ttu-id="59e84-140">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="59e84-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="59e84-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59e84-141">NOTES</span></span>

## <span data-ttu-id="59e84-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59e84-142">RELATED LINKS</span></span>

[<span data-ttu-id="59e84-143">Dodaj-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="59e84-143">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="59e84-144">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="59e84-144">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="59e84-145">Nowe — AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="59e84-145">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="59e84-146">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="59e84-146">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


