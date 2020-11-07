---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 353fd6365f85ba71105f80324ba740b4d829a85a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704665"
---
# <span data-ttu-id="0ef5c-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0ef5c-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="0ef5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ef5c-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef5c-103">Pobierz wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-103">Get the API Release.</span></span>

## <span data-ttu-id="0ef5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ef5c-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ef5c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0ef5c-105">DESCRIPTION</span></span>
<span data-ttu-id="0ef5c-106">Polecenie cmdlet **Get-AzApiManagementApiRelease umożliwia pobranie** co najmniej jednego wydania interfejsu API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-106">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="0ef5c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ef5c-107">EXAMPLES</span></span>

### <span data-ttu-id="0ef5c-108">Przykład 1. Uzyskaj wszystkie wersje interfejsu API</span><span class="sxs-lookup"><span data-stu-id="0ef5c-108">Example 1: Get all releases of the API</span></span>
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

<span data-ttu-id="0ef5c-109">To polecenie pobiera wszystkie wersje `echo-api` interfejsu API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="0ef5c-110">Przykład 2: uzyskiwanie informacji o wersji konkretnego wydania interfejsu API</span><span class="sxs-lookup"><span data-stu-id="0ef5c-110">Example 2: Get the release information of the particular API release</span></span>
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

<span data-ttu-id="0ef5c-111">To polecenie uzyskuje informacje o wersjach określonego interfejsu API z określoną releaseId.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="0ef5c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ef5c-112">PARAMETERS</span></span>

### <span data-ttu-id="0ef5c-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0ef5c-113">-ApiId</span></span>
<span data-ttu-id="0ef5c-114">Identyfikator API do wyszukania.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-114">API identifier to look for.</span></span>
<span data-ttu-id="0ef5c-115">Jeśli zostanie określona, spróbuje uzyskać interfejs API o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="0ef5c-116">-Context</span><span class="sxs-lookup"><span data-stu-id="0ef5c-116">-Context</span></span>
<span data-ttu-id="0ef5c-117">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0ef5c-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0ef5c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef5c-119">-DefaultProfile</span></span>
<span data-ttu-id="0ef5c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ef5c-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="0ef5c-121">-ReleaseId</span></span>
<span data-ttu-id="0ef5c-122">Identyfikator wydania.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="0ef5c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef5c-123">CommonParameters</span></span>
<span data-ttu-id="0ef5c-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ef5c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef5c-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ef5c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef5c-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ef5c-126">INPUTS</span></span>

### <span data-ttu-id="0ef5c-127">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0ef5c-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0ef5c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0ef5c-128">System.String</span></span>

## <span data-ttu-id="0ef5c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ef5c-129">OUTPUTS</span></span>

### <span data-ttu-id="0ef5c-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0ef5c-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="0ef5c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ef5c-131">NOTES</span></span>

## <span data-ttu-id="0ef5c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ef5c-132">RELATED LINKS</span></span>

[<span data-ttu-id="0ef5c-133">Nowe — AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0ef5c-133">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="0ef5c-134">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0ef5c-134">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="0ef5c-135">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0ef5c-135">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)