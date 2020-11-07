---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fe6c2ce03c238dadb53e8e0df88e4402d8f614d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526165"
---
# <span data-ttu-id="bc795-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc795-101">Set-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="bc795-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc795-102">SYNOPSIS</span></span>
<span data-ttu-id="bc795-103">Ustawia konfigurację przekierowania dla istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bc795-103">Sets the redirect configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc795-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc795-104">SYNTAX</span></span>

### <span data-ttu-id="bc795-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc795-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc795-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bc795-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc795-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="bc795-107">SetByURL</span></span>
```
Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc795-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bc795-108">DESCRIPTION</span></span>
<span data-ttu-id="bc795-109">Polecenie cmdlet **Set-AzureRmApplicationGatewayRequestRoutingRule** modyfikuje konfigurację przekierowania.</span><span class="sxs-lookup"><span data-stu-id="bc795-109">**The Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a redirect configuration.</span></span>

## <span data-ttu-id="bc795-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc795-110">EXAMPLES</span></span>

### <span data-ttu-id="bc795-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bc795-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw =  Set-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $appgw -Name "RedirectConfig01" -RedirectType Permanent -TargetUrl "https://www.contoso.com"
```

<span data-ttu-id="bc795-112">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bc795-112">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="bc795-113">Drugie polecenie modyfikuje konfigurację przekierowania dla bramy aplikacji w celu przekierowania typu Permanent, a następnie użyj docelowego adresu URL.</span><span class="sxs-lookup"><span data-stu-id="bc795-113">The second command modifies the redirect configuration for the application gateway to redirect type Permanent and use a target url.</span></span>

## <span data-ttu-id="bc795-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc795-114">PARAMETERS</span></span>

### <span data-ttu-id="bc795-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc795-115">-ApplicationGateway</span></span>
<span data-ttu-id="bc795-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc795-116">The applicationGateway</span></span>

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

### <span data-ttu-id="bc795-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc795-117">-DefaultProfile</span></span>
<span data-ttu-id="bc795-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc795-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc795-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="bc795-119">-IncludePath</span></span>
<span data-ttu-id="bc795-120">Dołącz ścieżkę w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="bc795-120">Include path in the redirected url.</span></span>
<span data-ttu-id="bc795-121">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="bc795-121">Default is true.</span></span>

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

### <span data-ttu-id="bc795-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="bc795-122">-IncludeQueryString</span></span>
<span data-ttu-id="bc795-123">Uwzględnij ciąg zapytania w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="bc795-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="bc795-124">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="bc795-124">Default is true.</span></span>

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

### <span data-ttu-id="bc795-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bc795-125">-Name</span></span>
<span data-ttu-id="bc795-126">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="bc795-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="bc795-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="bc795-127">-RedirectType</span></span>
<span data-ttu-id="bc795-128">Typ przekierowania</span><span class="sxs-lookup"><span data-stu-id="bc795-128">The type of redirect</span></span>

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

### <span data-ttu-id="bc795-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="bc795-129">-TargetListener</span></span>
<span data-ttu-id="bc795-130">HTTPListener, aby przekierować żądanie do</span><span class="sxs-lookup"><span data-stu-id="bc795-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="bc795-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="bc795-131">-TargetListenerID</span></span>
<span data-ttu-id="bc795-132">Identyfikator odbiornika, do którego ma zostać przekierowana prośba o</span><span class="sxs-lookup"><span data-stu-id="bc795-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="bc795-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="bc795-133">-TargetUrl</span></span>
<span data-ttu-id="bc795-134">Docelowy adres URL, przekierowanie</span><span class="sxs-lookup"><span data-stu-id="bc795-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="bc795-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc795-135">CommonParameters</span></span>
<span data-ttu-id="bc795-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc795-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc795-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc795-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc795-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc795-138">INPUTS</span></span>

### <span data-ttu-id="bc795-139">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc795-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="bc795-140">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bc795-140">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="bc795-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc795-141">OUTPUTS</span></span>

### <span data-ttu-id="bc795-142">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bc795-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bc795-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc795-143">NOTES</span></span>

## <span data-ttu-id="bc795-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc795-144">RELATED LINKS</span></span>