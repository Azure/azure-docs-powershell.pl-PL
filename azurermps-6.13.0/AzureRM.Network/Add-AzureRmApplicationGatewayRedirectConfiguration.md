---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 01f7daf47fa62e346dc7323ee5978f81f5797e29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719416"
---
# <span data-ttu-id="1e2b0-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e2b0-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="1e2b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e2b0-102">SYNOPSIS</span></span>
<span data-ttu-id="1e2b0-103">Dodaje konfigurację przekierowania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1e2b0-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e2b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e2b0-104">SYNTAX</span></span>

### <span data-ttu-id="1e2b0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e2b0-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e2b0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1e2b0-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e2b0-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="1e2b0-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e2b0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1e2b0-108">DESCRIPTION</span></span>
<span data-ttu-id="1e2b0-109">Polecenie cmdlet **Add-AzureRmApplicationGatewayRedirectConfiguration** umożliwia dodanie konfiguracji przekierowania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1e2b0-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="1e2b0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e2b0-110">EXAMPLES</span></span>

### <span data-ttu-id="1e2b0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1e2b0-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="1e2b0-112">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1e2b0-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1e2b0-113">Drugie polecenie dodaje konfigurację przekierowania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1e2b0-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="1e2b0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e2b0-114">PARAMETERS</span></span>

### <span data-ttu-id="1e2b0-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e2b0-115">-ApplicationGateway</span></span>
<span data-ttu-id="1e2b0-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e2b0-116">The applicationGateway</span></span>

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

### <span data-ttu-id="1e2b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e2b0-117">-DefaultProfile</span></span>
<span data-ttu-id="1e2b0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e2b0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e2b0-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="1e2b0-119">-IncludePath</span></span>
<span data-ttu-id="1e2b0-120">Dołącz ścieżkę w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="1e2b0-120">Include path in the redirected url.</span></span>
<span data-ttu-id="1e2b0-121">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="1e2b0-121">Default is true.</span></span>

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

### <span data-ttu-id="1e2b0-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="1e2b0-122">-IncludeQueryString</span></span>
<span data-ttu-id="1e2b0-123">Uwzględnij ciąg zapytania w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="1e2b0-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="1e2b0-124">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="1e2b0-124">Default is true.</span></span>

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

### <span data-ttu-id="1e2b0-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1e2b0-125">-Name</span></span>
<span data-ttu-id="1e2b0-126">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="1e2b0-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="1e2b0-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="1e2b0-127">-RedirectType</span></span>
<span data-ttu-id="1e2b0-128">Typ przekierowania</span><span class="sxs-lookup"><span data-stu-id="1e2b0-128">The type of redirect</span></span>

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

### <span data-ttu-id="1e2b0-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="1e2b0-129">-TargetListener</span></span>
<span data-ttu-id="1e2b0-130">HTTPListener, aby przekierować żądanie do</span><span class="sxs-lookup"><span data-stu-id="1e2b0-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="1e2b0-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="1e2b0-131">-TargetListenerID</span></span>
<span data-ttu-id="1e2b0-132">Identyfikator odbiornika, do którego ma zostać przekierowana prośba o</span><span class="sxs-lookup"><span data-stu-id="1e2b0-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="1e2b0-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="1e2b0-133">-TargetUrl</span></span>
<span data-ttu-id="1e2b0-134">Docelowy adres URL, przekierowanie</span><span class="sxs-lookup"><span data-stu-id="1e2b0-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="1e2b0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e2b0-135">CommonParameters</span></span>
<span data-ttu-id="1e2b0-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e2b0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e2b0-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e2b0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e2b0-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e2b0-138">INPUTS</span></span>

### <span data-ttu-id="1e2b0-139">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e2b0-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="1e2b0-140">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1e2b0-140">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="1e2b0-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e2b0-141">OUTPUTS</span></span>

### <span data-ttu-id="1e2b0-142">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e2b0-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1e2b0-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e2b0-143">NOTES</span></span>

## <span data-ttu-id="1e2b0-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e2b0-144">RELATED LINKS</span></span>
