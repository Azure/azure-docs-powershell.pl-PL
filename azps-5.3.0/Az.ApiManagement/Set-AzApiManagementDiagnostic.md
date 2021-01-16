---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381754"
---
# <span data-ttu-id="94bef-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="94bef-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="94bef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94bef-102">SYNOPSIS</span></span>
<span data-ttu-id="94bef-103">Modyfikuje diagnostykę zarządzania interfejsem API w zakresie globalnym lub interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="94bef-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="94bef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94bef-104">SYNTAX</span></span>

### <span data-ttu-id="94bef-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="94bef-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94bef-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="94bef-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94bef-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="94bef-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94bef-108">Opis</span><span class="sxs-lookup"><span data-stu-id="94bef-108">DESCRIPTION</span></span>
<span data-ttu-id="94bef-109">Polecenie cmdlet **Set-AzApiManagementDiagnostic** aktualizuje diagnostykę, która jest skonfigurowana w zakresie globalnym lub interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="94bef-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="94bef-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94bef-110">EXAMPLES</span></span>

### <span data-ttu-id="94bef-111">Przykład 1: modyfikowanie diagnostyki w zakresie globalnym</span><span class="sxs-lookup"><span data-stu-id="94bef-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="94bef-112">To polecenie modyfikuje określoną wartość procentową próbkowania diagnostycznego z 100 do 50%.</span><span class="sxs-lookup"><span data-stu-id="94bef-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="94bef-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="94bef-113">Example 2</span></span>

<span data-ttu-id="94bef-114">Modyfikuje diagnostykę zarządzania interfejsem API w zakresie globalnym lub interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="94bef-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="94bef-115">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="94bef-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="94bef-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94bef-116">PARAMETERS</span></span>

### <span data-ttu-id="94bef-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="94bef-117">-AlwaysLog</span></span>
<span data-ttu-id="94bef-118">Określa typy wiadomości, które nie powinny być stosowane przez ustawienia próbkowania.</span><span class="sxs-lookup"><span data-stu-id="94bef-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="94bef-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="94bef-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="94bef-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="94bef-120">-ApiId</span></span>
<span data-ttu-id="94bef-121">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="94bef-121">Identifier of existing API.</span></span>
<span data-ttu-id="94bef-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="94bef-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="94bef-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="94bef-123">-BackendSetting</span></span>
<span data-ttu-id="94bef-124">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="94bef-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="94bef-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="94bef-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="94bef-126">-Context</span><span class="sxs-lookup"><span data-stu-id="94bef-126">-Context</span></span>
<span data-ttu-id="94bef-127">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="94bef-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="94bef-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="94bef-128">This parameter is required.</span></span>

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

### <span data-ttu-id="94bef-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94bef-129">-DefaultProfile</span></span>
<span data-ttu-id="94bef-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94bef-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94bef-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="94bef-131">-DiagnosticId</span></span>
<span data-ttu-id="94bef-132">Identyfikator istniejącej diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="94bef-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="94bef-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="94bef-133">This parameter is required.</span></span>

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

### <span data-ttu-id="94bef-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="94bef-134">-FrontEndSetting</span></span>
<span data-ttu-id="94bef-135">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="94bef-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="94bef-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="94bef-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="94bef-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="94bef-137">-InputObject</span></span>
<span data-ttu-id="94bef-138">Wystąpienie PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="94bef-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="94bef-139">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="94bef-139">This parameter is required.</span></span>

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

### <span data-ttu-id="94bef-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="94bef-140">-LoggerId</span></span>
<span data-ttu-id="94bef-141">Identyfikator rejestratora, do którego mają być wypychane testy diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="94bef-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="94bef-142">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="94bef-142">This parameter is required.</span></span>

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

### <span data-ttu-id="94bef-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94bef-143">-PassThru</span></span>
<span data-ttu-id="94bef-144">Jeśli jest określone, wystąpienie systemu Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementDiagnostic reprezentujące zestaw danych diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="94bef-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="94bef-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94bef-145">-ResourceId</span></span>
<span data-ttu-id="94bef-146">Identyfikator zasobu ARM w diagnostyce diagnostycznej lub API.</span><span class="sxs-lookup"><span data-stu-id="94bef-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="94bef-147">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="94bef-147">This parameter is required.</span></span>

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

### <span data-ttu-id="94bef-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="94bef-148">-SamplingSetting</span></span>
<span data-ttu-id="94bef-149">Ustawienie próbkowania diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="94bef-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="94bef-150">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="94bef-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="94bef-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94bef-151">-Confirm</span></span>
<span data-ttu-id="94bef-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94bef-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94bef-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94bef-153">-WhatIf</span></span>
<span data-ttu-id="94bef-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94bef-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94bef-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="94bef-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94bef-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94bef-156">CommonParameters</span></span>
<span data-ttu-id="94bef-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94bef-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94bef-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94bef-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94bef-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94bef-159">INPUTS</span></span>

### <span data-ttu-id="94bef-160">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="94bef-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="94bef-161">System. String</span><span class="sxs-lookup"><span data-stu-id="94bef-161">System.String</span></span>

### <span data-ttu-id="94bef-162">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="94bef-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="94bef-163">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="94bef-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="94bef-164">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="94bef-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="94bef-165">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="94bef-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="94bef-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94bef-166">OUTPUTS</span></span>

### <span data-ttu-id="94bef-167">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="94bef-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="94bef-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94bef-168">NOTES</span></span>

## <span data-ttu-id="94bef-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94bef-169">RELATED LINKS</span></span>
