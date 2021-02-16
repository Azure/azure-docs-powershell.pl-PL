---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244378"
---
# <span data-ttu-id="c0d22-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c0d22-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="c0d22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0d22-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d22-103">Modyfikuje diagnostykę zarządzania interfejsem API w zakresie globalnym lub api.</span><span class="sxs-lookup"><span data-stu-id="c0d22-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="c0d22-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0d22-104">SYNTAX</span></span>

### <span data-ttu-id="c0d22-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c0d22-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0d22-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0d22-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0d22-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0d22-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0d22-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0d22-108">DESCRIPTION</span></span>
<span data-ttu-id="c0d22-109">Polecenie cmdlet **Set-AzApiManagementDiagnostic** aktualizuje diagnostykę skonfigurowaną w zakresie globalnym lub api.</span><span class="sxs-lookup"><span data-stu-id="c0d22-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="c0d22-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0d22-110">EXAMPLES</span></span>

### <span data-ttu-id="c0d22-111">Przykład 1. Modyfikowanie diagnostyki w zakresie globalnym</span><span class="sxs-lookup"><span data-stu-id="c0d22-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="c0d22-112">To polecenie modyfikuje określoną wartość procentową próbkowania diagnostycznego z 100 do 50%</span><span class="sxs-lookup"><span data-stu-id="c0d22-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="c0d22-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c0d22-113">Example 2</span></span>

<span data-ttu-id="c0d22-114">Modyfikuje diagnostykę zarządzania interfejsem API w zakresie globalnym lub api.</span><span class="sxs-lookup"><span data-stu-id="c0d22-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="c0d22-115">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="c0d22-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="c0d22-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0d22-116">PARAMETERS</span></span>

### <span data-ttu-id="c0d22-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="c0d22-117">-AlwaysLog</span></span>
<span data-ttu-id="c0d22-118">Określa, jakiego typu ustawienia próbkowania wiadomości nie powinny być stosowane.</span><span class="sxs-lookup"><span data-stu-id="c0d22-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="c0d22-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c0d22-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="c0d22-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c0d22-120">-ApiId</span></span>
<span data-ttu-id="c0d22-121">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c0d22-121">Identifier of existing API.</span></span>
<span data-ttu-id="c0d22-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c0d22-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="c0d22-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="c0d22-123">-BackendSetting</span></span>
<span data-ttu-id="c0d22-124">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP w zaplecza.</span><span class="sxs-lookup"><span data-stu-id="c0d22-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="c0d22-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c0d22-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="c0d22-126">— kontekst</span><span class="sxs-lookup"><span data-stu-id="c0d22-126">-Context</span></span>
<span data-ttu-id="c0d22-127">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c0d22-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c0d22-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c0d22-128">This parameter is required.</span></span>

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

### <span data-ttu-id="c0d22-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d22-129">-DefaultProfile</span></span>
<span data-ttu-id="c0d22-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0d22-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0d22-131">- DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="c0d22-131">-DiagnosticId</span></span>
<span data-ttu-id="c0d22-132">Identyfikator istniejącej diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="c0d22-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="c0d22-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c0d22-133">This parameter is required.</span></span>

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

### <span data-ttu-id="c0d22-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="c0d22-134">-FrontEndSetting</span></span>
<span data-ttu-id="c0d22-135">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="c0d22-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="c0d22-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c0d22-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="c0d22-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0d22-137">-InputObject</span></span>
<span data-ttu-id="c0d22-138">Wystąpienie programu PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="c0d22-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="c0d22-139">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c0d22-139">This parameter is required.</span></span>

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

### <span data-ttu-id="c0d22-140">-LogId</span><span class="sxs-lookup"><span data-stu-id="c0d22-140">-LoggerId</span></span>
<span data-ttu-id="c0d22-141">Identyfikator loglogii w celu wypychania diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="c0d22-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="c0d22-142">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c0d22-142">This parameter is required.</span></span>

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

### <span data-ttu-id="c0d22-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0d22-143">-PassThru</span></span>
<span data-ttu-id="c0d22-144">Jeśli określono, wówczas wystąpienie microsoft.azure.commands.apiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic (Diagnostyka zestawu).</span><span class="sxs-lookup"><span data-stu-id="c0d22-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="c0d22-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0d22-145">-ResourceId</span></span>
<span data-ttu-id="c0d22-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="c0d22-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="c0d22-147">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c0d22-147">This parameter is required.</span></span>

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

### <span data-ttu-id="c0d22-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c0d22-148">-SamplingSetting</span></span>
<span data-ttu-id="c0d22-149">Ustawienie próbkowania narzędzia diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="c0d22-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="c0d22-150">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c0d22-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="c0d22-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0d22-151">-Confirm</span></span>
<span data-ttu-id="c0d22-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0d22-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0d22-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0d22-153">-WhatIf</span></span>
<span data-ttu-id="c0d22-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0d22-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0d22-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c0d22-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0d22-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d22-156">CommonParameters</span></span>
<span data-ttu-id="c0d22-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0d22-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d22-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0d22-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d22-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0d22-159">INPUTS</span></span>

### <span data-ttu-id="c0d22-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c0d22-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c0d22-161">System.String</span><span class="sxs-lookup"><span data-stu-id="c0d22-161">System.String</span></span>

### <span data-ttu-id="c0d22-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c0d22-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="c0d22-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="c0d22-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="c0d22-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="c0d22-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="c0d22-165">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="c0d22-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c0d22-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c0d22-166">OUTPUTS</span></span>

### <span data-ttu-id="c0d22-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c0d22-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="c0d22-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0d22-168">NOTES</span></span>

## <span data-ttu-id="c0d22-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0d22-169">RELATED LINKS</span></span>
