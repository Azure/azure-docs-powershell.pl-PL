---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178051"
---
# <span data-ttu-id="4cec6-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4cec6-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="4cec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cec6-102">SYNOPSIS</span></span>
<span data-ttu-id="4cec6-103">Usuń jednostkę diagnostyczną z zakresu globalnego lub na poziomie interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="4cec6-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="4cec6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4cec6-104">SYNTAX</span></span>

### <span data-ttu-id="4cec6-105">ByResourceIdParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="4cec6-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cec6-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4cec6-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cec6-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cec6-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cec6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4cec6-108">DESCRIPTION</span></span>
<span data-ttu-id="4cec6-109">Polecenie cmdlet **Remove-AzApiManagementDiagnostic** usuwa jednostkę diagnostyczną określoną przez zakres `DiagnosticId` globalny lub `ApiId` zakres</span><span class="sxs-lookup"><span data-stu-id="4cec6-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="4cec6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4cec6-110">EXAMPLES</span></span>

### <span data-ttu-id="4cec6-111">Przykład 1. Usuwanie jednostki diagnostycznej</span><span class="sxs-lookup"><span data-stu-id="4cec6-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="4cec6-112">W tym przykładzie usuń narzędzie `applicationinsights` diagnostyczne z usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="4cec6-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="4cec6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cec6-113">PARAMETERS</span></span>

### <span data-ttu-id="4cec6-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4cec6-114">-ApiId</span></span>
<span data-ttu-id="4cec6-115">Identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="4cec6-115">Identifier of the API.</span></span>
<span data-ttu-id="4cec6-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4cec6-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cec6-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="4cec6-117">-Context</span></span>
<span data-ttu-id="4cec6-118">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4cec6-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4cec6-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4cec6-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cec6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cec6-120">-DefaultProfile</span></span>
<span data-ttu-id="4cec6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4cec6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cec6-122">- DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="4cec6-122">-DiagnosticId</span></span>
<span data-ttu-id="4cec6-123">Identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="4cec6-123">Identifier of existing product.</span></span>
<span data-ttu-id="4cec6-124">Jeśli zostanie określona, zostaną zwrócone zasady zakresu produktu.</span><span class="sxs-lookup"><span data-stu-id="4cec6-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="4cec6-125">Te parametry są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="4cec6-125">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cec6-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cec6-126">-InputObject</span></span>
<span data-ttu-id="4cec6-127">Wystąpienie programu PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="4cec6-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="4cec6-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4cec6-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cec6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cec6-129">-PassThru</span></span>
<span data-ttu-id="4cec6-130">Jeśli zostanie określona, w przypadku gdy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="4cec6-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="4cec6-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="4cec6-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="4cec6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cec6-132">-ResourceId</span></span>
<span data-ttu-id="4cec6-133">Arm ResourceId of Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="4cec6-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="4cec6-134">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4cec6-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cec6-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cec6-135">-Confirm</span></span>
<span data-ttu-id="4cec6-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4cec6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cec6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cec6-137">-WhatIf</span></span>
<span data-ttu-id="4cec6-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cec6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cec6-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4cec6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cec6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cec6-140">CommonParameters</span></span>
<span data-ttu-id="4cec6-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cec6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cec6-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cec6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cec6-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cec6-143">INPUTS</span></span>

### <span data-ttu-id="4cec6-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4cec6-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4cec6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4cec6-145">System.String</span></span>

### <span data-ttu-id="4cec6-146">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="4cec6-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4cec6-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cec6-147">OUTPUTS</span></span>

### <span data-ttu-id="4cec6-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4cec6-148">System.Boolean</span></span>

## <span data-ttu-id="4cec6-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4cec6-149">NOTES</span></span>

## <span data-ttu-id="4cec6-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cec6-150">RELATED LINKS</span></span>

[<span data-ttu-id="4cec6-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4cec6-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="4cec6-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4cec6-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="4cec6-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4cec6-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)