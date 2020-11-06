---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: e10b91994bdb7351a7154d04cb7de3231ed87a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542051"
---
# <span data-ttu-id="1f92a-101">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1f92a-101">New-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1f92a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f92a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f92a-103">Tworzy zestaw wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="1f92a-103">Creates an API Version Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f92a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f92a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -Name <String> -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f92a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1f92a-105">DESCRIPTION</span></span>
<span data-ttu-id="1f92a-106">Polecenie cmdlet **New-AzureRmApiManagementApiVersionSet** tworzy jednostkę zestawu wersji interfejsu API w kontekście zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="1f92a-106">The **New-AzureRmApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="1f92a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f92a-107">EXAMPLES</span></span>

### <span data-ttu-id="1f92a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1f92a-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

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

<span data-ttu-id="1f92a-109">To polecenie tworzy zestaw wersji interfejsu API, który ma schemat przechowywania wersji `Query` i parametr zapytania `api-version` .</span><span class="sxs-lookup"><span data-stu-id="1f92a-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="1f92a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f92a-110">PARAMETERS</span></span>

### <span data-ttu-id="1f92a-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="1f92a-111">-ApiVersionSetId</span></span>
<span data-ttu-id="1f92a-112">Identyfikator zestawu nowych wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="1f92a-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="1f92a-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1f92a-113">This parameter is optional.</span></span>
<span data-ttu-id="1f92a-114">Jeśli nie określono, zostanie wygenerowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="1f92a-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="1f92a-115">-Context</span><span class="sxs-lookup"><span data-stu-id="1f92a-115">-Context</span></span>
<span data-ttu-id="1f92a-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1f92a-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1f92a-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1f92a-117">This parameter is required.</span></span>

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

### <span data-ttu-id="1f92a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f92a-118">-DefaultProfile</span></span>
<span data-ttu-id="1f92a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f92a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f92a-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="1f92a-120">-Description</span></span>
<span data-ttu-id="1f92a-121">Opis zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="1f92a-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="1f92a-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="1f92a-122">-HeaderName</span></span>
<span data-ttu-id="1f92a-123">Wartość nagłówka, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="1f92a-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="1f92a-124">Jeśli nagłówek schematu przechowywania wersji to choosen, ta wartość musi być określona.</span><span class="sxs-lookup"><span data-stu-id="1f92a-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="1f92a-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f92a-125">-Name</span></span>
<span data-ttu-id="1f92a-126">Nazwa zestawu ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="1f92a-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="1f92a-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1f92a-127">This parameter is required.</span></span>

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

### <span data-ttu-id="1f92a-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="1f92a-128">-QueryName</span></span>
<span data-ttu-id="1f92a-129">Wartość kwerendy, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="1f92a-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="1f92a-130">Jeśli zapytanie schematu przechowywania wersji jest choosen, ta wartość musi być określona.</span><span class="sxs-lookup"><span data-stu-id="1f92a-130">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="1f92a-131">-Schemat</span><span class="sxs-lookup"><span data-stu-id="1f92a-131">-Scheme</span></span>
<span data-ttu-id="1f92a-132">Schemat przechowywania wersji w celu wybrania zestawu wersji API.</span><span class="sxs-lookup"><span data-stu-id="1f92a-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="1f92a-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1f92a-133">This parameter is required.</span></span>

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

### <span data-ttu-id="1f92a-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f92a-134">-Confirm</span></span>
<span data-ttu-id="1f92a-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f92a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f92a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f92a-136">-WhatIf</span></span>
<span data-ttu-id="1f92a-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f92a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f92a-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1f92a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f92a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f92a-139">CommonParameters</span></span>
<span data-ttu-id="1f92a-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f92a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f92a-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f92a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f92a-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f92a-142">INPUTS</span></span>

### <span data-ttu-id="1f92a-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1f92a-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="1f92a-144">Parametry: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1f92a-144">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="1f92a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="1f92a-145">System.String</span></span>

### <span data-ttu-id="1f92a-146">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="1f92a-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="1f92a-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f92a-147">OUTPUTS</span></span>

### <span data-ttu-id="1f92a-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1f92a-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1f92a-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f92a-149">NOTES</span></span>

## <span data-ttu-id="1f92a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f92a-150">RELATED LINKS</span></span>

[<span data-ttu-id="1f92a-151">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1f92a-151">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="1f92a-152">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1f92a-152">Remove-AzureRmApiManagementApiVersionSet</span></span>](./Remove-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="1f92a-153">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1f92a-153">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
