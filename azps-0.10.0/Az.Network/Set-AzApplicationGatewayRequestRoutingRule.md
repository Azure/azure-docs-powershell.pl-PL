---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c2c212d3cf80044ce7c81d9d4ebd318f6a1e93ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892830"
---
# <span data-ttu-id="f39d6-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f39d6-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="f39d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f39d6-102">SYNOPSIS</span></span>
<span data-ttu-id="f39d6-103">Modyfikuje regułę rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f39d6-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="f39d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f39d6-104">SYNTAX</span></span>

### <span data-ttu-id="f39d6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f39d6-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f39d6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f39d6-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f39d6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f39d6-107">DESCRIPTION</span></span>
<span data-ttu-id="f39d6-108">Polecenie cmdlet **Set-AzApplicationGatewayRequestRoutingRule** modyfikuje regułę rozsyłania żądań.</span><span class="sxs-lookup"><span data-stu-id="f39d6-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="f39d6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f39d6-109">EXAMPLES</span></span>

### <span data-ttu-id="f39d6-110">Przykład 1: aktualizowanie reguły routingu żądań</span><span class="sxs-lookup"><span data-stu-id="f39d6-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="f39d6-111">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f39d6-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f39d6-112">Drugie polecenie modyfikuje regułę rozsyłania żądań dla bramy aplikacji w celu użycia wewnętrznych ustawień HTTP określonych w zmiennej $Setting, odbiornika HTTP określonego w zmiennej $Listener i puli adresów zaplecza określonej w zmiennej $Pool.</span><span class="sxs-lookup"><span data-stu-id="f39d6-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="f39d6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f39d6-113">PARAMETERS</span></span>

### <span data-ttu-id="f39d6-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f39d6-114">-ApplicationGateway</span></span>
<span data-ttu-id="f39d6-115">Określa obiekt bramy aplikacji, z którym to polecenie cmdlet kojarzy regułę routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="f39d6-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="f39d6-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f39d6-116">-BackendAddressPool</span></span>
<span data-ttu-id="f39d6-117">Określa pulę adresów zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f39d6-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="f39d6-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f39d6-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="f39d6-119">Określa identyfikator puli adresów zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f39d6-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="f39d6-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f39d6-120">-BackendHttpSettings</span></span>
<span data-ttu-id="f39d6-121">Określa ustawienia HTTP zaplecza bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f39d6-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="f39d6-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="f39d6-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="f39d6-123">Określa identyfikator ustawień HTTP bramy Application end.</span><span class="sxs-lookup"><span data-stu-id="f39d6-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="f39d6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39d6-124">-DefaultProfile</span></span>
<span data-ttu-id="f39d6-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f39d6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f39d6-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="f39d6-126">-HttpListener</span></span>
<span data-ttu-id="f39d6-127">Określa odbiornik HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f39d6-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="f39d6-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="f39d6-128">-HttpListenerId</span></span>
<span data-ttu-id="f39d6-129">Określa identyfikator odbiornika HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f39d6-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="f39d6-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f39d6-130">-Name</span></span>
<span data-ttu-id="f39d6-131">Określa nazwę reguły rozsyłania żądań, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="f39d6-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f39d6-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f39d6-132">-RedirectConfiguration</span></span>
<span data-ttu-id="f39d6-133">Aplikacja Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f39d6-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="f39d6-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f39d6-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="f39d6-135">Identyfikator bramy Application RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f39d6-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="f39d6-136">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="f39d6-136">-RuleType</span></span>
<span data-ttu-id="f39d6-137">Określa typ reguły routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="f39d6-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="f39d6-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="f39d6-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="f39d6-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="f39d6-139">-UrlPathMapId</span></span>
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

### <span data-ttu-id="f39d6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39d6-140">CommonParameters</span></span>
<span data-ttu-id="f39d6-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f39d6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39d6-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f39d6-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39d6-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f39d6-143">INPUTS</span></span>

### <span data-ttu-id="f39d6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f39d6-144">System.String</span></span>

## <span data-ttu-id="f39d6-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f39d6-145">OUTPUTS</span></span>

### <span data-ttu-id="f39d6-146">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f39d6-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f39d6-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f39d6-147">NOTES</span></span>

## <span data-ttu-id="f39d6-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f39d6-148">RELATED LINKS</span></span>

[<span data-ttu-id="f39d6-149">Dodaj-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f39d6-149">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f39d6-150">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f39d6-150">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f39d6-151">Nowe — AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f39d6-151">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f39d6-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f39d6-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


