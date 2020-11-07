---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 60b98db10aab4456ea8ca463f49ee3f7f58ffdd2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891009"
---
# <span data-ttu-id="1f51e-101">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f51e-101">Add-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="1f51e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f51e-102">SYNOPSIS</span></span>
<span data-ttu-id="1f51e-103">Dodaje konfigurację przekierowania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f51e-103">Adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="1f51e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f51e-104">SYNTAX</span></span>

### <span data-ttu-id="1f51e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f51e-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f51e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1f51e-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>]
 [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f51e-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="1f51e-107">SetByURL</span></span>
```
Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RedirectType <String> [-TargetUrl <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f51e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1f51e-108">DESCRIPTION</span></span>
<span data-ttu-id="1f51e-109">Polecenie cmdlet **Add-AzApplicationGatewayRedirectConfiguration** umożliwia dodanie konfiguracji przekierowania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f51e-109">The **Add-AzApplicationGatewayRedirectConfiguration** cmdlet adds a redirect configuration to an Application Gateway.</span></span>

## <span data-ttu-id="1f51e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f51e-110">EXAMPLES</span></span>

### <span data-ttu-id="1f51e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1f51e-111">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$Appgw = Add-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="1f51e-112">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1f51e-112">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1f51e-113">Drugie polecenie dodaje konfigurację przekierowania do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1f51e-113">The second command adds the redirect configuration to the application gateway.</span></span>

## <span data-ttu-id="1f51e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f51e-114">PARAMETERS</span></span>

### <span data-ttu-id="1f51e-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f51e-115">-ApplicationGateway</span></span>
<span data-ttu-id="1f51e-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f51e-116">The applicationGateway</span></span>

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

### <span data-ttu-id="1f51e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f51e-117">-DefaultProfile</span></span>
<span data-ttu-id="1f51e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f51e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f51e-119">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="1f51e-119">-IncludePath</span></span>
<span data-ttu-id="1f51e-120">Dołącz ścieżkę w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="1f51e-120">Include path in the redirected url.</span></span>
<span data-ttu-id="1f51e-121">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="1f51e-121">Default is true.</span></span>

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

### <span data-ttu-id="1f51e-122">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="1f51e-122">-IncludeQueryString</span></span>
<span data-ttu-id="1f51e-123">Uwzględnij ciąg zapytania w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="1f51e-123">Include query string in the redirected url.</span></span>
<span data-ttu-id="1f51e-124">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="1f51e-124">Default is true.</span></span>

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

### <span data-ttu-id="1f51e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f51e-125">-Name</span></span>
<span data-ttu-id="1f51e-126">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="1f51e-126">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="1f51e-127">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="1f51e-127">-RedirectType</span></span>
<span data-ttu-id="1f51e-128">Typ przekierowania</span><span class="sxs-lookup"><span data-stu-id="1f51e-128">The type of redirect</span></span>

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

### <span data-ttu-id="1f51e-129">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="1f51e-129">-TargetListener</span></span>
<span data-ttu-id="1f51e-130">HTTPListener, aby przekierować żądanie do</span><span class="sxs-lookup"><span data-stu-id="1f51e-130">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="1f51e-131">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="1f51e-131">-TargetListenerID</span></span>
<span data-ttu-id="1f51e-132">Identyfikator odbiornika, do którego ma zostać przekierowana prośba o</span><span class="sxs-lookup"><span data-stu-id="1f51e-132">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="1f51e-133">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="1f51e-133">-TargetUrl</span></span>
<span data-ttu-id="1f51e-134">Docelowy adres URL, przekierowanie</span><span class="sxs-lookup"><span data-stu-id="1f51e-134">Target URL fo redirection</span></span>

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

### <span data-ttu-id="1f51e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f51e-135">CommonParameters</span></span>
<span data-ttu-id="1f51e-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f51e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f51e-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f51e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f51e-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f51e-138">INPUTS</span></span>

### <span data-ttu-id="1f51e-139">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f51e-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1f51e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f51e-140">OUTPUTS</span></span>

### <span data-ttu-id="1f51e-141">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f51e-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1f51e-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f51e-142">NOTES</span></span>

## <span data-ttu-id="1f51e-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f51e-143">RELATED LINKS</span></span>

