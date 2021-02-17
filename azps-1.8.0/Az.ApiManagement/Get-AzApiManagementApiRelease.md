---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 4f9e917f17037e5f47b52501007da5556bde1187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401083"
---
# <span data-ttu-id="5e1fc-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="5e1fc-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="5e1fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e1fc-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1fc-103">Pobierz wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="5e1fc-103">Get the API Release.</span></span>

## <span data-ttu-id="5e1fc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5e1fc-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e1fc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5e1fc-105">DESCRIPTION</span></span>
<span data-ttu-id="5e1fc-106">Polecenie **cmdlet Get-AzApiManagementApiRelease** otrzymuje jedną lub więcej wersji interfejsu API zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e1fc-106">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="5e1fc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5e1fc-107">EXAMPLES</span></span>

### <span data-ttu-id="5e1fc-108">Przykład 1. Uzyskiwanie wszystkich wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="5e1fc-108">Example 1: Get all releases of the API</span></span>
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
ServiceName       : contos
```

<span data-ttu-id="5e1fc-109">To polecenie pobiera wszystkie wersje interfejsu `echo-api` API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="5e1fc-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="5e1fc-110">Przykład 2. Uzyskiwanie informacji o wersji określonej wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="5e1fc-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contos/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="5e1fc-111">To polecenie pobiera informacje o wersjach określonego interfejsu API z określonym releaseId.</span><span class="sxs-lookup"><span data-stu-id="5e1fc-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="5e1fc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e1fc-112">PARAMETERS</span></span>

### <span data-ttu-id="5e1fc-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5e1fc-113">-ApiId</span></span>
<span data-ttu-id="5e1fc-114">Identyfikator API do wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="5e1fc-114">API identifier to look for.</span></span>
<span data-ttu-id="5e1fc-115">Jeśli zostanie określona, spróbuje uzyskać interfejs API za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="5e1fc-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="5e1fc-116">— kontekst</span><span class="sxs-lookup"><span data-stu-id="5e1fc-116">-Context</span></span>
<span data-ttu-id="5e1fc-117">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5e1fc-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5e1fc-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="5e1fc-118">This parameter is required.</span></span>

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

### <span data-ttu-id="5e1fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e1fc-119">-DefaultProfile</span></span>
<span data-ttu-id="5e1fc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e1fc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e1fc-121">- ReleaseId</span><span class="sxs-lookup"><span data-stu-id="5e1fc-121">-ReleaseId</span></span>
<span data-ttu-id="5e1fc-122">Identyfikator wydania.</span><span class="sxs-lookup"><span data-stu-id="5e1fc-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="5e1fc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1fc-123">CommonParameters</span></span>
<span data-ttu-id="5e1fc-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e1fc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1fc-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e1fc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1fc-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e1fc-126">INPUTS</span></span>

### <span data-ttu-id="5e1fc-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5e1fc-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5e1fc-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5e1fc-128">System.String</span></span>

## <span data-ttu-id="5e1fc-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e1fc-129">OUTPUTS</span></span>

### <span data-ttu-id="5e1fc-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="5e1fc-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="5e1fc-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5e1fc-131">NOTES</span></span>

## <span data-ttu-id="5e1fc-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e1fc-132">RELATED LINKS</span></span>

[<span data-ttu-id="5e1fc-133">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="5e1fc-133">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="5e1fc-134">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="5e1fc-134">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="5e1fc-135">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="5e1fc-135">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)