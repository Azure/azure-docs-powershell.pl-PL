---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 126f30e732bc9c55c78c94d6c802b05a18ce29db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993091"
---
# <span data-ttu-id="c5f53-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c5f53-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="c5f53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5f53-102">SYNOPSIS</span></span>
<span data-ttu-id="c5f53-103">Tworzy zestaw wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c5f53-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="c5f53-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c5f53-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5f53-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c5f53-105">DESCRIPTION</span></span>
<span data-ttu-id="c5f53-106">Polecenie **cmdlet New-AzApiManagementApiVersionSet** tworzy jednostkę zestawu wersji interfejsu API w kontekście zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c5f53-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="c5f53-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c5f53-107">EXAMPLES</span></span>

### <span data-ttu-id="c5f53-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c5f53-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="c5f53-109">To polecenie tworzy zestaw wersji interfejsu API, który określa schemat wersji `Query` i parametr `api-version` zapytania.</span><span class="sxs-lookup"><span data-stu-id="c5f53-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="c5f53-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5f53-110">PARAMETERS</span></span>

### <span data-ttu-id="c5f53-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="c5f53-111">-ApiVersionSetId</span></span>
<span data-ttu-id="c5f53-112">Identyfikator nowego zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c5f53-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="c5f53-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c5f53-113">This parameter is optional.</span></span>
<span data-ttu-id="c5f53-114">Jeśli nie określono identyfikatora, zostanie wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="c5f53-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="c5f53-115">— kontekst</span><span class="sxs-lookup"><span data-stu-id="c5f53-115">-Context</span></span>
<span data-ttu-id="c5f53-116">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c5f53-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c5f53-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c5f53-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5f53-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5f53-118">-DefaultProfile</span></span>
<span data-ttu-id="c5f53-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5f53-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5f53-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="c5f53-120">-Description</span></span>
<span data-ttu-id="c5f53-121">Opis zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c5f53-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="c5f53-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="c5f53-122">-HeaderName</span></span>
<span data-ttu-id="c5f53-123">Wartość nagłówka, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="c5f53-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="c5f53-124">Jeśli wybrano nagłówek schematu wersji, należy określić tę wartość.</span><span class="sxs-lookup"><span data-stu-id="c5f53-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="c5f53-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c5f53-125">-Name</span></span>
<span data-ttu-id="c5f53-126">Nazwa zestawu apiVersion.</span><span class="sxs-lookup"><span data-stu-id="c5f53-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="c5f53-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c5f53-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5f53-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="c5f53-128">-QueryName</span></span>
<span data-ttu-id="c5f53-129">Wartość zapytania, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="c5f53-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="c5f53-130">Jeśli wybrano zapytanie dotyczące schematu wersji, należy określić tę wartość.</span><span class="sxs-lookup"><span data-stu-id="c5f53-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="c5f53-131">- Schemat</span><span class="sxs-lookup"><span data-stu-id="c5f53-131">-Scheme</span></span>
<span data-ttu-id="c5f53-132">Schemat wersji do wyboru dla zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c5f53-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="c5f53-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c5f53-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5f53-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c5f53-134">-Confirm</span></span>
<span data-ttu-id="c5f53-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c5f53-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5f53-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5f53-136">-WhatIf</span></span>
<span data-ttu-id="c5f53-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5f53-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5f53-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c5f53-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5f53-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5f53-139">CommonParameters</span></span>
<span data-ttu-id="c5f53-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5f53-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5f53-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5f53-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5f53-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5f53-142">INPUTS</span></span>

### <span data-ttu-id="c5f53-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c5f53-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c5f53-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c5f53-144">System.String</span></span>

### <span data-ttu-id="c5f53-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="c5f53-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="c5f53-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5f53-146">OUTPUTS</span></span>

### <span data-ttu-id="c5f53-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c5f53-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="c5f53-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c5f53-148">NOTES</span></span>

## <span data-ttu-id="c5f53-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5f53-149">RELATED LINKS</span></span>

[<span data-ttu-id="c5f53-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c5f53-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="c5f53-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c5f53-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="c5f53-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c5f53-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)