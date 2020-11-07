---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 75a6dbf480e8b2f2f3d9f7524db4e57e5ed88f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718964"
---
# <span data-ttu-id="6502d-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6502d-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="6502d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6502d-102">SYNOPSIS</span></span>
<span data-ttu-id="6502d-103">Tworzy interfejs API.</span><span class="sxs-lookup"><span data-stu-id="6502d-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6502d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6502d-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6502d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6502d-105">DESCRIPTION</span></span>
<span data-ttu-id="6502d-106">Polecenie cmdlet **New-AzureRmApiManagementApi** tworzy interfejs API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="6502d-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="6502d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6502d-107">EXAMPLES</span></span>

### <span data-ttu-id="6502d-108">Przykład 1. Tworzenie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="6502d-108">Example 1: Create an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="6502d-109">To polecenie tworzy interfejs API o nazwie EchoApi z określonym adresem URL.</span><span class="sxs-lookup"><span data-stu-id="6502d-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="6502d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6502d-110">PARAMETERS</span></span>

### <span data-ttu-id="6502d-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6502d-111">-ApiId</span></span>
<span data-ttu-id="6502d-112">Określa identyfikator interfejsu API, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="6502d-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="6502d-113">Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje identyfikator.</span><span class="sxs-lookup"><span data-stu-id="6502d-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6502d-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="6502d-114">-AuthorizationScope</span></span>
<span data-ttu-id="6502d-115">Określa zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="6502d-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="6502d-116">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="6502d-116">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6502d-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="6502d-117">-AuthorizationServerId</span></span>
<span data-ttu-id="6502d-118">Określa identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="6502d-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="6502d-119">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="6502d-119">The default value is $Null.</span></span>
<span data-ttu-id="6502d-120">Ten parametr należy określić, jeśli *AuthorizationScope* jest określony.</span><span class="sxs-lookup"><span data-stu-id="6502d-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6502d-121">-Context</span><span class="sxs-lookup"><span data-stu-id="6502d-121">-Context</span></span>
<span data-ttu-id="6502d-122">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6502d-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6502d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6502d-123">-DefaultProfile</span></span>
<span data-ttu-id="6502d-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6502d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="6502d-125">— Opis</span><span class="sxs-lookup"><span data-stu-id="6502d-125">-Description</span></span>
<span data-ttu-id="6502d-126">Określa opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="6502d-126">Specifies a description for the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6502d-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6502d-127">-Name</span></span>
<span data-ttu-id="6502d-128">Określa nazwę internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="6502d-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="6502d-129">Jest to publiczna nazwa interfejsu API, która jest wyświetlana w portalach dewelopera i administratora.</span><span class="sxs-lookup"><span data-stu-id="6502d-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6502d-130">-Path</span><span class="sxs-lookup"><span data-stu-id="6502d-130">-Path</span></span>
<span data-ttu-id="6502d-131">Określa ścieżkę internetowego interfejsu API, która jest ostatnią częścią publicznego adresu URL interfejsu API i odpowiada polu sufiksu adresu URL interfejsu API sieci Web w portalu administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="6502d-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="6502d-132">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API do wysyłania żądań do usługi sieci Web i musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="6502d-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="6502d-133">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="6502d-133">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6502d-134">-ProductId</span><span class="sxs-lookup"><span data-stu-id="6502d-134">-ProductIds</span></span>
<span data-ttu-id="6502d-135">Określa tablicę identyfikatorów produktów, do których ma zostać dodany nowy interfejs API.</span><span class="sxs-lookup"><span data-stu-id="6502d-135">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6502d-136">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="6502d-136">-Protocols</span></span>
<span data-ttu-id="6502d-137">Określa tablicę protokołów API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="6502d-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="6502d-138">Prawidłowe wartości to http, https.</span><span class="sxs-lookup"><span data-stu-id="6502d-138">Valid values are http, https.</span></span>
<span data-ttu-id="6502d-139">To są protokoły sieci Web, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="6502d-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="6502d-140">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="6502d-140">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSchema[]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6502d-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="6502d-141">-ServiceUrl</span></span>
<span data-ttu-id="6502d-142">Określa adres URL usługi sieci Web, która udostępnia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="6502d-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="6502d-143">Ten adres URL jest wykorzystywany tylko przez usługę Azure API Management i nie został podany jako publiczny.</span><span class="sxs-lookup"><span data-stu-id="6502d-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="6502d-144">Adres URL musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="6502d-144">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6502d-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="6502d-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="6502d-146">Określa nazwę nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6502d-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="6502d-147">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="6502d-147">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6502d-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="6502d-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="6502d-149">Określa nazwę parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6502d-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="6502d-150">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="6502d-150">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6502d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6502d-151">CommonParameters</span></span>
<span data-ttu-id="6502d-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6502d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6502d-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6502d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6502d-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6502d-154">INPUTS</span></span>

### <span data-ttu-id="6502d-155">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6502d-155">None</span></span>
<span data-ttu-id="6502d-156">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6502d-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6502d-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6502d-157">OUTPUTS</span></span>

### <span data-ttu-id="6502d-158">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6502d-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="6502d-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6502d-159">NOTES</span></span>

## <span data-ttu-id="6502d-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6502d-160">RELATED LINKS</span></span>

[<span data-ttu-id="6502d-161">Eksportowanie — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6502d-161">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="6502d-162">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6502d-162">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="6502d-163">Import — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6502d-163">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="6502d-164">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6502d-164">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="6502d-165">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6502d-165">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


