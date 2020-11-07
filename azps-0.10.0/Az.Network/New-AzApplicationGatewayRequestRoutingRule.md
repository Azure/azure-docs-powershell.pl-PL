---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ec85b643294f65aceefae2d4a52e9a5d48f15191
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890557"
---
# <span data-ttu-id="483ef-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="483ef-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="483ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="483ef-102">SYNOPSIS</span></span>
<span data-ttu-id="483ef-103">Tworzy regułę rozsyłania żądań dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="483ef-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="483ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="483ef-104">SYNTAX</span></span>

### <span data-ttu-id="483ef-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="483ef-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="483ef-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="483ef-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="483ef-107">Opis</span><span class="sxs-lookup"><span data-stu-id="483ef-107">DESCRIPTION</span></span>
<span data-ttu-id="483ef-108">Polecenie cmdlet **Add-AzApplicationGatewayRequestRoutingRule** tworzy regułę rozsyłania żądań dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="483ef-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="483ef-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="483ef-109">EXAMPLES</span></span>

### <span data-ttu-id="483ef-110">Przykład 1. Tworzenie reguły rozsyłania żądań dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="483ef-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="483ef-111">To polecenie tworzy podstawową zasadę rozsyłania żądań o nazwie Rule01 i zapisuje wynik w zmiennej o nazwie $Rule.</span><span class="sxs-lookup"><span data-stu-id="483ef-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="483ef-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="483ef-112">PARAMETERS</span></span>

### <span data-ttu-id="483ef-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="483ef-113">-BackendAddressPool</span></span>
<span data-ttu-id="483ef-114">Określa pulę adresów zaplecza jako obiekt dla reguły rozsyłania żądań, którą można utworzyć.</span><span class="sxs-lookup"><span data-stu-id="483ef-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="483ef-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="483ef-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="483ef-116">Określa identyfikator puli adresów zaplecza reguły rozsyłania żądań, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="483ef-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="483ef-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="483ef-117">-BackendHttpSettings</span></span>
<span data-ttu-id="483ef-118">Określa ustawienia HTTP zaplecza jako obiekt do utworzenia reguły rozsyłania żądań.</span><span class="sxs-lookup"><span data-stu-id="483ef-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="483ef-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="483ef-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="483ef-120">Określa identyfikator HTTP zaplecza dla reguły rozsyłania żądań, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="483ef-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="483ef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483ef-121">-DefaultProfile</span></span>
<span data-ttu-id="483ef-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="483ef-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="483ef-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="483ef-123">-HttpListener</span></span>
<span data-ttu-id="483ef-124">Umożliwia określenie odbiornika HTTP zaplecza do utworzenia reguły routingu żądań.</span><span class="sxs-lookup"><span data-stu-id="483ef-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="483ef-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="483ef-125">-HttpListenerId</span></span>
<span data-ttu-id="483ef-126">Określa identyfikator odbiornika HTTP zaplecza dla reguły rozsyłania żądań, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="483ef-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="483ef-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="483ef-127">-Name</span></span>
<span data-ttu-id="483ef-128">Określa nazwę reguły rozsyłania żądań, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="483ef-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="483ef-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="483ef-129">-RedirectConfiguration</span></span>
<span data-ttu-id="483ef-130">Aplikacja Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="483ef-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="483ef-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="483ef-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="483ef-132">Identyfikator bramy Application RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="483ef-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="483ef-133">-Ruletype</span><span class="sxs-lookup"><span data-stu-id="483ef-133">-RuleType</span></span>
<span data-ttu-id="483ef-134">Określa typ reguły rozsyłania żądań.</span><span class="sxs-lookup"><span data-stu-id="483ef-134">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="483ef-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="483ef-135">-UrlPathMap</span></span>
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

### <span data-ttu-id="483ef-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="483ef-136">-UrlPathMapId</span></span>
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

### <span data-ttu-id="483ef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483ef-137">CommonParameters</span></span>
<span data-ttu-id="483ef-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483ef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483ef-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="483ef-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483ef-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="483ef-140">INPUTS</span></span>

### <span data-ttu-id="483ef-141">System. String</span><span class="sxs-lookup"><span data-stu-id="483ef-141">System.String</span></span>

## <span data-ttu-id="483ef-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="483ef-142">OUTPUTS</span></span>

### <span data-ttu-id="483ef-143">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="483ef-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="483ef-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="483ef-144">NOTES</span></span>

## <span data-ttu-id="483ef-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="483ef-145">RELATED LINKS</span></span>

[<span data-ttu-id="483ef-146">Dodaj-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="483ef-146">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="483ef-147">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="483ef-147">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="483ef-148">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="483ef-148">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="483ef-149">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="483ef-149">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


