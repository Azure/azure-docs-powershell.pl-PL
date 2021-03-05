---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 125e349fd2644fcfcd4cf2b6758fe45c40f323b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012762"
---
# <span data-ttu-id="d9aaf-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d9aaf-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="d9aaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="d9aaf-103">Aktualizuje zestaw wersji interfejsu API w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="d9aaf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9aaf-104">SYNTAX</span></span>

### <span data-ttu-id="d9aaf-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d9aaf-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9aaf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9aaf-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9aaf-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9aaf-107">DESCRIPTION</span></span>

<span data-ttu-id="d9aaf-108">Polecenie **cmdlet Set-AzApiManagementApiVersionSet** modyfikuje zestaw wersji interfejsu API zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="d9aaf-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9aaf-109">EXAMPLES</span></span>

### <span data-ttu-id="d9aaf-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9aaf-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="d9aaf-111">To polecenie aktualizuje istniejący zestaw wersji interfejsu API przy użyciu schematu wersji i `Header` parametru `api-version` nagłówka.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="d9aaf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9aaf-112">PARAMETERS</span></span>

### <span data-ttu-id="d9aaf-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="d9aaf-113">-ApiVersionSetId</span></span>
<span data-ttu-id="d9aaf-114">Identyfikator nowego zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="d9aaf-115">— kontekst</span><span class="sxs-lookup"><span data-stu-id="d9aaf-115">-Context</span></span>
<span data-ttu-id="d9aaf-116">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d9aaf-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-117">This parameter is required.</span></span>

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

### <span data-ttu-id="d9aaf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9aaf-118">-DefaultProfile</span></span>
<span data-ttu-id="d9aaf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9aaf-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="d9aaf-120">-Description</span></span>
<span data-ttu-id="d9aaf-121">Opis zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="d9aaf-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="d9aaf-122">-HeaderName</span></span>
<span data-ttu-id="d9aaf-123">Wartość nagłówka, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="d9aaf-124">Jeśli wybrano nagłówek schematu wersji, należy określić tę wartość.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="d9aaf-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9aaf-125">-InputObject</span></span>
<span data-ttu-id="d9aaf-126">Wystąpienie zestawu PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="d9aaf-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-127">This parameter is required.</span></span>

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

### <span data-ttu-id="d9aaf-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d9aaf-128">-Name</span></span>
<span data-ttu-id="d9aaf-129">Nazwa zestawu apiVersion.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="d9aaf-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="d9aaf-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9aaf-131">-PassThru</span></span>
<span data-ttu-id="d9aaf-132">Jeśli zostanie określone, wówczas wystąpienie właściwości Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet reprezentujące zmodyfikowany zestaw apiVersionSet zostanie zapisany w wyniku.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="d9aaf-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="d9aaf-133">-QueryName</span></span>
<span data-ttu-id="d9aaf-134">Wartość zapytania, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="d9aaf-135">Jeśli wybrano zapytanie dotyczące schematu wersji, należy określić tę wartość.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="d9aaf-136">- Schemat</span><span class="sxs-lookup"><span data-stu-id="d9aaf-136">-Scheme</span></span>
<span data-ttu-id="d9aaf-137">Schemat wersji do wyboru dla zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="d9aaf-138">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="d9aaf-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9aaf-139">-Confirm</span></span>
<span data-ttu-id="d9aaf-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9aaf-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9aaf-141">-WhatIf</span></span>
<span data-ttu-id="d9aaf-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9aaf-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9aaf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9aaf-144">CommonParameters</span></span>
<span data-ttu-id="d9aaf-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9aaf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9aaf-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9aaf-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9aaf-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9aaf-147">INPUTS</span></span>

### <span data-ttu-id="d9aaf-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d9aaf-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d9aaf-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d9aaf-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="d9aaf-150">System.String</span><span class="sxs-lookup"><span data-stu-id="d9aaf-150">System.String</span></span>

### <span data-ttu-id="d9aaf-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="d9aaf-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="d9aaf-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9aaf-152">OUTPUTS</span></span>

### <span data-ttu-id="d9aaf-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d9aaf-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="d9aaf-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9aaf-154">NOTES</span></span>

## <span data-ttu-id="d9aaf-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9aaf-155">RELATED LINKS</span></span>

[<span data-ttu-id="d9aaf-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d9aaf-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="d9aaf-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d9aaf-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="d9aaf-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d9aaf-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
