---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 0d2d9d9390f60c7d7eb74061a52b9b437acdf772
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528050"
---
# <span data-ttu-id="881b8-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="881b8-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="881b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="881b8-102">SYNOPSIS</span></span>
<span data-ttu-id="881b8-103">Tworzy konfigurację przekierowania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="881b8-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="881b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="881b8-104">SYNTAX</span></span>

### <span data-ttu-id="881b8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="881b8-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="881b8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="881b8-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="881b8-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="881b8-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="881b8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="881b8-108">DESCRIPTION</span></span>
<span data-ttu-id="881b8-109">Polecenie cmdlet **New-AzureRmApplicationGatewayRedirectConfiguration** umożliwia utworzenie konfiguracji przekierowywania dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="881b8-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="881b8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="881b8-110">EXAMPLES</span></span>

### <span data-ttu-id="881b8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="881b8-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="881b8-112">To polecenie tworzy konfigurację przekierowania o nazwie Redirect01 i zapisuje wynik w zmiennej o nazwie $RedirectConfig.</span><span class="sxs-lookup"><span data-stu-id="881b8-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="881b8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="881b8-113">PARAMETERS</span></span>

### <span data-ttu-id="881b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="881b8-114">-DefaultProfile</span></span>
<span data-ttu-id="881b8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="881b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="881b8-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="881b8-116">-IncludePath</span></span>
<span data-ttu-id="881b8-117">Dołącz ścieżkę w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="881b8-117">Include path in the redirected url.</span></span>
<span data-ttu-id="881b8-118">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="881b8-118">Default is true.</span></span>

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

### <span data-ttu-id="881b8-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="881b8-119">-IncludeQueryString</span></span>
<span data-ttu-id="881b8-120">Uwzględnij ciąg zapytania w przekierowanym adresie URL.</span><span class="sxs-lookup"><span data-stu-id="881b8-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="881b8-121">Wartość domyślna to prawda.</span><span class="sxs-lookup"><span data-stu-id="881b8-121">Default is true.</span></span>

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

### <span data-ttu-id="881b8-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="881b8-122">-Name</span></span>
<span data-ttu-id="881b8-123">Nazwa konfiguracji przekierowania</span><span class="sxs-lookup"><span data-stu-id="881b8-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="881b8-124">-Redirecttype</span><span class="sxs-lookup"><span data-stu-id="881b8-124">-RedirectType</span></span>
<span data-ttu-id="881b8-125">Typ przekierowania</span><span class="sxs-lookup"><span data-stu-id="881b8-125">The type of redirect</span></span>

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

### <span data-ttu-id="881b8-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="881b8-126">-TargetListener</span></span>
<span data-ttu-id="881b8-127">HTTPListener, aby przekierować żądanie do</span><span class="sxs-lookup"><span data-stu-id="881b8-127">HTTPListener to redirect the request to</span></span>

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

### <span data-ttu-id="881b8-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="881b8-128">-TargetListenerID</span></span>
<span data-ttu-id="881b8-129">Identyfikator odbiornika, do którego ma zostać przekierowana prośba o</span><span class="sxs-lookup"><span data-stu-id="881b8-129">ID of  listener to redirect the request to</span></span>

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

### <span data-ttu-id="881b8-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="881b8-130">-TargetUrl</span></span>
<span data-ttu-id="881b8-131">Docelowy adres URL, przekierowanie</span><span class="sxs-lookup"><span data-stu-id="881b8-131">Target URL fo redirection</span></span>

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

### <span data-ttu-id="881b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="881b8-132">CommonParameters</span></span>
<span data-ttu-id="881b8-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="881b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="881b8-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="881b8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="881b8-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="881b8-135">INPUTS</span></span>

### <span data-ttu-id="881b8-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="881b8-136">None</span></span>

## <span data-ttu-id="881b8-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="881b8-137">OUTPUTS</span></span>

### <span data-ttu-id="881b8-138">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="881b8-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="881b8-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="881b8-139">NOTES</span></span>

## <span data-ttu-id="881b8-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="881b8-140">RELATED LINKS</span></span>

