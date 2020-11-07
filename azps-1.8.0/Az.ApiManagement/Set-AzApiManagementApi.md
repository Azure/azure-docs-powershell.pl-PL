---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 190dfb075e16b6b7eaaa0cb6fafd0145b3211654
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869376"
---
# <span data-ttu-id="0db4f-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0db4f-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="0db4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0db4f-102">SYNOPSIS</span></span>
<span data-ttu-id="0db4f-103">Modyfikuje interfejs API.</span><span class="sxs-lookup"><span data-stu-id="0db4f-103">Modifies an API.</span></span>

## <span data-ttu-id="0db4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0db4f-104">SYNTAX</span></span>

### <span data-ttu-id="0db4f-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0db4f-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0db4f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0db4f-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0db4f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0db4f-107">DESCRIPTION</span></span>
<span data-ttu-id="0db4f-108">Polecenie cmdlet **Set-AzApiManagementApi** modyfikuje interfejs API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="0db4f-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="0db4f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0db4f-109">EXAMPLES</span></span>

### <span data-ttu-id="0db4f-110">Przykład 1 modyfikowanie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="0db4f-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="0db4f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0db4f-111">PARAMETERS</span></span>

### <span data-ttu-id="0db4f-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0db4f-112">-ApiId</span></span>
<span data-ttu-id="0db4f-113">Określa identyfikator interfejsu API do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="0db4f-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="0db4f-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="0db4f-114">-AuthorizationScope</span></span>
<span data-ttu-id="0db4f-115">Określa zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="0db4f-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="0db4f-116">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="0db4f-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="0db4f-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="0db4f-117">-AuthorizationServerId</span></span>
<span data-ttu-id="0db4f-118">Określa identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="0db4f-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="0db4f-119">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="0db4f-119">The default value is $Null.</span></span>
<span data-ttu-id="0db4f-120">Ten parametr należy określić, jeśli *AuthorizationScope* jest określony.</span><span class="sxs-lookup"><span data-stu-id="0db4f-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="0db4f-121">-Context</span><span class="sxs-lookup"><span data-stu-id="0db4f-121">-Context</span></span>
<span data-ttu-id="0db4f-122">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0db4f-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0db4f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db4f-123">-DefaultProfile</span></span>
<span data-ttu-id="0db4f-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0db4f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0db4f-125">— Opis</span><span class="sxs-lookup"><span data-stu-id="0db4f-125">-Description</span></span>
<span data-ttu-id="0db4f-126">Określa opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0db4f-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="0db4f-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0db4f-127">-InputObject</span></span>
<span data-ttu-id="0db4f-128">Wystąpienie PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="0db4f-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="0db4f-129">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0db4f-129">This parameter is required.</span></span>

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

### <span data-ttu-id="0db4f-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0db4f-130">-Name</span></span>
<span data-ttu-id="0db4f-131">Określa nazwę internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0db4f-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="0db4f-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0db4f-132">-PassThru</span></span>
<span data-ttu-id="0db4f-133">passthru</span><span class="sxs-lookup"><span data-stu-id="0db4f-133">passthru</span></span>

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

### <span data-ttu-id="0db4f-134">-Path</span><span class="sxs-lookup"><span data-stu-id="0db4f-134">-Path</span></span>
<span data-ttu-id="0db4f-135">Określa ścieżkę internetowego interfejsu API, która jest ostatnią częścią publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0db4f-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="0db4f-136">Ten adres URL jest wykorzystywany przez użytkowników korzystających z interfejsu API do wysyłania żądań do usługi sieci Web i musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="0db4f-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="0db4f-137">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="0db4f-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="0db4f-138">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="0db4f-138">-Protocols</span></span>
<span data-ttu-id="0db4f-139">Określa tablicę protokołów API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0db4f-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="0db4f-140">psdx_paramvalues http i https.</span><span class="sxs-lookup"><span data-stu-id="0db4f-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="0db4f-141">To są protokoły sieci Web, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="0db4f-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="0db4f-142">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="0db4f-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="0db4f-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="0db4f-143">-ServiceUrl</span></span>
<span data-ttu-id="0db4f-144">Określa adres URL usługi sieci Web, która udostępnia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="0db4f-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="0db4f-145">Ten adres URL jest wykorzystywany tylko przez usługę Azure API Management i nie został podany jako publiczny.</span><span class="sxs-lookup"><span data-stu-id="0db4f-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="0db4f-146">Adres URL musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="0db4f-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="0db4f-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="0db4f-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="0db4f-148">Określa nazwę nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0db4f-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="0db4f-149">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="0db4f-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="0db4f-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="0db4f-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="0db4f-151">Określa nazwę parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0db4f-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="0db4f-152">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="0db4f-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="0db4f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db4f-153">CommonParameters</span></span>
<span data-ttu-id="0db4f-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db4f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db4f-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db4f-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db4f-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0db4f-156">INPUTS</span></span>

### <span data-ttu-id="0db4f-157">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0db4f-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0db4f-158">System. String</span><span class="sxs-lookup"><span data-stu-id="0db4f-158">System.String</span></span>

### <span data-ttu-id="0db4f-159">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0db4f-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="0db4f-160">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="0db4f-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="0db4f-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0db4f-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0db4f-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0db4f-162">OUTPUTS</span></span>

### <span data-ttu-id="0db4f-163">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0db4f-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="0db4f-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0db4f-164">NOTES</span></span>

## <span data-ttu-id="0db4f-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0db4f-165">RELATED LINKS</span></span>

[<span data-ttu-id="0db4f-166">Eksportowanie — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0db4f-166">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="0db4f-167">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0db4f-167">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="0db4f-168">Import — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0db4f-168">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="0db4f-169">Nowe — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0db4f-169">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="0db4f-170">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0db4f-170">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


