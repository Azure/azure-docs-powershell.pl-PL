---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementBackend.md
ms.openlocfilehash: 4781800ea9a6f8526ddee5e06b90b73ea676bf88
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239890"
---
# <span data-ttu-id="0b987-101">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0b987-101">Get-AzApiManagementBackend</span></span>

## <span data-ttu-id="0b987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b987-102">SYNOPSIS</span></span>
<span data-ttu-id="0b987-103">Poznaj szczegóły dotyczące bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0b987-103">Get the details of the Backend.</span></span>

## <span data-ttu-id="0b987-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0b987-104">SYNTAX</span></span>

### <span data-ttu-id="0b987-105">ContextParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="0b987-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b987-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b987-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementBackend [-BackendId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b987-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0b987-107">DESCRIPTION</span></span>
<span data-ttu-id="0b987-108">Poznaj szczegóły dotyczące bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0b987-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="0b987-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0b987-109">EXAMPLES</span></span>

### <span data-ttu-id="0b987-110">Przykład 1. Pobierz wszystkie bazy danych</span><span class="sxs-lookup"><span data-stu-id="0b987-110">Example 1: Get all Backends</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext
```

<span data-ttu-id="0b987-111">Pobiera listę wszystkich zaplecza skonfigurowanych w usłudze zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="0b987-111">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="0b987-112">Przykład 2. Uzyskiwanie bazy danych określonej przez identyfikator 123</span><span class="sxs-lookup"><span data-stu-id="0b987-112">Example 2: Get the Backend specified by the Identifier 123</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="0b987-113">Szczegółowe informacje dotyczące wskazanej bazy danych oznaczonej identyfikatorem "123"</span><span class="sxs-lookup"><span data-stu-id="0b987-113">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="0b987-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b987-114">PARAMETERS</span></span>

### <span data-ttu-id="0b987-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="0b987-115">-BackendId</span></span>
<span data-ttu-id="0b987-116">Identyfikator zaplecza.</span><span class="sxs-lookup"><span data-stu-id="0b987-116">Identifier of a backend.</span></span>
<span data-ttu-id="0b987-117">Jeśli zostanie określona, spróbuje znaleźć kopię zapasową za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="0b987-117">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="0b987-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="0b987-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="0b987-119">— kontekst</span><span class="sxs-lookup"><span data-stu-id="0b987-119">-Context</span></span>
<span data-ttu-id="0b987-120">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0b987-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0b987-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0b987-121">This parameter is required.</span></span>

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

### <span data-ttu-id="0b987-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b987-122">-DefaultProfile</span></span>
<span data-ttu-id="0b987-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b987-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b987-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b987-124">-ResourceId</span></span>
<span data-ttu-id="0b987-125">Identyfikator zasobu arm bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0b987-125">Arm Resource Identifier of the backend.</span></span> <span data-ttu-id="0b987-126">Jeśli zostanie określona, spróbuje znaleźć kopię zapasową za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="0b987-126">If specified will try to find backend by the identifier.</span></span> <span data-ttu-id="0b987-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0b987-127">This parameter is required.</span></span>

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

### <span data-ttu-id="0b987-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b987-128">CommonParameters</span></span>
<span data-ttu-id="0b987-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b987-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b987-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b987-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b987-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b987-131">INPUTS</span></span>

### <span data-ttu-id="0b987-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0b987-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0b987-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0b987-133">System.String</span></span>

## <span data-ttu-id="0b987-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b987-134">OUTPUTS</span></span>

### <span data-ttu-id="0b987-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0b987-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="0b987-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0b987-136">NOTES</span></span>

## <span data-ttu-id="0b987-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b987-137">RELATED LINKS</span></span>

[<span data-ttu-id="0b987-138">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0b987-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="0b987-139">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0b987-139">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="0b987-140">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="0b987-140">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="0b987-141">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0b987-141">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="0b987-142">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0b987-142">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
