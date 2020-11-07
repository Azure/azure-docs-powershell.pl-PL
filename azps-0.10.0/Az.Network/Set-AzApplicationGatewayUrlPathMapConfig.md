---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 5eb4fb0f036331fe68755a3a8ebddcd7e1b6e424
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892813"
---
# <span data-ttu-id="ade87-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ade87-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="ade87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ade87-102">SYNOPSIS</span></span>
<span data-ttu-id="ade87-103">Ustawia konfigurację tablicy mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ade87-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ade87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ade87-104">SYNTAX</span></span>

### <span data-ttu-id="ade87-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ade87-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ade87-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ade87-106">SetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ade87-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ade87-107">DESCRIPTION</span></span>
<span data-ttu-id="ade87-108">Polecenie cmdlet **Set-AzApplicationGatewayUrlPathMapConfig** ustawia konfigurację tablicy mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ade87-108">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="ade87-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ade87-109">EXAMPLES</span></span>

### <span data-ttu-id="ade87-110">1:1</span><span class="sxs-lookup"><span data-stu-id="ade87-110">1:</span></span>
```

```

## <span data-ttu-id="ade87-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ade87-111">PARAMETERS</span></span>

### <span data-ttu-id="ade87-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ade87-112">-ApplicationGateway</span></span>
<span data-ttu-id="ade87-113">Określa bramę aplikacji, do której to polecenie cmdlet ustawia konfigurację mapowania ścieżki URL.</span><span class="sxs-lookup"><span data-stu-id="ade87-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="ade87-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ade87-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="ade87-115">Określa domyślną pulę adresów zaplecza, która ma być przekierowywana na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="ade87-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="ade87-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ade87-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="ade87-117">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="ade87-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="ade87-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ade87-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="ade87-119">Określa domyślne ustawienia protokołu HTTP zaplecza, których należy użyć na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="ade87-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="ade87-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="ade87-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="ade87-121">Określa identyfikator domyślnych ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="ade87-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="ade87-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade87-122">-DefaultProfile</span></span>
<span data-ttu-id="ade87-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ade87-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ade87-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ade87-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="ade87-125">Domyślny RedirectConfiguration bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="ade87-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="ade87-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ade87-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="ade87-127">Identyfikator domyślnej RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="ade87-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="ade87-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ade87-128">-Name</span></span>
<span data-ttu-id="ade87-129">Określa nazwę mapy ścieżki URL, w której to polecenie cmdlet ustawia konfigurację dla.</span><span class="sxs-lookup"><span data-stu-id="ade87-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="ade87-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="ade87-130">-PathRules</span></span>
<span data-ttu-id="ade87-131">Określa listę reguł ścieżek.</span><span class="sxs-lookup"><span data-stu-id="ade87-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="ade87-132">Pamiętaj, że reguły ścieżki są zależne od kolejności, są one stosowane w kolejności, w jakiej zostały określone.</span><span class="sxs-lookup"><span data-stu-id="ade87-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="ade87-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade87-133">CommonParameters</span></span>
<span data-ttu-id="ade87-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade87-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade87-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ade87-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade87-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ade87-136">INPUTS</span></span>

### <span data-ttu-id="ade87-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ade87-137">PSApplicationGateway</span></span>
<span data-ttu-id="ade87-138">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ade87-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="ade87-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ade87-139">OUTPUTS</span></span>

### <span data-ttu-id="ade87-140">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ade87-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ade87-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ade87-141">NOTES</span></span>

## <span data-ttu-id="ade87-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ade87-142">RELATED LINKS</span></span>

[<span data-ttu-id="ade87-143">Dodaj-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ade87-143">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ade87-144">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ade87-144">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ade87-145">Nowe — AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ade87-145">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="ade87-146">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ade87-146">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


