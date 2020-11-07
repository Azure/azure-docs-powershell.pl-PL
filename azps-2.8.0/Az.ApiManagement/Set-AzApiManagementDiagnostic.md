---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: 44a19d16cb5328f185370dcc407182a20a77bcfc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706907"
---
# <span data-ttu-id="ce8bb-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ce8bb-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="ce8bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce8bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ce8bb-103">Modyfikuje diagnostykę zarządzania interfejsem API w zakresie globalnym lub interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="ce8bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce8bb-104">SYNTAX</span></span>

### <span data-ttu-id="ce8bb-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ce8bb-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce8bb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ce8bb-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce8bb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ce8bb-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce8bb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ce8bb-108">DESCRIPTION</span></span>
<span data-ttu-id="ce8bb-109">Polecenie cmdlet **Set-AzApiManagementDiagnostic** aktualizuje diagnostykę, która jest skonfigurowana w zakresie globalnym lub interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="ce8bb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce8bb-110">EXAMPLES</span></span>

### <span data-ttu-id="ce8bb-111">Przykład 1: modyfikowanie diagnostyki w zakresie globalnym</span><span class="sxs-lookup"><span data-stu-id="ce8bb-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="ce8bb-112">To polecenie modyfikuje określoną wartość procentową próbkowania diagnostycznego z 100 do 50%.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

## <span data-ttu-id="ce8bb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce8bb-113">PARAMETERS</span></span>

### <span data-ttu-id="ce8bb-114">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="ce8bb-114">-AlwaysLog</span></span>
<span data-ttu-id="ce8bb-115">Określa typy wiadomości, które nie powinny być stosowane przez ustawienia próbkowania.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-115">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="ce8bb-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="ce8bb-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ce8bb-117">-ApiId</span></span>
<span data-ttu-id="ce8bb-118">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-118">Identifier of existing API.</span></span>
<span data-ttu-id="ce8bb-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="ce8bb-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="ce8bb-120">-BackendSetting</span></span>
<span data-ttu-id="ce8bb-121">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="ce8bb-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="ce8bb-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ce8bb-123">-Context</span></span>
<span data-ttu-id="ce8bb-124">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ce8bb-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-125">This parameter is required.</span></span>

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

### <span data-ttu-id="ce8bb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce8bb-126">-DefaultProfile</span></span>
<span data-ttu-id="ce8bb-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce8bb-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="ce8bb-128">-DiagnosticId</span></span>
<span data-ttu-id="ce8bb-129">Identyfikator istniejącej diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-129">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="ce8bb-130">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-130">This parameter is required.</span></span>

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

### <span data-ttu-id="ce8bb-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="ce8bb-131">-FrontEndSetting</span></span>
<span data-ttu-id="ce8bb-132">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="ce8bb-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="ce8bb-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ce8bb-134">-InputObject</span></span>
<span data-ttu-id="ce8bb-135">Wystąpienie PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-135">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="ce8bb-136">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-136">This parameter is required.</span></span>

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

### <span data-ttu-id="ce8bb-137">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="ce8bb-137">-LoggerId</span></span>
<span data-ttu-id="ce8bb-138">Identyfikator rejestratora, do którego mają być wypychane testy diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-138">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="ce8bb-139">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-139">This parameter is required.</span></span>

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

### <span data-ttu-id="ce8bb-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce8bb-140">-PassThru</span></span>
<span data-ttu-id="ce8bb-141">Jeśli jest określone, wystąpienie systemu Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementDiagnostic reprezentujące zestaw danych diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-141">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="ce8bb-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce8bb-142">-ResourceId</span></span>
<span data-ttu-id="ce8bb-143">Identyfikator zasobu ARM w diagnostyce diagnostycznej lub API.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-143">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="ce8bb-144">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-144">This parameter is required.</span></span>

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

### <span data-ttu-id="ce8bb-145">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="ce8bb-145">-SamplingSetting</span></span>
<span data-ttu-id="ce8bb-146">Ustawienie próbkowania diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-146">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="ce8bb-147">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="ce8bb-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce8bb-148">-Confirm</span></span>
<span data-ttu-id="ce8bb-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce8bb-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce8bb-150">-WhatIf</span></span>
<span data-ttu-id="ce8bb-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce8bb-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce8bb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce8bb-153">CommonParameters</span></span>
<span data-ttu-id="ce8bb-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce8bb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce8bb-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce8bb-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce8bb-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce8bb-156">INPUTS</span></span>

### <span data-ttu-id="ce8bb-157">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ce8bb-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ce8bb-158">System. String</span><span class="sxs-lookup"><span data-stu-id="ce8bb-158">System.String</span></span>

### <span data-ttu-id="ce8bb-159">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ce8bb-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="ce8bb-160">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="ce8bb-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="ce8bb-161">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="ce8bb-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="ce8bb-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ce8bb-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ce8bb-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce8bb-163">OUTPUTS</span></span>

### <span data-ttu-id="ce8bb-164">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ce8bb-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="ce8bb-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce8bb-165">NOTES</span></span>

## <span data-ttu-id="ce8bb-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce8bb-166">RELATED LINKS</span></span>
