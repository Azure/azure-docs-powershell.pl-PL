---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 3885298f58f3bc45b207ea14cdda0935d0724986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545620"
---
# <span data-ttu-id="0afd8-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0afd8-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="0afd8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0afd8-102">SYNOPSIS</span></span>
<span data-ttu-id="0afd8-103">Dodaje tablicę mapowań ścieżek adresów URL do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0afd8-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0afd8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0afd8-104">SYNTAX</span></span>

### <span data-ttu-id="0afd8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0afd8-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0afd8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0afd8-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0afd8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0afd8-107">DESCRIPTION</span></span>
<span data-ttu-id="0afd8-108">Polecenie cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** umożliwia dodanie tablicy mapowań ścieżek adresów URL do puli serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="0afd8-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="0afd8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0afd8-109">EXAMPLES</span></span>

## <span data-ttu-id="0afd8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0afd8-110">PARAMETERS</span></span>

### <span data-ttu-id="0afd8-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0afd8-111">-ApplicationGateway</span></span>
<span data-ttu-id="0afd8-112">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje konfigurację mapowania ścieżki adresu URL.</span><span class="sxs-lookup"><span data-stu-id="0afd8-112">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="0afd8-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0afd8-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="0afd8-114">Określa domyślną pulę adresów zaplecza, która ma być przekierowywana na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="0afd8-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="0afd8-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0afd8-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="0afd8-116">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="0afd8-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="0afd8-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0afd8-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="0afd8-118">Określa domyślne ustawienia protokołu HTTP zaplecza, których należy użyć na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="0afd8-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="0afd8-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="0afd8-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="0afd8-120">Określa identyfikator domyślnych ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="0afd8-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="0afd8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afd8-121">-DefaultProfile</span></span>
<span data-ttu-id="0afd8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0afd8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0afd8-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0afd8-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="0afd8-124">Domyślny RedirectConfiguration bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="0afd8-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="0afd8-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0afd8-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="0afd8-126">Identyfikator domyślnej RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="0afd8-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="0afd8-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0afd8-127">-Name</span></span>
<span data-ttu-id="0afd8-128">Określa nazwę mapy ścieżki URL, którą to polecenie cmdlet dodaje do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0afd8-128">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="0afd8-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="0afd8-129">-PathRules</span></span>
<span data-ttu-id="0afd8-130">Określa listę reguł ścieżek.</span><span class="sxs-lookup"><span data-stu-id="0afd8-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="0afd8-131">Reguły ścieżki są zależne od kolejności, są one stosowane w kolejności, w jakiej są określone.</span><span class="sxs-lookup"><span data-stu-id="0afd8-131">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="0afd8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afd8-132">CommonParameters</span></span>
<span data-ttu-id="0afd8-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0afd8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afd8-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0afd8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afd8-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0afd8-135">INPUTS</span></span>

### <span data-ttu-id="0afd8-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0afd8-136">PSApplicationGateway</span></span>
<span data-ttu-id="0afd8-137">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="0afd8-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="0afd8-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0afd8-138">OUTPUTS</span></span>

### <span data-ttu-id="0afd8-139">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0afd8-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0afd8-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0afd8-140">NOTES</span></span>

## <span data-ttu-id="0afd8-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0afd8-141">RELATED LINKS</span></span>

[<span data-ttu-id="0afd8-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0afd8-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0afd8-143">Nowe — AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0afd8-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0afd8-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0afd8-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0afd8-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0afd8-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


