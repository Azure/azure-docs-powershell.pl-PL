---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239682"
---
# <span data-ttu-id="e6533-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e6533-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="e6533-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6533-102">SYNOPSIS</span></span>
<span data-ttu-id="e6533-103">Aktualizuje zestaw wersji interfejsu API w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="e6533-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="e6533-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e6533-104">SYNTAX</span></span>

### <span data-ttu-id="e6533-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e6533-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6533-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e6533-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6533-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e6533-107">DESCRIPTION</span></span>

<span data-ttu-id="e6533-108">Polecenie **cmdlet Set-AzApiManagementApiVersionSet** modyfikuje zestaw wersji interfejsu API zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e6533-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="e6533-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e6533-109">EXAMPLES</span></span>

### <span data-ttu-id="e6533-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e6533-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="e6533-111">To polecenie aktualizuje istniejący zestaw wersji interfejsu API przy użyciu schematu wersji i `Header` parametru `api-version` nagłówka.</span><span class="sxs-lookup"><span data-stu-id="e6533-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="e6533-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6533-112">PARAMETERS</span></span>

### <span data-ttu-id="e6533-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="e6533-113">-ApiVersionSetId</span></span>
<span data-ttu-id="e6533-114">Identyfikator nowego zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e6533-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="e6533-115">— kontekst</span><span class="sxs-lookup"><span data-stu-id="e6533-115">-Context</span></span>
<span data-ttu-id="e6533-116">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e6533-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e6533-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e6533-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6533-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6533-118">-DefaultProfile</span></span>
<span data-ttu-id="e6533-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6533-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6533-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="e6533-120">-Description</span></span>
<span data-ttu-id="e6533-121">Opis zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e6533-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="e6533-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="e6533-122">-HeaderName</span></span>
<span data-ttu-id="e6533-123">Wartość nagłówka, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="e6533-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="e6533-124">Jeśli wybrano nagłówek schematu wersji, należy określić tę wartość.</span><span class="sxs-lookup"><span data-stu-id="e6533-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="e6533-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6533-125">-InputObject</span></span>
<span data-ttu-id="e6533-126">Wystąpienie zestawu PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="e6533-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="e6533-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e6533-127">This parameter is required.</span></span>

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

### <span data-ttu-id="e6533-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e6533-128">-Name</span></span>
<span data-ttu-id="e6533-129">Nazwa zestawu apiVersion.</span><span class="sxs-lookup"><span data-stu-id="e6533-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="e6533-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e6533-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6533-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6533-131">-PassThru</span></span>
<span data-ttu-id="e6533-132">Jeśli zostanie określone, wówczas wystąpienie właściwości Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet reprezentujące zmodyfikowany zestaw apiVersionSet zostanie zapisany w wyniku.</span><span class="sxs-lookup"><span data-stu-id="e6533-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="e6533-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="e6533-133">-QueryName</span></span>
<span data-ttu-id="e6533-134">Wartość zapytania, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="e6533-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="e6533-135">Jeśli wybrano zapytanie dotyczące schematu wersji, należy określić tę wartość.</span><span class="sxs-lookup"><span data-stu-id="e6533-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="e6533-136">- Schemat</span><span class="sxs-lookup"><span data-stu-id="e6533-136">-Scheme</span></span>
<span data-ttu-id="e6533-137">Schemat wersji do wyboru dla zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e6533-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="e6533-138">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e6533-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6533-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6533-139">-Confirm</span></span>
<span data-ttu-id="e6533-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e6533-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6533-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6533-141">-WhatIf</span></span>
<span data-ttu-id="e6533-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6533-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6533-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e6533-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6533-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6533-144">CommonParameters</span></span>
<span data-ttu-id="e6533-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6533-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6533-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6533-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6533-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6533-147">INPUTS</span></span>

### <span data-ttu-id="e6533-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e6533-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e6533-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e6533-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="e6533-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e6533-150">System.String</span></span>

### <span data-ttu-id="e6533-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="e6533-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="e6533-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6533-152">OUTPUTS</span></span>

### <span data-ttu-id="e6533-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e6533-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="e6533-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e6533-154">NOTES</span></span>

## <span data-ttu-id="e6533-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6533-155">RELATED LINKS</span></span>

[<span data-ttu-id="e6533-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e6533-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="e6533-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e6533-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="e6533-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e6533-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
