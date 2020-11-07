---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 09400d3111ffb3fda232e1cbb71fd0aac063a74c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717884"
---
# <span data-ttu-id="a8bff-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a8bff-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="a8bff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8bff-102">SYNOPSIS</span></span>
<span data-ttu-id="a8bff-103">Eksportuje interfejs API do pliku.</span><span class="sxs-lookup"><span data-stu-id="a8bff-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8bff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8bff-104">SYNTAX</span></span>

### <span data-ttu-id="a8bff-105">Eksportowanie do procesu planowanego (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a8bff-105">Export to pipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8bff-106">Eksportowanie do pliku</span><span class="sxs-lookup"><span data-stu-id="a8bff-106">Export to File</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8bff-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a8bff-107">DESCRIPTION</span></span>
<span data-ttu-id="a8bff-108">Polecenie cmdlet **Export-AzureRmApiManagementApi** eksportuje interfejs API zarządzania interfejsem Azure API do pliku w jednym z obsługiwanych formatów.</span><span class="sxs-lookup"><span data-stu-id="a8bff-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="a8bff-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8bff-109">EXAMPLES</span></span>

### <span data-ttu-id="a8bff-110">Przykład 1: eksportowanie interfejsu API w formacie programu Web Application Description Language (WADL)</span><span class="sxs-lookup"><span data-stu-id="a8bff-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="a8bff-111">To polecenie eksportuje interfejs API do pliku WADL.</span><span class="sxs-lookup"><span data-stu-id="a8bff-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="a8bff-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8bff-112">PARAMETERS</span></span>

### <span data-ttu-id="a8bff-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a8bff-113">-ApiId</span></span>
<span data-ttu-id="a8bff-114">Określa identyfikator interfejsu API do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="a8bff-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="a8bff-115">-Context</span><span class="sxs-lookup"><span data-stu-id="a8bff-115">-Context</span></span>
<span data-ttu-id="a8bff-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a8bff-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a8bff-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a8bff-117">-Force</span></span>
<span data-ttu-id="a8bff-118">Wskazuje, że ta operacja zastępuje plik o tej samej nazwie, jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="a8bff-118">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8bff-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8bff-119">-PassThru</span></span>
<span data-ttu-id="a8bff-120">Wskazuje, że ta operacja zwraca wartość $True, jeśli interfejs API został pomyślnie wyeksportowany lub $False w inny sposób.</span><span class="sxs-lookup"><span data-stu-id="a8bff-120">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8bff-121">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="a8bff-121">-SaveAs</span></span>
<span data-ttu-id="a8bff-122">Określa ścieżkę pliku, do którego ma zostać zapisany wyeksportowany interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a8bff-122">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8bff-123">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="a8bff-123">-SpecificationFormat</span></span>
<span data-ttu-id="a8bff-124">Określa format interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a8bff-124">Specifies the API format.</span></span>
<span data-ttu-id="a8bff-125">psdx_paramvalues WADL i struktury Swagger.</span><span class="sxs-lookup"><span data-stu-id="a8bff-125">psdx_paramvalues Wadl and Swagger.</span></span>

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

### <span data-ttu-id="a8bff-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8bff-126">-Confirm</span></span>
<span data-ttu-id="a8bff-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8bff-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8bff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8bff-128">-WhatIf</span></span>
<span data-ttu-id="a8bff-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8bff-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8bff-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a8bff-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8bff-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8bff-131">-DefaultProfile</span></span>
<span data-ttu-id="a8bff-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8bff-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8bff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8bff-133">CommonParameters</span></span>
<span data-ttu-id="a8bff-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8bff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8bff-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8bff-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8bff-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8bff-136">INPUTS</span></span>

## <span data-ttu-id="a8bff-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8bff-137">OUTPUTS</span></span>

### <span data-ttu-id="a8bff-138">Ciąg</span><span class="sxs-lookup"><span data-stu-id="a8bff-138">String</span></span>
<span data-ttu-id="a8bff-139">To polecenie cmdlet zwraca wartość wyeksportowanej zawartości API w postaci ciągu.</span><span class="sxs-lookup"><span data-stu-id="a8bff-139">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="a8bff-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8bff-140">NOTES</span></span>

## <span data-ttu-id="a8bff-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8bff-141">RELATED LINKS</span></span>

[<span data-ttu-id="a8bff-142">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a8bff-142">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="a8bff-143">Import — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a8bff-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="a8bff-144">Nowe — AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a8bff-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="a8bff-145">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a8bff-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="a8bff-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a8bff-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


