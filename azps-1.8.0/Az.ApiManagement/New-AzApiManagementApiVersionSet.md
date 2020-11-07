---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58f9fda87bc24b22a68e98d60092b80002e74e4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704610"
---
# <span data-ttu-id="21840-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="21840-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="21840-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21840-102">SYNOPSIS</span></span>
<span data-ttu-id="21840-103">Tworzy zestaw wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="21840-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="21840-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21840-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21840-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21840-105">DESCRIPTION</span></span>
<span data-ttu-id="21840-106">Polecenie cmdlet **New-AzApiManagementApiVersionSet** tworzy jednostkę zestawu wersji interfejsu API w kontekście zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="21840-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="21840-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21840-107">EXAMPLES</span></span>

### <span data-ttu-id="21840-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21840-108">Example 1</span></span>
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

<span data-ttu-id="21840-109">To polecenie tworzy zestaw wersji interfejsu API, który ma schemat przechowywania wersji `Query` i parametr zapytania `api-version` .</span><span class="sxs-lookup"><span data-stu-id="21840-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="21840-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21840-110">PARAMETERS</span></span>

### <span data-ttu-id="21840-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="21840-111">-ApiVersionSetId</span></span>
<span data-ttu-id="21840-112">Identyfikator zestawu nowych wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="21840-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="21840-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="21840-113">This parameter is optional.</span></span>
<span data-ttu-id="21840-114">Jeśli nie określono, zostanie wygenerowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="21840-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="21840-115">-Context</span><span class="sxs-lookup"><span data-stu-id="21840-115">-Context</span></span>
<span data-ttu-id="21840-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="21840-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="21840-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="21840-117">This parameter is required.</span></span>

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

### <span data-ttu-id="21840-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21840-118">-DefaultProfile</span></span>
<span data-ttu-id="21840-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21840-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21840-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="21840-120">-Description</span></span>
<span data-ttu-id="21840-121">Opis zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="21840-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="21840-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="21840-122">-HeaderName</span></span>
<span data-ttu-id="21840-123">Wartość nagłówka, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="21840-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="21840-124">Jeśli nagłówek schematu przechowywania wersji to choosen, ta wartość musi być określona.</span><span class="sxs-lookup"><span data-stu-id="21840-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="21840-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21840-125">-Name</span></span>
<span data-ttu-id="21840-126">Nazwa zestawu ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="21840-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="21840-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="21840-127">This parameter is required.</span></span>

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

### <span data-ttu-id="21840-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="21840-128">-QueryName</span></span>
<span data-ttu-id="21840-129">Wartość kwerendy, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="21840-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="21840-130">Jeśli zapytanie schematu przechowywania wersji jest choosen, ta wartość musi być określona.</span><span class="sxs-lookup"><span data-stu-id="21840-130">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="21840-131">-Schemat</span><span class="sxs-lookup"><span data-stu-id="21840-131">-Scheme</span></span>
<span data-ttu-id="21840-132">Schemat przechowywania wersji w celu wybrania zestawu wersji API.</span><span class="sxs-lookup"><span data-stu-id="21840-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="21840-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="21840-133">This parameter is required.</span></span>

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

### <span data-ttu-id="21840-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21840-134">-Confirm</span></span>
<span data-ttu-id="21840-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21840-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21840-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21840-136">-WhatIf</span></span>
<span data-ttu-id="21840-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21840-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21840-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="21840-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21840-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21840-139">CommonParameters</span></span>
<span data-ttu-id="21840-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21840-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21840-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21840-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21840-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21840-142">INPUTS</span></span>

### <span data-ttu-id="21840-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="21840-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="21840-144">System. String</span><span class="sxs-lookup"><span data-stu-id="21840-144">System.String</span></span>

### <span data-ttu-id="21840-145">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="21840-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="21840-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21840-146">OUTPUTS</span></span>

### <span data-ttu-id="21840-147">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="21840-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="21840-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21840-148">NOTES</span></span>

## <span data-ttu-id="21840-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21840-149">RELATED LINKS</span></span>

[<span data-ttu-id="21840-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="21840-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="21840-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="21840-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="21840-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="21840-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)