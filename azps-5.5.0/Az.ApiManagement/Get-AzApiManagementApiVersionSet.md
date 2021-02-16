---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: e6b9122481e5e506fc02a13a61b7ebeb71372e96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199755"
---
# <span data-ttu-id="97eba-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="97eba-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="97eba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97eba-102">SYNOPSIS</span></span>
<span data-ttu-id="97eba-103">Uzyskiwanie szczegółowych informacji o zestawach wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="97eba-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="97eba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="97eba-104">SYNTAX</span></span>

### <span data-ttu-id="97eba-105">ContextParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="97eba-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97eba-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97eba-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97eba-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="97eba-107">DESCRIPTION</span></span>
<span data-ttu-id="97eba-108">Polecenie **cmdlet Get-AzApiManagementApiVersionSet** pobiera szczegóły zestawów wersji interfejsu API skonfigurowanych w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="97eba-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="97eba-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="97eba-109">EXAMPLES</span></span>

### <span data-ttu-id="97eba-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="97eba-110">Example 1</span></span>

### <span data-ttu-id="97eba-111">Przykład 2. Pobierz wszystkie zestawy wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="97eba-111">Example 2: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext

ApiVersionSetId   : a93316c8-8b88-46cc-8260-380789a5d598
Description       :
VersionQueryName  :
VersionHeaderName :
DisplayName       : Echo API
VersioningScheme  : Segment
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/a916c8-8b88-46cc-8260-380789a5d598
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso

ApiVersionSetId   : 4cbdfa34-25f3-4a93-a9b6-76b6eade7562
Description       :
VersionQueryName  : api-version
VersionHeaderName :
DisplayName       : getproduct old
VersioningScheme  : Query
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/4cbdfa34-25f3-4a93-a9b6-76b6eade7562
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="97eba-112">To polecenie pobiera wszystkie zestawy wersji interfejsu API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="97eba-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="97eba-113">Przykład 3. Uzyskiwanie zestawu wersji interfejsu API według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="97eba-113">Example 3: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

ApiVersionSetId   : 8c441e0e-a0cd-47d8-8d88-f944a83b41bd
Description       :
VersionQueryName  :
VersionHeaderName : Api-Version
DisplayName       : ordersapi
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/8c441e0e-a0cd-47d8-8d88-f944a83b41bd
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="97eba-114">To polecenie pobiera zestaw wersji interfejsu API z określonym identyfikatorem.</span><span class="sxs-lookup"><span data-stu-id="97eba-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="97eba-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97eba-115">PARAMETERS</span></span>

### <span data-ttu-id="97eba-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="97eba-116">-ApiVersionSetId</span></span>
<span data-ttu-id="97eba-117">Identyfikator API do wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="97eba-117">API identifier to look for.</span></span>
<span data-ttu-id="97eba-118">Jeśli zostanie określona, spróbuje uzyskać interfejs API za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="97eba-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="97eba-119">— kontekst</span><span class="sxs-lookup"><span data-stu-id="97eba-119">-Context</span></span>
<span data-ttu-id="97eba-120">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="97eba-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="97eba-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="97eba-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97eba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97eba-122">-DefaultProfile</span></span>
<span data-ttu-id="97eba-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="97eba-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97eba-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97eba-124">-ResourceId</span></span>
<span data-ttu-id="97eba-125">Identyfikator zasobu arm zestawu ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="97eba-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="97eba-126">Jeśli zostanie określona, spróbuje znaleźć zestaw apiVersionSet według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="97eba-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="97eba-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="97eba-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97eba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97eba-128">CommonParameters</span></span>
<span data-ttu-id="97eba-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97eba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97eba-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97eba-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97eba-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97eba-131">INPUTS</span></span>

### <span data-ttu-id="97eba-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="97eba-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="97eba-133">System.String</span><span class="sxs-lookup"><span data-stu-id="97eba-133">System.String</span></span>

## <span data-ttu-id="97eba-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97eba-134">OUTPUTS</span></span>

### <span data-ttu-id="97eba-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="97eba-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="97eba-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="97eba-136">NOTES</span></span>

## <span data-ttu-id="97eba-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97eba-137">RELATED LINKS</span></span>

[<span data-ttu-id="97eba-138">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="97eba-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="97eba-139">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="97eba-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="97eba-140">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="97eba-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
