---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 95e46bfc1f90f4e9760077b11f52d8020cb7f409
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552619"
---
# <span data-ttu-id="6c9a0-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6c9a0-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="6c9a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9a0-103">Modyfikuje regułę rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-103">Modifies a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c9a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c9a0-104">SYNTAX</span></span>

### <span data-ttu-id="6c9a0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6c9a0-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c9a0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6c9a0-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c9a0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6c9a0-107">DESCRIPTION</span></span>
<span data-ttu-id="6c9a0-108">Polecenie cmdlet **Set-AzureRmApplicationGatewayRequestRoutingRule** modyfikuje regułę rozsyłania żądań.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-108">The **Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="6c9a0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c9a0-109">EXAMPLES</span></span>

### <span data-ttu-id="6c9a0-110">Przykład 1: aktualizowanie reguły routingu żądań</span><span class="sxs-lookup"><span data-stu-id="6c9a0-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="6c9a0-111">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6c9a0-112">Drugie polecenie modyfikuje regułę rozsyłania żądań dla bramy aplikacji w celu użycia wewnętrznych ustawień HTTP określonych w zmiennej $Setting, odbiornika HTTP określonego w zmiennej $Listener i puli adresów zaplecza określonej w zmiennej $Pool.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="6c9a0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c9a0-113">PARAMETERS</span></span>

### <span data-ttu-id="6c9a0-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c9a0-114">-ApplicationGateway</span></span>
<span data-ttu-id="6c9a0-115">Określa obiekt bramy aplikacji, z którym to polecenie cmdlet kojarzy regułę routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9a0-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6c9a0-116">-BackendAddressPool</span></span>
<span data-ttu-id="6c9a0-117">Określa pulę adresów zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="6c9a0-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="6c9a0-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="6c9a0-119">Określa identyfikator puli adresów zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="6c9a0-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6c9a0-120">-BackendHttpSettings</span></span>
<span data-ttu-id="6c9a0-121">Określa ustawienia HTTP zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="6c9a0-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="6c9a0-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="6c9a0-123">Określa identyfikator ustawień HTTP bramy Application end.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="6c9a0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9a0-124">-DefaultProfile</span></span>
<span data-ttu-id="6c9a0-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c9a0-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="6c9a0-126">-HttpListener</span></span>
<span data-ttu-id="6c9a0-127">Określa odbiornik HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="6c9a0-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="6c9a0-128">-HttpListenerId</span></span>
<span data-ttu-id="6c9a0-129">Określa identyfikator odbiornika HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="6c9a0-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c9a0-130">-Name</span></span>
<span data-ttu-id="6c9a0-131">Określa nazwę reguły rozsyłania żądań, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6c9a0-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c9a0-132">-RedirectConfiguration</span></span>
<span data-ttu-id="6c9a0-133">Aplikacja Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c9a0-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6c9a0-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6c9a0-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="6c9a0-135">Identyfikator bramy Application RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c9a0-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="6c9a0-136">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="6c9a0-136">-RuleType</span></span>
<span data-ttu-id="6c9a0-137">Określa typ reguły routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="6c9a0-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="6c9a0-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="6c9a0-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="6c9a0-139">-UrlPathMapId</span></span>
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

### <span data-ttu-id="6c9a0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9a0-140">CommonParameters</span></span>
<span data-ttu-id="6c9a0-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c9a0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9a0-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c9a0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9a0-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c9a0-143">INPUTS</span></span>

### <span data-ttu-id="6c9a0-144">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c9a0-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="6c9a0-145">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c9a0-145">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="6c9a0-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c9a0-146">OUTPUTS</span></span>

### <span data-ttu-id="6c9a0-147">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6c9a0-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6c9a0-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c9a0-148">NOTES</span></span>

## <span data-ttu-id="6c9a0-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c9a0-149">RELATED LINKS</span></span>

[<span data-ttu-id="6c9a0-150">Dodaj-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6c9a0-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6c9a0-151">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6c9a0-151">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6c9a0-152">Nowe — AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6c9a0-152">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="6c9a0-153">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6c9a0-153">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

