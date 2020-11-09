---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: df199c25a210a4975eccf96f9f7aa7e6c219689c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308928"
---
# <span data-ttu-id="e1c5b-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="e1c5b-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="e1c5b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1c5b-102">SYNOPSIS</span></span>
<span data-ttu-id="e1c5b-103">Pobiera szablon ARM What-If wyniku wdrożenia w zakresie grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-103">Gets an ARM template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="e1c5b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1c5b-104">SYNTAX</span></span>

### <span data-ttu-id="e1c5b-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e1c5b-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1c5b-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e1c5b-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1c5b-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e1c5b-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1c5b-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e1c5b-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1c5b-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e1c5b-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1c5b-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e1c5b-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1c5b-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e1c5b-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1c5b-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e1c5b-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1c5b-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e1c5b-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1c5b-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e1c5b-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1c5b-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e1c5b-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1c5b-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e1c5b-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1c5b-117">Opis</span><span class="sxs-lookup"><span data-stu-id="e1c5b-117">DESCRIPTION</span></span>
<span data-ttu-id="e1c5b-118">Polecenie cmdlet **Get-AzManagementGroupDeploymentWhatIfResult** pobiera szablon ARM What-If wyniku wdrożenia szablonu w określonym zakresie grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="e1c5b-119">Zwraca listę zmian wskazujących, które zasoby zostaną zaktualizowane po zastosowaniu wdrożenia bez wprowadzania zmian w rzeczywistych zasobach.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="e1c5b-120">Aby określić format wyniku zwracanego, użyj parametru *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="e1c5b-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="e1c5b-121">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1c5b-121">EXAMPLES</span></span>

### <span data-ttu-id="e1c5b-122">Przykład 1: uzyskiwanie What-If wyniku w zakresie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="e1c5b-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="e1c5b-123">To polecenie pobiera What-If wynik w zakresie grupy zarządzania przy użyciu pliku szablonu niestandardowego oraz pliku parametrów na dysku.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="e1c5b-124">W poleceniu użyto parametru *Location* w celu określenia miejsca, w którym mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="e1c5b-125">W poleceniu użyto parametru *ManagementGroupId* w celu określenia grupy zarządzania, w której szablon zostanie wdrożony.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="e1c5b-126">W poleceniu użyto parametru *TemplateFile* w celu określenia pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="e1c5b-127">W poleceniu użyto parametru *TemplateParameterFile* w celu określenia pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="e1c5b-128">W poleceniu użyto parametru *ResultFormat* w celu skonfigurowania wyniku What-If w celu uwzględnienia pełnych ładunków zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="e1c5b-129">Przykład 2: uzyskiwanie wyników What-If w zakresie grupy zarządzania przy użyciu ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="e1c5b-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="e1c5b-130">To polecenie pobiera What-If wynik w zakresie grupy zarządzania przy użyciu pliku szablonu niestandardowego oraz pliku parametrów na dysku.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="e1c5b-131">W poleceniu użyto parametru *Location* w celu określenia miejsca, w którym mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="e1c5b-132">W poleceniu użyto parametru *ManagementGroupId* w celu określenia grupy zarządzania, w której szablon zostanie wdrożony.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="e1c5b-133">W poleceniu użyto parametru *TemplateFile* w celu określenia pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="e1c5b-134">W poleceniu użyto parametru *TemplateParameterFile* w celu określenia pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="e1c5b-135">W poleceniu użyto parametru *ResultFormat* w celu skonfigurowania wyniku What-If tylko identyfikatorów zasobów.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="e1c5b-136">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1c5b-136">PARAMETERS</span></span>

### <span data-ttu-id="e1c5b-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1c5b-137">-DefaultProfile</span></span>
<span data-ttu-id="e1c5b-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1c5b-139">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="e1c5b-139">-ExcludeChangeType</span></span>
<span data-ttu-id="e1c5b-140">Lista rozdzielanych przecinkami typów zmian zasobów, które mają być wykluczone z wyników What-If.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-140">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="e1c5b-141">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e1c5b-141">-Location</span></span>
<span data-ttu-id="e1c5b-142">Lokalizacja przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-142">The location to store deployment data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c5b-143">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="e1c5b-143">-ManagementGroupId</span></span>
<span data-ttu-id="e1c5b-144">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-144">The management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c5b-145">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1c5b-145">-Name</span></span>
<span data-ttu-id="e1c5b-146">Nazwa wdrożenia, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-146">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="e1c5b-147">Jeśli ten parametr nie jest określony, domyślnie jest określana nazwa pliku szablonu, gdy jest dostarczany plik szablonu; Domyślnie jest to bieżąca godzina, w której jest dostarczany obiekt szablonu, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="e1c5b-147">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1c5b-148">-Pre</span><span class="sxs-lookup"><span data-stu-id="e1c5b-148">-Pre</span></span>
<span data-ttu-id="e1c5b-149">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-149">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e1c5b-150">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="e1c5b-150">-ResultFormat</span></span>
<span data-ttu-id="e1c5b-151">What-If format wyników.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-151">The What-If result format.</span></span>

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

### <span data-ttu-id="e1c5b-152">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="e1c5b-152">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="e1c5b-153">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-153">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="e1c5b-154">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-154">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="e1c5b-155">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-155">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="e1c5b-156">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e1c5b-156">-TemplateFile</span></span>
<span data-ttu-id="e1c5b-157">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-157">Local path to the template file.</span></span>

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

### <span data-ttu-id="e1c5b-158">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="e1c5b-158">-TemplateObject</span></span>
<span data-ttu-id="e1c5b-159">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-159">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="e1c5b-160">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e1c5b-160">-TemplateParameterFile</span></span>
<span data-ttu-id="e1c5b-161">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-161">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="e1c5b-162">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e1c5b-162">-TemplateParameterObject</span></span>
<span data-ttu-id="e1c5b-163">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-163">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="e1c5b-164">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e1c5b-164">-TemplateParameterUri</span></span>
<span data-ttu-id="e1c5b-165">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-165">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="e1c5b-166">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e1c5b-166">-TemplateUri</span></span>
<span data-ttu-id="e1c5b-167">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-167">Uri to the template file.</span></span>

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

### <span data-ttu-id="e1c5b-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1c5b-168">CommonParameters</span></span>
<span data-ttu-id="e1c5b-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1c5b-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1c5b-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1c5b-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1c5b-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1c5b-171">INPUTS</span></span>

### <span data-ttu-id="e1c5b-172">System. String</span><span class="sxs-lookup"><span data-stu-id="e1c5b-172">System.String</span></span>

### <span data-ttu-id="e1c5b-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e1c5b-173">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e1c5b-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1c5b-174">OUTPUTS</span></span>

### <span data-ttu-id="e1c5b-175">Microsoft. Azure. Commands. resourceName. cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="e1c5b-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="e1c5b-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1c5b-176">NOTES</span></span>

## <span data-ttu-id="e1c5b-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1c5b-177">RELATED LINKS</span></span>
