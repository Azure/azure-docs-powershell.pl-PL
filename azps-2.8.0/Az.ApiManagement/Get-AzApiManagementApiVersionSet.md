---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 4fefe6e7a763cdce60483342e8e8db880405e060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707090"
---
# <span data-ttu-id="40a88-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="40a88-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="40a88-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="40a88-102">SYNOPSIS</span></span>
<span data-ttu-id="40a88-103">Uzyskiwanie szczegółowych informacji o zestawach wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="40a88-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="40a88-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="40a88-104">SYNTAX</span></span>

### <span data-ttu-id="40a88-105">ContextParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="40a88-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40a88-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40a88-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40a88-107">Opis</span><span class="sxs-lookup"><span data-stu-id="40a88-107">DESCRIPTION</span></span>
<span data-ttu-id="40a88-108">Polecenie cmdlet **Get-AzApiManagementApiVersionSet** pobiera szczegóły zestawów wersji interfejsu API skonfigurowane w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="40a88-108">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="40a88-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="40a88-109">EXAMPLES</span></span>

### <span data-ttu-id="40a88-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="40a88-110">Example 1</span></span>

### <span data-ttu-id="40a88-111">Przykład 1: pobieranie wszystkich zestawów wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="40a88-111">Example 1: Get all API Version Sets</span></span>
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

<span data-ttu-id="40a88-112">To polecenie pobiera wszystkie zestawy wersji interfejsu API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="40a88-112">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="40a88-113">Przykład 2: uzyskiwanie wersji interfejsu API ustawionej na podstawie identyfikatora</span><span class="sxs-lookup"><span data-stu-id="40a88-113">Example 2: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="40a88-114">To polecenie pobiera zestaw wersji interfejsu API z określonym IDENTYFIKATORem.</span><span class="sxs-lookup"><span data-stu-id="40a88-114">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="40a88-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="40a88-115">PARAMETERS</span></span>

### <span data-ttu-id="40a88-116">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="40a88-116">-ApiVersionSetId</span></span>
<span data-ttu-id="40a88-117">Identyfikator API do wyszukania.</span><span class="sxs-lookup"><span data-stu-id="40a88-117">API identifier to look for.</span></span>
<span data-ttu-id="40a88-118">Jeśli zostanie określona, spróbuje uzyskać interfejs API o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="40a88-118">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="40a88-119">-Context</span><span class="sxs-lookup"><span data-stu-id="40a88-119">-Context</span></span>
<span data-ttu-id="40a88-120">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="40a88-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="40a88-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="40a88-121">This parameter is required.</span></span>

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

### <span data-ttu-id="40a88-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40a88-122">-DefaultProfile</span></span>
<span data-ttu-id="40a88-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="40a88-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40a88-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40a88-124">-ResourceId</span></span>
<span data-ttu-id="40a88-125">Identyfikator zasobu ARM ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="40a88-125">Arm Resource Identifier of the ApiVersionSet.</span></span> <span data-ttu-id="40a88-126">Jeśli zostanie określona, spróbuje znaleźć apiVersionSet za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="40a88-126">If specified will try to find apiVersionSet by the identifier.</span></span> <span data-ttu-id="40a88-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="40a88-127">This parameter is required.</span></span>

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

### <span data-ttu-id="40a88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40a88-128">CommonParameters</span></span>
<span data-ttu-id="40a88-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40a88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40a88-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40a88-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40a88-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40a88-131">INPUTS</span></span>

### <span data-ttu-id="40a88-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="40a88-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="40a88-133">System. String</span><span class="sxs-lookup"><span data-stu-id="40a88-133">System.String</span></span>

## <span data-ttu-id="40a88-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="40a88-134">OUTPUTS</span></span>

### <span data-ttu-id="40a88-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="40a88-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="40a88-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="40a88-136">NOTES</span></span>

## <span data-ttu-id="40a88-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40a88-137">RELATED LINKS</span></span>

[<span data-ttu-id="40a88-138">Nowe — AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="40a88-138">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="40a88-139">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="40a88-139">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="40a88-140">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="40a88-140">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiSet.md)