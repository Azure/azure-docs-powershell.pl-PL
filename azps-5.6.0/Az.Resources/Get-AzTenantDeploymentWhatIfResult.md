---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztenantdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentWhatIfResult.md
ms.openlocfilehash: d8fc37b886013b49e7e5ec00093744e276e683b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014913"
---
# <span data-ttu-id="7bcb3-101">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="7bcb3-101">Get-AzTenantDeploymentWhatIfResult</span></span>

## <span data-ttu-id="7bcb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bcb3-102">SYNOPSIS</span></span>
<span data-ttu-id="7bcb3-103">Pobiera wynik What-If dla wdrożenia w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-103">Gets a template What-If result for a deployment at tenant scope.</span></span> 

## <span data-ttu-id="7bcb3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7bcb3-104">SYNTAX</span></span>

### <span data-ttu-id="7bcb3-105">ByTemplateFileWithNoParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7bcb3-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bcb3-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7bcb3-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bcb3-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7bcb3-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bcb3-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7bcb3-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bcb3-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7bcb3-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bcb3-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7bcb3-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bcb3-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7bcb3-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bcb3-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7bcb3-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bcb3-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7bcb3-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bcb3-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7bcb3-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bcb3-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7bcb3-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bcb3-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7bcb3-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bcb3-117">OPIS</span><span class="sxs-lookup"><span data-stu-id="7bcb3-117">DESCRIPTION</span></span>
<span data-ttu-id="7bcb3-118">Polecenie **cmdlet Get-AzTenantDeploymentWhatIfResult** pobiera ARM szablonu What-If wynik wdrożenia szablonów w określonym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-118">The **Get-AzTenantDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified tenant scope.</span></span> <span data-ttu-id="7bcb3-119">Zwraca ona listę zmian wskazujących, które zasoby zostaną zaktualizowane, jeśli wdrożenie zostanie zastosowane bez dokonywania żadnych zmian w zasobach rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="7bcb3-120">Aby określić format zwracanych wyników, użyj *parametru ResultFormat.*</span><span class="sxs-lookup"><span data-stu-id="7bcb3-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="7bcb3-121">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7bcb3-121">EXAMPLES</span></span>

### <span data-ttu-id="7bcb3-122">Przykład 1. Uzyskiwanie What-If w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="7bcb3-122">Example 1: Get a What-If result at tenant scope</span></span>
```powershell
PS C:\> Get-AzTenantDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="7bcb3-123">To polecenie uzyskuje What-If w zakresie dzierżawy przy użyciu pliku szablonu niestandardowego i pliku parametru na dysku.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-123">This command gets a What-If result at tenant scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="7bcb3-124">To polecenie używa *parametru Location* w celu określenia, gdzie mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="7bcb3-125">To polecenie określa plik szablonu za pomocą parametru *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="7bcb3-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="7bcb3-126">To polecenie określa plik parametru szablonu za pomocą parametru *TemplateParametersFile.*</span><span class="sxs-lookup"><span data-stu-id="7bcb3-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="7bcb3-127">To polecenie używa *parametru ResultFormat* w celu What-If wyniku tak, aby uwzględniał pełne obciążenia zasobów.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="7bcb3-128">Przykład 2. Uzyskiwanie wyniku What-If w zakresie dzierżawy przy użyciu usługi ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="7bcb3-128">Example 2: Get a What-If result at tenant scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzTenantDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="7bcb3-129">To polecenie uzyskuje What-If w zakresie dzierżawy przy użyciu pliku szablonu niestandardowego i pliku parametru na dysku.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-129">This command gets a What-If result at tenant scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="7bcb3-130">To polecenie używa *parametru Location* w celu określenia, gdzie mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="7bcb3-131">To polecenie określa plik szablonu za pomocą parametru *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="7bcb3-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="7bcb3-132">To polecenie określa plik parametru szablonu za pomocą parametru *TemplateParametersFile.*</span><span class="sxs-lookup"><span data-stu-id="7bcb3-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="7bcb3-133">To polecenie używa *parametru ResultFormat* w celu What-If wyniku tak, aby zawierał tylko identyfikatory zasobów.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="7bcb3-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bcb3-134">PARAMETERS</span></span>

### <span data-ttu-id="7bcb3-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bcb3-135">-DefaultProfile</span></span>
<span data-ttu-id="7bcb3-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bcb3-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="7bcb3-137">-ExcludeChangeType</span></span>
<span data-ttu-id="7bcb3-138">Rozdzielona przecinkami lista typów zmian zasobów do wykluczenia z What-If wyników.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="7bcb3-139">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7bcb3-139">-Location</span></span>
<span data-ttu-id="7bcb3-140">Lokalizacja przechowywania danych wdrożeniowych.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="7bcb3-141">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7bcb3-141">-Name</span></span>
<span data-ttu-id="7bcb3-142">Nazwa wdrożenia, które zostanie utworzyć.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-142">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="7bcb3-143">W przypadku, gdy plik szablonu jest podany, domyślnie jest określana jego nazwa domyślna. domyślnie jest to bieżąca godzina, gdy obiekt szablonu jest podany, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="7bcb3-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="7bcb3-144">— Przed</span><span class="sxs-lookup"><span data-stu-id="7bcb3-144">-Pre</span></span>
<span data-ttu-id="7bcb3-145">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7bcb3-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="7bcb3-146">-ResultFormat</span></span>
<span data-ttu-id="7bcb3-147">Format What-If wynik.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-147">The What-If result format.</span></span>

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

### <span data-ttu-id="7bcb3-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="7bcb3-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="7bcb3-149">Pomija dynamiczne przetwarzanie parametrów programu PowerShell, które sprawdza, czy podany parametr szablonu zawiera wszystkie niezbędne parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="7bcb3-150">To sprawdzenie spowoduje monitowanie użytkownika o podanie wartości dla brakujących parametrów, ale podanie parametru -SkipTemplateParameterPrompt spowoduje natychmiastowe zignorowanie tego monitu i błędu, jeśli znaleziono, że parametr nie jest powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="7bcb3-151">W przypadku skryptów nieinterakcyjnych można udostępnić komunikat -SkipTemplateParameterPrompt w celu zapewnienia lepszego komunikatu o błędzie w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="7bcb3-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="7bcb3-152">-TemplateFile</span></span>
<span data-ttu-id="7bcb3-153">Ścieżka lokalna do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-153">Local path to the template file.</span></span> <span data-ttu-id="7bcb3-154">Obsługiwany typ pliku szablonu: json i biceps.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-154">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="7bcb3-155">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="7bcb3-155">-TemplateObject</span></span>
<span data-ttu-id="7bcb3-156">Tabela skrótów reprezentująca szablon.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-156">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="7bcb3-157">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="7bcb3-157">-TemplateParameterFile</span></span>
<span data-ttu-id="7bcb3-158">Plik z parametrami szablonu.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-158">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="7bcb3-159">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="7bcb3-159">-TemplateParameterObject</span></span>
<span data-ttu-id="7bcb3-160">Tabela skrótów reprezentująca parametry.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-160">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="7bcb3-161">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="7bcb3-161">-TemplateParameterUri</span></span>
<span data-ttu-id="7bcb3-162">Uri do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-162">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="7bcb3-163">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="7bcb3-163">-TemplateUri</span></span>
<span data-ttu-id="7bcb3-164">Uri do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-164">Uri to the template file.</span></span>

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

### <span data-ttu-id="7bcb3-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bcb3-165">CommonParameters</span></span>
<span data-ttu-id="7bcb3-166">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bcb3-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bcb3-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bcb3-168">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7bcb3-168">INPUTS</span></span>

### <span data-ttu-id="7bcb3-169">System.String</span><span class="sxs-lookup"><span data-stu-id="7bcb3-169">System.String</span></span>

### <span data-ttu-id="7bcb3-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7bcb3-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7bcb3-171">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7bcb3-171">OUTPUTS</span></span>

### <span data-ttu-id="7bcb3-172">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="7bcb3-172">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="7bcb3-173">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7bcb3-173">NOTES</span></span>

## <span data-ttu-id="7bcb3-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7bcb3-174">RELATED LINKS</span></span>
