---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: 87292946f41da6d56f44351edc6a0ec8bbbfe3c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704664"
---
# <span data-ttu-id="dcdfd-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="dcdfd-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="dcdfd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcdfd-102">SYNOPSIS</span></span>
<span data-ttu-id="dcdfd-103">Zawiera szczegółowe informacje o wszystkich poprawkach API interfejsu API</span><span class="sxs-lookup"><span data-stu-id="dcdfd-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="dcdfd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcdfd-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcdfd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dcdfd-105">DESCRIPTION</span></span>
<span data-ttu-id="dcdfd-106">Polecenie cmdlet **Get-AzApiManagementApiRevision** pobiera szczegóły wszystkich poprawek interfejsu API</span><span class="sxs-lookup"><span data-stu-id="dcdfd-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="dcdfd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcdfd-107">EXAMPLES</span></span>

### <span data-ttu-id="dcdfd-108">Przykład 1: pobieranie wszystkich wersji API interfejsu API</span><span class="sxs-lookup"><span data-stu-id="dcdfd-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=3
ApiRevision     : 3
CreatedDateTime : 4/26/2018 10:57:42 PM
UpdatedDateTime : 4/26/2018 10:57:42 PM
Description     : ddsds
PrivateUrl      : /httpbin/v1;rev=3
IsOnline        : True
IsCurrent       : False

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=2
ApiRevision     : 2
CreatedDateTime : 4/26/2018 10:57:33 PM
UpdatedDateTime : 4/26/2018 10:57:33 PM
Description     : AA
PrivateUrl      : /httpbin/v1
IsOnline        : True
IsCurrent       : True

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=1
ApiRevision     : 1
CreatedDateTime : 4/24/2018 5:56:17 PM
UpdatedDateTime : 5/9/2018 9:29:06 PM
Description     :
PrivateUrl      : /httpbin/v1;rev=1
IsOnline        : True
IsCurrent       : False
```

<span data-ttu-id="dcdfd-109">To polecenie umożliwia wyświetlenie całej wersji interfejsu API określonego interfejsu API dla określonego kontekstu ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="dcdfd-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="dcdfd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcdfd-110">PARAMETERS</span></span>

### <span data-ttu-id="dcdfd-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dcdfd-111">-ApiId</span></span>
<span data-ttu-id="dcdfd-112">Identyfikator API, którego poprawki należy wyświetlić.</span><span class="sxs-lookup"><span data-stu-id="dcdfd-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="dcdfd-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dcdfd-113">This parameter is required.</span></span>

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

### <span data-ttu-id="dcdfd-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="dcdfd-114">-ApiRevision</span></span>
<span data-ttu-id="dcdfd-115">Identyfikator poprawki konkretnej wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="dcdfd-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="dcdfd-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dcdfd-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="dcdfd-117">-Context</span><span class="sxs-lookup"><span data-stu-id="dcdfd-117">-Context</span></span>
<span data-ttu-id="dcdfd-118">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dcdfd-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dcdfd-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dcdfd-119">This parameter is required.</span></span>

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

### <span data-ttu-id="dcdfd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcdfd-120">-DefaultProfile</span></span>
<span data-ttu-id="dcdfd-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcdfd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcdfd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcdfd-122">CommonParameters</span></span>
<span data-ttu-id="dcdfd-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcdfd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcdfd-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcdfd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcdfd-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcdfd-125">INPUTS</span></span>

### <span data-ttu-id="dcdfd-126">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dcdfd-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dcdfd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="dcdfd-127">System.String</span></span>

## <span data-ttu-id="dcdfd-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcdfd-128">OUTPUTS</span></span>

### <span data-ttu-id="dcdfd-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="dcdfd-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="dcdfd-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcdfd-130">NOTES</span></span>

## <span data-ttu-id="dcdfd-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcdfd-131">RELATED LINKS</span></span>