---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 1b45c08f2906f3b1bec827a7f870d2c901bbb2b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963802"
---
# <span data-ttu-id="9e4bf-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="9e4bf-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="9e4bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e4bf-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4bf-103">Pobiera wynik What-If dla wdrożenia w zakresie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-103">Gets a template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="9e4bf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e4bf-104">SYNTAX</span></span>

### <span data-ttu-id="9e4bf-105">ByTemplateFileWithNoParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9e4bf-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e4bf-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9e4bf-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4bf-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9e4bf-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4bf-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9e4bf-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4bf-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9e4bf-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4bf-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9e4bf-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4bf-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9e4bf-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4bf-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9e4bf-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4bf-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9e4bf-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4bf-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9e4bf-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4bf-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9e4bf-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e4bf-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9e4bf-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e4bf-117">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e4bf-117">DESCRIPTION</span></span>
<span data-ttu-id="9e4bf-118">Polecenie **cmdlet Get-AzResourceGroupDeploymentWhatIfResult** pobiera ARM szablonu What-If wynik wdrożenia szablonu w określonym zakresie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="9e4bf-119">Zwraca ona listę zmian wskazujących, które zasoby zostaną zaktualizowane, jeśli wdrożenie zostanie zastosowane bez dokonywania żadnych zmian w zasobach rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="9e4bf-120">Aby określić format zwracanych wyników, użyj *parametru ResultFormat.*</span><span class="sxs-lookup"><span data-stu-id="9e4bf-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="9e4bf-121">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e4bf-121">EXAMPLES</span></span>

### <span data-ttu-id="9e4bf-122">Przykład 1. Uzyskiwanie What-If w zakresie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9e4bf-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="9e4bf-123">To polecenie uzyskuje What-If w zakresie określonej grupy zasobów przy użyciu pliku szablonu niestandardowego i pliku parametru na dysku.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="9e4bf-124">To polecenie używa *parametru ResourceGroupName* w celu określenia grupy zasobów, w której szablon zostanie wdrożony.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="9e4bf-125">To polecenie określa plik szablonu za pomocą parametru *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="9e4bf-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="9e4bf-126">To polecenie określa plik parametru szablonu za pomocą parametru *TemplateParametersFile.*</span><span class="sxs-lookup"><span data-stu-id="9e4bf-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="9e4bf-127">To polecenie używa *parametru ResultFormat* w celu What-If wyniku tak, aby uwzględniał pełne obciążenia zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="9e4bf-128">Przykład 2. Uzyskiwanie What-If w zakresie grupy zasobów przy użyciu tylko zasobu</span><span class="sxs-lookup"><span data-stu-id="9e4bf-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="9e4bf-129">To polecenie uzyskuje What-If w zakresie określonej grupy zasobów przy użyciu pliku szablonu niestandardowego i pliku parametru na dysku.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="9e4bf-130">To polecenie używa *parametru ResourceGroupName* w celu określenia grupy zasobów, w której szablon zostanie wdrożony.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="9e4bf-131">To polecenie określa plik szablonu za pomocą parametru *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="9e4bf-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="9e4bf-132">To polecenie określa plik parametru szablonu za pomocą parametru *TemplateParametersFile.*</span><span class="sxs-lookup"><span data-stu-id="9e4bf-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="9e4bf-133">To polecenie używa *parametru ResultFormat* w celu What-If wyniku tak, aby zawierał tylko identyfikatory zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="9e4bf-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e4bf-134">PARAMETERS</span></span>

### <span data-ttu-id="9e4bf-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4bf-135">-DefaultProfile</span></span>
<span data-ttu-id="9e4bf-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e4bf-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="9e4bf-137">-ExcludeChangeType</span></span>
<span data-ttu-id="9e4bf-138">Typy zmian zasobów rozdzielane przecinkami, które mają być wykluczone What-If wyników.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4bf-139">— tryb</span><span class="sxs-lookup"><span data-stu-id="9e4bf-139">-Mode</span></span>
<span data-ttu-id="9e4bf-140">Tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-140">The deployment mode.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4bf-141">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9e4bf-141">-Name</span></span>
<span data-ttu-id="9e4bf-142">Nazwa wdrożenia, które zostanie utworzyć.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="9e4bf-143">W przypadku, gdy plik szablonu jest podany, domyślnie jest określana jego nazwa domyślna. domyślnie jest to bieżąca godzina, gdy obiekt szablonu jest podany, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="9e4bf-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4bf-144">— Przed</span><span class="sxs-lookup"><span data-stu-id="9e4bf-144">-Pre</span></span>
<span data-ttu-id="9e4bf-145">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9e4bf-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e4bf-146">-ResourceGroupName</span></span>
<span data-ttu-id="9e4bf-147">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-147">The resource group name.</span></span>

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

### <span data-ttu-id="9e4bf-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="9e4bf-148">-ResultFormat</span></span>
<span data-ttu-id="9e4bf-149">Format What-If wynik.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-149">The What-If result format.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.WhatIfResultFormat
Parameter Sets: (All)
Aliases:
Accepted values: ResourceIdOnly, FullResourcePayloads

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e4bf-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="9e4bf-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="9e4bf-151">Pomija dynamiczne przetwarzanie parametrów programu PowerShell, które sprawdza, czy podany parametr szablonu zawiera wszystkie niezbędne parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="9e4bf-152">To sprawdzenie spowoduje monitowanie użytkownika o podanie wartości dla brakujących parametrów, ale podanie parametru -SkipTemplateParameterPrompt spowoduje natychmiastowe zignorowanie tego monitu i błędu, jeśli znaleziono, że parametr nie jest powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="9e4bf-153">W przypadku skryptów nieinterakcyjnych można udostępnić komunikat -SkipTemplateParameterPrompt w celu zapewnienia lepszego komunikatu o błędzie w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="9e4bf-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9e4bf-154">-TemplateFile</span></span>
<span data-ttu-id="9e4bf-155">Ścieżka lokalna do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-155">Local path to the template file.</span></span> <span data-ttu-id="9e4bf-156">Obsługiwany typ pliku szablonu: json i biceps.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-156">Supported template file type: json and bicep.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4bf-157">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="9e4bf-157">-TemplateObject</span></span>
<span data-ttu-id="9e4bf-158">Tabela skrótów reprezentująca szablon.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-158">A hash table which represents the template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4bf-159">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="9e4bf-159">-TemplateParameterFile</span></span>
<span data-ttu-id="9e4bf-160">Plik z parametrami szablonu.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-160">A file that has the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4bf-161">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="9e4bf-161">-TemplateParameterObject</span></span>
<span data-ttu-id="9e4bf-162">Tabela skrótów reprezentująca parametry.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-162">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4bf-163">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="9e4bf-163">-TemplateParameterUri</span></span>
<span data-ttu-id="9e4bf-164">Uri do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-164">Uri to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4bf-165">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="9e4bf-165">-TemplateUri</span></span>
<span data-ttu-id="9e4bf-166">Uri do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-166">Uri to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4bf-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4bf-167">CommonParameters</span></span>
<span data-ttu-id="9e4bf-168">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e4bf-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4bf-169">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e4bf-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4bf-170">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e4bf-170">INPUTS</span></span>

### <span data-ttu-id="9e4bf-171">System.String</span><span class="sxs-lookup"><span data-stu-id="9e4bf-171">System.String</span></span>

### <span data-ttu-id="9e4bf-172">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="9e4bf-172">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="9e4bf-173">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9e4bf-173">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9e4bf-174">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e4bf-174">OUTPUTS</span></span>

### <span data-ttu-id="9e4bf-175">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="9e4bf-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="9e4bf-176">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e4bf-176">NOTES</span></span>

## <span data-ttu-id="9e4bf-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e4bf-177">RELATED LINKS</span></span>
