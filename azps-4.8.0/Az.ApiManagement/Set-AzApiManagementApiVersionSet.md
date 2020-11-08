---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064582"
---
# <span data-ttu-id="9ee9f-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9ee9f-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9ee9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ee9f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee9f-103">Aktualizuje wersję interfejsu API ustawioną w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="9ee9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ee9f-104">SYNTAX</span></span>

### <span data-ttu-id="9ee9f-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9ee9f-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ee9f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9ee9f-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ee9f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9ee9f-107">DESCRIPTION</span></span>

<span data-ttu-id="9ee9f-108">Polecenie cmdlet **Set-AzApiManagementApiVersionSet** modyfikuje zestaw wersji API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="9ee9f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ee9f-109">EXAMPLES</span></span>

### <span data-ttu-id="9ee9f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9ee9f-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="9ee9f-111">To polecenie umożliwia zaktualizowanie istniejącej wersji interfejsu API za pomocą schematu przechowywania wersji `Header` i parametru nagłówka `api-version` .</span><span class="sxs-lookup"><span data-stu-id="9ee9f-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="9ee9f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ee9f-112">PARAMETERS</span></span>

### <span data-ttu-id="9ee9f-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="9ee9f-113">-ApiVersionSetId</span></span>
<span data-ttu-id="9ee9f-114">Identyfikator zestawu nowych wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="9ee9f-115">-Context</span><span class="sxs-lookup"><span data-stu-id="9ee9f-115">-Context</span></span>
<span data-ttu-id="9ee9f-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9ee9f-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-117">This parameter is required.</span></span>

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

### <span data-ttu-id="9ee9f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee9f-118">-DefaultProfile</span></span>
<span data-ttu-id="9ee9f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ee9f-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="9ee9f-120">-Description</span></span>
<span data-ttu-id="9ee9f-121">Opis zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="9ee9f-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="9ee9f-122">-HeaderName</span></span>
<span data-ttu-id="9ee9f-123">Wartość nagłówka, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="9ee9f-124">Jeśli wybrano nagłówek schematu przechowywania wersji, ta wartość musi być określona.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="9ee9f-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9ee9f-125">-InputObject</span></span>
<span data-ttu-id="9ee9f-126">Wystąpienie PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="9ee9f-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-127">This parameter is required.</span></span>

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

### <span data-ttu-id="9ee9f-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9ee9f-128">-Name</span></span>
<span data-ttu-id="9ee9f-129">Nazwa zestawu ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="9ee9f-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="9ee9f-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ee9f-131">-PassThru</span></span>
<span data-ttu-id="9ee9f-132">Jeśli zostanie określone, wystąpienie programu Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet reprezentujące zmodyfikowane apiVersionSet zostanie zapisane w wyniku.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="9ee9f-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="9ee9f-133">-QueryName</span></span>
<span data-ttu-id="9ee9f-134">Wartość kwerendy, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="9ee9f-135">Jeśli zostanie wybrana kwerenda schematu przechowywania wersji, ta wartość musi być określona.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="9ee9f-136">-Schemat</span><span class="sxs-lookup"><span data-stu-id="9ee9f-136">-Scheme</span></span>
<span data-ttu-id="9ee9f-137">Schemat przechowywania wersji w celu wybrania zestawu wersji API.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="9ee9f-138">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="9ee9f-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9ee9f-139">-Confirm</span></span>
<span data-ttu-id="9ee9f-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ee9f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ee9f-141">-WhatIf</span></span>
<span data-ttu-id="9ee9f-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ee9f-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ee9f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee9f-144">CommonParameters</span></span>
<span data-ttu-id="9ee9f-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ee9f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee9f-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ee9f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee9f-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ee9f-147">INPUTS</span></span>

### <span data-ttu-id="9ee9f-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9ee9f-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9ee9f-149">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9ee9f-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="9ee9f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9ee9f-150">System.String</span></span>

### <span data-ttu-id="9ee9f-151">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="9ee9f-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="9ee9f-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ee9f-152">OUTPUTS</span></span>

### <span data-ttu-id="9ee9f-153">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9ee9f-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9ee9f-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ee9f-154">NOTES</span></span>

## <span data-ttu-id="9ee9f-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ee9f-155">RELATED LINKS</span></span>

[<span data-ttu-id="9ee9f-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9ee9f-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9ee9f-157">Nowe — AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9ee9f-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9ee9f-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9ee9f-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
