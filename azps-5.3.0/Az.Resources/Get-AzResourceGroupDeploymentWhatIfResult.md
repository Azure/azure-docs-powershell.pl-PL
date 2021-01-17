---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 09b0a1a6691b4c3d491d15d226fb8260fb7ae00e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490494"
---
# <span data-ttu-id="c64c3-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="c64c3-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="c64c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c64c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c64c3-103">Pobiera szablon ARM What-If wyniku wdrożenia w zakresie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c64c3-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="c64c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c64c3-104">SYNTAX</span></span>

### <span data-ttu-id="c64c3-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c64c3-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c64c3-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c64c3-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c64c3-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c64c3-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c64c3-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c64c3-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c64c3-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c64c3-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c64c3-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c64c3-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c64c3-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c64c3-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c64c3-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c64c3-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c64c3-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c64c3-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c64c3-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c64c3-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c64c3-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c64c3-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c64c3-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c64c3-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c64c3-117">Opis</span><span class="sxs-lookup"><span data-stu-id="c64c3-117">DESCRIPTION</span></span>
<span data-ttu-id="c64c3-118">Polecenie cmdlet **Get-AzResourceGroupDeploymentWhatIfResult** pobiera szablon ARM What-If wyniku wdrożenia szablonu w określonym zakresie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c64c3-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="c64c3-119">Zwraca listę zmian wskazujących, które zasoby zostaną zaktualizowane po zastosowaniu wdrożenia bez wprowadzania zmian w rzeczywistych zasobach.</span><span class="sxs-lookup"><span data-stu-id="c64c3-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="c64c3-120">Aby określić format wyniku zwracanego, użyj parametru *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="c64c3-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="c64c3-121">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c64c3-121">EXAMPLES</span></span>

### <span data-ttu-id="c64c3-122">Przykład 1: uzyskiwanie What-If wyniku w zakresie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c64c3-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="c64c3-123">To polecenie pobiera What-If wynik z określonego zakresu grupy zasobów przy użyciu pliku szablonu niestandardowego i pliku parametrów na dysku.</span><span class="sxs-lookup"><span data-stu-id="c64c3-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="c64c3-124">W poleceniu użyto parametru *ResourceGroupName* w celu określenia grupy zasobów, w której zostanie wdrożony szablon.</span><span class="sxs-lookup"><span data-stu-id="c64c3-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="c64c3-125">W poleceniu użyto parametru *TemplateFile* w celu określenia pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="c64c3-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="c64c3-126">W poleceniu użyto parametru *TemplateParameterFile* w celu określenia pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="c64c3-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="c64c3-127">W poleceniu użyto parametru *ResultFormat* w celu skonfigurowania wyniku What-If w celu uwzględnienia pełnych ładunków zasobów.</span><span class="sxs-lookup"><span data-stu-id="c64c3-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="c64c3-128">Przykład 2: uzyskiwanie What-If wyniku w zakresie grupy zasobów z ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="c64c3-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="c64c3-129">To polecenie pobiera What-If wynik z określonego zakresu grupy zasobów przy użyciu pliku szablonu niestandardowego i pliku parametrów na dysku.</span><span class="sxs-lookup"><span data-stu-id="c64c3-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="c64c3-130">W poleceniu użyto parametru *ResourceGroupName* w celu określenia grupy zasobów, w której zostanie wdrożony szablon.</span><span class="sxs-lookup"><span data-stu-id="c64c3-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="c64c3-131">W poleceniu użyto parametru *TemplateFile* w celu określenia pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="c64c3-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="c64c3-132">W poleceniu użyto parametru *TemplateParameterFile* w celu określenia pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="c64c3-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="c64c3-133">W poleceniu użyto parametru *ResultFormat* w celu skonfigurowania wyniku What-If tylko identyfikatorów zasobów.</span><span class="sxs-lookup"><span data-stu-id="c64c3-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="c64c3-134">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c64c3-134">PARAMETERS</span></span>

### <span data-ttu-id="c64c3-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c64c3-135">-DefaultProfile</span></span>
<span data-ttu-id="c64c3-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c64c3-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c64c3-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="c64c3-137">-ExcludeChangeType</span></span>
<span data-ttu-id="c64c3-138">Typy zmian zasobów rozdzielanych przecinkami, które mają być wykluczone z wyników What-If.</span><span class="sxs-lookup"><span data-stu-id="c64c3-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="c64c3-139">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="c64c3-139">-Mode</span></span>
<span data-ttu-id="c64c3-140">Tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="c64c3-140">The deployment mode.</span></span>

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

### <span data-ttu-id="c64c3-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c64c3-141">-Name</span></span>
<span data-ttu-id="c64c3-142">Nazwa wdrożenia, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="c64c3-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="c64c3-143">Jeśli ten parametr nie jest określony, domyślnie jest określana nazwa pliku szablonu, gdy jest dostarczany plik szablonu; Domyślnie jest to bieżąca godzina, w której jest dostarczany obiekt szablonu, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="c64c3-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="c64c3-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="c64c3-144">-Pre</span></span>
<span data-ttu-id="c64c3-145">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="c64c3-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c64c3-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c64c3-146">-ResourceGroupName</span></span>
<span data-ttu-id="c64c3-147">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c64c3-147">The resource group name.</span></span>

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

### <span data-ttu-id="c64c3-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="c64c3-148">-ResultFormat</span></span>
<span data-ttu-id="c64c3-149">What-If format wyników.</span><span class="sxs-lookup"><span data-stu-id="c64c3-149">The What-If result format.</span></span>

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

### <span data-ttu-id="c64c3-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="c64c3-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="c64c3-151">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="c64c3-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="c64c3-152">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="c64c3-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="c64c3-153">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="c64c3-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="c64c3-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c64c3-154">-TemplateFile</span></span>
<span data-ttu-id="c64c3-155">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="c64c3-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="c64c3-156">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="c64c3-156">-TemplateObject</span></span>
<span data-ttu-id="c64c3-157">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="c64c3-157">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="c64c3-158">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c64c3-158">-TemplateParameterFile</span></span>
<span data-ttu-id="c64c3-159">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="c64c3-159">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="c64c3-160">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="c64c3-160">-TemplateParameterObject</span></span>
<span data-ttu-id="c64c3-161">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="c64c3-161">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="c64c3-162">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="c64c3-162">-TemplateParameterUri</span></span>
<span data-ttu-id="c64c3-163">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="c64c3-163">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="c64c3-164">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c64c3-164">-TemplateUri</span></span>
<span data-ttu-id="c64c3-165">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="c64c3-165">Uri to the template file.</span></span>

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

### <span data-ttu-id="c64c3-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c64c3-166">CommonParameters</span></span>
<span data-ttu-id="c64c3-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c64c3-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c64c3-168">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c64c3-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c64c3-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c64c3-169">INPUTS</span></span>

### <span data-ttu-id="c64c3-170">System. String</span><span class="sxs-lookup"><span data-stu-id="c64c3-170">System.String</span></span>

### <span data-ttu-id="c64c3-171">Microsoft. Azure. Management. ResourceManager. modele. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="c64c3-171">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="c64c3-172">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c64c3-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c64c3-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c64c3-173">OUTPUTS</span></span>

### <span data-ttu-id="c64c3-174">Microsoft. Azure. Commands. resourceName. cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="c64c3-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="c64c3-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c64c3-175">NOTES</span></span>

## <span data-ttu-id="c64c3-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c64c3-176">RELATED LINKS</span></span>
