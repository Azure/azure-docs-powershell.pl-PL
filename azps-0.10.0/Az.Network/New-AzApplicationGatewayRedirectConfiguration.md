---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 5cf1e01be8d0a76ba8dc319c5241f40613ad4304
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890553"
---
# <span data-ttu-id="71621-101">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="71621-101">New-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="71621-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71621-102">SYNOPSIS</span></span>
<span data-ttu-id="71621-103">Tworzy konfigurację przekierowania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="71621-103">Creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="71621-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71621-104">SYNTAX</span></span>

### <span data-ttu-id="71621-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="71621-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71621-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="71621-106">SetByResource</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71621-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="71621-107">SetByURL</span></span>
```
New-AzApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71621-108">Opis</span><span class="sxs-lookup"><span data-stu-id="71621-108">DESCRIPTION</span></span>
<span data-ttu-id="71621-109">Polecenie cmdlet **New-AzApplicationGatewayRedirectConfiguration** umożliwia utworzenie konfiguracji przekierowywania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="71621-109">**The New-AzApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="71621-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71621-110">EXAMPLES</span></span>

### <span data-ttu-id="71621-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71621-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="71621-112">To polecenie tworzy konfigurację przekierowania o nazwie Redirect01 i zapisuje wynik w zmiennej o nazwie $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="71621-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="71621-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71621-113">PARAMETERS</span></span>

### <span data-ttu-id="71621-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71621-114">-DefaultProfile</span></span>
<span data-ttu-id="71621-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71621-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71621-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="71621-116">-IncludePath</span></span>
<span data-ttu-id="71621-117">Dołącz ścieżkę w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="71621-117">Include path in the redirected url.</span></span>
<span data-ttu-id="71621-118">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="71621-118">Default is true.</span></span>

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

### <span data-ttu-id="71621-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="71621-119">-IncludeQueryString</span></span>
<span data-ttu-id="71621-120">Uwzględnij ciąg zapytania w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="71621-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="71621-121">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="71621-121">Default is true.</span></span>

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

### <span data-ttu-id="71621-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71621-122">-Name</span></span>
<span data-ttu-id="71621-123">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="71621-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="71621-124">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="71621-124">-RedirectType</span></span>
<span data-ttu-id="71621-125">Typ przekierowania</span><span class="sxs-lookup"><span data-stu-id="71621-125">The type of redirect</span></span>

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

### <span data-ttu-id="71621-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="71621-126">-TargetListener</span></span>
<span data-ttu-id="71621-127">HTTPListener, aby przekierować żądanie do</span><span class="sxs-lookup"><span data-stu-id="71621-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="71621-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="71621-128">-TargetListenerID</span></span>
<span data-ttu-id="71621-129">Identyfikator odbiornika, do którego ma zostać przekierowana prośba o</span><span class="sxs-lookup"><span data-stu-id="71621-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="71621-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="71621-130">-TargetUrl</span></span>
<span data-ttu-id="71621-131">Docelowy adres URL, przekierowanie</span><span class="sxs-lookup"><span data-stu-id="71621-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="71621-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71621-132">CommonParameters</span></span>
<span data-ttu-id="71621-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71621-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71621-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71621-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71621-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71621-135">INPUTS</span></span>

### <span data-ttu-id="71621-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="71621-136">None</span></span>

## <span data-ttu-id="71621-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71621-137">OUTPUTS</span></span>

### <span data-ttu-id="71621-138">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="71621-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="71621-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71621-139">NOTES</span></span>

## <span data-ttu-id="71621-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71621-140">RELATED LINKS</span></span>

