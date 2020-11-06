---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: fe709b560c790ad010469bf2f0a2043231124138
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550383"
---
# <span data-ttu-id="80317-101">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="80317-101">Set-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="80317-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="80317-102">SYNOPSIS</span></span>
<span data-ttu-id="80317-103">Modyfikuje wersję interfejsu API</span><span class="sxs-lookup"><span data-stu-id="80317-103">Modifies an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80317-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="80317-104">SYNTAX</span></span>

### <span data-ttu-id="80317-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="80317-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80317-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="80317-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80317-107">Opis</span><span class="sxs-lookup"><span data-stu-id="80317-107">DESCRIPTION</span></span>
<span data-ttu-id="80317-108">Polecenie cmdlet **Set-AzureRmApiManagementApiRevision** modyfikuje wersję interfejsu API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="80317-108">The **Set-AzureRmApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="80317-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="80317-109">EXAMPLES</span></span>

### <span data-ttu-id="80317-110">Przykład 1 modyfikowanie poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="80317-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="80317-111">Polecenie cmdlet umożliwia zaktualizowanie `2` poprawki interfejsu API `echo-api` o nowy opis, protokół i ścieżkę.</span><span class="sxs-lookup"><span data-stu-id="80317-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="80317-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="80317-112">PARAMETERS</span></span>

### <span data-ttu-id="80317-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="80317-113">-ApiId</span></span>
<span data-ttu-id="80317-114">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="80317-114">Identifier of existing API.</span></span>
<span data-ttu-id="80317-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="80317-115">This parameter is required.</span></span>

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

### <span data-ttu-id="80317-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="80317-116">-ApiRevision</span></span>
<span data-ttu-id="80317-117">Identyfikator istniejącej poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="80317-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="80317-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="80317-118">This parameter is required.</span></span>

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

### <span data-ttu-id="80317-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="80317-119">-AuthorizationScope</span></span>
<span data-ttu-id="80317-120">Zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="80317-120">OAuth operations scope.</span></span>
<span data-ttu-id="80317-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="80317-121">This parameter is optional.</span></span>
<span data-ttu-id="80317-122">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="80317-122">Default value is $null.</span></span>

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

### <span data-ttu-id="80317-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="80317-123">-AuthorizationServerId</span></span>
<span data-ttu-id="80317-124">Identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="80317-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="80317-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="80317-125">This parameter is optional.</span></span>
<span data-ttu-id="80317-126">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="80317-126">Default value is $null.</span></span>
<span data-ttu-id="80317-127">Należy określić, czy AuthorizationScope.</span><span class="sxs-lookup"><span data-stu-id="80317-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="80317-128">-Context</span><span class="sxs-lookup"><span data-stu-id="80317-128">-Context</span></span>
<span data-ttu-id="80317-129">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="80317-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="80317-130">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="80317-130">This parameter is required.</span></span>

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

### <span data-ttu-id="80317-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80317-131">-DefaultProfile</span></span>
<span data-ttu-id="80317-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="80317-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80317-133">— Opis</span><span class="sxs-lookup"><span data-stu-id="80317-133">-Description</span></span>
<span data-ttu-id="80317-134">Opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="80317-134">Web API description.</span></span>
<span data-ttu-id="80317-135">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="80317-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="80317-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="80317-136">-InputObject</span></span>
<span data-ttu-id="80317-137">Wystąpienie PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="80317-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="80317-138">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="80317-138">This parameter is required.</span></span>

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

### <span data-ttu-id="80317-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="80317-139">-Name</span></span>
<span data-ttu-id="80317-140">Nazwa API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="80317-140">Web API name.</span></span>
<span data-ttu-id="80317-141">Publiczna nazwa interfejsu API, która będzie wyświetlana na portalach dewelopera i administratora.</span><span class="sxs-lookup"><span data-stu-id="80317-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="80317-142">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="80317-142">This parameter is required.</span></span>

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

### <span data-ttu-id="80317-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80317-143">-PassThru</span></span>
<span data-ttu-id="80317-144">Jeśli jest określone, wystąpienie systemu Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementApi reprezentujące zestaw interfejsów API.</span><span class="sxs-lookup"><span data-stu-id="80317-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="80317-145">-Path</span><span class="sxs-lookup"><span data-stu-id="80317-145">-Path</span></span>
<span data-ttu-id="80317-146">Ścieżka internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="80317-146">Web API Path.</span></span>
<span data-ttu-id="80317-147">Ostatnia część publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="80317-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="80317-148">Ten adres URL będzie wykorzystywany przez użytkowników korzystających z interfejsu API w celu wysyłania żądań do usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="80317-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="80317-149">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="80317-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="80317-150">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="80317-150">This parameter is optional.</span></span>
<span data-ttu-id="80317-151">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="80317-151">Default value is $null.</span></span>

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

### <span data-ttu-id="80317-152">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="80317-152">-Protocols</span></span>
<span data-ttu-id="80317-153">Protokoły API sieci Web (http, https).</span><span class="sxs-lookup"><span data-stu-id="80317-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="80317-154">Protokoły, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="80317-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="80317-155">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="80317-155">This parameter is required.</span></span>
<span data-ttu-id="80317-156">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="80317-156">Default value is $null.</span></span>

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

### <span data-ttu-id="80317-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="80317-157">-ServiceUrl</span></span>
<span data-ttu-id="80317-158">Adres URL usługi sieci Web, która uwidacznia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="80317-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="80317-159">Ten adres URL będzie wykorzystany tylko przez funkcję zarządzania interfejsem Azure API i nie zostanie udostępniony publicznie.</span><span class="sxs-lookup"><span data-stu-id="80317-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="80317-160">Musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="80317-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="80317-161">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="80317-161">This parameter is required.</span></span>

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

### <span data-ttu-id="80317-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="80317-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="80317-163">Nazwa nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="80317-163">Subscription key header name.</span></span>
<span data-ttu-id="80317-164">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="80317-164">This parameter is optional.</span></span>
<span data-ttu-id="80317-165">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="80317-165">Default value is $null.</span></span>

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

### <span data-ttu-id="80317-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="80317-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="80317-167">Nazwa parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="80317-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="80317-168">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="80317-168">This parameter is optional.</span></span>
<span data-ttu-id="80317-169">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="80317-169">Default value is $null.</span></span>

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

### <span data-ttu-id="80317-170">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="80317-170">-Confirm</span></span>
<span data-ttu-id="80317-171">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80317-171">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80317-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80317-172">-WhatIf</span></span>
<span data-ttu-id="80317-173">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80317-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80317-174">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="80317-174">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80317-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80317-175">CommonParameters</span></span>
<span data-ttu-id="80317-176">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80317-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80317-177">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80317-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80317-178">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="80317-178">INPUTS</span></span>

### <span data-ttu-id="80317-179">System. String</span><span class="sxs-lookup"><span data-stu-id="80317-179">System.String</span></span>

### <span data-ttu-id="80317-180">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="80317-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="80317-181">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="80317-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="80317-182">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="80317-182">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="80317-183">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="80317-183">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="80317-184">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="80317-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="80317-185">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="80317-185">OUTPUTS</span></span>

### <span data-ttu-id="80317-186">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="80317-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="80317-187">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="80317-187">NOTES</span></span>

## <span data-ttu-id="80317-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="80317-188">RELATED LINKS</span></span>

[<span data-ttu-id="80317-189">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="80317-189">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="80317-190">Nowe — AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="80317-190">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="80317-191">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="80317-191">Remove-AzureRmApiManagementApiRevision</span></span>](./Remove-AzureRmApiManagementApiRevision.md)
