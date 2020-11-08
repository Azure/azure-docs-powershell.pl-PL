---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: aa011c7a858f08e3528fb2cdd7d67bcff37d76d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219948"
---
# <span data-ttu-id="268f4-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="268f4-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="268f4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="268f4-102">SYNOPSIS</span></span>
<span data-ttu-id="268f4-103">Pobiera szablon ARM What-If wyniku wdrożenia w zakresie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="268f4-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="268f4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="268f4-104">SYNTAX</span></span>

### <span data-ttu-id="268f4-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="268f4-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="268f4-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="268f4-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268f4-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="268f4-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268f4-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="268f4-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268f4-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="268f4-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268f4-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="268f4-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268f4-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="268f4-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268f4-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="268f4-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268f4-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="268f4-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268f4-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="268f4-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268f4-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="268f4-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="268f4-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="268f4-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="268f4-117">Opis</span><span class="sxs-lookup"><span data-stu-id="268f4-117">DESCRIPTION</span></span>
<span data-ttu-id="268f4-118">Polecenie cmdlet **Get-AzResourceGroupDeploymentWhatIfResult** pobiera szablon ARM What-If wyniku wdrożenia szablonu w określonym zakresie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="268f4-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="268f4-119">Zwraca listę zmian wskazujących, które zasoby zostaną zaktualizowane po zastosowaniu wdrożenia bez wprowadzania zmian w rzeczywistych zasobach.</span><span class="sxs-lookup"><span data-stu-id="268f4-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="268f4-120">Aby określić format wyniku zwracanego, użyj parametru *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="268f4-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="268f4-121">Przykłady</span><span class="sxs-lookup"><span data-stu-id="268f4-121">EXAMPLES</span></span>

### <span data-ttu-id="268f4-122">Przykład 1: uzyskiwanie What-If wyniku w zakresie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="268f4-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="268f4-123">To polecenie pobiera What-If wynik z określonego zakresu grupy zasobów przy użyciu pliku szablonu niestandardowego i pliku parametrów na dysku.</span><span class="sxs-lookup"><span data-stu-id="268f4-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="268f4-124">W poleceniu użyto parametru *ResourceGroupName* w celu określenia grupy zasobów, w której zostanie wdrożony szablon.</span><span class="sxs-lookup"><span data-stu-id="268f4-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="268f4-125">W poleceniu użyto parametru *TemplateFile* w celu określenia pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="268f4-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="268f4-126">W poleceniu użyto parametru *TemplateParameterFile* w celu określenia pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="268f4-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="268f4-127">W poleceniu użyto parametru *ResultFormat* w celu skonfigurowania wyniku What-If w celu uwzględnienia pełnych ładunków zasobów.</span><span class="sxs-lookup"><span data-stu-id="268f4-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="268f4-128">Przykład 2: uzyskiwanie What-If wyniku w zakresie grupy zasobów z ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="268f4-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="268f4-129">To polecenie pobiera What-If wynik z określonego zakresu grupy zasobów przy użyciu pliku szablonu niestandardowego i pliku parametrów na dysku.</span><span class="sxs-lookup"><span data-stu-id="268f4-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="268f4-130">W poleceniu użyto parametru *ResourceGroupName* w celu określenia grupy zasobów, w której zostanie wdrożony szablon.</span><span class="sxs-lookup"><span data-stu-id="268f4-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="268f4-131">W poleceniu użyto parametru *TemplateFile* w celu określenia pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="268f4-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="268f4-132">W poleceniu użyto parametru *TemplateParameterFile* w celu określenia pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="268f4-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="268f4-133">W poleceniu użyto parametru *ResultFormat* w celu skonfigurowania wyniku What-If tylko identyfikatorów zasobów.</span><span class="sxs-lookup"><span data-stu-id="268f4-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="268f4-134">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="268f4-134">PARAMETERS</span></span>

### <span data-ttu-id="268f4-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="268f4-135">-ApiVersion</span></span>
<span data-ttu-id="268f4-136">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="268f4-136">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="268f4-137">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="268f4-137">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="268f4-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268f4-138">-DefaultProfile</span></span>
<span data-ttu-id="268f4-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="268f4-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="268f4-140">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="268f4-140">-ExcludeChangeType</span></span>
<span data-ttu-id="268f4-141">Typy zmian zasobów rozdzielanych przecinkami, które mają być wykluczone z wyników What-If.</span><span class="sxs-lookup"><span data-stu-id="268f4-141">Comma-separated resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="268f4-142">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="268f4-142">-Mode</span></span>
<span data-ttu-id="268f4-143">Tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="268f4-143">The deployment mode.</span></span>

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

### <span data-ttu-id="268f4-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="268f4-144">-Name</span></span>
<span data-ttu-id="268f4-145">Nazwa wdrożenia, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="268f4-145">The name of the deployment it's going to create.</span></span> <span data-ttu-id="268f4-146">Jeśli ten parametr nie jest określony, domyślnie jest określana nazwa pliku szablonu, gdy jest dostarczany plik szablonu; Domyślnie jest to bieżąca godzina, w której jest dostarczany obiekt szablonu, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="268f4-146">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="268f4-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="268f4-147">-Pre</span></span>
<span data-ttu-id="268f4-148">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="268f4-148">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="268f4-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="268f4-149">-ResourceGroupName</span></span>
<span data-ttu-id="268f4-150">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="268f4-150">The resource group name.</span></span>

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

### <span data-ttu-id="268f4-151">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="268f4-151">-ResultFormat</span></span>
<span data-ttu-id="268f4-152">What-If format wyników.</span><span class="sxs-lookup"><span data-stu-id="268f4-152">The What-If result format.</span></span>

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

### <span data-ttu-id="268f4-153">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="268f4-153">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="268f4-154">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="268f4-154">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="268f4-155">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="268f4-155">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="268f4-156">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="268f4-156">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="268f4-157">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="268f4-157">-TemplateFile</span></span>
<span data-ttu-id="268f4-158">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="268f4-158">Local path to the template file.</span></span>

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

### <span data-ttu-id="268f4-159">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="268f4-159">-TemplateObject</span></span>
<span data-ttu-id="268f4-160">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="268f4-160">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="268f4-161">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="268f4-161">-TemplateParameterFile</span></span>
<span data-ttu-id="268f4-162">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="268f4-162">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="268f4-163">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="268f4-163">-TemplateParameterObject</span></span>
<span data-ttu-id="268f4-164">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="268f4-164">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="268f4-165">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="268f4-165">-TemplateParameterUri</span></span>
<span data-ttu-id="268f4-166">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="268f4-166">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="268f4-167">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="268f4-167">-TemplateUri</span></span>
<span data-ttu-id="268f4-168">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="268f4-168">Uri to the template file.</span></span>

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

### <span data-ttu-id="268f4-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268f4-169">CommonParameters</span></span>
<span data-ttu-id="268f4-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="268f4-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268f4-171">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="268f4-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268f4-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="268f4-172">INPUTS</span></span>

### <span data-ttu-id="268f4-173">System. String</span><span class="sxs-lookup"><span data-stu-id="268f4-173">System.String</span></span>

### <span data-ttu-id="268f4-174">Microsoft. Azure. Management. ResourceManager. modele. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="268f4-174">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="268f4-175">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="268f4-175">System.Collections.Hashtable</span></span>

## <span data-ttu-id="268f4-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="268f4-176">OUTPUTS</span></span>

### <span data-ttu-id="268f4-177">Microsoft. Azure. Commands. resourceName. cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="268f4-177">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="268f4-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="268f4-178">NOTES</span></span>

## <span data-ttu-id="268f4-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="268f4-179">RELATED LINKS</span></span>
