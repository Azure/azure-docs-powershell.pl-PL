---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: bb27324c2c8524f36d9f3362dee8968fbfb0cc8c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409787"
---
# <span data-ttu-id="e5212-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e5212-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="e5212-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5212-102">SYNOPSIS</span></span>
<span data-ttu-id="e5212-103">Pobierz wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e5212-103">Get the API Release.</span></span>

## <span data-ttu-id="e5212-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e5212-104">SYNTAX</span></span>

### <span data-ttu-id="e5212-105">ContextParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e5212-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5212-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5212-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5212-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e5212-107">DESCRIPTION</span></span>
<span data-ttu-id="e5212-108">Polecenie **cmdlet Get-AzApiManagementApiRelease** otrzymuje jedną lub więcej wersji interfejsu API zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e5212-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="e5212-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e5212-109">EXAMPLES</span></span>

### <span data-ttu-id="e5212-110">Przykład 1. Uzyskiwanie wszystkich wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="e5212-110">Example 1: Get all releases of the API</span></span>
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

<span data-ttu-id="e5212-111">To polecenie pobiera wszystkie wersje interfejsu `echo-api` API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="e5212-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="e5212-112">Przykład 2. Uzyskiwanie informacji o wersji określonej wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="e5212-112">Example 2: Get the release information of the particular API release</span></span>
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

<span data-ttu-id="e5212-113">To polecenie pobiera informacje o wersjach określonego interfejsu API z określonym releaseId.</span><span class="sxs-lookup"><span data-stu-id="e5212-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="e5212-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5212-114">PARAMETERS</span></span>

### <span data-ttu-id="e5212-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e5212-115">-ApiId</span></span>
<span data-ttu-id="e5212-116">Identyfikator API do wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="e5212-116">API identifier to look for.</span></span>
<span data-ttu-id="e5212-117">Jeśli zostanie określona, spróbuje uzyskać interfejs API za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="e5212-117">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="e5212-118">— kontekst</span><span class="sxs-lookup"><span data-stu-id="e5212-118">-Context</span></span>
<span data-ttu-id="e5212-119">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e5212-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e5212-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e5212-120">This parameter is required.</span></span>

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

### <span data-ttu-id="e5212-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5212-121">-DefaultProfile</span></span>
<span data-ttu-id="e5212-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5212-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5212-123">- ReleaseId</span><span class="sxs-lookup"><span data-stu-id="e5212-123">-ReleaseId</span></span>
<span data-ttu-id="e5212-124">Identyfikator wydania.</span><span class="sxs-lookup"><span data-stu-id="e5212-124">The identifier of the Release.</span></span>

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

### <span data-ttu-id="e5212-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5212-125">-ResourceId</span></span>
<span data-ttu-id="e5212-126">Identyfikator zasobu arm wydania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e5212-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="e5212-127">Jeśli zostanie określona, spróbuje znaleźć zwolnienie interfejsu API za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="e5212-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="e5212-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e5212-128">This parameter is required.</span></span>

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

### <span data-ttu-id="e5212-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5212-129">CommonParameters</span></span>
<span data-ttu-id="e5212-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5212-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5212-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5212-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5212-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5212-132">INPUTS</span></span>

### <span data-ttu-id="e5212-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e5212-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e5212-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e5212-134">System.String</span></span>

## <span data-ttu-id="e5212-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5212-135">OUTPUTS</span></span>

### <span data-ttu-id="e5212-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e5212-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="e5212-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e5212-137">NOTES</span></span>

## <span data-ttu-id="e5212-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5212-138">RELATED LINKS</span></span>

[<span data-ttu-id="e5212-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e5212-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="e5212-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e5212-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="e5212-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e5212-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)