---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: 2d0eb49a46e0d6fbbe02d145e42195d059c5176f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490350"
---
# <span data-ttu-id="64150-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="64150-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="64150-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64150-102">SYNOPSIS</span></span>
<span data-ttu-id="64150-103">Tworzy nową specyfikację szablonu.</span><span class="sxs-lookup"><span data-stu-id="64150-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="64150-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64150-104">SYNTAX</span></span>

### <span data-ttu-id="64150-105">FromJsonStringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="64150-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64150-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="64150-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64150-107">Opis</span><span class="sxs-lookup"><span data-stu-id="64150-107">DESCRIPTION</span></span>
<span data-ttu-id="64150-108">Tworzy nową wersję specyfikacji szablonu z określoną zawartością szablonu ARM.</span><span class="sxs-lookup"><span data-stu-id="64150-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="64150-109">Zawartość może pochodzić z nieprzetworzonego ciągu JSON (za pomocą zestawu parametrów **FromJsonStringParameterSet** ) lub z określonego pliku JSON (za pomocą zestawu parametrów **FromJsonFileParameterSet** ).</span><span class="sxs-lookup"><span data-stu-id="64150-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="64150-110">Jeśli Specyfikacja szablonu głównego jeszcze nie istnieje, zostanie utworzona wraz z wersją specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="64150-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="64150-111">Jeśli istnieje już Specyfikacja szablonu o podanej nazwie, a określona wersja zostanie zaktualizowana (wszelkie inne istniejące wersje zostaną zachowane).</span><span class="sxs-lookup"><span data-stu-id="64150-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="64150-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64150-112">EXAMPLES</span></span>

### <span data-ttu-id="64150-113">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="64150-113">Example 1:</span></span>
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

<span data-ttu-id="64150-114">Tworzy nową wersję specyfikacji szablonu "v 1.0" w specyfikacji szablonu o nazwie "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="64150-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="64150-115">Określona wersja będzie $templateJson jako zawartość szablonu ARM tej wersji.</span><span class="sxs-lookup"><span data-stu-id="64150-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="64150-116">**Uwaga:** Szablon ARM w przykładzie to no-op, ponieważ nie zawiera rzeczywistych zasobów.</span><span class="sxs-lookup"><span data-stu-id="64150-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="64150-117">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="64150-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="64150-118">Tworzy nową wersję specyfikacji szablonu "v 2.0" w specyfikacji szablonu o nazwie "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="64150-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="64150-119">Określona wersja będzie zawierać zawartość z pliku lokalnego "myTemplateContent.jswłączony" jako zawartość szablonu ARM tej wersji.</span><span class="sxs-lookup"><span data-stu-id="64150-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="64150-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64150-120">PARAMETERS</span></span>

### <span data-ttu-id="64150-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64150-121">-DefaultProfile</span></span>
<span data-ttu-id="64150-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64150-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64150-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="64150-123">-Description</span></span>
<span data-ttu-id="64150-124">Opis specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="64150-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="64150-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="64150-125">-DisplayName</span></span>
<span data-ttu-id="64150-126">Nazwa wyświetlana specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="64150-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="64150-127">-Force</span><span class="sxs-lookup"><span data-stu-id="64150-127">-Force</span></span>
<span data-ttu-id="64150-128">Nie pytaj o potwierdzenie podczas zastępowania istniejącej wersji.</span><span class="sxs-lookup"><span data-stu-id="64150-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="64150-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="64150-129">-Location</span></span>
<span data-ttu-id="64150-130">Lokalizacja specyfikacji szablonu. Wymagane tylko w przypadku, gdy Specyfikacja szablonu jeszcze nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="64150-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="64150-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64150-131">-Name</span></span>
<span data-ttu-id="64150-132">Nazwa specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="64150-132">The name of the template spec.</span></span>

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

### <span data-ttu-id="64150-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64150-133">-ResourceGroupName</span></span>
<span data-ttu-id="64150-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="64150-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="64150-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="64150-135">-Tag</span></span>
<span data-ttu-id="64150-136">Hashtable znaczników nowych zasobów specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="64150-136">Hashtable of tags for the new template spec resource(s).</span></span>

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

### <span data-ttu-id="64150-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="64150-137">-TemplateFile</span></span>
<span data-ttu-id="64150-138">Ścieżka do pliku JSON szablonu Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="64150-138">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="64150-139">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="64150-139">-TemplateJson</span></span>
<span data-ttu-id="64150-140">KOD JSON szablonu Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="64150-140">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="64150-141">-Version</span><span class="sxs-lookup"><span data-stu-id="64150-141">-Version</span></span>
<span data-ttu-id="64150-142">Wersja specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="64150-142">The version of the template spec.</span></span>

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

### <span data-ttu-id="64150-143">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="64150-143">-VersionDescription</span></span>
<span data-ttu-id="64150-144">Opis wersji.</span><span class="sxs-lookup"><span data-stu-id="64150-144">The description of the version.</span></span>

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

### <span data-ttu-id="64150-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64150-145">-Confirm</span></span>
<span data-ttu-id="64150-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64150-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64150-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64150-147">-WhatIf</span></span>
<span data-ttu-id="64150-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64150-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64150-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="64150-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64150-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64150-150">CommonParameters</span></span>
<span data-ttu-id="64150-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64150-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64150-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64150-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64150-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64150-153">INPUTS</span></span>

### <span data-ttu-id="64150-154">System. String</span><span class="sxs-lookup"><span data-stu-id="64150-154">System.String</span></span>

## <span data-ttu-id="64150-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64150-155">OUTPUTS</span></span>

### <span data-ttu-id="64150-156">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="64150-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="64150-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64150-157">NOTES</span></span>

## <span data-ttu-id="64150-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64150-158">RELATED LINKS</span></span>
