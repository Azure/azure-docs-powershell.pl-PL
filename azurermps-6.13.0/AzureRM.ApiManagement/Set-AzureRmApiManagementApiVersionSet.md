---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 5d9bc89eb2d4188b7b2903bee7a8b0a44bec1216
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547672"
---
# <span data-ttu-id="7651c-101">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7651c-101">Set-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="7651c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7651c-102">SYNOPSIS</span></span>
<span data-ttu-id="7651c-103">Aktualizuje wersję interfejsu API ustawioną w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="7651c-103">Updates an API Version Set in the API Management Context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7651c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7651c-104">SYNTAX</span></span>

### <span data-ttu-id="7651c-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7651c-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-Name <String>] [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7651c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7651c-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7651c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7651c-107">DESCRIPTION</span></span>

<span data-ttu-id="7651c-108">Polecenie cmdlet **Set-AzureRmApiManagementApiVersionSet** modyfikuje zestaw wersji API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="7651c-108">The **Set-AzureRmApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="7651c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7651c-109">EXAMPLES</span></span>

### <span data-ttu-id="7651c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7651c-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="7651c-111">To polecenie umożliwia zaktualizowanie istniejącej wersji interfejsu API za pomocą schematu przechowywania wersji `Header` i parametru nagłówka `api-version` .</span><span class="sxs-lookup"><span data-stu-id="7651c-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="7651c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7651c-112">PARAMETERS</span></span>

### <span data-ttu-id="7651c-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="7651c-113">-ApiVersionSetId</span></span>
<span data-ttu-id="7651c-114">Identyfikator zestawu nowych wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7651c-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="7651c-115">-Context</span><span class="sxs-lookup"><span data-stu-id="7651c-115">-Context</span></span>
<span data-ttu-id="7651c-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7651c-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7651c-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7651c-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7651c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7651c-118">-DefaultProfile</span></span>
<span data-ttu-id="7651c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7651c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7651c-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="7651c-120">-Description</span></span>
<span data-ttu-id="7651c-121">Opis zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7651c-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="7651c-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="7651c-122">-HeaderName</span></span>
<span data-ttu-id="7651c-123">Wartość nagłówka, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="7651c-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="7651c-124">Jeśli nagłówek schematu przechowywania wersji to choosen, ta wartość musi być określona.</span><span class="sxs-lookup"><span data-stu-id="7651c-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="7651c-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7651c-125">-InputObject</span></span>
<span data-ttu-id="7651c-126">Wystąpienie PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="7651c-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="7651c-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7651c-127">This parameter is required.</span></span>

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

### <span data-ttu-id="7651c-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7651c-128">-Name</span></span>
<span data-ttu-id="7651c-129">Nazwa zestawu ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="7651c-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="7651c-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7651c-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="7651c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7651c-131">-PassThru</span></span>
<span data-ttu-id="7651c-132">Jeśli zostanie określone, wystąpienie programu Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet reprezentujące zmodyfikowane apiVersionSet zostanie zapisane w wyniku.</span><span class="sxs-lookup"><span data-stu-id="7651c-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="7651c-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="7651c-133">-QueryName</span></span>
<span data-ttu-id="7651c-134">Wartość kwerendy, która będzie zawierać informacje o wersji.</span><span class="sxs-lookup"><span data-stu-id="7651c-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="7651c-135">Jeśli zapytanie schematu przechowywania wersji jest choosen, ta wartość musi być określona.</span><span class="sxs-lookup"><span data-stu-id="7651c-135">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="7651c-136">-Schemat</span><span class="sxs-lookup"><span data-stu-id="7651c-136">-Scheme</span></span>
<span data-ttu-id="7651c-137">Schemat przechowywania wersji w celu wybrania zestawu wersji API.</span><span class="sxs-lookup"><span data-stu-id="7651c-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="7651c-138">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7651c-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="7651c-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7651c-139">-Confirm</span></span>
<span data-ttu-id="7651c-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7651c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7651c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7651c-141">-WhatIf</span></span>
<span data-ttu-id="7651c-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7651c-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7651c-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7651c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7651c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7651c-144">CommonParameters</span></span>
<span data-ttu-id="7651c-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7651c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7651c-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7651c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7651c-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7651c-147">INPUTS</span></span>

### <span data-ttu-id="7651c-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7651c-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7651c-149">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7651c-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="7651c-150">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7651c-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7651c-151">System. String</span><span class="sxs-lookup"><span data-stu-id="7651c-151">System.String</span></span>

### <span data-ttu-id="7651c-152">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="7651c-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="7651c-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7651c-153">OUTPUTS</span></span>

### <span data-ttu-id="7651c-154">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7651c-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="7651c-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7651c-155">NOTES</span></span>

## <span data-ttu-id="7651c-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7651c-156">RELATED LINKS</span></span>

[<span data-ttu-id="7651c-157">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7651c-157">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="7651c-158">Nowe — AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7651c-158">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="7651c-159">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7651c-159">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
