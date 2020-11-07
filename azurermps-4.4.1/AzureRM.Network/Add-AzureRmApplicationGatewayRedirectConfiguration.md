---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 449c3999a3041be819b9f5f665054969223c1557
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718521"
---
# <span data-ttu-id="74a4e-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="74a4e-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="74a4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74a4e-102">SYNOPSIS</span></span>
<span data-ttu-id="74a4e-103">Dodaje konfigurację przekierowania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="74a4e-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74a4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74a4e-104">SYNTAX</span></span>

### <span data-ttu-id="74a4e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="74a4e-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74a4e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="74a4e-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74a4e-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="74a4e-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74a4e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="74a4e-108">DESCRIPTION</span></span>
<span data-ttu-id="74a4e-109">Polecenie cmdlet **Add-AzureRmApplicationGatewayRedirectConfiguration** umożliwia dodanie konfiguracji przekierowania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="74a4e-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="74a4e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74a4e-110">EXAMPLES</span></span>

### <span data-ttu-id="74a4e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="74a4e-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="74a4e-112">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="74a4e-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="74a4e-113">Drugie polecenie dodaje konfigurację przekierowania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="74a4e-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="74a4e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74a4e-114">PARAMETERS</span></span>

### <span data-ttu-id="74a4e-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74a4e-115">-ApplicationGateway</span></span>
<span data-ttu-id="74a4e-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74a4e-116">The applicationGateway</span></span>

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

### <span data-ttu-id="74a4e-117">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="74a4e-117">-IncludePath</span></span>
<span data-ttu-id="74a4e-118">Dołącz ścieżkę w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="74a4e-118">Include path in the redirected url.</span></span>
<span data-ttu-id="74a4e-119">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="74a4e-119">Default is true.</span></span>

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

### <span data-ttu-id="74a4e-120">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="74a4e-120">-IncludeQueryString</span></span>
<span data-ttu-id="74a4e-121">Uwzględnij ciąg zapytania w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="74a4e-121">Include query string in the redirected url.</span></span>
<span data-ttu-id="74a4e-122">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="74a4e-122">Default is true.</span></span>

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

### <span data-ttu-id="74a4e-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74a4e-123">-Name</span></span>
<span data-ttu-id="74a4e-124">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="74a4e-124">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="74a4e-125">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="74a4e-125">-RedirectType</span></span>
<span data-ttu-id="74a4e-126">Typ przekierowania</span><span class="sxs-lookup"><span data-stu-id="74a4e-126">The type of redirect</span></span>

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

### <span data-ttu-id="74a4e-127">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="74a4e-127">-TargetListener</span></span>
<span data-ttu-id="74a4e-128">HTTPListener, aby przekierować żądanie do</span><span class="sxs-lookup"><span data-stu-id="74a4e-128">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="74a4e-129">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="74a4e-129">-TargetListenerID</span></span>
<span data-ttu-id="74a4e-130">Identyfikator odbiornika, do którego ma zostać przekierowana prośba o</span><span class="sxs-lookup"><span data-stu-id="74a4e-130">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="74a4e-131">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="74a4e-131">-TargetUrl</span></span>
<span data-ttu-id="74a4e-132">Docelowy adres URL, przekierowanie</span><span class="sxs-lookup"><span data-stu-id="74a4e-132">Target URL fo redirection</span></span>

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

### <span data-ttu-id="74a4e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a4e-133">-DefaultProfile</span></span>
<span data-ttu-id="74a4e-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74a4e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74a4e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a4e-135">CommonParameters</span></span>
<span data-ttu-id="74a4e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74a4e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a4e-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74a4e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a4e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74a4e-138">INPUTS</span></span>

### <span data-ttu-id="74a4e-139">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74a4e-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="74a4e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74a4e-140">OUTPUTS</span></span>

### <span data-ttu-id="74a4e-141">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74a4e-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="74a4e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74a4e-142">NOTES</span></span>

## <span data-ttu-id="74a4e-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74a4e-143">RELATED LINKS</span></span>

