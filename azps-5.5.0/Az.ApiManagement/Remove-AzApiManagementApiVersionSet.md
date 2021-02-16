---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244410"
---
# <span data-ttu-id="d6fb6-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d6fb6-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="d6fb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="d6fb6-103">Usuwa określony zestaw wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="d6fb6-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="d6fb6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6fb6-104">SYNTAX</span></span>

### <span data-ttu-id="d6fb6-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d6fb6-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6fb6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d6fb6-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6fb6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6fb6-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6fb6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6fb6-108">DESCRIPTION</span></span>

<span data-ttu-id="d6fb6-109">Polecenie **cmdlet Remove-AzAzureRmApiManagementApiVersionSet** usuwa istniejący zestaw wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="d6fb6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6fb6-110">EXAMPLES</span></span>

### <span data-ttu-id="d6fb6-111">Przykład 1. Usuwanie zestawu wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="d6fb6-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="d6fb6-112">To polecenie usuwa zestaw wersji interfejsu API z określoną wartością ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="d6fb6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6fb6-113">PARAMETERS</span></span>

### <span data-ttu-id="d6fb6-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="d6fb6-114">-ApiVersionSetId</span></span>
<span data-ttu-id="d6fb6-115">Identyfikator zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="d6fb6-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-116">This parameter is required.</span></span>

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

### <span data-ttu-id="d6fb6-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="d6fb6-117">-Context</span></span>
<span data-ttu-id="d6fb6-118">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d6fb6-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-119">This parameter is required.</span></span>

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

### <span data-ttu-id="d6fb6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6fb6-120">-DefaultProfile</span></span>
<span data-ttu-id="d6fb6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6fb6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6fb6-122">-InputObject</span></span>
<span data-ttu-id="d6fb6-123">Wystąpienie zestawu PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="d6fb6-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6fb6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6fb6-125">-PassThru</span></span>
<span data-ttu-id="d6fb6-126">Jeśli zostanie określona, na wypadek, gdyby operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d6fb6-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-127">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fb6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6fb6-128">-ResourceId</span></span>
<span data-ttu-id="d6fb6-129">Arm ResourceId of ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="d6fb6-130">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-130">This parameter is required.</span></span>

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

### <span data-ttu-id="d6fb6-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6fb6-131">-Confirm</span></span>
<span data-ttu-id="d6fb6-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6fb6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6fb6-133">-WhatIf</span></span>
<span data-ttu-id="d6fb6-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6fb6-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6fb6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6fb6-136">CommonParameters</span></span>
<span data-ttu-id="d6fb6-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6fb6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6fb6-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6fb6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6fb6-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6fb6-139">INPUTS</span></span>

### <span data-ttu-id="d6fb6-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d6fb6-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d6fb6-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d6fb6-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="d6fb6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d6fb6-142">System.String</span></span>

## <span data-ttu-id="d6fb6-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d6fb6-143">OUTPUTS</span></span>

### <span data-ttu-id="d6fb6-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6fb6-144">System.Boolean</span></span>

## <span data-ttu-id="d6fb6-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6fb6-145">NOTES</span></span>

## <span data-ttu-id="d6fb6-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6fb6-146">RELATED LINKS</span></span>

[<span data-ttu-id="d6fb6-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d6fb6-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="d6fb6-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d6fb6-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="d6fb6-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d6fb6-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)