---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 1816b7407ec1d36f8eb5fd213484e22a9e89998c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897638"
---
# <span data-ttu-id="4b5ed-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b5ed-101">Add-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="4b5ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b5ed-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5ed-103">Dodaje konfigurację przekierowania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4b5ed-103">Adds a redirect configuration to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b5ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b5ed-104">SYNTAX</span></span>

### <span data-ttu-id="4b5ed-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4b5ed-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b5ed-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4b5ed-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b5ed-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="4b5ed-107">SetByURL</span></span>
```
Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b5ed-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4b5ed-108">DESCRIPTION</span></span>
<span data-ttu-id="4b5ed-109">Polecenie cmdlet **Add-AzureRmApplicationGatewayRedirectConfiguration** umożliwia dodanie konfiguracji przekierowania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4b5ed-109">The **Add-AzureRmApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="4b5ed-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b5ed-110">EXAMPLES</span></span>

### <span data-ttu-id="4b5ed-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4b5ed-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="4b5ed-112">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4b5ed-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4b5ed-113">Drugie polecenie dodaje konfigurację przekierowania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4b5ed-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="4b5ed-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b5ed-114">PARAMETERS</span></span>

### <span data-ttu-id="4b5ed-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b5ed-115">-ApplicationGateway</span></span>
<span data-ttu-id="4b5ed-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b5ed-116">The applicationGateway</span></span>

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

### <span data-ttu-id="4b5ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5ed-117">-DefaultProfile</span></span>
<span data-ttu-id="4b5ed-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b5ed-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b5ed-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="4b5ed-119">-IncludePath</span></span>
<span data-ttu-id="4b5ed-120">Dołącz ścieżkę w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="4b5ed-120">Include path in the redirected url.</span></span>
<span data-ttu-id="4b5ed-121">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="4b5ed-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b5ed-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="4b5ed-122">-IncludeQueryString</span></span>
<span data-ttu-id="4b5ed-123">Uwzględnij ciąg zapytania w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="4b5ed-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="4b5ed-124">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="4b5ed-124">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b5ed-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4b5ed-125">-Name</span></span>
<span data-ttu-id="4b5ed-126">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="4b5ed-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="4b5ed-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="4b5ed-127">-RedirectType</span></span>
<span data-ttu-id="4b5ed-128">Typ przekierowania</span><span class="sxs-lookup"><span data-stu-id="4b5ed-128">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b5ed-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="4b5ed-129">-TargetListener</span></span>
<span data-ttu-id="4b5ed-130">HTTPListener, aby przekierować żądanie do</span><span class="sxs-lookup"><span data-stu-id="4b5ed-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="4b5ed-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="4b5ed-131">-TargetListenerID</span></span>
<span data-ttu-id="4b5ed-132">Identyfikator odbiornika, do którego ma zostać przekierowana prośba o</span><span class="sxs-lookup"><span data-stu-id="4b5ed-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="4b5ed-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="4b5ed-133">-TargetUrl</span></span>
<span data-ttu-id="4b5ed-134">Docelowy adres URL, przekierowanie</span><span class="sxs-lookup"><span data-stu-id="4b5ed-134">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b5ed-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5ed-135">CommonParameters</span></span>
<span data-ttu-id="4b5ed-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b5ed-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5ed-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b5ed-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5ed-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b5ed-138">INPUTS</span></span>

### <span data-ttu-id="4b5ed-139">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b5ed-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4b5ed-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b5ed-140">OUTPUTS</span></span>

### <span data-ttu-id="4b5ed-141">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b5ed-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4b5ed-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b5ed-142">NOTES</span></span>

## <span data-ttu-id="4b5ed-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b5ed-143">RELATED LINKS</span></span>

