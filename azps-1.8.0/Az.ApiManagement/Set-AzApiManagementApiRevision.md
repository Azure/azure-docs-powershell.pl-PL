---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: 8b2e29da3c3f6140cbab422e74d09656c921c16c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869367"
---
# <span data-ttu-id="8d323-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8d323-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="8d323-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d323-102">SYNOPSIS</span></span>
<span data-ttu-id="8d323-103">Modyfikuje wersję interfejsu API</span><span class="sxs-lookup"><span data-stu-id="8d323-103">Modifies an API Revision</span></span>

## <span data-ttu-id="8d323-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d323-104">SYNTAX</span></span>

### <span data-ttu-id="8d323-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8d323-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d323-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8d323-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d323-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8d323-107">DESCRIPTION</span></span>
<span data-ttu-id="8d323-108">Polecenie cmdlet **Set-AzApiManagementApiRevision** modyfikuje wersję interfejsu API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="8d323-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="8d323-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d323-109">EXAMPLES</span></span>

### <span data-ttu-id="8d323-110">Przykład 1 modyfikowanie poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="8d323-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="8d323-111">Polecenie cmdlet umożliwia zaktualizowanie `2` poprawki interfejsu API `echo-api` o nowy opis, protokół i ścieżkę.</span><span class="sxs-lookup"><span data-stu-id="8d323-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="8d323-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d323-112">PARAMETERS</span></span>

### <span data-ttu-id="8d323-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8d323-113">-ApiId</span></span>
<span data-ttu-id="8d323-114">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8d323-114">Identifier of existing API.</span></span>
<span data-ttu-id="8d323-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8d323-115">This parameter is required.</span></span>

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

### <span data-ttu-id="8d323-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="8d323-116">-ApiRevision</span></span>
<span data-ttu-id="8d323-117">Identyfikator istniejącej poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8d323-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="8d323-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8d323-118">This parameter is required.</span></span>

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

### <span data-ttu-id="8d323-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="8d323-119">-AuthorizationScope</span></span>
<span data-ttu-id="8d323-120">Zakres operacji uwierzytelniania OAuth.</span><span class="sxs-lookup"><span data-stu-id="8d323-120">OAuth operations scope.</span></span>
<span data-ttu-id="8d323-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8d323-121">This parameter is optional.</span></span>
<span data-ttu-id="8d323-122">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="8d323-122">Default value is $null.</span></span>

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

### <span data-ttu-id="8d323-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="8d323-123">-AuthorizationServerId</span></span>
<span data-ttu-id="8d323-124">Identyfikator serwera autoryzacji OAuth.</span><span class="sxs-lookup"><span data-stu-id="8d323-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="8d323-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8d323-125">This parameter is optional.</span></span>
<span data-ttu-id="8d323-126">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="8d323-126">Default value is $null.</span></span>
<span data-ttu-id="8d323-127">Należy określić, czy AuthorizationScope.</span><span class="sxs-lookup"><span data-stu-id="8d323-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="8d323-128">-Context</span><span class="sxs-lookup"><span data-stu-id="8d323-128">-Context</span></span>
<span data-ttu-id="8d323-129">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8d323-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8d323-130">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8d323-130">This parameter is required.</span></span>

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

### <span data-ttu-id="8d323-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d323-131">-DefaultProfile</span></span>
<span data-ttu-id="8d323-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d323-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d323-133">— Opis</span><span class="sxs-lookup"><span data-stu-id="8d323-133">-Description</span></span>
<span data-ttu-id="8d323-134">Opis interfejsu API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="8d323-134">Web API description.</span></span>
<span data-ttu-id="8d323-135">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8d323-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="8d323-136">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8d323-136">-InputObject</span></span>
<span data-ttu-id="8d323-137">Wystąpienie PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="8d323-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="8d323-138">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8d323-138">This parameter is required.</span></span>

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

### <span data-ttu-id="8d323-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8d323-139">-Name</span></span>
<span data-ttu-id="8d323-140">Nazwa API sieci Web.</span><span class="sxs-lookup"><span data-stu-id="8d323-140">Web API name.</span></span>
<span data-ttu-id="8d323-141">Publiczna nazwa interfejsu API, która będzie wyświetlana na portalach dewelopera i administratora.</span><span class="sxs-lookup"><span data-stu-id="8d323-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="8d323-142">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8d323-142">This parameter is required.</span></span>

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

### <span data-ttu-id="8d323-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d323-143">-PassThru</span></span>
<span data-ttu-id="8d323-144">Jeśli jest określone, wystąpienie systemu Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementApi reprezentujące zestaw interfejsów API.</span><span class="sxs-lookup"><span data-stu-id="8d323-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="8d323-145">-Path</span><span class="sxs-lookup"><span data-stu-id="8d323-145">-Path</span></span>
<span data-ttu-id="8d323-146">Ścieżka internetowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8d323-146">Web API Path.</span></span>
<span data-ttu-id="8d323-147">Ostatnia część publicznego adresu URL interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8d323-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="8d323-148">Ten adres URL będzie wykorzystywany przez użytkowników korzystających z interfejsu API w celu wysyłania żądań do usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="8d323-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="8d323-149">Musi zawierać od 1 do 400 znaków.</span><span class="sxs-lookup"><span data-stu-id="8d323-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="8d323-150">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8d323-150">This parameter is optional.</span></span>
<span data-ttu-id="8d323-151">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="8d323-151">Default value is $null.</span></span>

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

### <span data-ttu-id="8d323-152">-Protokoły</span><span class="sxs-lookup"><span data-stu-id="8d323-152">-Protocols</span></span>
<span data-ttu-id="8d323-153">Protokoły API sieci Web (http, https).</span><span class="sxs-lookup"><span data-stu-id="8d323-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="8d323-154">Protokoły, w których udostępniono interfejs API.</span><span class="sxs-lookup"><span data-stu-id="8d323-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="8d323-155">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8d323-155">This parameter is required.</span></span>
<span data-ttu-id="8d323-156">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="8d323-156">Default value is $null.</span></span>

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

### <span data-ttu-id="8d323-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="8d323-157">-ServiceUrl</span></span>
<span data-ttu-id="8d323-158">Adres URL usługi sieci Web, która uwidacznia interfejs API.</span><span class="sxs-lookup"><span data-stu-id="8d323-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="8d323-159">Ten adres URL będzie wykorzystany tylko przez funkcję zarządzania interfejsem Azure API i nie zostanie udostępniony publicznie.</span><span class="sxs-lookup"><span data-stu-id="8d323-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="8d323-160">Musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="8d323-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="8d323-161">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8d323-161">This parameter is required.</span></span>

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

### <span data-ttu-id="8d323-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="8d323-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="8d323-163">Nazwa nagłówka klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8d323-163">Subscription key header name.</span></span>
<span data-ttu-id="8d323-164">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8d323-164">This parameter is optional.</span></span>
<span data-ttu-id="8d323-165">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="8d323-165">Default value is $null.</span></span>

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

### <span data-ttu-id="8d323-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="8d323-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="8d323-167">Nazwa parametru ciągu kwerendy klucza subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8d323-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="8d323-168">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8d323-168">This parameter is optional.</span></span>
<span data-ttu-id="8d323-169">Wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="8d323-169">Default value is $null.</span></span>

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

### <span data-ttu-id="8d323-170">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d323-170">-Confirm</span></span>
<span data-ttu-id="8d323-171">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d323-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d323-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d323-172">-WhatIf</span></span>
<span data-ttu-id="8d323-173">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d323-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d323-174">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8d323-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d323-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d323-175">CommonParameters</span></span>
<span data-ttu-id="8d323-176">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d323-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d323-177">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d323-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d323-178">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d323-178">INPUTS</span></span>

### <span data-ttu-id="8d323-179">System. String</span><span class="sxs-lookup"><span data-stu-id="8d323-179">System.String</span></span>

### <span data-ttu-id="8d323-180">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8d323-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8d323-181">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8d323-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="8d323-182">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="8d323-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="8d323-183">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8d323-183">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8d323-184">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d323-184">OUTPUTS</span></span>

### <span data-ttu-id="8d323-185">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8d323-185">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="8d323-186">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d323-186">NOTES</span></span>

## <span data-ttu-id="8d323-187">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d323-187">RELATED LINKS</span></span>

[<span data-ttu-id="8d323-188">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8d323-188">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="8d323-189">Nowe — AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8d323-189">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="8d323-190">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8d323-190">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)