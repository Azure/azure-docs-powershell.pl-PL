---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 590793e8a2caeb360b88a7d41d91dcea07baacfd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890526"
---
# <span data-ttu-id="e96cd-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e96cd-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="e96cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e96cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e96cd-103">Tworzy tablicę mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e96cd-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e96cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e96cd-104">SYNTAX</span></span>

### <span data-ttu-id="e96cd-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e96cd-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e96cd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e96cd-106">SetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e96cd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e96cd-107">DESCRIPTION</span></span>
<span data-ttu-id="e96cd-108">Polecenie cmdlet **New-AzApplicationGatewayUrlPathMapConfig** tworzy tablicę mapowań ścieżek adresów URL na pulę serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e96cd-108">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e96cd-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e96cd-109">EXAMPLES</span></span>

### <span data-ttu-id="e96cd-110">Przykład 1. tworzenie tablicy mapowań ścieżek adresów URL do puli serwerów zaplecza</span><span class="sxs-lookup"><span data-stu-id="e96cd-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="e96cd-111">To polecenie tworzy tablicę mapowań ścieżki URL do puli serwerów wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e96cd-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="e96cd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e96cd-112">PARAMETERS</span></span>

### <span data-ttu-id="e96cd-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e96cd-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="e96cd-114">Określa domyślną pulę adresów zaplecza, która ma być przekierowywana na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="e96cd-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e96cd-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e96cd-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="e96cd-116">Określa domyślny identyfikator puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e96cd-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="e96cd-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e96cd-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="e96cd-118">Określa domyślne ustawienia protokołu HTTP zaplecza, których należy użyć na wypadek, gdyby żadna z reguł określonych w parametrze *pathRules* nie była zgodna.</span><span class="sxs-lookup"><span data-stu-id="e96cd-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="e96cd-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e96cd-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="e96cd-120">Określa identyfikator domyślnych ustawień protokołu HTTP zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e96cd-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="e96cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e96cd-121">-DefaultProfile</span></span>
<span data-ttu-id="e96cd-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e96cd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e96cd-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e96cd-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="e96cd-124">Domyślny RedirectConfiguration bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e96cd-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e96cd-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e96cd-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="e96cd-126">Identyfikator domyślnej RedirectConfiguration bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e96cd-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="e96cd-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e96cd-127">-Name</span></span>
<span data-ttu-id="e96cd-128">Określa nazwę mapy ścieżki URL, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e96cd-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e96cd-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="e96cd-129">-PathRules</span></span>
<span data-ttu-id="e96cd-130">Określa listę reguł ścieżek.</span><span class="sxs-lookup"><span data-stu-id="e96cd-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="e96cd-131">Pamiętaj, że reguły ścieżki są zależne od kolejności, są one stosowane w kolejności, w jakiej zostały określone.</span><span class="sxs-lookup"><span data-stu-id="e96cd-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="e96cd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e96cd-132">CommonParameters</span></span>
<span data-ttu-id="e96cd-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e96cd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e96cd-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e96cd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e96cd-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e96cd-135">INPUTS</span></span>

## <span data-ttu-id="e96cd-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e96cd-136">OUTPUTS</span></span>

### <span data-ttu-id="e96cd-137">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="e96cd-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="e96cd-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e96cd-138">NOTES</span></span>

## <span data-ttu-id="e96cd-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e96cd-139">RELATED LINKS</span></span>

[<span data-ttu-id="e96cd-140">Dodaj-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e96cd-140">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e96cd-141">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e96cd-141">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e96cd-142">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e96cd-142">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="e96cd-143">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e96cd-143">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


