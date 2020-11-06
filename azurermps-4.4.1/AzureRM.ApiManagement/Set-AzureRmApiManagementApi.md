---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 4c9dc60ad1c531a5da9f32abc0090475c32a7ad5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552448"
---
# <span data-ttu-id="a5429-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a5429-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="a5429-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5429-102">SYNOPSIS</span></span>
<span data-ttu-id="a5429-103">Modyfikuje interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a5429-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5429-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5429-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5429-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a5429-105">DESCRIPTION</span></span>
<span data-ttu-id="a5429-106">Polecenie cmdlet **Set-AzureRmApiManagementApi** modyfikuje interfejs API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="a5429-106">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="a5429-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5429-107">EXAMPLES</span></span>

### <span data-ttu-id="a5429-108">Przykład 1 modyfikowanie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="a5429-108">Example 1 Modify an API</span></span>
```
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="a5429-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5429-109">PARAMETERS</span></span>

### <span data-ttu-id="a5429-110">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a5429-110">-ApiId</span></span>
<span data-ttu-id="a5429-111">Określa identyfikator interfejsu API do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="a5429-111">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="a5429-112">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="a5429-112">-AuthorizationScope</span></span>
<span data-ttu-id="a5429-113">Określa zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="a5429-113">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="a5429-114">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="a5429-114">The default value is $Null.</span></span>

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

### <span data-ttu-id="a5429-115">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="a5429-115">-AuthorizationServerId</span></span>
<span data-ttu-id="a5429-116">Określa identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="a5429-116">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="a5429-117">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="a5429-117">The default value is $Null.</span></span>
<span data-ttu-id="a5429-118">Ten parametr należy określić, jeśli *AuthorizationScope* jest określony.</span><span class="sxs-lookup"><span data-stu-id="a5429-118">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="a5429-119">-Context</span><span class="sxs-lookup"><span data-stu-id="a5429-119">-Context</span></span>
<span data-ttu-id="a5429-120">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a5429-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a5429-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="a5429-121">-Description</span></span>
<span data-ttu-id="a5429-122">Określa opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a5429-122">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="a5429-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5429-123">-Name</span></span>
<span data-ttu-id="a5429-124">Określa nazwę internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a5429-124">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="a5429-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5429-125">-PassThru</span></span>
<span data-ttu-id="a5429-126">passthru</span><span class="sxs-lookup"><span data-stu-id="a5429-126">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5429-127">-Path</span><span class="sxs-lookup"><span data-stu-id="a5429-127">-Path</span></span>
<span data-ttu-id="a5429-128">Określa ścieżkę internetowego interfejsu API, która jest ostatnią częścią publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a5429-128">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="a5429-129">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API do wysyłania żądań do usługi sieci Web i musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="a5429-129">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="a5429-130">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="a5429-130">The default value is $Null.</span></span>

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

### <span data-ttu-id="a5429-131">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="a5429-131">-Protocols</span></span>
<span data-ttu-id="a5429-132">Określa tablicę protokołów API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="a5429-132">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="a5429-133">psdx_paramvalues http i https.</span><span class="sxs-lookup"><span data-stu-id="a5429-133">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="a5429-134">To są protokoły sieci Web, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a5429-134">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="a5429-135">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="a5429-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="a5429-136">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="a5429-136">-ServiceUrl</span></span>
<span data-ttu-id="a5429-137">Określa adres URL usługi sieci Web, która udostępnia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a5429-137">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="a5429-138">Ten adres URL jest wykorzystywany tylko przez usługę Azure API Management i nie został podany jako publiczny.</span><span class="sxs-lookup"><span data-stu-id="a5429-138">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="a5429-139">Adres URL musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="a5429-139">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="a5429-140">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="a5429-140">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="a5429-141">Określa nazwę nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a5429-141">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="a5429-142">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="a5429-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="a5429-143">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="a5429-143">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="a5429-144">Określa nazwę parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a5429-144">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="a5429-145">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="a5429-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="a5429-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5429-146">-DefaultProfile</span></span>
<span data-ttu-id="a5429-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5429-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5429-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5429-148">CommonParameters</span></span>
<span data-ttu-id="a5429-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5429-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5429-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5429-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5429-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5429-151">INPUTS</span></span>

## <span data-ttu-id="a5429-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5429-152">OUTPUTS</span></span>

### <span data-ttu-id="a5429-153">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a5429-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="a5429-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5429-154">NOTES</span></span>

## <span data-ttu-id="a5429-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5429-155">RELATED LINKS</span></span>

[<span data-ttu-id="a5429-156">Eksportowanie — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a5429-156">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="a5429-157">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a5429-157">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="a5429-158">Import — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a5429-158">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="a5429-159">Nowe — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a5429-159">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="a5429-160">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a5429-160">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


