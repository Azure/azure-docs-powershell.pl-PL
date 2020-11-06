---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 11d832bc74aca4ac274ee17ff0b38de06b77e377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542068"
---
# <span data-ttu-id="0c166-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0c166-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="0c166-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c166-102">SYNOPSIS</span></span>
<span data-ttu-id="0c166-103">Zapoznaj się z informacjami o wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="0c166-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c166-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c166-104">SYNTAX</span></span>

### <span data-ttu-id="0c166-105">GetAllBackends (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0c166-105">GetAllBackends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c166-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="0c166-106">GetByBackendId</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c166-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0c166-107">DESCRIPTION</span></span>
<span data-ttu-id="0c166-108">Zapoznaj się z informacjami o wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="0c166-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="0c166-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c166-109">EXAMPLES</span></span>

### <span data-ttu-id="0c166-110">Przykład 1: uzyskiwanie wszystkich zakończeń</span><span class="sxs-lookup"><span data-stu-id="0c166-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="0c166-111">Pobiera listę wszystkich punktów końcowych skonfigurowanych w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0c166-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="0c166-112">Przykład 2: pobieranie wewnętrznej bazy danych określonej przez identyfikator 123</span><span class="sxs-lookup"><span data-stu-id="0c166-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="0c166-113">Uzyskiwanie szczegółów dotyczących określonej zaplecza wewnętrznego określonego identyfikatorem ' 123 '</span><span class="sxs-lookup"><span data-stu-id="0c166-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="0c166-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c166-114">PARAMETERS</span></span>

### <span data-ttu-id="0c166-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="0c166-115">-BackendId</span></span>
<span data-ttu-id="0c166-116">Identyfikator wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0c166-116">Identifier of a backend.</span></span>
<span data-ttu-id="0c166-117">Jeśli zostanie określona, spróbuje znaleźć zaplecze o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="0c166-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="0c166-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="0c166-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByBackendId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c166-119">-Context</span><span class="sxs-lookup"><span data-stu-id="0c166-119">-Context</span></span>
<span data-ttu-id="0c166-120">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0c166-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0c166-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0c166-121">This parameter is required.</span></span>

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

### <span data-ttu-id="0c166-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c166-122">-DefaultProfile</span></span>
<span data-ttu-id="0c166-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c166-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c166-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c166-124">CommonParameters</span></span>
<span data-ttu-id="0c166-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c166-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c166-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c166-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c166-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c166-127">INPUTS</span></span>

### <span data-ttu-id="0c166-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0c166-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0c166-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0c166-129">System.String</span></span>

## <span data-ttu-id="0c166-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c166-130">OUTPUTS</span></span>

### <span data-ttu-id="0c166-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0c166-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="0c166-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c166-132">NOTES</span></span>

## <span data-ttu-id="0c166-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c166-133">RELATED LINKS</span></span>

[<span data-ttu-id="0c166-134">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0c166-134">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="0c166-135">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0c166-135">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="0c166-136">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="0c166-136">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="0c166-137">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0c166-137">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="0c166-138">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0c166-138">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
