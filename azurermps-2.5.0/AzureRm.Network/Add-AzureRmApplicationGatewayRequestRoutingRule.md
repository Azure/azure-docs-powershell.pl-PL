---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: fdbbb28d69d5094b52d8ac7340839fa570bce55d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897626"
---
# <span data-ttu-id="1228a-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1228a-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="1228a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1228a-102">SYNOPSIS</span></span>
<span data-ttu-id="1228a-103">Dodaje regułę rozsyłania żądań do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1228a-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1228a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1228a-104">SYNTAX</span></span>

### <span data-ttu-id="1228a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1228a-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1228a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1228a-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1228a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1228a-107">DESCRIPTION</span></span>
<span data-ttu-id="1228a-108">Polecenie cmdlet **Add-AzureRmApplicationGatewayRequestRoutingRule** umożliwia dodanie reguły rozsyłania żądań do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1228a-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="1228a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1228a-109">EXAMPLES</span></span>

### <span data-ttu-id="1228a-110">Przykład 1: Dodawanie reguły rozsyłania żądań do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="1228a-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="1228a-111">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1228a-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1228a-112">Drugie polecenie dodaje regułę rozsyłania żądań do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1228a-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="1228a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1228a-113">PARAMETERS</span></span>

### <span data-ttu-id="1228a-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1228a-114">-ApplicationGateway</span></span>
<span data-ttu-id="1228a-115">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje regułę routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="1228a-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="1228a-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1228a-116">-BackendAddressPool</span></span>
<span data-ttu-id="1228a-117">Określa obiekt puli adresów zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1228a-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="1228a-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="1228a-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="1228a-119">Określa identyfikator puli adresów zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1228a-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="1228a-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1228a-120">-BackendHttpSettings</span></span>
<span data-ttu-id="1228a-121">Określa obiekt ustawienia HTTP zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1228a-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="1228a-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="1228a-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="1228a-123">Określa identyfikator ustawień HTTP zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1228a-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="1228a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1228a-124">-DefaultProfile</span></span>
<span data-ttu-id="1228a-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1228a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1228a-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="1228a-126">-HttpListener</span></span>
<span data-ttu-id="1228a-127">Określa obiekt odbiornika HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1228a-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1228a-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="1228a-128">-HttpListenerId</span></span>
<span data-ttu-id="1228a-129">Określa identyfikator odbiornika HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1228a-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="1228a-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1228a-130">-Name</span></span>
<span data-ttu-id="1228a-131">Określa nazwę reguły rozsyłania żądań, którą dodaje polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1228a-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="1228a-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1228a-132">-RedirectConfiguration</span></span>
<span data-ttu-id="1228a-133">Aplikacja Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1228a-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="1228a-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1228a-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="1228a-135">Identyfikator bramy Application RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1228a-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="1228a-136">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="1228a-136">-RuleType</span></span>
<span data-ttu-id="1228a-137">Określa typ reguły routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="1228a-137">Specifies the type of request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1228a-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="1228a-138">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1228a-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="1228a-139">-UrlPathMapId</span></span>
<span data-ttu-id="1228a-140">Określa identyfikator mapy ścieżki URL dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="1228a-140">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="1228a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1228a-141">CommonParameters</span></span>
<span data-ttu-id="1228a-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1228a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1228a-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1228a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1228a-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1228a-144">INPUTS</span></span>

### <span data-ttu-id="1228a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="1228a-145">System.String</span></span>

## <span data-ttu-id="1228a-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1228a-146">OUTPUTS</span></span>

### <span data-ttu-id="1228a-147">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1228a-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1228a-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1228a-148">NOTES</span></span>

## <span data-ttu-id="1228a-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1228a-149">RELATED LINKS</span></span>

[<span data-ttu-id="1228a-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1228a-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1228a-151">Nowe — AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1228a-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1228a-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1228a-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1228a-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1228a-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


