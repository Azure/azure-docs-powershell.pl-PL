---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 16fea88f5a5a1ad8a0e39f62b26d918ca7a64dbd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704661"
---
# <span data-ttu-id="46b63-101">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="46b63-101">Get-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="46b63-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46b63-102">SYNOPSIS</span></span>
<span data-ttu-id="46b63-103">Uzyskiwanie szczegółowych informacji o zestawach wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="46b63-103">Get the details of the API Version Sets</span></span>

## <span data-ttu-id="46b63-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46b63-104">SYNTAX</span></span>

```
Get-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46b63-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46b63-105">DESCRIPTION</span></span>
<span data-ttu-id="46b63-106">Polecenie cmdlet **Get-AzApiManagementApiVersionSet** pobiera szczegóły zestawów wersji interfejsu API skonfigurowane w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="46b63-106">The **Get-AzApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="46b63-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46b63-107">EXAMPLES</span></span>

### <span data-ttu-id="46b63-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46b63-108">Example 1</span></span>

### <span data-ttu-id="46b63-109">Przykład 1: pobieranie wszystkich zestawów wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="46b63-109">Example 1: Get all API Version Sets</span></span>
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

<span data-ttu-id="46b63-110">To polecenie pobiera wszystkie zestawy wersji interfejsu API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="46b63-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="46b63-111">Przykład 2: uzyskiwanie wersji interfejsu API ustawionej na podstawie identyfikatora</span><span class="sxs-lookup"><span data-stu-id="46b63-111">Example 2: Get a API Version Set by ID</span></span>
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

<span data-ttu-id="46b63-112">To polecenie pobiera zestaw wersji interfejsu API z określonym IDENTYFIKATORem.</span><span class="sxs-lookup"><span data-stu-id="46b63-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="46b63-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46b63-113">PARAMETERS</span></span>

### <span data-ttu-id="46b63-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="46b63-114">-ApiVersionSetId</span></span>
<span data-ttu-id="46b63-115">Identyfikator API do wyszukania.</span><span class="sxs-lookup"><span data-stu-id="46b63-115">API identifier to look for.</span></span>
<span data-ttu-id="46b63-116">Jeśli zostanie określona, spróbuje uzyskać interfejs API o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="46b63-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="46b63-117">-Context</span><span class="sxs-lookup"><span data-stu-id="46b63-117">-Context</span></span>
<span data-ttu-id="46b63-118">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="46b63-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="46b63-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="46b63-119">This parameter is required.</span></span>

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

### <span data-ttu-id="46b63-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b63-120">-DefaultProfile</span></span>
<span data-ttu-id="46b63-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46b63-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46b63-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b63-122">CommonParameters</span></span>
<span data-ttu-id="46b63-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b63-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b63-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46b63-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b63-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46b63-125">INPUTS</span></span>

### <span data-ttu-id="46b63-126">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="46b63-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="46b63-127">System. String</span><span class="sxs-lookup"><span data-stu-id="46b63-127">System.String</span></span>

## <span data-ttu-id="46b63-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46b63-128">OUTPUTS</span></span>

### <span data-ttu-id="46b63-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="46b63-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="46b63-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46b63-130">NOTES</span></span>

## <span data-ttu-id="46b63-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46b63-131">RELATED LINKS</span></span>

[<span data-ttu-id="46b63-132">Nowe — AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="46b63-132">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="46b63-133">Remove-AzApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="46b63-133">Remove-AzApiManagementApiSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="46b63-134">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="46b63-134">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiSet.md)
