---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 291188d8eac7f5031079e477fe2e6a3a0106b4a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718516"
---
# <span data-ttu-id="be998-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="be998-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="be998-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be998-102">SYNOPSIS</span></span>
<span data-ttu-id="be998-103">Tworzy regułę rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="be998-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be998-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be998-104">SYNTAX</span></span>

### <span data-ttu-id="be998-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="be998-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be998-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="be998-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be998-107">Opis</span><span class="sxs-lookup"><span data-stu-id="be998-107">DESCRIPTION</span></span>
<span data-ttu-id="be998-108">Polecenie cmdlet **Add-AzureRmApplicationGatewayRequestRoutingRule** tworzy regułę rozsyłania żądań dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="be998-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="be998-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be998-109">EXAMPLES</span></span>

### <span data-ttu-id="be998-110">Przykład 1. Tworzenie reguły rozsyłania żądań dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="be998-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="be998-111">To polecenie tworzy podstawową zasadę rozsyłania żądań o nazwie Rule01 i zapisuje wynik w zmiennej o nazwie $Rule.</span><span class="sxs-lookup"><span data-stu-id="be998-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="be998-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be998-112">PARAMETERS</span></span>

### <span data-ttu-id="be998-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="be998-113">-BackendAddressPool</span></span>
<span data-ttu-id="be998-114">Określa pulę adresów zaplecza jako obiekt dla reguły rozsyłania żądań, którą można utworzyć.</span><span class="sxs-lookup"><span data-stu-id="be998-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="be998-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="be998-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="be998-116">Określa identyfikator puli adresów zaplecza reguły rozsyłania żądań, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="be998-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="be998-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="be998-117">-BackendHttpSettings</span></span>
<span data-ttu-id="be998-118">Określa ustawienia HTTP zaplecza jako obiekt do utworzenia reguły rozsyłania żądań.</span><span class="sxs-lookup"><span data-stu-id="be998-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="be998-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="be998-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="be998-120">Określa identyfikator HTTP zaplecza dla reguły rozsyłania żądań, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="be998-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="be998-121">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="be998-121">-HttpListener</span></span>
<span data-ttu-id="be998-122">Umożliwia określenie odbiornika HTTP zaplecza do utworzenia reguły routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="be998-122">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be998-123">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="be998-123">-HttpListenerId</span></span>
<span data-ttu-id="be998-124">Określa identyfikator odbiornika HTTP zaplecza dla reguły rozsyłania żądań, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="be998-124">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="be998-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be998-125">-Name</span></span>
<span data-ttu-id="be998-126">Określa nazwę reguły rozsyłania żądań, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be998-126">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="be998-127">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="be998-127">-RedirectConfiguration</span></span>
<span data-ttu-id="be998-128">Aplikacja Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="be998-128">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="be998-129">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="be998-129">-RedirectConfigurationId</span></span>
<span data-ttu-id="be998-130">Identyfikator bramy Application RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="be998-130">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="be998-131">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="be998-131">-RuleType</span></span>
<span data-ttu-id="be998-132">Określa typ reguły rozsyłania żądań.</span><span class="sxs-lookup"><span data-stu-id="be998-132">Specifies type of the request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be998-133">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="be998-133">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be998-134">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="be998-134">-UrlPathMapId</span></span>
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

### <span data-ttu-id="be998-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be998-135">-DefaultProfile</span></span>
<span data-ttu-id="be998-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="be998-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be998-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be998-137">CommonParameters</span></span>
<span data-ttu-id="be998-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be998-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be998-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be998-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be998-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be998-140">INPUTS</span></span>

### <span data-ttu-id="be998-141">System. String</span><span class="sxs-lookup"><span data-stu-id="be998-141">System.String</span></span>

## <span data-ttu-id="be998-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be998-142">OUTPUTS</span></span>

### <span data-ttu-id="be998-143">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="be998-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="be998-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be998-144">NOTES</span></span>

## <span data-ttu-id="be998-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be998-145">RELATED LINKS</span></span>

[<span data-ttu-id="be998-146">Dodaj-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="be998-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="be998-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="be998-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="be998-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="be998-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="be998-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="be998-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


