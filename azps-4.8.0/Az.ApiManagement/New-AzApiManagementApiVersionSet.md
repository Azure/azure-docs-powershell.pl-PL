---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 0e007634659d842b0c59712a2ee191a79e1aeb58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064364"
---
# <span data-ttu-id="6f76b-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6f76b-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="6f76b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6f76b-102">SYNOPSIS</span></span>
<span data-ttu-id="6f76b-103">Tworzy zestaw wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="6f76b-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="6f76b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6f76b-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f76b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6f76b-105">DESCRIPTION</span></span>
<span data-ttu-id="6f76b-106">Polecenie cmdlet **New-AzApiManagementApiVersionSet** tworzy jednostkę zestawu wersji interfejsu API w kontekście zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="6f76b-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="6f76b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6f76b-107">EXAMPLES</span></span>

### <span data-ttu-id="6f76b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6f76b-108">Example 1</span></span>
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

<span data-ttu-id="6f76b-109">To polecenie tworzy zestaw wersji interfejsu API, który ma schemat przechowywania wersji `Query` i parametr zapytania `api-version` .</span><span class="sxs-lookup"><span data-stu-id="6f76b-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="6f76b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6f76b-110">PARAMETERS</span></span>

### <span data-ttu-id="6f76b-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="6f76b-111">-ApiVersionSetId</span></span>
<span data-ttu-id="6f76b-112">Identyfikator zestawu nowych wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="6f76b-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="6f76b-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6f76b-113">This parameter is optional.</span></span>
<span data-ttu-id="6f76b-114">Jeśli nie określono, zostanie wygenerowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="6f76b-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="6f76b-115">-Context</span><span class="sxs-lookup"><span data-stu-id="6f76b-115">-Context</span></span>
<span data-ttu-id="6f76b-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6f76b-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6f76b-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="6f76b-117">This parameter is required.</span></span>

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

### <span data-ttu-id="6f76b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f76b-118">-DefaultProfile</span></span>
<span data-ttu-id="6f76b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6f76b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f76b-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="6f76b-120">-Description</span></span>
<span data-ttu-id="6f76b-121">Opis zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="6f76b-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="6f76b-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="6f76b-122">-HeaderName</span></span>
<span data-ttu-id="6f76b-123">Wartość nagłówka, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="6f76b-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="6f76b-124">Jeśli wybrano nagłówek schematu przechowywania wersji, ta wartość musi być określona.</span><span class="sxs-lookup"><span data-stu-id="6f76b-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="6f76b-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6f76b-125">-Name</span></span>
<span data-ttu-id="6f76b-126">Nazwa zestawu ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="6f76b-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="6f76b-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="6f76b-127">This parameter is required.</span></span>

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

### <span data-ttu-id="6f76b-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="6f76b-128">-QueryName</span></span>
<span data-ttu-id="6f76b-129">Wartość kwerendy, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="6f76b-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="6f76b-130">Jeśli zostanie wybrana kwerenda schematu przechowywania wersji, ta wartość musi być określona.</span><span class="sxs-lookup"><span data-stu-id="6f76b-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="6f76b-131">-Schemat</span><span class="sxs-lookup"><span data-stu-id="6f76b-131">-Scheme</span></span>
<span data-ttu-id="6f76b-132">Schemat przechowywania wersji w celu wybrania zestawu wersji API.</span><span class="sxs-lookup"><span data-stu-id="6f76b-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="6f76b-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="6f76b-133">This parameter is required.</span></span>

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

### <span data-ttu-id="6f76b-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6f76b-134">-Confirm</span></span>
<span data-ttu-id="6f76b-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f76b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f76b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f76b-136">-WhatIf</span></span>
<span data-ttu-id="6f76b-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f76b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f76b-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6f76b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f76b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f76b-139">CommonParameters</span></span>
<span data-ttu-id="6f76b-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f76b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f76b-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f76b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f76b-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6f76b-142">INPUTS</span></span>

### <span data-ttu-id="6f76b-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6f76b-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6f76b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6f76b-144">System.String</span></span>

### <span data-ttu-id="6f76b-145">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="6f76b-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="6f76b-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6f76b-146">OUTPUTS</span></span>

### <span data-ttu-id="6f76b-147">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6f76b-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="6f76b-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6f76b-148">NOTES</span></span>

## <span data-ttu-id="6f76b-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6f76b-149">RELATED LINKS</span></span>

[<span data-ttu-id="6f76b-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6f76b-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="6f76b-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6f76b-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="6f76b-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6f76b-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)