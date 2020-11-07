---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 46a6a9663e7e22fd1182656bab9cab8a263f6c44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717506"
---
# <span data-ttu-id="561ce-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="561ce-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="561ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="561ce-102">SYNOPSIS</span></span>
<span data-ttu-id="561ce-103">Dodaje regułę rozsyłania żądań do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="561ce-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="561ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="561ce-104">SYNTAX</span></span>

### <span data-ttu-id="561ce-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="561ce-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="561ce-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="561ce-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="561ce-107">Opis</span><span class="sxs-lookup"><span data-stu-id="561ce-107">DESCRIPTION</span></span>
<span data-ttu-id="561ce-108">Polecenie cmdlet **Add-AzureRmApplicationGatewayRequestRoutingRule** umożliwia dodanie reguły rozsyłania żądań do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="561ce-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="561ce-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="561ce-109">EXAMPLES</span></span>

### <span data-ttu-id="561ce-110">Przykład 1: Dodawanie reguły rozsyłania żądań do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="561ce-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="561ce-111">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="561ce-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="561ce-112">Drugie polecenie dodaje regułę rozsyłania żądań do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="561ce-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="561ce-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="561ce-113">PARAMETERS</span></span>

### <span data-ttu-id="561ce-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="561ce-114">-ApplicationGateway</span></span>
<span data-ttu-id="561ce-115">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje regułę routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="561ce-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="561ce-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="561ce-116">-BackendAddressPool</span></span>
<span data-ttu-id="561ce-117">Określa obiekt puli adresów zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="561ce-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="561ce-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="561ce-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="561ce-119">Określa identyfikator puli adresów zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="561ce-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="561ce-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="561ce-120">-BackendHttpSettings</span></span>
<span data-ttu-id="561ce-121">Określa obiekt ustawienia HTTP zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="561ce-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="561ce-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="561ce-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="561ce-123">Określa identyfikator ustawień HTTP zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="561ce-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="561ce-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="561ce-124">-DefaultProfile</span></span>
<span data-ttu-id="561ce-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="561ce-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="561ce-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="561ce-126">-HttpListener</span></span>
<span data-ttu-id="561ce-127">Określa obiekt odbiornika HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="561ce-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="561ce-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="561ce-128">-HttpListenerId</span></span>
<span data-ttu-id="561ce-129">Określa identyfikator odbiornika HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="561ce-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="561ce-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="561ce-130">-Name</span></span>
<span data-ttu-id="561ce-131">Określa nazwę reguły rozsyłania żądań, którą dodaje polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="561ce-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="561ce-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="561ce-132">-RedirectConfiguration</span></span>
<span data-ttu-id="561ce-133">Aplikacja Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="561ce-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="561ce-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="561ce-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="561ce-135">Identyfikator bramy Application RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="561ce-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="561ce-136">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="561ce-136">-RuleType</span></span>
<span data-ttu-id="561ce-137">Określa typ reguły routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="561ce-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="561ce-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="561ce-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="561ce-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="561ce-139">-UrlPathMapId</span></span>
<span data-ttu-id="561ce-140">Określa identyfikator mapy ścieżki URL dla reguły routingu.</span><span class="sxs-lookup"><span data-stu-id="561ce-140">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="561ce-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="561ce-141">CommonParameters</span></span>
<span data-ttu-id="561ce-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="561ce-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="561ce-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="561ce-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="561ce-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="561ce-144">INPUTS</span></span>

### <span data-ttu-id="561ce-145">System. String</span><span class="sxs-lookup"><span data-stu-id="561ce-145">System.String</span></span>

## <span data-ttu-id="561ce-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="561ce-146">OUTPUTS</span></span>

### <span data-ttu-id="561ce-147">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="561ce-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="561ce-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="561ce-148">NOTES</span></span>

## <span data-ttu-id="561ce-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="561ce-149">RELATED LINKS</span></span>

[<span data-ttu-id="561ce-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="561ce-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="561ce-151">Nowe — AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="561ce-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="561ce-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="561ce-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="561ce-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="561ce-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


