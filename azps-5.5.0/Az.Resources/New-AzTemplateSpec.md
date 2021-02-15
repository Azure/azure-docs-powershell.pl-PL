---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: 2d0eb49a46e0d6fbbe02d145e42195d059c5176f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201882"
---
# <span data-ttu-id="d0522-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="d0522-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="d0522-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0522-102">SYNOPSIS</span></span>
<span data-ttu-id="d0522-103">Tworzy nową specyfikację szablonu.</span><span class="sxs-lookup"><span data-stu-id="d0522-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="d0522-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d0522-104">SYNTAX</span></span>

### <span data-ttu-id="d0522-105">FromJsonStringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d0522-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0522-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0522-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0522-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d0522-107">DESCRIPTION</span></span>
<span data-ttu-id="d0522-108">Tworzy nową wersję specyfikacji szablonu z określoną ARM szablonu.</span><span class="sxs-lookup"><span data-stu-id="d0522-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="d0522-109">Zawartość może pochodzić z nieprzetworzonych ciągów JSON (przy użyciu zestawu parametrów **FromJsonStringParameterSet)** lub z określonego pliku JSON (przy użyciu zestawu parametrów **FromJsonFileParameterSet).**</span><span class="sxs-lookup"><span data-stu-id="d0522-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="d0522-110">Jeśli główna specyfikacja szablonu jeszcze nie istnieje, zostanie utworzona wraz z wersją specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="d0522-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="d0522-111">Jeśli specyfikacja szablonu już istnieje z podaną nazwą, zostanie zaktualizowana i określona wersja zostanie zaktualizowana (wszystkie istniejące wersje zostaną zachowane).</span><span class="sxs-lookup"><span data-stu-id="d0522-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="d0522-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d0522-112">EXAMPLES</span></span>

### <span data-ttu-id="d0522-113">Przykład 1.</span><span class="sxs-lookup"><span data-stu-id="d0522-113">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="d0522-114">Tworzy nową wersję specyfikacji szablonu "v1.0" w specyfikacji szablonu o nazwie "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="d0522-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="d0522-115">Określona wersja będzie $templateJson jako zawartość szablonu ARM wersji.</span><span class="sxs-lookup"><span data-stu-id="d0522-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="d0522-116">**Uwaga:** Szablon ARM w tym przykładzie to brak możliwości, ponieważ nie zawiera on żadnych rzeczywistych zasobów.</span><span class="sxs-lookup"><span data-stu-id="d0522-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="d0522-117">Przykład 2.</span><span class="sxs-lookup"><span data-stu-id="d0522-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="d0522-118">Tworzy nową wersję specyfikacji szablonu "v2.0" w specyfikacji szablonu o nazwie "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="d0522-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="d0522-119">Określona wersja będzie zawierała zawartość lokalnego pliku "myTemplateContent.js", jako zawartość szablonu ARM wersji.</span><span class="sxs-lookup"><span data-stu-id="d0522-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="d0522-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0522-120">PARAMETERS</span></span>

### <span data-ttu-id="d0522-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0522-121">-DefaultProfile</span></span>
<span data-ttu-id="d0522-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0522-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0522-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="d0522-123">-Description</span></span>
<span data-ttu-id="d0522-124">Opis specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="d0522-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="d0522-125">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="d0522-125">-DisplayName</span></span>
<span data-ttu-id="d0522-126">Nazwa wyświetlana specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="d0522-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="d0522-127">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d0522-127">-Force</span></span>
<span data-ttu-id="d0522-128">Nie należy prosić o potwierdzenie przy podsyłaniu istniejącej wersji.</span><span class="sxs-lookup"><span data-stu-id="d0522-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="d0522-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d0522-129">-Location</span></span>
<span data-ttu-id="d0522-130">Lokalizacja specyfikacji szablonu. Wymagane tylko wtedy, gdy specyfikacja szablonu jeszcze nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="d0522-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="d0522-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d0522-131">-Name</span></span>
<span data-ttu-id="d0522-132">Nazwa specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="d0522-132">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0522-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0522-133">-ResourceGroupName</span></span>
<span data-ttu-id="d0522-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d0522-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0522-135">— Tag</span><span class="sxs-lookup"><span data-stu-id="d0522-135">-Tag</span></span>
<span data-ttu-id="d0522-136">Skróty tagów dla nowych zasobów specyfikacji szablonów.</span><span class="sxs-lookup"><span data-stu-id="d0522-136">Hashtable of tags for the new template spec resource(s).</span></span>

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

### <span data-ttu-id="d0522-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d0522-137">-TemplateFile</span></span>
<span data-ttu-id="d0522-138">Ścieżka pliku do lokalnego pliku JSON szablonu usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d0522-138">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0522-139">- TemplateJson</span><span class="sxs-lookup"><span data-stu-id="d0522-139">-TemplateJson</span></span>
<span data-ttu-id="d0522-140">JSON szablonu usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d0522-140">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0522-141">— Wersja</span><span class="sxs-lookup"><span data-stu-id="d0522-141">-Version</span></span>
<span data-ttu-id="d0522-142">Wersja specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="d0522-142">The version of the template spec.</span></span>

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

### <span data-ttu-id="d0522-143">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="d0522-143">-VersionDescription</span></span>
<span data-ttu-id="d0522-144">Opis wersji.</span><span class="sxs-lookup"><span data-stu-id="d0522-144">The description of the version.</span></span>

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

### <span data-ttu-id="d0522-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0522-145">-Confirm</span></span>
<span data-ttu-id="d0522-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d0522-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0522-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0522-147">-WhatIf</span></span>
<span data-ttu-id="d0522-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0522-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0522-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d0522-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0522-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0522-150">CommonParameters</span></span>
<span data-ttu-id="d0522-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0522-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0522-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0522-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0522-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0522-153">INPUTS</span></span>

### <span data-ttu-id="d0522-154">System.String</span><span class="sxs-lookup"><span data-stu-id="d0522-154">System.String</span></span>

## <span data-ttu-id="d0522-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0522-155">OUTPUTS</span></span>

### <span data-ttu-id="d0522-156">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="d0522-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="d0522-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d0522-157">NOTES</span></span>

## <span data-ttu-id="d0522-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0522-158">RELATED LINKS</span></span>
