---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: c646e7f39b5149803161bfc7b97ed64b5517dd9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063005"
---
# <span data-ttu-id="33c9e-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="33c9e-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="33c9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33c9e-102">SYNOPSIS</span></span>
<span data-ttu-id="33c9e-103">Modyfikuje diagnostykę zarządzania interfejsem API w zakresie globalnym lub interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="33c9e-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="33c9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33c9e-104">SYNTAX</span></span>

### <span data-ttu-id="33c9e-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="33c9e-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33c9e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="33c9e-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33c9e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="33c9e-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33c9e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="33c9e-108">DESCRIPTION</span></span>
<span data-ttu-id="33c9e-109">Polecenie cmdlet **Set-AzApiManagementDiagnostic** aktualizuje diagnostykę, która jest skonfigurowana w zakresie globalnym lub interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="33c9e-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="33c9e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33c9e-110">EXAMPLES</span></span>

### <span data-ttu-id="33c9e-111">Przykład 1: modyfikowanie diagnostyki w zakresie globalnym</span><span class="sxs-lookup"><span data-stu-id="33c9e-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="33c9e-112">To polecenie modyfikuje określoną wartość procentową próbkowania diagnostycznego z 100 do 50%.</span><span class="sxs-lookup"><span data-stu-id="33c9e-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

### <span data-ttu-id="33c9e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="33c9e-113">Example 2</span></span>

<span data-ttu-id="33c9e-114">Modyfikuje diagnostykę zarządzania interfejsem API w zakresie globalnym lub interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="33c9e-114">Modifies an API Management diagnostic at the Global or Api scope.</span></span> <span data-ttu-id="33c9e-115">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="33c9e-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementDiagnostic -AlwaysLog allErrors -ApiId '0001' -Context <PsApiManagementContext> -DiagnosticId 'applicationinsights' -LoggerId 'Logger123' -SamplingSetting <PsApiManagementSamplingSetting>
```

## <span data-ttu-id="33c9e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33c9e-116">PARAMETERS</span></span>

### <span data-ttu-id="33c9e-117">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="33c9e-117">-AlwaysLog</span></span>
<span data-ttu-id="33c9e-118">Określa typy wiadomości, które nie powinny być stosowane przez ustawienia próbkowania.</span><span class="sxs-lookup"><span data-stu-id="33c9e-118">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="33c9e-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="33c9e-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="33c9e-120">-ApiId</span><span class="sxs-lookup"><span data-stu-id="33c9e-120">-ApiId</span></span>
<span data-ttu-id="33c9e-121">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="33c9e-121">Identifier of existing API.</span></span>
<span data-ttu-id="33c9e-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="33c9e-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="33c9e-123">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="33c9e-123">-BackendSetting</span></span>
<span data-ttu-id="33c9e-124">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="33c9e-124">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="33c9e-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="33c9e-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="33c9e-126">-Context</span><span class="sxs-lookup"><span data-stu-id="33c9e-126">-Context</span></span>
<span data-ttu-id="33c9e-127">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="33c9e-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="33c9e-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="33c9e-128">This parameter is required.</span></span>

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

### <span data-ttu-id="33c9e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c9e-129">-DefaultProfile</span></span>
<span data-ttu-id="33c9e-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33c9e-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33c9e-131">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="33c9e-131">-DiagnosticId</span></span>
<span data-ttu-id="33c9e-132">Identyfikator istniejącej diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="33c9e-132">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="33c9e-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="33c9e-133">This parameter is required.</span></span>

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

### <span data-ttu-id="33c9e-134">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="33c9e-134">-FrontEndSetting</span></span>
<span data-ttu-id="33c9e-135">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="33c9e-135">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="33c9e-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="33c9e-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="33c9e-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="33c9e-137">-InputObject</span></span>
<span data-ttu-id="33c9e-138">Wystąpienie PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="33c9e-138">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="33c9e-139">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="33c9e-139">This parameter is required.</span></span>

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

### <span data-ttu-id="33c9e-140">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="33c9e-140">-LoggerId</span></span>
<span data-ttu-id="33c9e-141">Identyfikator rejestratora, do którego mają być wypychane testy diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="33c9e-141">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="33c9e-142">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="33c9e-142">This parameter is required.</span></span>

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

### <span data-ttu-id="33c9e-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33c9e-143">-PassThru</span></span>
<span data-ttu-id="33c9e-144">Jeśli jest określone, wystąpienie systemu Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementDiagnostic reprezentujące zestaw danych diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="33c9e-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="33c9e-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33c9e-145">-ResourceId</span></span>
<span data-ttu-id="33c9e-146">Identyfikator zasobu ARM w diagnostyce diagnostycznej lub API.</span><span class="sxs-lookup"><span data-stu-id="33c9e-146">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="33c9e-147">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="33c9e-147">This parameter is required.</span></span>

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

### <span data-ttu-id="33c9e-148">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="33c9e-148">-SamplingSetting</span></span>
<span data-ttu-id="33c9e-149">Ustawienie próbkowania diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="33c9e-149">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="33c9e-150">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="33c9e-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="33c9e-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33c9e-151">-Confirm</span></span>
<span data-ttu-id="33c9e-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33c9e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33c9e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33c9e-153">-WhatIf</span></span>
<span data-ttu-id="33c9e-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33c9e-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33c9e-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="33c9e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33c9e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c9e-156">CommonParameters</span></span>
<span data-ttu-id="33c9e-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33c9e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c9e-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33c9e-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c9e-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33c9e-159">INPUTS</span></span>

### <span data-ttu-id="33c9e-160">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="33c9e-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="33c9e-161">System. String</span><span class="sxs-lookup"><span data-stu-id="33c9e-161">System.String</span></span>

### <span data-ttu-id="33c9e-162">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="33c9e-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="33c9e-163">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="33c9e-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="33c9e-164">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="33c9e-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="33c9e-165">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="33c9e-165">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="33c9e-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33c9e-166">OUTPUTS</span></span>

### <span data-ttu-id="33c9e-167">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="33c9e-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="33c9e-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33c9e-168">NOTES</span></span>

## <span data-ttu-id="33c9e-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33c9e-169">RELATED LINKS</span></span>
