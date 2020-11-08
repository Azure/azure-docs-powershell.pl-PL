---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050909"
---
# <span data-ttu-id="aa488-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aa488-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="aa488-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa488-102">SYNOPSIS</span></span>
<span data-ttu-id="aa488-103">Zapoznaj się z informacjami o wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="aa488-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="aa488-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa488-104">SYNTAX</span></span>

### <span data-ttu-id="aa488-105">ContextParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aa488-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa488-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa488-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa488-107">Opis</span><span class="sxs-lookup"><span data-stu-id="aa488-107">DESCRIPTION</span></span>
<span data-ttu-id="aa488-108">Zapoznaj się z informacjami o wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="aa488-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="aa488-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa488-109">EXAMPLES</span></span>

### <span data-ttu-id="aa488-110">Przykład 1: uzyskiwanie wszystkich zakończeń</span><span class="sxs-lookup"><span data-stu-id="aa488-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="aa488-111">Pobiera listę wszystkich punktów końcowych skonfigurowanych w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="aa488-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="aa488-112">Przykład 2: pobieranie wewnętrznej bazy danych określonej przez identyfikator 123</span><span class="sxs-lookup"><span data-stu-id="aa488-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="aa488-113">Uzyskiwanie szczegółów dotyczących określonej zaplecza wewnętrznego określonego identyfikatorem ' 123 '</span><span class="sxs-lookup"><span data-stu-id="aa488-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="aa488-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa488-114">PARAMETERS</span></span>

### <span data-ttu-id="aa488-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="aa488-115">-BackendId</span></span>
<span data-ttu-id="aa488-116">Identyfikator wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="aa488-116">Identifier of a backend.</span></span>
<span data-ttu-id="aa488-117">Jeśli zostanie określona, spróbuje znaleźć zaplecze o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="aa488-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="aa488-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="aa488-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="aa488-119">-Context</span><span class="sxs-lookup"><span data-stu-id="aa488-119">-Context</span></span>
<span data-ttu-id="aa488-120">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="aa488-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aa488-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="aa488-121">This parameter is required.</span></span>

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

### <span data-ttu-id="aa488-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa488-122">-DefaultProfile</span></span>
<span data-ttu-id="aa488-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa488-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa488-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa488-124">-ResourceId</span></span>
<span data-ttu-id="aa488-125">Identyfikator zasobu ARM wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="aa488-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="aa488-126">Jeśli zostanie określona, spróbuje znaleźć zaplecze o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="aa488-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="aa488-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="aa488-127">This parameter is required.</span></span>

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

### <span data-ttu-id="aa488-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa488-128">CommonParameters</span></span>
<span data-ttu-id="aa488-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa488-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa488-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa488-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa488-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa488-131">INPUTS</span></span>

### <span data-ttu-id="aa488-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aa488-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aa488-133">System. String</span><span class="sxs-lookup"><span data-stu-id="aa488-133">System.String</span></span>

## <span data-ttu-id="aa488-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa488-134">OUTPUTS</span></span>

### <span data-ttu-id="aa488-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aa488-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="aa488-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa488-136">NOTES</span></span>

## <span data-ttu-id="aa488-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa488-137">RELATED LINKS</span></span>

[<span data-ttu-id="aa488-138">Nowe — AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aa488-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="aa488-139">Nowe — AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="aa488-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="aa488-140">Nowe — AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="aa488-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="aa488-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aa488-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="aa488-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aa488-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
