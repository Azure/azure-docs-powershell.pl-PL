---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 88a48edf3ae7e576aa78e989a5fda7515499a7f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704653"
---
# <span data-ttu-id="49cd3-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="49cd3-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="49cd3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="49cd3-103">Zapoznaj się z informacjami o wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="49cd3-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="49cd3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49cd3-104">SYNTAX</span></span>

### <span data-ttu-id="49cd3-105">GetAllBackends (domyślny)</span><span class="sxs-lookup"><span data-stu-id="49cd3-105">GetAllBackends (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49cd3-106">GetByBackendId</span><span class="sxs-lookup"><span data-stu-id="49cd3-106">GetByBackendId</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49cd3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="49cd3-107">DESCRIPTION</span></span>
<span data-ttu-id="49cd3-108">Zapoznaj się z informacjami o wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="49cd3-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="49cd3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49cd3-109">EXAMPLES</span></span>

### <span data-ttu-id="49cd3-110">Przykład 1: uzyskiwanie wszystkich zakończeń</span><span class="sxs-lookup"><span data-stu-id="49cd3-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="49cd3-111">Pobiera listę wszystkich punktów końcowych skonfigurowanych w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="49cd3-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="49cd3-112">Przykład 2: pobieranie wewnętrznej bazy danych określonej przez identyfikator 123</span><span class="sxs-lookup"><span data-stu-id="49cd3-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="49cd3-113">Uzyskiwanie szczegółów dotyczących określonej zaplecza wewnętrznego określonego identyfikatorem ' 123 '</span><span class="sxs-lookup"><span data-stu-id="49cd3-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="49cd3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49cd3-114">PARAMETERS</span></span>

### <span data-ttu-id="49cd3-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="49cd3-115">-BackendId</span></span>
<span data-ttu-id="49cd3-116">Identyfikator wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="49cd3-116">Identifier of a backend.</span></span>
<span data-ttu-id="49cd3-117">Jeśli zostanie określona, spróbuje znaleźć zaplecze o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="49cd3-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="49cd3-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="49cd3-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="49cd3-119">-Context</span><span class="sxs-lookup"><span data-stu-id="49cd3-119">-Context</span></span>
<span data-ttu-id="49cd3-120">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="49cd3-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="49cd3-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="49cd3-121">This parameter is required.</span></span>

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

### <span data-ttu-id="49cd3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49cd3-122">-DefaultProfile</span></span>
<span data-ttu-id="49cd3-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="49cd3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49cd3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49cd3-124">CommonParameters</span></span>
<span data-ttu-id="49cd3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49cd3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49cd3-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49cd3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49cd3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49cd3-127">INPUTS</span></span>

### <span data-ttu-id="49cd3-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="49cd3-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="49cd3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="49cd3-129">System.String</span></span>

## <span data-ttu-id="49cd3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49cd3-130">OUTPUTS</span></span>

### <span data-ttu-id="49cd3-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="49cd3-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="49cd3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49cd3-132">NOTES</span></span>

## <span data-ttu-id="49cd3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49cd3-133">RELATED LINKS</span></span>

[<span data-ttu-id="49cd3-134">Nowe — AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="49cd3-134">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="49cd3-135">Nowe — AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="49cd3-135">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="49cd3-136">Nowe — AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="49cd3-136">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="49cd3-137">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="49cd3-137">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="49cd3-138">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="49cd3-138">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
