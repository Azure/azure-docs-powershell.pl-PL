---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190362"
---
# <span data-ttu-id="62cb4-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="62cb4-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="62cb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="62cb4-103">Tworzy nową nazwaną wartość.</span><span class="sxs-lookup"><span data-stu-id="62cb4-103">Creates new Named Value.</span></span>

## <span data-ttu-id="62cb4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62cb4-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62cb4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="62cb4-105">DESCRIPTION</span></span>
<span data-ttu-id="62cb4-106">Polecenie **cmdlet New-AzApiManagementNamedValue** tworzy wartość nazwaną usługi Azure API **Management.**</span><span class="sxs-lookup"><span data-stu-id="62cb4-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="62cb4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62cb4-107">EXAMPLES</span></span>

### <span data-ttu-id="62cb4-108">Przykład 1. Tworzenie nazwanej wartości, która zawiera tagi</span><span class="sxs-lookup"><span data-stu-id="62cb4-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="62cb4-109">Pierwsze polecenie przypisuje dwie wartości do zmiennej $Tags zmienną.</span><span class="sxs-lookup"><span data-stu-id="62cb4-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="62cb4-110">Drugie polecenie tworzy nazwaną wartość i przypisuje ciągi w $Tags jako tagi właściwości.</span><span class="sxs-lookup"><span data-stu-id="62cb4-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="62cb4-111">Przykład 2. Tworzenie nazwanej wartości o wartości tajnej</span><span class="sxs-lookup"><span data-stu-id="62cb4-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="62cb4-112">To polecenie tworzy **nazwaną wartość,** która ma zaszyfrowaną wartość.</span><span class="sxs-lookup"><span data-stu-id="62cb4-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="62cb4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62cb4-113">PARAMETERS</span></span>

### <span data-ttu-id="62cb4-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="62cb4-114">-Context</span></span>
<span data-ttu-id="62cb4-115">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="62cb4-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="62cb4-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="62cb4-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62cb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62cb4-117">-DefaultProfile</span></span>
<span data-ttu-id="62cb4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="62cb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62cb4-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="62cb4-119">-Name</span></span>
<span data-ttu-id="62cb4-120">Nazwa nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="62cb4-120">Name of the named value.</span></span>
<span data-ttu-id="62cb4-121">Maksymalna długość to 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="62cb4-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="62cb4-122">Może zawierać tylko litery, cyfry, kropki, kreski i znaki podkreślenia.</span><span class="sxs-lookup"><span data-stu-id="62cb4-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="62cb4-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="62cb4-123">This parameter is required.</span></span>

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

### <span data-ttu-id="62cb4-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="62cb4-124">-NamedValueId</span></span>
<span data-ttu-id="62cb4-125">Identyfikator nowej nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="62cb4-125">Identifier of new named value.</span></span>
<span data-ttu-id="62cb4-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="62cb4-126">This parameter is optional.</span></span>
<span data-ttu-id="62cb4-127">Jeśli nie określono, zostanie wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="62cb4-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="62cb4-128">- Tajna</span><span class="sxs-lookup"><span data-stu-id="62cb4-128">-Secret</span></span>
<span data-ttu-id="62cb4-129">Określa, czy wartość jest tajny i powinna być zaszyfrowana.</span><span class="sxs-lookup"><span data-stu-id="62cb4-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="62cb4-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="62cb4-130">This parameter is optional.</span></span>
<span data-ttu-id="62cb4-131">Wartość domyślna ma wartość fałszywą.</span><span class="sxs-lookup"><span data-stu-id="62cb4-131">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62cb4-132">— Tag</span><span class="sxs-lookup"><span data-stu-id="62cb4-132">-Tag</span></span>
<span data-ttu-id="62cb4-133">Tagi, które mają być skojarzone z nazwaną wartością.</span><span class="sxs-lookup"><span data-stu-id="62cb4-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="62cb4-134">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="62cb4-134">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62cb4-135">— Wartość</span><span class="sxs-lookup"><span data-stu-id="62cb4-135">-Value</span></span>
<span data-ttu-id="62cb4-136">Wartość nazwanej wartości.</span><span class="sxs-lookup"><span data-stu-id="62cb4-136">Value of the named value.</span></span>
<span data-ttu-id="62cb4-137">Może zawierać wyrażenia zasad.</span><span class="sxs-lookup"><span data-stu-id="62cb4-137">Can contain policy expressions.</span></span>
<span data-ttu-id="62cb4-138">Maksymalna długość to 1000 znaków.</span><span class="sxs-lookup"><span data-stu-id="62cb4-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="62cb4-139">Nie może on być pusty ani składać się tylko z białych znaków.</span><span class="sxs-lookup"><span data-stu-id="62cb4-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="62cb4-140">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="62cb4-140">This parameter is required.</span></span>

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

### <span data-ttu-id="62cb4-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62cb4-141">-Confirm</span></span>
<span data-ttu-id="62cb4-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="62cb4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62cb4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62cb4-143">-WhatIf</span></span>
<span data-ttu-id="62cb4-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62cb4-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62cb4-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="62cb4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62cb4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62cb4-146">CommonParameters</span></span>
<span data-ttu-id="62cb4-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62cb4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62cb4-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62cb4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62cb4-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62cb4-149">INPUTS</span></span>

### <span data-ttu-id="62cb4-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="62cb4-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="62cb4-151">System.String</span><span class="sxs-lookup"><span data-stu-id="62cb4-151">System.String</span></span>

### <span data-ttu-id="62cb4-152">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="62cb4-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="62cb4-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="62cb4-153">System.String[]</span></span>

## <span data-ttu-id="62cb4-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62cb4-154">OUTPUTS</span></span>

### <span data-ttu-id="62cb4-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="62cb4-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="62cb4-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62cb4-156">NOTES</span></span>

## <span data-ttu-id="62cb4-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62cb4-157">RELATED LINKS</span></span>
