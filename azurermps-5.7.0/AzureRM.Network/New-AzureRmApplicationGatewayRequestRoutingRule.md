---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ab053235c928f109321cdf9adf3429e589958ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546695"
---
# <span data-ttu-id="01f76-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01f76-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="01f76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01f76-102">SYNOPSIS</span></span>
<span data-ttu-id="01f76-103">Tworzy regułę rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="01f76-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01f76-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01f76-104">SYNTAX</span></span>

### <span data-ttu-id="01f76-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="01f76-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01f76-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="01f76-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01f76-107">Opis</span><span class="sxs-lookup"><span data-stu-id="01f76-107">DESCRIPTION</span></span>
<span data-ttu-id="01f76-108">Polecenie cmdlet **Add-AzureRmApplicationGatewayRequestRoutingRule** tworzy regułę rozsyłania żądań dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="01f76-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="01f76-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01f76-109">EXAMPLES</span></span>

### <span data-ttu-id="01f76-110">Przykład 1. Tworzenie reguły rozsyłania żądań dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="01f76-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="01f76-111">To polecenie tworzy podstawową zasadę rozsyłania żądań o nazwie Rule01 i zapisuje wynik w zmiennej o nazwie $Rule.</span><span class="sxs-lookup"><span data-stu-id="01f76-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="01f76-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01f76-112">PARAMETERS</span></span>

### <span data-ttu-id="01f76-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="01f76-113">-BackendAddressPool</span></span>
<span data-ttu-id="01f76-114">Określa pulę adresów zaplecza jako obiekt dla reguły rozsyłania żądań, którą można utworzyć.</span><span class="sxs-lookup"><span data-stu-id="01f76-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="01f76-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="01f76-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="01f76-116">Określa identyfikator puli adresów zaplecza reguły rozsyłania żądań, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="01f76-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="01f76-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="01f76-117">-BackendHttpSettings</span></span>
<span data-ttu-id="01f76-118">Określa ustawienia HTTP zaplecza jako obiekt do utworzenia reguły rozsyłania żądań.</span><span class="sxs-lookup"><span data-stu-id="01f76-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="01f76-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="01f76-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="01f76-120">Określa identyfikator HTTP zaplecza dla reguły rozsyłania żądań, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="01f76-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="01f76-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f76-121">-DefaultProfile</span></span>
<span data-ttu-id="01f76-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01f76-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01f76-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="01f76-123">-HttpListener</span></span>
<span data-ttu-id="01f76-124">Umożliwia określenie odbiornika HTTP zaplecza do utworzenia reguły routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="01f76-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="01f76-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="01f76-125">-HttpListenerId</span></span>
<span data-ttu-id="01f76-126">Określa identyfikator odbiornika HTTP zaplecza dla reguły rozsyłania żądań, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="01f76-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="01f76-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="01f76-127">-Name</span></span>
<span data-ttu-id="01f76-128">Określa nazwę reguły rozsyłania żądań, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01f76-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="01f76-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="01f76-129">-RedirectConfiguration</span></span>
<span data-ttu-id="01f76-130">Aplikacja Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="01f76-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="01f76-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="01f76-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="01f76-132">Identyfikator bramy Application RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="01f76-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="01f76-133">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="01f76-133">-RuleType</span></span>
<span data-ttu-id="01f76-134">Określa typ reguły rozsyłania żądań.</span><span class="sxs-lookup"><span data-stu-id="01f76-134">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="01f76-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="01f76-135">-UrlPathMap</span></span>
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

### <span data-ttu-id="01f76-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="01f76-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="01f76-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f76-137">CommonParameters</span></span>
<span data-ttu-id="01f76-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f76-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f76-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01f76-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f76-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01f76-140">INPUTS</span></span>

### <span data-ttu-id="01f76-141">System. String</span><span class="sxs-lookup"><span data-stu-id="01f76-141">System.String</span></span>

## <span data-ttu-id="01f76-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01f76-142">OUTPUTS</span></span>

### <span data-ttu-id="01f76-143">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01f76-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="01f76-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01f76-144">NOTES</span></span>

## <span data-ttu-id="01f76-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01f76-145">RELATED LINKS</span></span>

[<span data-ttu-id="01f76-146">Dodaj-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01f76-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="01f76-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01f76-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="01f76-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01f76-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="01f76-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01f76-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


