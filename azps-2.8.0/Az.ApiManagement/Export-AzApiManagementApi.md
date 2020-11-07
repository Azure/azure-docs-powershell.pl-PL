---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 7b4163b18905fd0676543de1b0ead26d11c7096a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707102"
---
# <span data-ttu-id="7b1ad-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b1ad-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="7b1ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b1ad-102">SYNOPSIS</span></span>
<span data-ttu-id="7b1ad-103">Eksportuje interfejs API do pliku.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-103">Exports an API to a file.</span></span>

## <span data-ttu-id="7b1ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b1ad-104">SYNTAX</span></span>

### <span data-ttu-id="7b1ad-105">ExportToPipeline (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7b1ad-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b1ad-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="7b1ad-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b1ad-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7b1ad-107">DESCRIPTION</span></span>
<span data-ttu-id="7b1ad-108">Polecenie cmdlet **Export-AzApiManagementApi** eksportuje interfejs API zarządzania interfejsem Azure API do pliku w jednym z obsługiwanych formatów.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="7b1ad-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b1ad-109">EXAMPLES</span></span>

### <span data-ttu-id="7b1ad-110">Przykład 1: eksportowanie interfejsu API w formacie programu Web Application Description Language (WADL)</span><span class="sxs-lookup"><span data-stu-id="7b1ad-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="7b1ad-111">To polecenie eksportuje interfejs API do pliku WADL.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="7b1ad-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b1ad-112">PARAMETERS</span></span>

### <span data-ttu-id="7b1ad-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7b1ad-113">-ApiId</span></span>
<span data-ttu-id="7b1ad-114">Określa identyfikator interfejsu API do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="7b1ad-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="7b1ad-115">-ApiRevision</span></span>
<span data-ttu-id="7b1ad-116">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-116">Identifier of API Revision.</span></span> <span data-ttu-id="7b1ad-117">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-117">This parameter is optional.</span></span> <span data-ttu-id="7b1ad-118">Jeśli ta pozycja nie zostanie określona, zostanie wyeksportowana wersja aktualnie aktywnej wersji API.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="7b1ad-119">-Context</span><span class="sxs-lookup"><span data-stu-id="7b1ad-119">-Context</span></span>
<span data-ttu-id="7b1ad-120">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7b1ad-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7b1ad-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b1ad-121">-DefaultProfile</span></span>
<span data-ttu-id="7b1ad-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b1ad-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7b1ad-123">-Force</span></span>
<span data-ttu-id="7b1ad-124">Wskazuje, że ta operacja zastępuje plik o tej samej nazwie, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="7b1ad-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b1ad-125">-PassThru</span></span>
<span data-ttu-id="7b1ad-126">Wskazuje, że ta operacja zwraca wartość $True, jeśli interfejs API został pomyślnie wyeksportowany lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="7b1ad-127">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="7b1ad-127">-SaveAs</span></span>
<span data-ttu-id="7b1ad-128">Określa ścieżkę pliku, do którego ma zostać zapisany wyeksportowany interfejs API.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="7b1ad-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="7b1ad-129">-SpecificationFormat</span></span>
<span data-ttu-id="7b1ad-130">Określa format interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-130">Specifies the API format.</span></span>
<span data-ttu-id="7b1ad-131">psdx_paramvalues WADL i struktury Swagger.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-131">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b1ad-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b1ad-132">-Confirm</span></span>
<span data-ttu-id="7b1ad-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b1ad-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b1ad-134">-WhatIf</span></span>
<span data-ttu-id="7b1ad-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b1ad-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b1ad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b1ad-137">CommonParameters</span></span>
<span data-ttu-id="7b1ad-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b1ad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b1ad-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b1ad-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b1ad-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b1ad-140">INPUTS</span></span>

### <span data-ttu-id="7b1ad-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7b1ad-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7b1ad-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7b1ad-142">System.String</span></span>

### <span data-ttu-id="7b1ad-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="7b1ad-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="7b1ad-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7b1ad-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7b1ad-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b1ad-145">OUTPUTS</span></span>

### <span data-ttu-id="7b1ad-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7b1ad-146">System.String</span></span>

## <span data-ttu-id="7b1ad-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b1ad-147">NOTES</span></span>

## <span data-ttu-id="7b1ad-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b1ad-148">RELATED LINKS</span></span>

[<span data-ttu-id="7b1ad-149">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b1ad-149">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="7b1ad-150">Import — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b1ad-150">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="7b1ad-151">Nowe — AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b1ad-151">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="7b1ad-152">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b1ad-152">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="7b1ad-153">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7b1ad-153">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)

