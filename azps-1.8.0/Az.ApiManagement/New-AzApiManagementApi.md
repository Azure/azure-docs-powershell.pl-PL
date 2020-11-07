---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 43793ef7d1d3f9a4e5e63687e1eaf785d237e86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704616"
---
# <span data-ttu-id="87ae6-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="87ae6-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="87ae6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="87ae6-103">Tworzy interfejs API.</span><span class="sxs-lookup"><span data-stu-id="87ae6-103">Creates an API.</span></span>

## <span data-ttu-id="87ae6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87ae6-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87ae6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87ae6-105">DESCRIPTION</span></span>
<span data-ttu-id="87ae6-106">Polecenie cmdlet **New-AzApiManagementApi** tworzy interfejs API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="87ae6-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="87ae6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87ae6-107">EXAMPLES</span></span>

### <span data-ttu-id="87ae6-108">Przykład 1. Tworzenie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="87ae6-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="87ae6-109">To polecenie tworzy interfejs API o nazwie EchoApi z określonym adresem URL.</span><span class="sxs-lookup"><span data-stu-id="87ae6-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="87ae6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87ae6-110">PARAMETERS</span></span>

### <span data-ttu-id="87ae6-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="87ae6-111">-ApiId</span></span>
<span data-ttu-id="87ae6-112">Określa identyfikator interfejsu API, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="87ae6-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="87ae6-113">Jeśli nie określisz tego parametru, to polecenie cmdlet wygeneruje identyfikator.</span><span class="sxs-lookup"><span data-stu-id="87ae6-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="87ae6-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="87ae6-114">-AuthorizationScope</span></span>
<span data-ttu-id="87ae6-115">Określa zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="87ae6-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="87ae6-116">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="87ae6-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="87ae6-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="87ae6-117">-AuthorizationServerId</span></span>
<span data-ttu-id="87ae6-118">Określa identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="87ae6-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="87ae6-119">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="87ae6-119">The default value is $Null.</span></span>
<span data-ttu-id="87ae6-120">Ten parametr należy określić, jeśli *AuthorizationScope* jest określony.</span><span class="sxs-lookup"><span data-stu-id="87ae6-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="87ae6-121">-Context</span><span class="sxs-lookup"><span data-stu-id="87ae6-121">-Context</span></span>
<span data-ttu-id="87ae6-122">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="87ae6-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="87ae6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ae6-123">-DefaultProfile</span></span>
<span data-ttu-id="87ae6-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87ae6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87ae6-125">— Opis</span><span class="sxs-lookup"><span data-stu-id="87ae6-125">-Description</span></span>
<span data-ttu-id="87ae6-126">Określa opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="87ae6-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="87ae6-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87ae6-127">-Name</span></span>
<span data-ttu-id="87ae6-128">Określa nazwę internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="87ae6-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="87ae6-129">Jest to publiczna nazwa interfejsu API, która jest wyświetlana w portalach dewelopera i administratora.</span><span class="sxs-lookup"><span data-stu-id="87ae6-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="87ae6-130">-Path</span><span class="sxs-lookup"><span data-stu-id="87ae6-130">-Path</span></span>
<span data-ttu-id="87ae6-131">Określa ścieżkę internetowego interfejsu API, która jest ostatnią częścią publicznego adresu URL interfejsu API i odpowiada polu sufiksu adresu URL interfejsu API sieci Web w portalu administracyjnym.</span><span class="sxs-lookup"><span data-stu-id="87ae6-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="87ae6-132">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API do wysyłania żądań do usługi sieci Web i musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="87ae6-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="87ae6-133">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="87ae6-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="87ae6-134">-ProductId</span><span class="sxs-lookup"><span data-stu-id="87ae6-134">-ProductIds</span></span>
<span data-ttu-id="87ae6-135">Określa tablicę identyfikatorów produktów, do których ma zostać dodany nowy interfejs API.</span><span class="sxs-lookup"><span data-stu-id="87ae6-135">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="87ae6-136">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="87ae6-136">-Protocols</span></span>
<span data-ttu-id="87ae6-137">Określa tablicę protokołów API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="87ae6-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="87ae6-138">Prawidłowe wartości to http, https.</span><span class="sxs-lookup"><span data-stu-id="87ae6-138">Valid values are http, https.</span></span>
<span data-ttu-id="87ae6-139">To są protokoły sieci Web, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="87ae6-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="87ae6-140">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="87ae6-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="87ae6-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="87ae6-141">-ServiceUrl</span></span>
<span data-ttu-id="87ae6-142">Określa adres URL usługi sieci Web, która udostępnia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="87ae6-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="87ae6-143">Ten adres URL jest wykorzystywany tylko przez usługę Azure API Management i nie został podany jako publiczny.</span><span class="sxs-lookup"><span data-stu-id="87ae6-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="87ae6-144">Adres URL musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="87ae6-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="87ae6-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="87ae6-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="87ae6-146">Określa nazwę nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="87ae6-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="87ae6-147">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="87ae6-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="87ae6-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="87ae6-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="87ae6-149">Określa nazwę parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="87ae6-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="87ae6-150">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="87ae6-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="87ae6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ae6-151">CommonParameters</span></span>
<span data-ttu-id="87ae6-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87ae6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ae6-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87ae6-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ae6-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87ae6-154">INPUTS</span></span>

### <span data-ttu-id="87ae6-155">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="87ae6-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="87ae6-156">System. String</span><span class="sxs-lookup"><span data-stu-id="87ae6-156">System.String</span></span>

### <span data-ttu-id="87ae6-157">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="87ae6-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="87ae6-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="87ae6-158">System.String[]</span></span>

## <span data-ttu-id="87ae6-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87ae6-159">OUTPUTS</span></span>

### <span data-ttu-id="87ae6-160">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="87ae6-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="87ae6-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87ae6-161">NOTES</span></span>

## <span data-ttu-id="87ae6-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87ae6-162">RELATED LINKS</span></span>

[<span data-ttu-id="87ae6-163">Eksportowanie — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="87ae6-163">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="87ae6-164">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="87ae6-164">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="87ae6-165">Import — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="87ae6-165">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="87ae6-166">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="87ae6-166">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="87ae6-167">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="87ae6-167">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


