---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 7a3c418c5f55aa70b23972e5cd51065557335866
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223173"
---
# <span data-ttu-id="a1841-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a1841-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="a1841-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1841-102">SYNOPSIS</span></span>
<span data-ttu-id="a1841-103">Pobierz wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a1841-103">Get the API Release.</span></span>

## <span data-ttu-id="a1841-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1841-104">SYNTAX</span></span>

### <span data-ttu-id="a1841-105">ContextParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a1841-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1841-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1841-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1841-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a1841-107">DESCRIPTION</span></span>
<span data-ttu-id="a1841-108">Polecenie cmdlet **Get-AzApiManagementApiRelease umożliwia pobranie** co najmniej jednego wydania interfejsu API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="a1841-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="a1841-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1841-109">EXAMPLES</span></span>

### <span data-ttu-id="a1841-110">Przykład 1. Uzyskaj wszystkie wersje interfejsu API</span><span class="sxs-lookup"><span data-stu-id="a1841-110">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="a1841-111">To polecenie pobiera wszystkie wersje `echo-api` interfejsu API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="a1841-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="a1841-112">Przykład 2: uzyskiwanie informacji o wersji konkretnego wydania interfejsu API</span><span class="sxs-lookup"><span data-stu-id="a1841-112">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="a1841-113">To polecenie uzyskuje informacje o wersjach określonego interfejsu API z określoną releaseId.</span><span class="sxs-lookup"><span data-stu-id="a1841-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="a1841-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1841-114">PARAMETERS</span></span>

### <span data-ttu-id="a1841-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a1841-115">-ApiId</span></span>
<span data-ttu-id="a1841-116">Identyfikator API do wyszukania.</span><span class="sxs-lookup"><span data-stu-id="a1841-116">API identifier to look for.</span></span>
<span data-ttu-id="a1841-117">Jeśli zostanie określona, spróbuje uzyskać interfejs API o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="a1841-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1841-118">-Context</span><span class="sxs-lookup"><span data-stu-id="a1841-118">-Context</span></span>
<span data-ttu-id="a1841-119">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a1841-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a1841-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a1841-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1841-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1841-121">-DefaultProfile</span></span>
<span data-ttu-id="a1841-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1841-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1841-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="a1841-123">-ReleaseId</span></span>
<span data-ttu-id="a1841-124">Identyfikator wydania.</span><span class="sxs-lookup"><span data-stu-id="a1841-124">The identifier of the Release.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1841-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1841-125">-ResourceId</span></span>
<span data-ttu-id="a1841-126">Identyfikator zasobu ARM w wersji API.</span><span class="sxs-lookup"><span data-stu-id="a1841-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="a1841-127">Jeśli zostanie określona, spróbuje znaleźć zwolnienie interfejsu API o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="a1841-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="a1841-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a1841-128">This parameter is required.</span></span>

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

### <span data-ttu-id="a1841-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1841-129">CommonParameters</span></span>
<span data-ttu-id="a1841-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1841-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1841-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1841-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1841-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1841-132">INPUTS</span></span>

### <span data-ttu-id="a1841-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a1841-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a1841-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a1841-134">System.String</span></span>

## <span data-ttu-id="a1841-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1841-135">OUTPUTS</span></span>

### <span data-ttu-id="a1841-136">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a1841-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="a1841-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1841-137">NOTES</span></span>

## <span data-ttu-id="a1841-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1841-138">RELATED LINKS</span></span>

[<span data-ttu-id="a1841-139">Nowe — AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a1841-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="a1841-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a1841-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="a1841-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a1841-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)