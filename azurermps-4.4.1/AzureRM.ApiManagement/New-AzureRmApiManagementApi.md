---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 295551f9d4ddf751980ec81626e3714a37aa47a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547239"
---
# <span data-ttu-id="45707-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="45707-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="45707-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45707-102">SYNOPSIS</span></span>
<span data-ttu-id="45707-103">Tworzy interfejs API.</span><span class="sxs-lookup"><span data-stu-id="45707-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45707-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45707-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45707-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45707-105">DESCRIPTION</span></span>
<span data-ttu-id="45707-106">Polecenie cmdlet **New-AzureRmApiManagementApi** tworzy interfejs API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="45707-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="45707-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45707-107">EXAMPLES</span></span>

### <span data-ttu-id="45707-108">Przykład 1. Tworzenie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="45707-108">Example 1: Create an API</span></span>
```
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="45707-109">To polecenie tworzy interfejs API o nazwie EchoApi z określonym adresem URL.</span><span class="sxs-lookup"><span data-stu-id="45707-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="45707-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45707-110">PARAMETERS</span></span>

### <span data-ttu-id="45707-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="45707-111">-ApiId</span></span>
<span data-ttu-id="45707-112">Określa identyfikator interfejsu API, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="45707-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="45707-113">Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje identyfikator.</span><span class="sxs-lookup"><span data-stu-id="45707-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45707-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="45707-114">-AuthorizationScope</span></span>
<span data-ttu-id="45707-115">Określa zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="45707-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="45707-116">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="45707-116">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45707-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="45707-117">-AuthorizationServerId</span></span>
<span data-ttu-id="45707-118">Określa identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="45707-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="45707-119">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="45707-119">The default value is $Null.</span></span>
<span data-ttu-id="45707-120">Ten parametr należy określić, jeśli *AuthorizationScope* jest określony.</span><span class="sxs-lookup"><span data-stu-id="45707-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45707-121">-Context</span><span class="sxs-lookup"><span data-stu-id="45707-121">-Context</span></span>
<span data-ttu-id="45707-122">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="45707-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45707-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="45707-123">-Description</span></span>
<span data-ttu-id="45707-124">Określa opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="45707-124">Specifies a description for the web API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45707-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45707-125">-Name</span></span>
<span data-ttu-id="45707-126">Określa nazwę internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="45707-126">Specifies the name of the web API.</span></span>
<span data-ttu-id="45707-127">Jest to publiczna nazwa interfejsu API, która jest wyświetlana w portalach dewelopera i administratora.</span><span class="sxs-lookup"><span data-stu-id="45707-127">This is the public name of the API as it appears on the developer and admin portals.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45707-128">-Path</span><span class="sxs-lookup"><span data-stu-id="45707-128">-Path</span></span>
<span data-ttu-id="45707-129">Określa ścieżkę internetowego interfejsu API, która jest ostatnią częścią publicznego adresu URL interfejsu API i odpowiada polu sufiksu adresu URL interfejsu API sieci Web w portalu administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="45707-129">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="45707-130">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API do wysyłania żądań do usługi sieci Web i musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="45707-130">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="45707-131">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="45707-131">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45707-132">-ProductId</span><span class="sxs-lookup"><span data-stu-id="45707-132">-ProductIds</span></span>
<span data-ttu-id="45707-133">Określa tablicę identyfikatorów produktów, do których ma zostać dodany nowy interfejs API.</span><span class="sxs-lookup"><span data-stu-id="45707-133">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45707-134">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="45707-134">-Protocols</span></span>
<span data-ttu-id="45707-135">Określa tablicę protokołów API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="45707-135">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="45707-136">Prawidłowe wartości to http, https.</span><span class="sxs-lookup"><span data-stu-id="45707-136">Valid values are http, https.</span></span>
<span data-ttu-id="45707-137">To są protokoły sieci Web, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="45707-137">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="45707-138">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="45707-138">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45707-139">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="45707-139">-ServiceUrl</span></span>
<span data-ttu-id="45707-140">Określa adres URL usługi sieci Web, która udostępnia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="45707-140">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="45707-141">Ten adres URL jest wykorzystywany tylko przez usługę Azure API Management i nie został podany jako publiczny.</span><span class="sxs-lookup"><span data-stu-id="45707-141">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="45707-142">Adres URL musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="45707-142">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45707-143">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="45707-143">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="45707-144">Określa nazwę nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="45707-144">Specifies the subscription key header name.</span></span>
<span data-ttu-id="45707-145">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="45707-145">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45707-146">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="45707-146">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="45707-147">Określa nazwę parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="45707-147">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="45707-148">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="45707-148">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45707-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45707-149">-DefaultProfile</span></span>
<span data-ttu-id="45707-150">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45707-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45707-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45707-151">CommonParameters</span></span>
<span data-ttu-id="45707-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45707-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45707-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45707-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45707-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45707-154">INPUTS</span></span>

## <span data-ttu-id="45707-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45707-155">OUTPUTS</span></span>

### <span data-ttu-id="45707-156">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="45707-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="45707-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45707-157">NOTES</span></span>

## <span data-ttu-id="45707-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45707-158">RELATED LINKS</span></span>

[<span data-ttu-id="45707-159">Eksportowanie — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="45707-159">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="45707-160">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="45707-160">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="45707-161">Import — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="45707-161">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="45707-162">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="45707-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="45707-163">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="45707-163">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


