---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 60a811aaa097ccc95f8dd57fa105ba4b1388b060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547707"
---
# <span data-ttu-id="3e2b5-101">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3e2b5-101">Get-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="3e2b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e2b5-102">SYNOPSIS</span></span>
<span data-ttu-id="3e2b5-103">Uzyskiwanie szczegółowych informacji o zestawach wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="3e2b5-103">Get the details of the API Version Sets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e2b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e2b5-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e2b5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3e2b5-105">DESCRIPTION</span></span>
<span data-ttu-id="3e2b5-106">Polecenie cmdlet **Get-AzureRmApiManagementApiVersionSet** pobiera szczegóły zestawów wersji interfejsu API skonfigurowane w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3e2b5-106">The **Get-AzureRmApiManagementApiVersionSet** cmdlet gets the details of the API Version Sets configured in an API Management context.</span></span>

## <span data-ttu-id="3e2b5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e2b5-107">EXAMPLES</span></span>

### <span data-ttu-id="3e2b5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3e2b5-108">Example 1</span></span>

### <span data-ttu-id="3e2b5-109">Przykład 1: pobieranie wszystkich zestawów wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="3e2b5-109">Example 1: Get all API Version Sets</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext

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

<span data-ttu-id="3e2b5-110">To polecenie pobiera wszystkie zestawy wersji interfejsu API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="3e2b5-110">This command gets all of the API Version sets for the specified context.</span></span>

### <span data-ttu-id="3e2b5-111">Przykład 2: uzyskiwanie wersji interfejsu API ustawionej na podstawie identyfikatora</span><span class="sxs-lookup"><span data-stu-id="3e2b5-111">Example 2: Get a API Version Set by ID</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId $ApiVersionSetId

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

<span data-ttu-id="3e2b5-112">To polecenie pobiera zestaw wersji interfejsu API z określonym IDENTYFIKATORem.</span><span class="sxs-lookup"><span data-stu-id="3e2b5-112">This command gets the API Version Set with the specified ID.</span></span>

## <span data-ttu-id="3e2b5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e2b5-113">PARAMETERS</span></span>

### <span data-ttu-id="3e2b5-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="3e2b5-114">-ApiVersionSetId</span></span>
<span data-ttu-id="3e2b5-115">Identyfikator API do wyszukania.</span><span class="sxs-lookup"><span data-stu-id="3e2b5-115">API identifier to look for.</span></span>
<span data-ttu-id="3e2b5-116">Jeśli zostanie określona, spróbuje uzyskać interfejs API o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="3e2b5-116">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="3e2b5-117">-Context</span><span class="sxs-lookup"><span data-stu-id="3e2b5-117">-Context</span></span>
<span data-ttu-id="3e2b5-118">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3e2b5-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3e2b5-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="3e2b5-119">This parameter is required.</span></span>

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

### <span data-ttu-id="3e2b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e2b5-120">-DefaultProfile</span></span>
<span data-ttu-id="3e2b5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e2b5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e2b5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e2b5-122">CommonParameters</span></span>
<span data-ttu-id="3e2b5-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e2b5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e2b5-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e2b5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e2b5-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e2b5-125">INPUTS</span></span>

### <span data-ttu-id="3e2b5-126">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3e2b5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3e2b5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3e2b5-127">System.String</span></span>

## <span data-ttu-id="3e2b5-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e2b5-128">OUTPUTS</span></span>

### <span data-ttu-id="3e2b5-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3e2b5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="3e2b5-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e2b5-130">NOTES</span></span>

## <span data-ttu-id="3e2b5-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e2b5-131">RELATED LINKS</span></span>

[<span data-ttu-id="3e2b5-132">Nowe — AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3e2b5-132">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="3e2b5-133">Remove-AzureRmApiManagementApiSet</span><span class="sxs-lookup"><span data-stu-id="3e2b5-133">Remove-AzureRmApiManagementApiSet</span></span>](./Remove-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="3e2b5-134">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3e2b5-134">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiSet.md)
