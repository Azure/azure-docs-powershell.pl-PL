---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 681cbc620a5c6067102dfe2a67f20dd9edc42046
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490270"
---
# <span data-ttu-id="e098c-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="e098c-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="e098c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e098c-102">SYNOPSIS</span></span>
<span data-ttu-id="e098c-103">Modyfikuje specyfikację szablonu.</span><span class="sxs-lookup"><span data-stu-id="e098c-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="e098c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e098c-104">SYNTAX</span></span>

### <span data-ttu-id="e098c-105">FromJsonStringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e098c-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e098c-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e098c-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e098c-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e098c-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e098c-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="e098c-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e098c-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e098c-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e098c-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e098c-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e098c-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="e098c-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e098c-112">Opis</span><span class="sxs-lookup"><span data-stu-id="e098c-112">DESCRIPTION</span></span>
<span data-ttu-id="e098c-113">Modyfikuje specyfikację Templace. Jeśli Specyfikacja szablonu o określonej nazwie i/lub konkretnej wersji jeszcze nie istnieje, zostanie utworzona.</span><span class="sxs-lookup"><span data-stu-id="e098c-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="e098c-114">Po zmodyfikowaniu zawartości szablonu ARM w wersji specyfikacji szablonu zawartość może pochodzić z nieprzetworzonego ciągu JSON (za pomocą zestawu parametrów **UpdateVersionByNameFromJsonParameterSet** ) lub z określonego pliku JSON (za pomocą zestawu parametrów **UpdateVersionByNameFromJsonFileParameterSet** ).</span><span class="sxs-lookup"><span data-stu-id="e098c-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="e098c-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e098c-115">EXAMPLES</span></span>

### <span data-ttu-id="e098c-116">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="e098c-116">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="e098c-117">Modyfikuje wersję "v 1.0" specyfikacji szablonu o nazwie "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="e098c-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="e098c-118">Określona wersja będzie $templateJson jako zawartość szablonu ARM tej wersji.</span><span class="sxs-lookup"><span data-stu-id="e098c-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="e098c-119">Jeśli Specyfikacja i/lub wersja szablonu głównego nie istnieją, zostaną one utworzone.</span><span class="sxs-lookup"><span data-stu-id="e098c-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="e098c-120">**Informacyjn**</span><span class="sxs-lookup"><span data-stu-id="e098c-120">**Notes:**</span></span> 

* <span data-ttu-id="e098c-121">Szablon ARM w przykładzie to no-op, ponieważ nie zawiera rzeczywistych zasobów.</span><span class="sxs-lookup"><span data-stu-id="e098c-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="e098c-122">Lokalizacja jest wymagana tylko wtedy, gdy Specyfikacja szablonu jeszcze nie istnieje</span><span class="sxs-lookup"><span data-stu-id="e098c-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="e098c-123">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="e098c-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="e098c-124">Modyfikuje wersję "v 2.0" specyfikacji szablonu o nazwie "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="e098c-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="e098c-125">Określona wersja będzie zawierać zawartość z pliku lokalnego "myTemplateContent.jswłączony" jako zawartość szablonu ARM tej wersji.</span><span class="sxs-lookup"><span data-stu-id="e098c-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="e098c-126">Jeśli Specyfikacja i/lub wersja szablonu głównego nie istnieją, zostaną one utworzone.</span><span class="sxs-lookup"><span data-stu-id="e098c-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="e098c-127">**Uwaga:** Lokalizacja jest wymagana tylko wtedy, gdy Specyfikacja szablonu jeszcze nie istnieje</span><span class="sxs-lookup"><span data-stu-id="e098c-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="e098c-128">Przykład 3:</span><span class="sxs-lookup"><span data-stu-id="e098c-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="e098c-129">Modyfikuje opis specyfikacji szablonu o nazwie "myTemplateSpec" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="e098c-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="e098c-130">Jeśli Specyfikacja szablonu jeszcze nie istnieje, zostanie utworzona.</span><span class="sxs-lookup"><span data-stu-id="e098c-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="e098c-131">**Uwaga:** Lokalizacja jest wymagana tylko wtedy, gdy Specyfikacja szablonu jeszcze nie istnieje</span><span class="sxs-lookup"><span data-stu-id="e098c-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="e098c-132">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e098c-132">PARAMETERS</span></span>

### <span data-ttu-id="e098c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e098c-133">-DefaultProfile</span></span>
<span data-ttu-id="e098c-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e098c-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e098c-135">— Opis</span><span class="sxs-lookup"><span data-stu-id="e098c-135">-Description</span></span>
<span data-ttu-id="e098c-136">Opis specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="e098c-136">The description of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e098c-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e098c-137">-DisplayName</span></span>
<span data-ttu-id="e098c-138">Nazwa wyświetlana specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="e098c-138">The display name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e098c-139">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e098c-139">-Location</span></span>
<span data-ttu-id="e098c-140">Lokalizacja specyfikacji szablonu. Wymagane tylko w przypadku, gdy Specyfikacja szablonu jeszcze nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="e098c-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="e098c-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e098c-141">-Name</span></span>
<span data-ttu-id="e098c-142">Nazwa specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="e098c-142">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e098c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e098c-143">-ResourceGroupName</span></span>
<span data-ttu-id="e098c-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e098c-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e098c-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e098c-145">-ResourceId</span></span>
<span data-ttu-id="e098c-146">W pełni kwalifikowany identyfikator zasobu specyfikacji szablonu. przykład:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="e098c-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e098c-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="e098c-147">-Tag</span></span>
<span data-ttu-id="e098c-148">Obiekt Hashtable znaczników specyfikacji i/lub wersji szablonu</span><span class="sxs-lookup"><span data-stu-id="e098c-148">Hashtable of tags for the template spec and/or version</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e098c-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e098c-149">-TemplateFile</span></span>
<span data-ttu-id="e098c-150">Ścieżka do pliku JSON szablonu Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e098c-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByNameFromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e098c-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="e098c-151">-TemplateJson</span></span>
<span data-ttu-id="e098c-152">KOD JSON szablonu Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e098c-152">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e098c-153">-Version</span><span class="sxs-lookup"><span data-stu-id="e098c-153">-Version</span></span>
<span data-ttu-id="e098c-154">Wersja specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="e098c-154">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e098c-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="e098c-155">-VersionDescription</span></span>
<span data-ttu-id="e098c-156">Opis wersji.</span><span class="sxs-lookup"><span data-stu-id="e098c-156">The description of the version.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e098c-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e098c-157">-Confirm</span></span>
<span data-ttu-id="e098c-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e098c-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e098c-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e098c-159">-WhatIf</span></span>
<span data-ttu-id="e098c-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e098c-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e098c-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e098c-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e098c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e098c-162">CommonParameters</span></span>
<span data-ttu-id="e098c-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e098c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e098c-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e098c-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e098c-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e098c-165">INPUTS</span></span>

### <span data-ttu-id="e098c-166">System. String</span><span class="sxs-lookup"><span data-stu-id="e098c-166">System.String</span></span>

## <span data-ttu-id="e098c-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e098c-167">OUTPUTS</span></span>

### <span data-ttu-id="e098c-168">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="e098c-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="e098c-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e098c-169">NOTES</span></span>

## <span data-ttu-id="e098c-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e098c-170">RELATED LINKS</span></span>
