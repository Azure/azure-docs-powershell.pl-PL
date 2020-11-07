---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: eedf03e2468be36fadc519fc2e6b931c82433fc0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891001"
---
# <span data-ttu-id="d0460-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d0460-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="d0460-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0460-102">SYNOPSIS</span></span>
<span data-ttu-id="d0460-103">Dodaje tablicę mapowań ścieżek adresów URL do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d0460-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="d0460-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0460-104">SYNTAX</span></span>

### <span data-ttu-id="d0460-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0460-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0460-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d0460-106">SetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0460-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d0460-107">DESCRIPTION</span></span>
<span data-ttu-id="d0460-108">Polecenie cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** umożliwia dodanie tablicy mapowań ścieżek adresów URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d0460-108">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="d0460-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0460-109">EXAMPLES</span></span>

### <span data-ttu-id="d0460-110">1:1</span><span class="sxs-lookup"><span data-stu-id="d0460-110">1:</span></span>
```

```

## <span data-ttu-id="d0460-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0460-111">PARAMETERS</span></span>

### <span data-ttu-id="d0460-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0460-112">-ApplicationGateway</span></span>
<span data-ttu-id="d0460-113">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje konfigurację mapowania ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="d0460-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="d0460-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d0460-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="d0460-115">Określa domyślną pulę adresów zaplecza, która ma być przekierowywana na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="d0460-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d0460-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d0460-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="d0460-117">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d0460-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="d0460-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d0460-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="d0460-119">Określa domyślne ustawienia protokołu HTTP zaplecza, których należy użyć na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="d0460-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="d0460-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d0460-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="d0460-121">Określa identyfikator domyślnych ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d0460-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="d0460-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0460-122">-DefaultProfile</span></span>
<span data-ttu-id="d0460-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0460-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0460-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0460-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="d0460-125">Domyślny RedirectConfiguration bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d0460-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d0460-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d0460-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="d0460-127">Identyfikator domyślnej RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="d0460-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="d0460-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0460-128">-Name</span></span>
<span data-ttu-id="d0460-129">Określa nazwę mapy ścieżki URL, którą to polecenie cmdlet dodaje do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d0460-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="d0460-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="d0460-130">-PathRules</span></span>
<span data-ttu-id="d0460-131">Określa listę reguł ścieżek.</span><span class="sxs-lookup"><span data-stu-id="d0460-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="d0460-132">Reguły ścieżki są zależne od kolejności, są one stosowane w kolejności, w jakiej są określone.</span><span class="sxs-lookup"><span data-stu-id="d0460-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="d0460-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0460-133">CommonParameters</span></span>
<span data-ttu-id="d0460-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0460-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0460-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0460-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0460-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0460-136">INPUTS</span></span>

### <span data-ttu-id="d0460-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0460-137">PSApplicationGateway</span></span>
<span data-ttu-id="d0460-138">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="d0460-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="d0460-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0460-139">OUTPUTS</span></span>

### <span data-ttu-id="d0460-140">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0460-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d0460-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0460-141">NOTES</span></span>

## <span data-ttu-id="d0460-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0460-142">RELATED LINKS</span></span>

[<span data-ttu-id="d0460-143">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d0460-143">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d0460-144">Nowe — AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d0460-144">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d0460-145">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d0460-145">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="d0460-146">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d0460-146">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


