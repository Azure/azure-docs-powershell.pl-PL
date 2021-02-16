---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 833351c3abbf95eb898405f23241a20fe9affefa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190395"
---
# <span data-ttu-id="8f9cd-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8f9cd-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="8f9cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f9cd-102">SYNOPSIS</span></span>
<span data-ttu-id="8f9cd-103">Tworzy nową poprawkę istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="8f9cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8f9cd-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f9cd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8f9cd-105">DESCRIPTION</span></span>

<span data-ttu-id="8f9cd-106">Polecenie **cmdlet New-AzApiManagementApiRevision** tworzy poprawkę interfejsu API dla istniejącego interfejsu API w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="8f9cd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8f9cd-107">EXAMPLES</span></span>

### <span data-ttu-id="8f9cd-108">Przykład 1. Tworzenie pustej poprawki interfejsu API dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="8f9cd-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="8f9cd-109">To polecenie tworzy poprawkę interfejsu `2` `echo-api` API interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="8f9cd-110">Przykład 2. Tworzenie poprawki interfejsu API z istniejącego interfejsu API i kopiowanie wszystkich operacji, tagów i zasad</span><span class="sxs-lookup"><span data-stu-id="8f9cd-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5" -SourceApiRevision "1" -ServiceUrl "https://echoapi.cloudapp.net/rev4"


ApiId                         : echo-api;rev=5
Name                          : Echo API
Description                   :
ServiceUrl                    : http://echoapi.cloudapp.net/api
Path                          : echo
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 5
ApiVersion                    :
IsCurrent                     : False
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/apimService1/providers/Microsoft.ApiManagement/service/sdktestapim4163/apis/echo-api;rev=5
ResourceGroupName             : apimService1
ServiceName                   : sdktestapim4163
```

<span data-ttu-id="8f9cd-111">To polecenie tworzy poprawkę interfejsu `5` `echo-api` API interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="8f9cd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f9cd-112">PARAMETERS</span></span>

### <span data-ttu-id="8f9cd-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8f9cd-113">-ApiId</span></span>
<span data-ttu-id="8f9cd-114">Identyfikator interfejsu API, którego poprawka ma zostać utworzona.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="8f9cd-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="8f9cd-115">-ApiRevision</span></span>
<span data-ttu-id="8f9cd-116">Identyfikator poprawek interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="8f9cd-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="8f9cd-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="8f9cd-118">Opis poprawek interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-118">Api Revision Description.</span></span> <span data-ttu-id="8f9cd-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="8f9cd-120">— kontekst</span><span class="sxs-lookup"><span data-stu-id="8f9cd-120">-Context</span></span>
<span data-ttu-id="8f9cd-121">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8f9cd-122">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f9cd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f9cd-123">-DefaultProfile</span></span>
<span data-ttu-id="8f9cd-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f9cd-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="8f9cd-125">-ServiceUrl</span></span>
<span data-ttu-id="8f9cd-126">Adres URL usługi sieci Web, która ujawnia interfejs API w usłudze Backend.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="8f9cd-127">Ten adres URL będzie używany tylko w usłudze Azure API Management i nie będzie publiczny.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="8f9cd-128">Musi to być od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="8f9cd-129">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-129">This parameter is required.</span></span>

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

### <span data-ttu-id="8f9cd-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="8f9cd-130">-SourceApiRevision</span></span>
<span data-ttu-id="8f9cd-131">Identyfikator poprawki interfejsu API źródłowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="8f9cd-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="8f9cd-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f9cd-133">-Confirm</span></span>
<span data-ttu-id="8f9cd-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f9cd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f9cd-135">-WhatIf</span></span>
<span data-ttu-id="8f9cd-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f9cd-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f9cd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f9cd-138">CommonParameters</span></span>
<span data-ttu-id="8f9cd-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f9cd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f9cd-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f9cd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f9cd-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f9cd-141">INPUTS</span></span>

### <span data-ttu-id="8f9cd-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8f9cd-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8f9cd-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8f9cd-143">System.String</span></span>

## <span data-ttu-id="8f9cd-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f9cd-144">OUTPUTS</span></span>

### <span data-ttu-id="8f9cd-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8f9cd-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="8f9cd-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8f9cd-146">NOTES</span></span>

## <span data-ttu-id="8f9cd-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f9cd-147">RELATED LINKS</span></span>

[<span data-ttu-id="8f9cd-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8f9cd-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="8f9cd-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8f9cd-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="8f9cd-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8f9cd-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
