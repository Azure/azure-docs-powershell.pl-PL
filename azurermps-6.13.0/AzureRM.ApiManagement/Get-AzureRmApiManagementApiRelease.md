---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 880d96ba0e9eff053084517452c03ffb018b72a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716598"
---
# <span data-ttu-id="57adf-101">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="57adf-101">Get-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="57adf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57adf-102">SYNOPSIS</span></span>
<span data-ttu-id="57adf-103">Pobierz wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="57adf-103">Get the API Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57adf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57adf-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57adf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="57adf-105">DESCRIPTION</span></span>
<span data-ttu-id="57adf-106">Polecenie cmdlet **Get-AzureRmApiManagementApiRelease umożliwia pobranie** co najmniej jednego wydania interfejsu API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="57adf-106">The **Get-AzureRmApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="57adf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57adf-107">EXAMPLES</span></span>

### <span data-ttu-id="57adf-108">Przykład 1. Uzyskaj wszystkie wersje interfejsu API</span><span class="sxs-lookup"><span data-stu-id="57adf-108">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="57adf-109">To polecenie pobiera wszystkie wersje `echo-api` interfejsu API dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="57adf-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="57adf-110">Przykład 2: uzyskiwanie informacji o wersji konkretnego wydania interfejsu API</span><span class="sxs-lookup"><span data-stu-id="57adf-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
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

<span data-ttu-id="57adf-111">To polecenie uzyskuje informacje o wersjach określonego interfejsu API z określoną releaseId.</span><span class="sxs-lookup"><span data-stu-id="57adf-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="57adf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57adf-112">PARAMETERS</span></span>

### <span data-ttu-id="57adf-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="57adf-113">-ApiId</span></span>
<span data-ttu-id="57adf-114">Identyfikator API do wyszukania.</span><span class="sxs-lookup"><span data-stu-id="57adf-114">API identifier to look for.</span></span>
<span data-ttu-id="57adf-115">Jeśli zostanie określona, spróbuje uzyskać interfejs API o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="57adf-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="57adf-116">-Context</span><span class="sxs-lookup"><span data-stu-id="57adf-116">-Context</span></span>
<span data-ttu-id="57adf-117">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="57adf-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="57adf-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="57adf-118">This parameter is required.</span></span>

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

### <span data-ttu-id="57adf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57adf-119">-DefaultProfile</span></span>
<span data-ttu-id="57adf-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57adf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57adf-121">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="57adf-121">-ReleaseId</span></span>
<span data-ttu-id="57adf-122">Identyfikator wydania.</span><span class="sxs-lookup"><span data-stu-id="57adf-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="57adf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57adf-123">CommonParameters</span></span>
<span data-ttu-id="57adf-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57adf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57adf-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57adf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57adf-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57adf-126">INPUTS</span></span>

### <span data-ttu-id="57adf-127">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="57adf-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="57adf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="57adf-128">System.String</span></span>

## <span data-ttu-id="57adf-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57adf-129">OUTPUTS</span></span>

### <span data-ttu-id="57adf-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="57adf-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="57adf-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57adf-131">NOTES</span></span>

## <span data-ttu-id="57adf-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57adf-132">RELATED LINKS</span></span>

[<span data-ttu-id="57adf-133">Nowe — AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="57adf-133">New-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="57adf-134">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="57adf-134">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="57adf-135">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="57adf-135">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
