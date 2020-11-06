---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 10df1034b414260cb618c7de0b31b8ad93d30d0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550384"
---
# <span data-ttu-id="cd596-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd596-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="cd596-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd596-102">SYNOPSIS</span></span>
<span data-ttu-id="cd596-103">Modyfikuje interfejs API.</span><span class="sxs-lookup"><span data-stu-id="cd596-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd596-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd596-104">SYNTAX</span></span>

### <span data-ttu-id="cd596-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd596-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd596-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cd596-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd596-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cd596-107">DESCRIPTION</span></span>
<span data-ttu-id="cd596-108">Polecenie cmdlet **Set-AzureRmApiManagementApi** modyfikuje interfejs API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="cd596-108">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="cd596-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd596-109">EXAMPLES</span></span>

### <span data-ttu-id="cd596-110">Przykład 1 modyfikowanie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="cd596-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="cd596-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd596-111">PARAMETERS</span></span>

### <span data-ttu-id="cd596-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cd596-112">-ApiId</span></span>
<span data-ttu-id="cd596-113">Określa identyfikator interfejsu API do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="cd596-113">Specifies the ID of the API to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd596-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="cd596-114">-AuthorizationScope</span></span>
<span data-ttu-id="cd596-115">Określa zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="cd596-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="cd596-116">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="cd596-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="cd596-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="cd596-117">-AuthorizationServerId</span></span>
<span data-ttu-id="cd596-118">Określa identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="cd596-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="cd596-119">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="cd596-119">The default value is $Null.</span></span>
<span data-ttu-id="cd596-120">Ten parametr należy określić, jeśli *AuthorizationScope* jest określony.</span><span class="sxs-lookup"><span data-stu-id="cd596-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="cd596-121">-Context</span><span class="sxs-lookup"><span data-stu-id="cd596-121">-Context</span></span>
<span data-ttu-id="cd596-122">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cd596-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd596-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd596-123">-DefaultProfile</span></span>
<span data-ttu-id="cd596-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd596-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd596-125">— Opis</span><span class="sxs-lookup"><span data-stu-id="cd596-125">-Description</span></span>
<span data-ttu-id="cd596-126">Określa opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="cd596-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="cd596-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cd596-127">-InputObject</span></span>
<span data-ttu-id="cd596-128">Wystąpienie PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="cd596-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="cd596-129">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="cd596-129">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd596-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd596-130">-Name</span></span>
<span data-ttu-id="cd596-131">Określa nazwę internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="cd596-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="cd596-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd596-132">-PassThru</span></span>
<span data-ttu-id="cd596-133">passthru</span><span class="sxs-lookup"><span data-stu-id="cd596-133">passthru</span></span>

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

### <span data-ttu-id="cd596-134">-Path</span><span class="sxs-lookup"><span data-stu-id="cd596-134">-Path</span></span>
<span data-ttu-id="cd596-135">Określa ścieżkę internetowego interfejsu API, która jest ostatnią częścią publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="cd596-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="cd596-136">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API do wysyłania żądań do usługi sieci Web i musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="cd596-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="cd596-137">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="cd596-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="cd596-138">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="cd596-138">-Protocols</span></span>
<span data-ttu-id="cd596-139">Określa tablicę protokołów API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="cd596-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="cd596-140">psdx_paramvalues http i https.</span><span class="sxs-lookup"><span data-stu-id="cd596-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="cd596-141">To są protokoły sieci Web, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="cd596-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="cd596-142">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="cd596-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="cd596-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="cd596-143">-ServiceUrl</span></span>
<span data-ttu-id="cd596-144">Określa adres URL usługi sieci Web, która udostępnia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="cd596-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="cd596-145">Ten adres URL jest wykorzystywany tylko przez usługę Azure API Management i nie został podany jako publiczny.</span><span class="sxs-lookup"><span data-stu-id="cd596-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="cd596-146">Adres URL musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="cd596-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="cd596-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="cd596-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="cd596-148">Określa nazwę nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cd596-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="cd596-149">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="cd596-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="cd596-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="cd596-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="cd596-151">Określa nazwę parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cd596-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="cd596-152">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="cd596-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="cd596-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd596-153">CommonParameters</span></span>
<span data-ttu-id="cd596-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd596-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd596-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd596-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd596-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd596-156">INPUTS</span></span>

### <span data-ttu-id="cd596-157">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cd596-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cd596-158">System. String</span><span class="sxs-lookup"><span data-stu-id="cd596-158">System.String</span></span>

### <span data-ttu-id="cd596-159">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd596-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="cd596-160">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd596-160">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="cd596-161">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="cd596-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="cd596-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cd596-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cd596-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd596-163">OUTPUTS</span></span>

### <span data-ttu-id="cd596-164">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd596-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="cd596-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd596-165">NOTES</span></span>

## <span data-ttu-id="cd596-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd596-166">RELATED LINKS</span></span>

[<span data-ttu-id="cd596-167">Eksportowanie — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd596-167">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="cd596-168">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd596-168">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="cd596-169">Import — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd596-169">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="cd596-170">Nowe — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd596-170">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="cd596-171">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="cd596-171">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


