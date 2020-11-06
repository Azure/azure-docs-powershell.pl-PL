---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 5c3a59b497208c761ffcf7a24bc12b5ab2c50f27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544691"
---
# <span data-ttu-id="a002e-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a002e-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="a002e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a002e-102">SYNOPSIS</span></span>
<span data-ttu-id="a002e-103">Tworzy tablicę mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a002e-103">Creates an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a002e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a002e-104">SYNTAX</span></span>

### <span data-ttu-id="a002e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a002e-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a002e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a002e-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a002e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a002e-107">DESCRIPTION</span></span>
<span data-ttu-id="a002e-108">Polecenie cmdlet **New-AzureRmApplicationGatewayUrlPathMapConfig** tworzy tablicę mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a002e-108">The **New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a002e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a002e-109">EXAMPLES</span></span>

### <span data-ttu-id="a002e-110">Przykład 1. tworzenie tablicy mapowań ścieżek adresów URL do puli serwerów zaplecza</span><span class="sxs-lookup"><span data-stu-id="a002e-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzureRmApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="a002e-111">To polecenie tworzy tablicę mapowań ścieżki URL do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a002e-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a002e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a002e-112">PARAMETERS</span></span>

### <span data-ttu-id="a002e-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a002e-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="a002e-114">Określa domyślną pulę adresów zaplecza, która ma być przekierowywana na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="a002e-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="a002e-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a002e-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="a002e-116">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="a002e-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="a002e-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a002e-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="a002e-118">Określa domyślne ustawienia protokołu HTTP zaplecza, których należy użyć na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="a002e-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="a002e-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="a002e-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="a002e-120">Określa identyfikator domyślnych ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="a002e-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="a002e-121">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a002e-121">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="a002e-122">Domyślny RedirectConfiguration bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="a002e-122">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="a002e-123">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a002e-123">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="a002e-124">Identyfikator domyślnej RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a002e-124">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="a002e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a002e-125">-Name</span></span>
<span data-ttu-id="a002e-126">Określa nazwę mapy ścieżki URL, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a002e-126">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a002e-127">-PathRules</span><span class="sxs-lookup"><span data-stu-id="a002e-127">-PathRules</span></span>
<span data-ttu-id="a002e-128">Określa listę reguł ścieżek.</span><span class="sxs-lookup"><span data-stu-id="a002e-128">Specifies a list of path rules.</span></span>
<span data-ttu-id="a002e-129">Pamiętaj, że reguły ścieżki są zależne od kolejności, są one stosowane w kolejności, w jakiej zostały określone.</span><span class="sxs-lookup"><span data-stu-id="a002e-129">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="a002e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a002e-130">-DefaultProfile</span></span>
<span data-ttu-id="a002e-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a002e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a002e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a002e-132">CommonParameters</span></span>
<span data-ttu-id="a002e-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a002e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a002e-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a002e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a002e-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a002e-135">INPUTS</span></span>

## <span data-ttu-id="a002e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a002e-136">OUTPUTS</span></span>

### <span data-ttu-id="a002e-137">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="a002e-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="a002e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a002e-138">NOTES</span></span>

## <span data-ttu-id="a002e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a002e-139">RELATED LINKS</span></span>

[<span data-ttu-id="a002e-140">Dodaj-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a002e-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a002e-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a002e-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a002e-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a002e-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a002e-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a002e-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


