---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: f977b4dab003b3d1a1b83f1b81701a6089e1cefa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232347"
---
# <span data-ttu-id="38a42-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="38a42-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="38a42-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38a42-102">SYNOPSIS</span></span>
<span data-ttu-id="38a42-103">Tworzy nową diagnostykę w zakresie globalnym lub w zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="38a42-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="38a42-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38a42-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38a42-105">Opis</span><span class="sxs-lookup"><span data-stu-id="38a42-105">DESCRIPTION</span></span>
<span data-ttu-id="38a42-106">Polecenie cmdlet **New-AzApiManagementDiagnostic** tworzy jednostkę diagnostyczną w zakresie globalnym lub w konkretnym zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="38a42-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="38a42-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38a42-107">EXAMPLES</span></span>

### <span data-ttu-id="38a42-108">Przykład 1. Tworzenie nowego globalnego zakresu diagnostycznego</span><span class="sxs-lookup"><span data-stu-id="38a42-108">Example 1: Create a new Global scope Diagnostic</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId "backendapisachinc"
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -AlwaysLog allErrors -SamplingSetting $samplingSetting  -DiagnosticId "applicationinsights"

DiagnosticId                 : applicationinsights
ApiId                        :
AlwaysLog                    : allErrors
LoggerId                     : backendapisachinc
EnableHttpCorrelationHeaders : True
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              :
BackendSetting               :
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUs/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName            : Api-Default-WestUs
ServiceName                  : contoso
```

<span data-ttu-id="38a42-109">W tym przykładzie pokazano, jak utworzyć jednostkę diagnostyczną w zakresie globalnym.</span><span class="sxs-lookup"><span data-stu-id="38a42-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="38a42-110">Przykład 2: Tworzenie diagnostyki w zakresie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="38a42-110">Example 2: Create a diagnostic at Api scope</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS D:\github\azure-powershell> $logger = Get-AzApiManagementLogger -Context $context -LoggerId azuremonitor
PS D:\github\azure-powershell> $samplingsetting = New-AzApiManagementSamplingSetting -SamplingType fixed -SamplingPercentage 100
PS D:\github\azure-powershell> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -HeadersToLog 'Content-Type', 'User-Agent' -BodyBytesToLog 100
PS D:\github\azure-powershell> $pipelineDiagnostic = New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic
PS D:\github\azure-powershell> New-AzApiManagementDiagnostic -LoggerId $logger.LoggerId -Context $context -ApiId httpbin -AlwaysLog allErrors -SamplingSetting $samplingsetting -FrontEndSetting $pipelineDiagnostic -BackendSetting $pipelineDiagnostic -DiagnosticId azuremonitor

DiagnosticId                 : azuremonitor
ApiId                        : httpbin
AlwaysLog                    : allErrors
LoggerId                     : azuremonitor
EnableHttpCorrelationHeaders :
SamplingSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
FrontendSetting              : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
BackendSetting               : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Id                           : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/httpbin/diagnostics/azuremonitor      
ResourceGroupName            : Api-Default-WestUS
ServiceName                  : contoso
```

<span data-ttu-id="38a42-111">Powyższym przykładem jest utworzenie diagnostycznego interfejsu API `httpbin` w celu zarejestrowania nagłówka i 100 bajtów treści do `azuremonitor` rejestratora.</span><span class="sxs-lookup"><span data-stu-id="38a42-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="38a42-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38a42-112">PARAMETERS</span></span>

### <span data-ttu-id="38a42-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="38a42-113">-AlwaysLog</span></span>
<span data-ttu-id="38a42-114">Określa typy wiadomości, które nie powinny być stosowane przez ustawienia próbkowania.</span><span class="sxs-lookup"><span data-stu-id="38a42-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="38a42-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="38a42-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="38a42-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="38a42-116">-ApiId</span></span>
<span data-ttu-id="38a42-117">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="38a42-117">Identifier of existing API.</span></span>
<span data-ttu-id="38a42-118">Jeśli określisz, ustaw zasady dotyczące zakresu interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="38a42-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="38a42-119">Te parametry są wymagane.</span><span class="sxs-lookup"><span data-stu-id="38a42-119">This parameters is required.</span></span>

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

### <span data-ttu-id="38a42-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="38a42-120">-BackendSetting</span></span>
<span data-ttu-id="38a42-121">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="38a42-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="38a42-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="38a42-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a42-123">-Context</span><span class="sxs-lookup"><span data-stu-id="38a42-123">-Context</span></span>
<span data-ttu-id="38a42-124">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="38a42-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="38a42-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="38a42-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38a42-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a42-126">-DefaultProfile</span></span>
<span data-ttu-id="38a42-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38a42-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38a42-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="38a42-128">-DiagnosticId</span></span>
<span data-ttu-id="38a42-129">Identyfikator jednostki diagnostycznej.</span><span class="sxs-lookup"><span data-stu-id="38a42-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="38a42-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="38a42-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="38a42-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="38a42-131">-FrontEndSetting</span></span>
<span data-ttu-id="38a42-132">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="38a42-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="38a42-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="38a42-133">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a42-134">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="38a42-134">-LoggerId</span></span>
<span data-ttu-id="38a42-135">Identyfikator rejestratora, do którego mają być wypychane testy diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="38a42-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="38a42-136">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="38a42-136">This parameter is required.</span></span>

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

### <span data-ttu-id="38a42-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="38a42-137">-SamplingSetting</span></span>
<span data-ttu-id="38a42-138">Ustawienie próbkowania diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="38a42-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="38a42-139">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="38a42-139">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a42-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38a42-140">-Confirm</span></span>
<span data-ttu-id="38a42-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38a42-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a42-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38a42-142">-WhatIf</span></span>
<span data-ttu-id="38a42-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38a42-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38a42-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="38a42-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a42-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a42-145">CommonParameters</span></span>
<span data-ttu-id="38a42-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a42-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a42-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38a42-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a42-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38a42-148">INPUTS</span></span>

### <span data-ttu-id="38a42-149">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="38a42-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="38a42-150">System. String</span><span class="sxs-lookup"><span data-stu-id="38a42-150">System.String</span></span>

### <span data-ttu-id="38a42-151">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="38a42-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="38a42-152">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="38a42-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="38a42-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38a42-153">OUTPUTS</span></span>

### <span data-ttu-id="38a42-154">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="38a42-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="38a42-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38a42-155">NOTES</span></span>

## <span data-ttu-id="38a42-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38a42-156">RELATED LINKS</span></span>

[<span data-ttu-id="38a42-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="38a42-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="38a42-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="38a42-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="38a42-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="38a42-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="38a42-160">Nowe — AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="38a42-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="38a42-161">Nowe — AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="38a42-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)