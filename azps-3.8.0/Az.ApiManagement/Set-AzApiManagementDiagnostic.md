---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementDiagnostic.md
ms.openlocfilehash: f3add9f35e56d4ba6d92b8438b970ddf8c682804
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052823"
---
# <span data-ttu-id="8f18f-101">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8f18f-101">Set-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="8f18f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f18f-102">SYNOPSIS</span></span>
<span data-ttu-id="8f18f-103">Modyfikuje diagnostykę zarządzania interfejsem API w zakresie globalnym lub interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="8f18f-103">Modifies an API Management diagnostic at the Global or Api scope.</span></span>

## <span data-ttu-id="8f18f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f18f-104">SYNTAX</span></span>

### <span data-ttu-id="8f18f-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8f18f-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementDiagnostic -Context <PsApiManagementContext> -DiagnosticId <String> [-ApiId <String>]
 [-LoggerId <String>] [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f18f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8f18f-106">ByInputObject</span></span>
```
Set-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-LoggerId <String>]
 [-AlwaysLog <String>] [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f18f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8f18f-107">ByResourceId</span></span>
```
Set-AzApiManagementDiagnostic -ResourceId <String> [-LoggerId <String>] [-AlwaysLog <String>]
 [-SamplingSetting <PsApiManagementSamplingSetting>]
 [-FrontEndSetting <PsApiManagementPipelineDiagnosticSetting>]
 [-BackendSetting <PsApiManagementPipelineDiagnosticSetting>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f18f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8f18f-108">DESCRIPTION</span></span>
<span data-ttu-id="8f18f-109">Polecenie cmdlet **Set-AzApiManagementDiagnostic** aktualizuje diagnostykę, która jest skonfigurowana w zakresie globalnym lub interfejsie API.</span><span class="sxs-lookup"><span data-stu-id="8f18f-109">The cmdlet **Set-AzApiManagementDiagnostic** updates the diagnostics which is configured at the Global or Api Scope.</span></span>

## <span data-ttu-id="8f18f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f18f-110">EXAMPLES</span></span>

### <span data-ttu-id="8f18f-111">Przykład 1: modyfikowanie diagnostyki w zakresie globalnym</span><span class="sxs-lookup"><span data-stu-id="8f18f-111">Example 1: Modify a diagnostic at the Global scope</span></span>
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

<span data-ttu-id="8f18f-112">To polecenie modyfikuje określoną wartość procentową próbkowania diagnostycznego z 100 do 50%.</span><span class="sxs-lookup"><span data-stu-id="8f18f-112">This command modifies the specified diagnostic Sampling Percentage from 100 to 50%</span></span>

## <span data-ttu-id="8f18f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f18f-113">PARAMETERS</span></span>

### <span data-ttu-id="8f18f-114">-AlwaysLog</span><span class="sxs-lookup"><span data-stu-id="8f18f-114">-AlwaysLog</span></span>
<span data-ttu-id="8f18f-115">Określa typy wiadomości, które nie powinny być stosowane przez ustawienia próbkowania.</span><span class="sxs-lookup"><span data-stu-id="8f18f-115">Specifies for what type of messages sampling settings should not apply.</span></span>
<span data-ttu-id="8f18f-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8f18f-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="8f18f-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8f18f-117">-ApiId</span></span>
<span data-ttu-id="8f18f-118">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8f18f-118">Identifier of existing API.</span></span>
<span data-ttu-id="8f18f-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8f18f-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="8f18f-120">-BackendSetting</span><span class="sxs-lookup"><span data-stu-id="8f18f-120">-BackendSetting</span></span>
<span data-ttu-id="8f18f-121">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8f18f-121">Diagnostic setting for incoming/outgoing Http Messages to the Backend.</span></span> <span data-ttu-id="8f18f-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8f18f-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="8f18f-123">-Context</span><span class="sxs-lookup"><span data-stu-id="8f18f-123">-Context</span></span>
<span data-ttu-id="8f18f-124">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8f18f-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8f18f-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8f18f-125">This parameter is required.</span></span>

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

### <span data-ttu-id="8f18f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f18f-126">-DefaultProfile</span></span>
<span data-ttu-id="8f18f-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f18f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f18f-128">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="8f18f-128">-DiagnosticId</span></span>
<span data-ttu-id="8f18f-129">Identyfikator istniejącej diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="8f18f-129">Identifier of existing Diagnostic.</span></span>
<span data-ttu-id="8f18f-130">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8f18f-130">This parameter is required.</span></span>

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

### <span data-ttu-id="8f18f-131">-FrontEndSetting</span><span class="sxs-lookup"><span data-stu-id="8f18f-131">-FrontEndSetting</span></span>
<span data-ttu-id="8f18f-132">Ustawienie diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="8f18f-132">Diagnostic setting for incoming/outgoing Http Messages to the Gateway.</span></span> <span data-ttu-id="8f18f-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8f18f-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="8f18f-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8f18f-134">-InputObject</span></span>
<span data-ttu-id="8f18f-135">Wystąpienie PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="8f18f-135">Instance of PsApiManagementDiagnostic.</span></span>
<span data-ttu-id="8f18f-136">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8f18f-136">This parameter is required.</span></span>

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

### <span data-ttu-id="8f18f-137">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="8f18f-137">-LoggerId</span></span>
<span data-ttu-id="8f18f-138">Identyfikator rejestratora, do którego mają być wypychane testy diagnostyczne.</span><span class="sxs-lookup"><span data-stu-id="8f18f-138">Identifier of the logger to push diagnostics to.</span></span>
<span data-ttu-id="8f18f-139">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8f18f-139">This parameter is required.</span></span>

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

### <span data-ttu-id="8f18f-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f18f-140">-PassThru</span></span>
<span data-ttu-id="8f18f-141">Jeśli jest określone, wystąpienie systemu Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementDiagnostic reprezentujące zestaw danych diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="8f18f-141">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic type representing the set Diagnostic.</span></span>

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

### <span data-ttu-id="8f18f-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f18f-142">-ResourceId</span></span>
<span data-ttu-id="8f18f-143">Identyfikator zasobu ARM w diagnostyce diagnostycznej lub API.</span><span class="sxs-lookup"><span data-stu-id="8f18f-143">Arm ResourceId of Diagnostic or Api Diagnostic.</span></span> <span data-ttu-id="8f18f-144">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8f18f-144">This parameter is required.</span></span>

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

### <span data-ttu-id="8f18f-145">-SamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8f18f-145">-SamplingSetting</span></span>
<span data-ttu-id="8f18f-146">Ustawienie próbkowania diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="8f18f-146">Sampling Setting of the Diagnostic.</span></span>
<span data-ttu-id="8f18f-147">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8f18f-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="8f18f-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f18f-148">-Confirm</span></span>
<span data-ttu-id="8f18f-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f18f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f18f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f18f-150">-WhatIf</span></span>
<span data-ttu-id="8f18f-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f18f-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f18f-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8f18f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f18f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f18f-153">CommonParameters</span></span>
<span data-ttu-id="8f18f-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f18f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f18f-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f18f-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f18f-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f18f-156">INPUTS</span></span>

### <span data-ttu-id="8f18f-157">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8f18f-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8f18f-158">System. String</span><span class="sxs-lookup"><span data-stu-id="8f18f-158">System.String</span></span>

### <span data-ttu-id="8f18f-159">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8f18f-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

### <span data-ttu-id="8f18f-160">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8f18f-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

### <span data-ttu-id="8f18f-161">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8f18f-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

### <span data-ttu-id="8f18f-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8f18f-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8f18f-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f18f-163">OUTPUTS</span></span>

### <span data-ttu-id="8f18f-164">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8f18f-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic</span></span>

## <span data-ttu-id="8f18f-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f18f-165">NOTES</span></span>

## <span data-ttu-id="8f18f-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f18f-166">RELATED LINKS</span></span>
