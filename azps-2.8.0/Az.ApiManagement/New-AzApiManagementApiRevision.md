---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 1a58c34aac272f6c8278833cd356de66774c5a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707038"
---
# <span data-ttu-id="817b9-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="817b9-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="817b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="817b9-102">SYNOPSIS</span></span>
<span data-ttu-id="817b9-103">Tworzy nową poprawkę istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="817b9-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="817b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="817b9-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="817b9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="817b9-105">DESCRIPTION</span></span>

<span data-ttu-id="817b9-106">Polecenie cmdlet **New-AzApiManagementApiRevision** tworzy poprawkę API dla istniejącego interfejsu API w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="817b9-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="817b9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="817b9-107">EXAMPLES</span></span>

### <span data-ttu-id="817b9-108">Przykład 1: Tworzenie pustej wersji interfejsu API dla interfejsu API</span><span class="sxs-lookup"><span data-stu-id="817b9-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="817b9-109">To polecenie tworzy wersję API `2` `echo-api` interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="817b9-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="817b9-110">Przykład 2: Tworzenie poprawki interfejsu API z istniejącego interfejsu API i kopiowanie wszystkich operacji, tagów i zasad</span><span class="sxs-lookup"><span data-stu-id="817b9-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
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

<span data-ttu-id="817b9-111">To polecenie tworzy wersję API `5` `echo-api` interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="817b9-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="817b9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="817b9-112">PARAMETERS</span></span>

### <span data-ttu-id="817b9-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="817b9-113">-ApiId</span></span>
<span data-ttu-id="817b9-114">Identyfikator interfejsu API, dla którego ma zostać utworzona poprawka.</span><span class="sxs-lookup"><span data-stu-id="817b9-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="817b9-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="817b9-115">-ApiRevision</span></span>
<span data-ttu-id="817b9-116">Identyfikator poprawki API.</span><span class="sxs-lookup"><span data-stu-id="817b9-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="817b9-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="817b9-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="817b9-118">Opis poprawki API.</span><span class="sxs-lookup"><span data-stu-id="817b9-118">Api Revision Description.</span></span> <span data-ttu-id="817b9-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="817b9-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="817b9-120">-Context</span><span class="sxs-lookup"><span data-stu-id="817b9-120">-Context</span></span>
<span data-ttu-id="817b9-121">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="817b9-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="817b9-122">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="817b9-122">This parameter is required.</span></span>

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

### <span data-ttu-id="817b9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="817b9-123">-DefaultProfile</span></span>
<span data-ttu-id="817b9-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="817b9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="817b9-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="817b9-125">-ServiceUrl</span></span>
<span data-ttu-id="817b9-126">Adres URL usługi sieci Web, która uwidacznia interfejs API w usłudze wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="817b9-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="817b9-127">Ten adres URL będzie wykorzystany tylko przez funkcję zarządzania interfejsem Azure API i nie zostanie udostępniony publicznie.</span><span class="sxs-lookup"><span data-stu-id="817b9-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="817b9-128">Musi zawierać od 1 do 2000 znaków.</span><span class="sxs-lookup"><span data-stu-id="817b9-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="817b9-129">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="817b9-129">This parameter is required.</span></span>

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

### <span data-ttu-id="817b9-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="817b9-130">-SourceApiRevision</span></span>
<span data-ttu-id="817b9-131">Identyfikator poprawki interfejsu API źródłowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="817b9-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="817b9-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="817b9-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="817b9-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="817b9-133">-Confirm</span></span>
<span data-ttu-id="817b9-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="817b9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="817b9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="817b9-135">-WhatIf</span></span>
<span data-ttu-id="817b9-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="817b9-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="817b9-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="817b9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="817b9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="817b9-138">CommonParameters</span></span>
<span data-ttu-id="817b9-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="817b9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="817b9-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="817b9-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="817b9-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="817b9-141">INPUTS</span></span>

### <span data-ttu-id="817b9-142">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="817b9-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="817b9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="817b9-143">System.String</span></span>

## <span data-ttu-id="817b9-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="817b9-144">OUTPUTS</span></span>

### <span data-ttu-id="817b9-145">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="817b9-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="817b9-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="817b9-146">NOTES</span></span>

## <span data-ttu-id="817b9-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="817b9-147">RELATED LINKS</span></span>

[<span data-ttu-id="817b9-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="817b9-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="817b9-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="817b9-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="817b9-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="817b9-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
