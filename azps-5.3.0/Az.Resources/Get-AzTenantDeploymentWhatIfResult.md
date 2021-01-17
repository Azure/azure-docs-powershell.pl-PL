---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentWhatIfResult.md
ms.openlocfilehash: 8e25d83eda64bb9705829ff0a8b1dd40d6055953
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490458"
---
# <span data-ttu-id="de6f6-101">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="de6f6-101">Get-AzTenantDeploymentWhatIfResult</span></span>

## <span data-ttu-id="de6f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="de6f6-103">Pobiera szablon ARM What-If wyniku wdrożenia w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="de6f6-103">Gets an ARM template What-If result for a deployment at tenant scope.</span></span> 

## <span data-ttu-id="de6f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de6f6-104">SYNTAX</span></span>

### <span data-ttu-id="de6f6-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="de6f6-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de6f6-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="de6f6-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de6f6-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="de6f6-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de6f6-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="de6f6-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de6f6-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="de6f6-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de6f6-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="de6f6-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de6f6-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="de6f6-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de6f6-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="de6f6-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de6f6-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="de6f6-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de6f6-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="de6f6-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de6f6-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="de6f6-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de6f6-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="de6f6-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de6f6-117">Opis</span><span class="sxs-lookup"><span data-stu-id="de6f6-117">DESCRIPTION</span></span>
<span data-ttu-id="de6f6-118">Polecenie cmdlet **Get-AzTenantDeploymentWhatIfResult** pobiera szablon ARM What-If wyniku wdrożenia szablonu w określonym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="de6f6-118">The **Get-AzTenantDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified tenant scope.</span></span> <span data-ttu-id="de6f6-119">Zwraca listę zmian wskazujących, które zasoby zostaną zaktualizowane po zastosowaniu wdrożenia bez wprowadzania zmian w rzeczywistych zasobach.</span><span class="sxs-lookup"><span data-stu-id="de6f6-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="de6f6-120">Aby określić format wyniku zwracanego, użyj parametru *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="de6f6-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="de6f6-121">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de6f6-121">EXAMPLES</span></span>

### <span data-ttu-id="de6f6-122">Przykład 1: uzyskiwanie What-If wyniku w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="de6f6-122">Example 1: Get a What-If result at tenant scope</span></span>
```powershell
PS C:\> Get-AzTenantDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="de6f6-123">To polecenie pobiera What-If wynik w zakresie dzierżawy przy użyciu pliku szablonu niestandardowego i pliku parametrów na dysku.</span><span class="sxs-lookup"><span data-stu-id="de6f6-123">This command gets a What-If result at tenant scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="de6f6-124">W poleceniu użyto parametru *Location* w celu określenia miejsca, w którym mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="de6f6-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="de6f6-125">W poleceniu użyto parametru *TemplateFile* w celu określenia pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="de6f6-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="de6f6-126">W poleceniu użyto parametru *TemplateParameterFile* w celu określenia pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="de6f6-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="de6f6-127">W poleceniu użyto parametru *ResultFormat* w celu skonfigurowania wyniku What-If w celu uwzględnienia pełnych ładunków zasobów.</span><span class="sxs-lookup"><span data-stu-id="de6f6-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="de6f6-128">Przykład 2: uzyskiwanie What-If wyniku w zakresie dzierżawy przy użyciu ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="de6f6-128">Example 2: Get a What-If result at tenant scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzTenantDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="de6f6-129">To polecenie pobiera What-If wynik w zakresie dzierżawy przy użyciu pliku szablonu niestandardowego i pliku parametrów na dysku.</span><span class="sxs-lookup"><span data-stu-id="de6f6-129">This command gets a What-If result at tenant scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="de6f6-130">W poleceniu użyto parametru *Location* w celu określenia miejsca, w którym mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="de6f6-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="de6f6-131">W poleceniu użyto parametru *TemplateFile* w celu określenia pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="de6f6-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="de6f6-132">W poleceniu użyto parametru *TemplateParameterFile* w celu określenia pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="de6f6-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="de6f6-133">W poleceniu użyto parametru *ResultFormat* w celu skonfigurowania wyniku What-If tylko identyfikatorów zasobów.</span><span class="sxs-lookup"><span data-stu-id="de6f6-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="de6f6-134">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de6f6-134">PARAMETERS</span></span>

### <span data-ttu-id="de6f6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de6f6-135">-DefaultProfile</span></span>
<span data-ttu-id="de6f6-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de6f6-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de6f6-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="de6f6-137">-ExcludeChangeType</span></span>
<span data-ttu-id="de6f6-138">Lista rozdzielanych przecinkami typów zmian zasobów, które mają być wykluczone z wyników What-If.</span><span class="sxs-lookup"><span data-stu-id="de6f6-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="de6f6-139">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="de6f6-139">-Location</span></span>
<span data-ttu-id="de6f6-140">Lokalizacja przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="de6f6-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="de6f6-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de6f6-141">-Name</span></span>
<span data-ttu-id="de6f6-142">Nazwa wdrożenia, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="de6f6-142">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="de6f6-143">Jeśli ten parametr nie jest określony, domyślnie jest określana nazwa pliku szablonu, gdy jest dostarczany plik szablonu; Domyślnie jest to bieżąca godzina, w której jest dostarczany obiekt szablonu, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="de6f6-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="de6f6-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="de6f6-144">-Pre</span></span>
<span data-ttu-id="de6f6-145">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="de6f6-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="de6f6-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="de6f6-146">-ResultFormat</span></span>
<span data-ttu-id="de6f6-147">What-If format wyników.</span><span class="sxs-lookup"><span data-stu-id="de6f6-147">The What-If result format.</span></span>

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

### <span data-ttu-id="de6f6-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="de6f6-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="de6f6-149">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="de6f6-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="de6f6-150">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="de6f6-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="de6f6-151">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="de6f6-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="de6f6-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="de6f6-152">-TemplateFile</span></span>
<span data-ttu-id="de6f6-153">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="de6f6-153">Local path to the template file.</span></span>

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

### <span data-ttu-id="de6f6-154">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="de6f6-154">-TemplateObject</span></span>
<span data-ttu-id="de6f6-155">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="de6f6-155">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="de6f6-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="de6f6-156">-TemplateParameterFile</span></span>
<span data-ttu-id="de6f6-157">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="de6f6-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="de6f6-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="de6f6-158">-TemplateParameterObject</span></span>
<span data-ttu-id="de6f6-159">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="de6f6-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="de6f6-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="de6f6-160">-TemplateParameterUri</span></span>
<span data-ttu-id="de6f6-161">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="de6f6-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="de6f6-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="de6f6-162">-TemplateUri</span></span>
<span data-ttu-id="de6f6-163">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="de6f6-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="de6f6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6f6-164">CommonParameters</span></span>
<span data-ttu-id="de6f6-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de6f6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6f6-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de6f6-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6f6-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de6f6-167">INPUTS</span></span>

### <span data-ttu-id="de6f6-168">System. String</span><span class="sxs-lookup"><span data-stu-id="de6f6-168">System.String</span></span>

### <span data-ttu-id="de6f6-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="de6f6-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="de6f6-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de6f6-170">OUTPUTS</span></span>

### <span data-ttu-id="de6f6-171">Microsoft. Azure. Commands. resourceName. cmdlets. SdkModels. Deployments. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="de6f6-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="de6f6-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de6f6-172">NOTES</span></span>

## <span data-ttu-id="de6f6-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de6f6-173">RELATED LINKS</span></span>
