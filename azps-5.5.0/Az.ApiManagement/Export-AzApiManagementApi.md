---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187763"
---
# <span data-ttu-id="e4ab2-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e4ab2-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="e4ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ab2-103">Eksportuje interfejs API do pliku.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-103">Exports an API to a file.</span></span>

## <span data-ttu-id="e4ab2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e4ab2-104">SYNTAX</span></span>

### <span data-ttu-id="e4ab2-105">ExportToPipeline (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e4ab2-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4ab2-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="e4ab2-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4ab2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e4ab2-107">DESCRIPTION</span></span>
<span data-ttu-id="e4ab2-108">Polecenie **cmdlet Export-AzApiManagementApi** eksportuje interfejs API zarządzania interfejsem Azure API do pliku w jednym z obsługiwanych formatów.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="e4ab2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e4ab2-109">EXAMPLES</span></span>

### <span data-ttu-id="e4ab2-110">Przykład 1. Eksportowanie interfejsu API w formacie WADL (Web Application Description Language)</span><span class="sxs-lookup"><span data-stu-id="e4ab2-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="e4ab2-111">To polecenie eksportuje interfejs API do pliku WADL.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="e4ab2-112">Przykład 2. Eksportowanie interfejsu API w formacie specyfikacji OpenApi 3.0 jako dokumentu Json</span><span class="sxs-lookup"><span data-stu-id="e4ab2-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="e4ab2-113">To polecenie eksportuje definicje interfejsu API w formacie Open Api jako dokument Json</span><span class="sxs-lookup"><span data-stu-id="e4ab2-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="e4ab2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4ab2-114">PARAMETERS</span></span>

### <span data-ttu-id="e4ab2-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e4ab2-115">-ApiId</span></span>
<span data-ttu-id="e4ab2-116">Określa identyfikator interfejsu API do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="e4ab2-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e4ab2-117">-ApiRevision</span></span>
<span data-ttu-id="e4ab2-118">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-118">Identifier of API Revision.</span></span> <span data-ttu-id="e4ab2-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-119">This parameter is optional.</span></span> <span data-ttu-id="e4ab2-120">Jeśli nie zostanie określona, eksport zostanie wykonana dla aktualnie aktywnej poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="e4ab2-121">— kontekst</span><span class="sxs-lookup"><span data-stu-id="e4ab2-121">-Context</span></span>
<span data-ttu-id="e4ab2-122">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="e4ab2-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ab2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4ab2-123">-DefaultProfile</span></span>
<span data-ttu-id="e4ab2-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4ab2-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e4ab2-125">-Force</span></span>
<span data-ttu-id="e4ab2-126">Oznacza, że ta operacja spowoduje zastąpienie pliku o tej samej nazwie, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ab2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4ab2-127">-PassThru</span></span>
<span data-ttu-id="e4ab2-128">Wskazuje, że ta operacja zwraca $True, jeśli interfejs API zostanie pomyślnie wyeksportowany lub $False inny.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ab2-129">— SaveAs</span><span class="sxs-lookup"><span data-stu-id="e4ab2-129">-SaveAs</span></span>
<span data-ttu-id="e4ab2-130">Określa ścieżkę pliku, w której ma być zapisywany wyeksportowany interfejs API.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-130">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ab2-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="e4ab2-131">-SpecificationFormat</span></span>
<span data-ttu-id="e4ab2-132">Określa format interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-132">Specifies the API format.</span></span>
<span data-ttu-id="e4ab2-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi i OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="e4ab2-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4ab2-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4ab2-134">-Confirm</span></span>
<span data-ttu-id="e4ab2-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4ab2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4ab2-136">-WhatIf</span></span>
<span data-ttu-id="e4ab2-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4ab2-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4ab2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ab2-139">CommonParameters</span></span>
<span data-ttu-id="e4ab2-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4ab2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ab2-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4ab2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ab2-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4ab2-142">INPUTS</span></span>

### <span data-ttu-id="e4ab2-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e4ab2-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e4ab2-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e4ab2-144">System.String</span></span>

### <span data-ttu-id="e4ab2-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="e4ab2-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="e4ab2-146">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e4ab2-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e4ab2-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e4ab2-147">OUTPUTS</span></span>

### <span data-ttu-id="e4ab2-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e4ab2-148">System.String</span></span>

## <span data-ttu-id="e4ab2-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e4ab2-149">NOTES</span></span>

## <span data-ttu-id="e4ab2-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4ab2-150">RELATED LINKS</span></span>

[<span data-ttu-id="e4ab2-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e4ab2-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="e4ab2-152">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e4ab2-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="e4ab2-153">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e4ab2-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="e4ab2-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e4ab2-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="e4ab2-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e4ab2-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


