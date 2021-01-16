---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341461"
---
# <span data-ttu-id="9a14e-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9a14e-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="9a14e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a14e-102">SYNOPSIS</span></span>
<span data-ttu-id="9a14e-103">Usuń jednostkę diagnostyczną z zakresu poziomu globalnego lub interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="9a14e-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="9a14e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a14e-104">SYNTAX</span></span>

### <span data-ttu-id="9a14e-105">ByResourceIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9a14e-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a14e-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9a14e-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a14e-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a14e-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a14e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9a14e-108">DESCRIPTION</span></span>
<span data-ttu-id="9a14e-109">Polecenie cmdlet **Remove-AzApiManagementDiagnostic** usuwa jednostkę diagnostyczną określoną za pomocą `DiagnosticId` zakresu globalnego lub `ApiId` zakresu.</span><span class="sxs-lookup"><span data-stu-id="9a14e-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="9a14e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a14e-110">EXAMPLES</span></span>

### <span data-ttu-id="9a14e-111">Przykład 1. Usuń jednostkę diagnostyczną</span><span class="sxs-lookup"><span data-stu-id="9a14e-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="9a14e-112">W tym przykładzie pokazano, jak usunąć diagnostykę `applicationinsights` z usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9a14e-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="9a14e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a14e-113">PARAMETERS</span></span>

### <span data-ttu-id="9a14e-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9a14e-114">-ApiId</span></span>
<span data-ttu-id="9a14e-115">Identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="9a14e-115">Identifier of the API.</span></span>
<span data-ttu-id="9a14e-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9a14e-116">This parameter is required.</span></span>

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

### <span data-ttu-id="9a14e-117">-Context</span><span class="sxs-lookup"><span data-stu-id="9a14e-117">-Context</span></span>
<span data-ttu-id="9a14e-118">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9a14e-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9a14e-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9a14e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="9a14e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a14e-120">-DefaultProfile</span></span>
<span data-ttu-id="9a14e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a14e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a14e-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="9a14e-122">-DiagnosticId</span></span>
<span data-ttu-id="9a14e-123">Identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="9a14e-123">Identifier of existing product.</span></span>
<span data-ttu-id="9a14e-124">Jeśli ta określona, zwróci zasady dotyczące zakresu produktów.</span><span class="sxs-lookup"><span data-stu-id="9a14e-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="9a14e-125">Parametry te są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="9a14e-125">This parameters is optional.</span></span>

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

### <span data-ttu-id="9a14e-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9a14e-126">-InputObject</span></span>
<span data-ttu-id="9a14e-127">Wystąpienie PsApiManagementDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="9a14e-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="9a14e-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9a14e-128">This parameter is required.</span></span>

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

### <span data-ttu-id="9a14e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a14e-129">-PassThru</span></span>
<span data-ttu-id="9a14e-130">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="9a14e-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="9a14e-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="9a14e-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="9a14e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a14e-132">-ResourceId</span></span>
<span data-ttu-id="9a14e-133">ARM identyfikator zasobu diagnostycznego.</span><span class="sxs-lookup"><span data-stu-id="9a14e-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="9a14e-134">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9a14e-134">This parameter is required.</span></span>

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

### <span data-ttu-id="9a14e-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a14e-135">-Confirm</span></span>
<span data-ttu-id="9a14e-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a14e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a14e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a14e-137">-WhatIf</span></span>
<span data-ttu-id="9a14e-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a14e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a14e-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a14e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a14e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a14e-140">CommonParameters</span></span>
<span data-ttu-id="9a14e-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a14e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a14e-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a14e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a14e-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a14e-143">INPUTS</span></span>

### <span data-ttu-id="9a14e-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9a14e-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9a14e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9a14e-145">System.String</span></span>

### <span data-ttu-id="9a14e-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9a14e-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9a14e-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a14e-147">OUTPUTS</span></span>

### <span data-ttu-id="9a14e-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a14e-148">System.Boolean</span></span>

## <span data-ttu-id="9a14e-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a14e-149">NOTES</span></span>

## <span data-ttu-id="9a14e-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a14e-150">RELATED LINKS</span></span>

[<span data-ttu-id="9a14e-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9a14e-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="9a14e-152">Nowe — AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9a14e-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="9a14e-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9a14e-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)