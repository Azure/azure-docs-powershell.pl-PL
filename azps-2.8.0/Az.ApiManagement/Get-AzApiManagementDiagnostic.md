---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementDiagnostic.md
ms.openlocfilehash: 2ff4660a0e8f4929e8f79c20a8e42e0deac11f3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707081"
---
# <span data-ttu-id="98ad8-101">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="98ad8-101">Get-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="98ad8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="98ad8-103">Uzyskaj szczegółowe informacje o diagnostyce skonfigurowanej na poziomie usługi lub interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="98ad8-103">Get details of the Diagnostic configured at the service level or the Api Level.</span></span> <span data-ttu-id="98ad8-104">Diagnostyka umożliwia rejestrowanie żądań/odpowiedzi z bramy zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="98ad8-104">Diagnostics are used to log requests/responses from Api Management gateway.</span></span>

## <span data-ttu-id="98ad8-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98ad8-105">SYNTAX</span></span>

### <span data-ttu-id="98ad8-106">ContextParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98ad8-106">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-DiagnosticId <String>] [-ApiId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98ad8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98ad8-107">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementDiagnostic -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98ad8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="98ad8-108">DESCRIPTION</span></span>
<span data-ttu-id="98ad8-109">**AzApiManagementDiagnostic** pobiera szczegóły dotyczące diagnostyki skonfigurowanej w usłudze zarządzania interfejsem API w danym zakresie.</span><span class="sxs-lookup"><span data-stu-id="98ad8-109">The **Get-AzApiManagementDiagnostic** gets details of the diagnostics configured in the Api management service at a given scope.</span></span>

## <span data-ttu-id="98ad8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98ad8-110">EXAMPLES</span></span>

### <span data-ttu-id="98ad8-111">Przykład 1: Uzyskaj wszystkie funkcje diagnostyczne skonfigurowane w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="98ad8-111">Example 1: Get all the diagnostic configured at the tenant scope.</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso

DiagnosticId                 : azuremonitor
ApiId                        :
AlwaysLog                    :
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               : 
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/azuremonitor
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="98ad8-112">To polecenie pobiera wszystkie testy diagnostyczne skonfigurowane w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="98ad8-112">This command gets all the diagnostics configured in the Api Management service.</span></span>

### <span data-ttu-id="98ad8-113">Przykład 2: uzyskiwanie wszystkich testów skonfigurowanych w zakresie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="98ad8-113">Example 2: Get all the diagnostics configured at the Api scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="98ad8-114">To polecenie pobiera wszystkie testy diagnostyczne skonfigurowane w `echo-api` zakresie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="98ad8-114">This command gets all the diagnostics configured at the `echo-api` Api scope</span></span>

### <span data-ttu-id="98ad8-115">Przykład 3: pobieranie diagnostycznego o zakresie interfejsów API określonego przez identyfikator</span><span class="sxs-lookup"><span data-stu-id="98ad8-115">Example 3: Get the API-scope diagnostic specified by an Id</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementDiagnostic -Context $apimContext -ApiId "echo-api" -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        : echo-api
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="98ad8-116">To polecenie pobiera `applicationinsights` diagnostykę skonfigurowaną w interfejsie API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="98ad8-116">This command gets the `applicationinsights` diagnostics configured in api `echo-api`.</span></span>

## <span data-ttu-id="98ad8-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98ad8-117">PARAMETERS</span></span>

### <span data-ttu-id="98ad8-118">-ApiId</span><span class="sxs-lookup"><span data-stu-id="98ad8-118">-ApiId</span></span>
<span data-ttu-id="98ad8-119">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="98ad8-119">Identifier of existing API.</span></span>
<span data-ttu-id="98ad8-120">Jeśli ta określona, zwróci komunikat o zakresie diagnostyki zakresu API.</span><span class="sxs-lookup"><span data-stu-id="98ad8-120">If specified will return API-scope diagnostic.</span></span>
<span data-ttu-id="98ad8-121">Te parametry są wymagane.</span><span class="sxs-lookup"><span data-stu-id="98ad8-121">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ad8-122">-Context</span><span class="sxs-lookup"><span data-stu-id="98ad8-122">-Context</span></span>
<span data-ttu-id="98ad8-123">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="98ad8-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="98ad8-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="98ad8-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98ad8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ad8-125">-DefaultProfile</span></span>
<span data-ttu-id="98ad8-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98ad8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98ad8-127">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="98ad8-127">-DiagnosticId</span></span>
<span data-ttu-id="98ad8-128">Identyfikator istniejącej diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="98ad8-128">Identifier of existing diagnostic.</span></span>
<span data-ttu-id="98ad8-129">Jeśli ta określona, zwróci zasady dotyczące zakresu produktów.</span><span class="sxs-lookup"><span data-stu-id="98ad8-129">If specified will return product-scope policy.</span></span>
<span data-ttu-id="98ad8-130">Parametry te są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="98ad8-130">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ad8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98ad8-131">-ResourceId</span></span>
<span data-ttu-id="98ad8-132">Identyfikator zasobu ARM diagnostyki diagnostycznej lub API.</span><span class="sxs-lookup"><span data-stu-id="98ad8-132">Arm Resource Identifier of a Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="98ad8-133">Jeśli zostanie określona, spróbuje znaleźć diagnostykę za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="98ad8-133">If specified will try to find diagnostic by the identifier.</span></span> <span data-ttu-id="98ad8-134">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="98ad8-134">This parameter is required.</span></span>

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

### <span data-ttu-id="98ad8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ad8-135">CommonParameters</span></span>
<span data-ttu-id="98ad8-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98ad8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ad8-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98ad8-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ad8-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98ad8-138">INPUTS</span></span>

### <span data-ttu-id="98ad8-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="98ad8-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="98ad8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="98ad8-140">System.String</span></span>

## <span data-ttu-id="98ad8-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98ad8-141">OUTPUTS</span></span>

### <span data-ttu-id="98ad8-142">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="98ad8-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="98ad8-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98ad8-143">NOTES</span></span>

## <span data-ttu-id="98ad8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98ad8-144">RELATED LINKS</span></span>