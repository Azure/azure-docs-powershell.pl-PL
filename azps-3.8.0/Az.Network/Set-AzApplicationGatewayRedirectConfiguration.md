---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: da6acfddcee30861b73145d7d8e66871de02568d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050314"
---
# <span data-ttu-id="048ef-101">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="048ef-101">Set-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="048ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="048ef-102">SYNOPSIS</span></span>
<span data-ttu-id="048ef-103">Ustawia konfigurację przekierowania dla istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="048ef-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="048ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="048ef-104">SYNTAX</span></span>

### <span data-ttu-id="048ef-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="048ef-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="048ef-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="048ef-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="048ef-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="048ef-107">SetByURL</span></span>
```
Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="048ef-108">Opis</span><span class="sxs-lookup"><span data-stu-id="048ef-108">DESCRIPTION</span></span>
<span data-ttu-id="048ef-109">Polecenie cmdlet **Set-AzApplicationGatewayRequestRoutingRule** modyfikuje konfigurację przekierowania.</span><span class="sxs-lookup"><span data-stu-id="048ef-109">**The Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="048ef-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="048ef-110">EXAMPLES</span></span>

### <span data-ttu-id="048ef-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="048ef-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="048ef-112">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="048ef-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="048ef-113">Drugie polecenie modyfikuje konfigurację przekierowania dla bramy aplikacji w celu przekierowania typu Permanent, a następnie użyj docelowego adresu URL.</span><span class="sxs-lookup"><span data-stu-id="048ef-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="048ef-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="048ef-114">PARAMETERS</span></span>

### <span data-ttu-id="048ef-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="048ef-115">-ApplicationGateway</span></span>
<span data-ttu-id="048ef-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="048ef-116">The applicationGateway</span></span>

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

### <span data-ttu-id="048ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="048ef-117">-DefaultProfile</span></span>
<span data-ttu-id="048ef-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="048ef-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048ef-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="048ef-119">-IncludePath</span></span>
<span data-ttu-id="048ef-120">Dołącz ścieżkę w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="048ef-120">Include path in the redirected url.</span></span>
<span data-ttu-id="048ef-121">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="048ef-121">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048ef-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="048ef-122">-IncludeQueryString</span></span>
<span data-ttu-id="048ef-123">Uwzględnij ciąg zapytania w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="048ef-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="048ef-124">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="048ef-124">Default is true.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048ef-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="048ef-125">-Name</span></span>
<span data-ttu-id="048ef-126">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="048ef-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="048ef-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="048ef-127">-RedirectType</span></span>
<span data-ttu-id="048ef-128">Typ przekierowania</span><span class="sxs-lookup"><span data-stu-id="048ef-128">The type of redirect</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048ef-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="048ef-129">-TargetListener</span></span>
<span data-ttu-id="048ef-130">Odbiornik HTTP umożliwiający przekierowanie żądania do</span><span class="sxs-lookup"><span data-stu-id="048ef-130">HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="048ef-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="048ef-131">-TargetListenerID</span></span>
<span data-ttu-id="048ef-132">Identyfikator odbiornika HTTP do przekierowania żądania do</span><span class="sxs-lookup"><span data-stu-id="048ef-132">ID of HTTP listener to redirect the request to</span></span>

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

### <span data-ttu-id="048ef-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="048ef-133">-TargetUrl</span></span>
<span data-ttu-id="048ef-134">Docelowy adres URL, przekierowanie</span><span class="sxs-lookup"><span data-stu-id="048ef-134">Target URL fo redirection</span></span>

```yaml
Type: System.String
Parameter Sets: SetByURL
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="048ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="048ef-135">CommonParameters</span></span>
<span data-ttu-id="048ef-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="048ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="048ef-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="048ef-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="048ef-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="048ef-138">INPUTS</span></span>

### <span data-ttu-id="048ef-139">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="048ef-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="048ef-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="048ef-140">OUTPUTS</span></span>

### <span data-ttu-id="048ef-141">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="048ef-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="048ef-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="048ef-142">NOTES</span></span>

## <span data-ttu-id="048ef-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="048ef-143">RELATED LINKS</span></span>

[<span data-ttu-id="048ef-144">Dodaj-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="048ef-144">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="048ef-145">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="048ef-145">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="048ef-146">Nowe — AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="048ef-146">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="048ef-147">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="048ef-147">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)
