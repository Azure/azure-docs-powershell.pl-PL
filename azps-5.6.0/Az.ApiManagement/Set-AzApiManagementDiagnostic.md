---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c9cb592713f7a24739651d36855fdf595ffc7eeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965425"
---
# <span data-ttu-id="2f41c-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2f41c-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="2f41c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f41c-102">SYNOPSIS</span></span>
<span data-ttu-id="2f41c-103">Modyfikuje diagnostykę zarządzania interfejsem API w zakresie globalnym lub api.</span><span class="sxs-lookup"><span data-stu-id="2f41c-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="2f41c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2f41c-104">SYNTAX</span></span>

### <span data-ttu-id="2f41c-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="2f41c-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f41c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2f41c-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f41c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f41c-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f41c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2f41c-108">DESCRIPTION</span></span>
<span data-ttu-id="2f41c-109">Polecenie cmdlet **Set-AzApiManagementDiagnostic** aktualizuje diagnostykę skonfigurowaną w zakresie globalnym lub api.</span><span class="sxs-lookup"><span data-stu-id="2f41c-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="2f41c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2f41c-110">EXAMPLES</span></span>

### <span data-ttu-id="2f41c-111">Przykład 1. Modyfikowanie diagnostyki w zakresie globalnym</span><span class="sxs-lookup"><span data-stu-id="2f41c-111">Example 1: Modify a diagnostic at the Global scope</span></span>
```powershell
PS c:\> $context =New-AzApiManagementContext -ResourceGroupName Api-Default-WestUS -ServiceName contoso
PS c:\> $diagnostic=Get-AzApiManagementDiagnostic -Context $context -DiagnosticId "applicationinsights"
PS c:\> $diagnostic

DiagnosticId      : applicationinsights
AlwaysLog         : allErrors
LoggerId          : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/loggers/backendapisachinc
Sampling          : Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting
Frontend          :
Backend           :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/diagnostics/applicationinsights
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso


PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed               100

PS c:\> $diagnostic.Sampling.Percentage = 50
PS c:\> $diagnostic.Sampling

SamplingType Percentage
------------ ----------
fixed                50

PS c:\> Set-AzApiManagementDiagnostic -InputObject $diagnostic
```

<span data-ttu-id="2f41c-112">To polecenie modyfikuje określoną wartość procentową próbkowania diagnostycznego z 100 do 50%</span><span class="sxs-lookup"><span data-stu-id="2f41c-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="2f41c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2f41c-113">Example 2</span></span>

<span data-ttu-id="2f41c-114">Modyfikuje diagnostykę zarządzania interfejsem API w zakresie globalnym lub api.</span><span class="sxs-lookup"><span data-stu-id="2f41c-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="2f41c-115">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="2f41c-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="2f41c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f41c-116">PARAMETERS</span></span>

### <span data-ttu-id="2f41c-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="2f41c-117">-AlwaysLog</span></span>
<span data-ttu-id="2f41c-118">Określa, jakiego typu ustawienia próbkowania wiadomości nie powinny być stosowane.</span><span class="sxs-lookup"><span data-stu-id="2f41c-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="2f41c-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2f41c-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="2f41c-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2f41c-120">-ApiId</span></span>
<span data-ttu-id="2f41c-121">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="2f41c-121">Identifier of existing API.</span></span>
<span data-ttu-id="2f41c-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2f41c-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f41c-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="2f41c-123">-BackendSetting</span></span>
<span data-ttu-id="2f41c-124">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP w zaplecza.</span><span class="sxs-lookup"><span data-stu-id="2f41c-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="2f41c-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2f41c-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="2f41c-126">— kontekst</span><span class="sxs-lookup"><span data-stu-id="2f41c-126">-Context</span></span>
<span data-ttu-id="2f41c-127">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2f41c-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2f41c-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2f41c-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f41c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f41c-129">-DefaultProfile</span></span>
<span data-ttu-id="2f41c-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f41c-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f41c-131">- DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="2f41c-131">-DiagnosticId</span></span>
<span data-ttu-id="2f41c-132">Identyfikator istniejącej diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="2f41c-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="2f41c-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2f41c-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f41c-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="2f41c-134">-FrontEndSetting</span></span>
<span data-ttu-id="2f41c-135">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="2f41c-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="2f41c-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2f41c-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="2f41c-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f41c-137">-InputObject</span></span>
<span data-ttu-id="2f41c-138">Wystąpienie programu PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="2f41c-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="2f41c-139">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2f41c-139">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f41c-140">-LogId</span><span class="sxs-lookup"><span data-stu-id="2f41c-140">-LoggerId</span></span>
<span data-ttu-id="2f41c-141">Identyfikator loglogii w celu wypychania diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="2f41c-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="2f41c-142">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2f41c-142">This parameter is required.</span></span>

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

### <span data-ttu-id="2f41c-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f41c-143">-PassThru</span></span>
<span data-ttu-id="2f41c-144">Jeśli określono, wówczas wystąpienie microsoft.azure.commands.apiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic (Diagnostyka zestawu).</span><span class="sxs-lookup"><span data-stu-id="2f41c-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f41c-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f41c-145">-ResourceId</span></span>
<span data-ttu-id="2f41c-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="2f41c-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="2f41c-147">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2f41c-147">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f41c-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="2f41c-148">-SamplingSetting</span></span>
<span data-ttu-id="2f41c-149">Ustawienie próbkowania narzędzia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="2f41c-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="2f41c-150">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2f41c-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="2f41c-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f41c-151">-Confirm</span></span>
<span data-ttu-id="2f41c-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2f41c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f41c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f41c-153">-WhatIf</span></span>
<span data-ttu-id="2f41c-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f41c-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f41c-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2f41c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f41c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f41c-156">CommonParameters</span></span>
<span data-ttu-id="2f41c-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f41c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f41c-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f41c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f41c-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f41c-159">INPUTS</span></span>

### <span data-ttu-id="2f41c-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2f41c-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2f41c-161">System.String</span><span class="sxs-lookup"><span data-stu-id="2f41c-161">System.String</span></span>

### <span data-ttu-id="2f41c-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2f41c-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="2f41c-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="2f41c-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="2f41c-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="2f41c-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="2f41c-165">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="2f41c-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2f41c-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f41c-166">OUTPUTS</span></span>

### <span data-ttu-id="2f41c-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2f41c-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="2f41c-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2f41c-168">NOTES</span></span>

## <span data-ttu-id="2f41c-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f41c-169">RELATED LINKS</span></span>
