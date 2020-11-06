---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 0074ed7ec0d3aa88f813d138be71083195e6b10a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527153"
---
# <span data-ttu-id="e9b78-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e9b78-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="e9b78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9b78-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b78-103">Zapoznaj się z informacjami o wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="e9b78-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9b78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9b78-104">SYNTAX</span></span>

### <span data-ttu-id="e9b78-105">GetAllBackends (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e9b78-105">GetAllBackends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9b78-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="e9b78-106">GetByBackendId</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9b78-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e9b78-107">DESCRIPTION</span></span>
<span data-ttu-id="e9b78-108">Zapoznaj się z informacjami o wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="e9b78-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="e9b78-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9b78-109">EXAMPLES</span></span>

### <span data-ttu-id="e9b78-110">Przykład 1: uzyskiwanie wszystkich zakończeń</span><span class="sxs-lookup"><span data-stu-id="e9b78-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="e9b78-111">Pobiera listę wszystkich punktów końcowych skonfigurowanych w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="e9b78-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="e9b78-112">Przykład 2: pobieranie wewnętrznej bazy danych określonej przez identyfikator 123</span><span class="sxs-lookup"><span data-stu-id="e9b78-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="e9b78-113">Uzyskiwanie szczegółów dotyczących określonej zaplecza wewnętrznego określonego identyfikatorem ' 123 '</span><span class="sxs-lookup"><span data-stu-id="e9b78-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="e9b78-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9b78-114">PARAMETERS</span></span>

### <span data-ttu-id="e9b78-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="e9b78-115">-BackendId</span></span>
<span data-ttu-id="e9b78-116">Identyfikator wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e9b78-116">Identifier of a backend.</span></span>
<span data-ttu-id="e9b78-117">Jeśli zostanie określona, spróbuje znaleźć zaplecze o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="e9b78-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="e9b78-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e9b78-118">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByBackendId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b78-119">-Context</span><span class="sxs-lookup"><span data-stu-id="e9b78-119">-Context</span></span>
<span data-ttu-id="e9b78-120">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e9b78-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e9b78-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e9b78-121">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b78-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b78-122">-DefaultProfile</span></span>
<span data-ttu-id="e9b78-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b78-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b78-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b78-124">CommonParameters</span></span>
<span data-ttu-id="e9b78-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b78-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b78-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9b78-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b78-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9b78-127">INPUTS</span></span>

### <span data-ttu-id="e9b78-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e9b78-128">None</span></span>
<span data-ttu-id="e9b78-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e9b78-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9b78-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9b78-130">OUTPUTS</span></span>

### <span data-ttu-id="e9b78-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e9b78-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>
<span data-ttu-id="e9b78-132">Szczegóły dotyczące wewnętrznej bazy danych skonfigurowane w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="e9b78-132">The details of the Backend configured in API Management service.</span></span>

### <span data-ttu-id="e9b78-133">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementBackend></span><span class="sxs-lookup"><span data-stu-id="e9b78-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>
<span data-ttu-id="e9b78-134">Lista zaplecza skonfigurowana w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="e9b78-134">The list of Backend configured in API Management service.</span></span>

## <span data-ttu-id="e9b78-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9b78-135">NOTES</span></span>

## <span data-ttu-id="e9b78-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9b78-136">RELATED LINKS</span></span>

[<span data-ttu-id="e9b78-137">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e9b78-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="e9b78-138">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e9b78-138">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="e9b78-139">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e9b78-139">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="e9b78-140">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e9b78-140">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="e9b78-141">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e9b78-141">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
