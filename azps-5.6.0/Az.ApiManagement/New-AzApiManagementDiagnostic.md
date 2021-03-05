---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementDiagnostic.md
ms.openlocfilehash: a330aa6df0da0be08de925d59e72018a028e7d82
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988576"
---
# <span data-ttu-id="1c3ec-101">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1c3ec-101">New-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="1c3ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3ec-103">Tworzy nową diagnostykę w zakresie globalnym lub zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-103">Creates a new diagnostics at the Global scope or Api Scope.</span></span>

## <span data-ttu-id="1c3ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1c3ec-104">SYNTAX</span></span>

```
New-AzApiManagementDiagnostic -Context <PsApiManagementContext> -LoggerId <String> [-DiagnosticId <String>]
 [-AlwaysLog <String>] [-ApiId <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c3ec-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1c3ec-105">DESCRIPTION</span></span>
<span data-ttu-id="1c3ec-106">Polecenie cmdlet **New-AzApiManagementDiagnostic** tworzy jednostkę diagnostyczną w zakresie globalnym lub określonym zakresie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-106">The cmdlet **New-AzApiManagementDiagnostic** creates a diagnostic entity either at Global scope or specific Api scope.</span></span>

## <span data-ttu-id="1c3ec-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1c3ec-107">EXAMPLES</span></span>

### <span data-ttu-id="1c3ec-108">Przykład 1. Tworzenie nowego narzędzia diagnostycznego zakresów globalnych</span><span class="sxs-lookup"><span data-stu-id="1c3ec-108">Example 1: Create a new Global scope Diagnostic</span></span>
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

<span data-ttu-id="1c3ec-109">W tym przykładzie utworzymy jednostkę diagnostyczną w zakresie globalnym.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-109">This example create a diagnostic entity at the Global Scope.</span></span>

### <span data-ttu-id="1c3ec-110">Przykład 2. Tworzenie diagnostyki w zakresie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="1c3ec-110">Example 2: Create a diagnostic at Api scope</span></span>
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

<span data-ttu-id="1c3ec-111">W powyższym przykładzie jest tworzyć diagnostyczne interfejsu API do dziennika nagłówka i `httpbin` 100 bajtów treści `azuremonitor` do logowania.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-111">The example above create a diagnostic for the API `httpbin` to log the Header and 100 Bytes of Body to `azuremonitor` logger.</span></span>

## <span data-ttu-id="1c3ec-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c3ec-112">PARAMETERS</span></span>

### <span data-ttu-id="1c3ec-113">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="1c3ec-113">-AlwaysLog</span></span>
<span data-ttu-id="1c3ec-114">Określa, jakiego typu ustawienia próbkowania wiadomości nie powinny być stosowane.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-114">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="1c3ec-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="1c3ec-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1c3ec-116">-ApiId</span></span>
<span data-ttu-id="1c3ec-117">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-117">Identifier of existing API.</span></span>
<span data-ttu-id="1c3ec-118">Jeśli zostanie określona, zostaną ustawione zasady zakresu interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-118">If specified will set API-scope policy.</span></span>
<span data-ttu-id="1c3ec-119">Te parametry są wymagane.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-119">This parameters is required.</span></span>

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

### <span data-ttu-id="1c3ec-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="1c3ec-120">-BackendSetting</span></span>
<span data-ttu-id="1c3ec-121">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP w zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="1c3ec-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="1c3ec-123">— kontekst</span><span class="sxs-lookup"><span data-stu-id="1c3ec-123">-Context</span></span>
<span data-ttu-id="1c3ec-124">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1c3ec-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-125">This parameter is required.</span></span>

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

### <span data-ttu-id="1c3ec-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3ec-126">-DefaultProfile</span></span>
<span data-ttu-id="1c3ec-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c3ec-128">- DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="1c3ec-128">-DiagnosticId</span></span>
<span data-ttu-id="1c3ec-129">Identyfikator jednostki diagnostycznej.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-129">Identifier of the diagnostics entity.</span></span>
<span data-ttu-id="1c3ec-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="1c3ec-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="1c3ec-131">-FrontEndSetting</span></span>
<span data-ttu-id="1c3ec-132">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="1c3ec-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="1c3ec-134">-LogId</span><span class="sxs-lookup"><span data-stu-id="1c3ec-134">-LoggerId</span></span>
<span data-ttu-id="1c3ec-135">Identyfikator loglogii w celu wypychania diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-135">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="1c3ec-136">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-136">This parameter is required.</span></span>

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

### <span data-ttu-id="1c3ec-137">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="1c3ec-137">-SamplingSetting</span></span>
<span data-ttu-id="1c3ec-138">Ustawienie próbkowania narzędzia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-138">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="1c3ec-139">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="1c3ec-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c3ec-140">-Confirm</span></span>
<span data-ttu-id="1c3ec-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c3ec-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c3ec-142">-WhatIf</span></span>
<span data-ttu-id="1c3ec-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c3ec-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c3ec-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3ec-145">CommonParameters</span></span>
<span data-ttu-id="1c3ec-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3ec-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c3ec-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3ec-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c3ec-148">INPUTS</span></span>

### <span data-ttu-id="1c3ec-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1c3ec-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1c3ec-150">System.String</span><span class="sxs-lookup"><span data-stu-id="1c3ec-150">System.String</span></span>

### <span data-ttu-id="1c3ec-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="1c3ec-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="1c3ec-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="1c3ec-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="1c3ec-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c3ec-153">OUTPUTS</span></span>

### <span data-ttu-id="1c3ec-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1c3ec-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="1c3ec-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1c3ec-155">NOTES</span></span>

## <span data-ttu-id="1c3ec-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c3ec-156">RELATED LINKS</span></span>

[<span data-ttu-id="1c3ec-157">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1c3ec-157">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="1c3ec-158">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1c3ec-158">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="1c3ec-159">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1c3ec-159">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="1c3ec-160">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="1c3ec-160">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

[<span data-ttu-id="1c3ec-161">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="1c3ec-161">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)