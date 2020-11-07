---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/export-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 7dc06f280595551a9e054c251339e96163b798b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717281"
---
# <span data-ttu-id="a9382-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a9382-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="a9382-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9382-102">SYNOPSIS</span></span>
<span data-ttu-id="a9382-103">Eksportuje interfejs API do pliku.</span><span class="sxs-lookup"><span data-stu-id="a9382-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9382-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9382-104">SYNTAX</span></span>

### <span data-ttu-id="a9382-105">ExportToPipeline (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9382-105">ExportToPipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9382-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="a9382-106">ExportToFile</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9382-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a9382-107">DESCRIPTION</span></span>
<span data-ttu-id="a9382-108">Polecenie cmdlet **Export-AzureRmApiManagementApi** eksportuje interfejs API zarządzania interfejsem Azure API do pliku w jednym z obsługiwanych formatów.</span><span class="sxs-lookup"><span data-stu-id="a9382-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="a9382-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9382-109">EXAMPLES</span></span>

### <span data-ttu-id="a9382-110">Przykład 1: eksportowanie interfejsu API w formacie programu Web Application Description Language (WADL)</span><span class="sxs-lookup"><span data-stu-id="a9382-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="a9382-111">To polecenie eksportuje interfejs API do pliku WADL.</span><span class="sxs-lookup"><span data-stu-id="a9382-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="a9382-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9382-112">PARAMETERS</span></span>

### <span data-ttu-id="a9382-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a9382-113">-ApiId</span></span>
<span data-ttu-id="a9382-114">Określa identyfikator interfejsu API do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="a9382-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="a9382-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a9382-115">-ApiRevision</span></span>
<span data-ttu-id="a9382-116">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a9382-116">Identifier of API Revision.</span></span> <span data-ttu-id="a9382-117">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a9382-117">This parameter is optional.</span></span> <span data-ttu-id="a9382-118">Jeśli ta pozycja nie zostanie określona, zostanie wyeksportowana wersja aktualnie aktywnej wersji API.</span><span class="sxs-lookup"><span data-stu-id="a9382-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="a9382-119">-Context</span><span class="sxs-lookup"><span data-stu-id="a9382-119">-Context</span></span>
<span data-ttu-id="a9382-120">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a9382-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a9382-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9382-121">-DefaultProfile</span></span>
<span data-ttu-id="a9382-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9382-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9382-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a9382-123">-Force</span></span>
<span data-ttu-id="a9382-124">Wskazuje, że ta operacja zastępuje plik o tej samej nazwie, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="a9382-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="a9382-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9382-125">-PassThru</span></span>
<span data-ttu-id="a9382-126">Wskazuje, że ta operacja zwraca wartość $True, jeśli interfejs API został pomyślnie wyeksportowany lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="a9382-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="a9382-127">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="a9382-127">-SaveAs</span></span>
<span data-ttu-id="a9382-128">Określa ścieżkę pliku, do którego ma zostać zapisany wyeksportowany interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a9382-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="a9382-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="a9382-129">-SpecificationFormat</span></span>
<span data-ttu-id="a9382-130">Określa format interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a9382-130">Specifies the API format.</span></span>
<span data-ttu-id="a9382-131">psdx_paramvalues WADL i struktury Swagger.</span><span class="sxs-lookup"><span data-stu-id="a9382-131">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9382-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9382-132">-Confirm</span></span>
<span data-ttu-id="a9382-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9382-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9382-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9382-134">-WhatIf</span></span>
<span data-ttu-id="a9382-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9382-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9382-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9382-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9382-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9382-137">CommonParameters</span></span>
<span data-ttu-id="a9382-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9382-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9382-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9382-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9382-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9382-140">INPUTS</span></span>

### <span data-ttu-id="a9382-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a9382-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a9382-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a9382-142">System.String</span></span>

### <span data-ttu-id="a9382-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="a9382-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="a9382-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a9382-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a9382-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9382-145">OUTPUTS</span></span>

### <span data-ttu-id="a9382-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a9382-146">System.String</span></span>
<span data-ttu-id="a9382-147">To polecenie cmdlet zwraca wartość wyeksportowanej zawartości API w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="a9382-147">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="a9382-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9382-148">NOTES</span></span>

## <span data-ttu-id="a9382-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9382-149">RELATED LINKS</span></span>

[<span data-ttu-id="a9382-150">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a9382-150">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="a9382-151">Import — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a9382-151">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="a9382-152">Nowe — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a9382-152">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="a9382-153">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a9382-153">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="a9382-154">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a9382-154">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


