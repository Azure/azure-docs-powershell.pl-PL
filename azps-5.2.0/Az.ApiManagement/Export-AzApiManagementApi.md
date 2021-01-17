---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351001"
---
# <span data-ttu-id="a488b-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a488b-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="a488b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a488b-102">SYNOPSIS</span></span>
<span data-ttu-id="a488b-103">Eksportuje interfejs API do pliku.</span><span class="sxs-lookup"><span data-stu-id="a488b-103">Exports an API to a file.</span></span>

## <span data-ttu-id="a488b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a488b-104">SYNTAX</span></span>

### <span data-ttu-id="a488b-105">ExportToPipeline (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a488b-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a488b-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="a488b-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a488b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a488b-107">DESCRIPTION</span></span>
<span data-ttu-id="a488b-108">Polecenie cmdlet **Export-AzApiManagementApi** eksportuje interfejs API zarządzania interfejsem Azure API do pliku w jednym z obsługiwanych formatów.</span><span class="sxs-lookup"><span data-stu-id="a488b-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="a488b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a488b-109">EXAMPLES</span></span>

### <span data-ttu-id="a488b-110">Przykład 1: eksportowanie interfejsu API w formacie programu Web Application Description Language (WADL)</span><span class="sxs-lookup"><span data-stu-id="a488b-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="a488b-111">To polecenie eksportuje interfejs API do pliku WADL.</span><span class="sxs-lookup"><span data-stu-id="a488b-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="a488b-112">Przykład 2: eksportowanie interfejsu API w programie OpenApi 3,0 format specyfikacji jako dokumentu JSON</span><span class="sxs-lookup"><span data-stu-id="a488b-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="a488b-113">To polecenie eksportuje definicje interfejsów API w otwartym formacie API jako dokument JSON.</span><span class="sxs-lookup"><span data-stu-id="a488b-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="a488b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a488b-114">PARAMETERS</span></span>

### <span data-ttu-id="a488b-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a488b-115">-ApiId</span></span>
<span data-ttu-id="a488b-116">Określa identyfikator interfejsu API do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="a488b-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="a488b-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a488b-117">-ApiRevision</span></span>
<span data-ttu-id="a488b-118">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a488b-118">Identifier of API Revision.</span></span> <span data-ttu-id="a488b-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a488b-119">This parameter is optional.</span></span> <span data-ttu-id="a488b-120">Jeśli ta pozycja nie zostanie określona, zostanie wyeksportowana wersja aktualnie aktywnej wersji API.</span><span class="sxs-lookup"><span data-stu-id="a488b-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="a488b-121">-Context</span><span class="sxs-lookup"><span data-stu-id="a488b-121">-Context</span></span>
<span data-ttu-id="a488b-122">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a488b-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a488b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a488b-123">-DefaultProfile</span></span>
<span data-ttu-id="a488b-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a488b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a488b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a488b-125">-Force</span></span>
<span data-ttu-id="a488b-126">Wskazuje, że ta operacja zastępuje plik o tej samej nazwie, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="a488b-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="a488b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a488b-127">-PassThru</span></span>
<span data-ttu-id="a488b-128">Wskazuje, że ta operacja zwraca wartość $True, jeśli interfejs API został pomyślnie wyeksportowany lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="a488b-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="a488b-129">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="a488b-129">-SaveAs</span></span>
<span data-ttu-id="a488b-130">Określa ścieżkę pliku, do którego ma zostać zapisany wyeksportowany interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a488b-130">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="a488b-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="a488b-131">-SpecificationFormat</span></span>
<span data-ttu-id="a488b-132">Określa format interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a488b-132">Specifies the API format.</span></span>
<span data-ttu-id="a488b-133">psdx_paramvalues WADL, WSDL, Swagger, OpenApi i OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="a488b-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

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

### <span data-ttu-id="a488b-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a488b-134">-Confirm</span></span>
<span data-ttu-id="a488b-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a488b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a488b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a488b-136">-WhatIf</span></span>
<span data-ttu-id="a488b-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a488b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a488b-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a488b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a488b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a488b-139">CommonParameters</span></span>
<span data-ttu-id="a488b-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a488b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a488b-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a488b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a488b-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a488b-142">INPUTS</span></span>

### <span data-ttu-id="a488b-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a488b-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a488b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a488b-144">System.String</span></span>

### <span data-ttu-id="a488b-145">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="a488b-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="a488b-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a488b-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a488b-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a488b-147">OUTPUTS</span></span>

### <span data-ttu-id="a488b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a488b-148">System.String</span></span>

## <span data-ttu-id="a488b-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a488b-149">NOTES</span></span>

## <span data-ttu-id="a488b-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a488b-150">RELATED LINKS</span></span>

[<span data-ttu-id="a488b-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a488b-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="a488b-152">Import — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a488b-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="a488b-153">Nowe — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a488b-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="a488b-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a488b-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="a488b-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a488b-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


