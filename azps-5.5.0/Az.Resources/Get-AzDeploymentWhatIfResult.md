---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 0ad3df8e010beec777bd059bbef708774570792d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240091"
---
# <span data-ttu-id="b0b46-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="b0b46-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="b0b46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b46-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b46-103">Pobiera ARM szablonu What-If dla wdrożenia w zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b0b46-103">Gets an ARM template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="b0b46-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b0b46-104">SYNTAX</span></span>

### <span data-ttu-id="b0b46-105">ByTemplateFileWithNoParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b0b46-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b46-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b0b46-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b46-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b0b46-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b46-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b0b46-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b46-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b0b46-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b46-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b0b46-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b46-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b0b46-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b46-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b0b46-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b46-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b0b46-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b46-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b0b46-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b46-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b0b46-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0b46-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b0b46-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0b46-117">OPIS</span><span class="sxs-lookup"><span data-stu-id="b0b46-117">DESCRIPTION</span></span>
<span data-ttu-id="b0b46-118">Polecenie **cmdlet Get-AzDeploymentWhatIfResult** pobiera ARM szablonu What-If dla wdrożenia szablonów w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b0b46-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="b0b46-119">Zwraca ona listę zmian wskazujących, które zasoby zostaną zaktualizowane, jeśli wdrożenie zostanie zastosowane bez dokonywania zmian w zasobach rzeczywistych.</span><span class="sxs-lookup"><span data-stu-id="b0b46-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="b0b46-120">Aby określić format zwracanych wyników, użyj *parametru ResultFormat.*</span><span class="sxs-lookup"><span data-stu-id="b0b46-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="b0b46-121">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b0b46-121">EXAMPLES</span></span>

### <span data-ttu-id="b0b46-122">Przykład 1. Uzyskiwanie What-If w zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b0b46-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="b0b46-123">To polecenie uzyskuje What-If w zakresie bieżącej subskrypcji przy użyciu pliku szablonu niestandardowego i pliku parametru na dysku.</span><span class="sxs-lookup"><span data-stu-id="b0b46-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="b0b46-124">To polecenie używa *parametru Location* w celu określenia miejsca przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b0b46-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="b0b46-125">To polecenie określa plik szablonu za pomocą parametru *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="b0b46-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="b0b46-126">To polecenie używa *parametru TemplateParameterFile* do określenia pliku parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="b0b46-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="b0b46-127">To polecenie używa *parametru ResultFormat* w celu What-If wyniku tak, aby uwzględniał pełne obciążenia zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0b46-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="b0b46-128">Przykład 2. Uzyskiwanie What-If w zakresie subskrypcji z resourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="b0b46-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="b0b46-129">To polecenie uzyskuje What-If w zakresie bieżącej subskrypcji przy użyciu pliku szablonu niestandardowego i pliku parametru na dysku.</span><span class="sxs-lookup"><span data-stu-id="b0b46-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="b0b46-130">To polecenie używa *parametru Location* w celu określenia miejsca przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b0b46-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="b0b46-131">To polecenie określa plik szablonu za pomocą parametru *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="b0b46-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="b0b46-132">To polecenie używa *parametru TemplateParameterFile* do określenia pliku parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="b0b46-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="b0b46-133">To polecenie używa *parametru ResultFormat* w celu What-If wyniku tak, aby zawierał tylko identyfikatory zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0b46-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="b0b46-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0b46-134">PARAMETERS</span></span>

### <span data-ttu-id="b0b46-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b46-135">-DefaultProfile</span></span>
<span data-ttu-id="b0b46-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0b46-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0b46-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="b0b46-137">-ExcludeChangeType</span></span>
<span data-ttu-id="b0b46-138">Rozdzielona przecinkami lista typów zmian zasobów do wykluczenia z What-If wyników.</span><span class="sxs-lookup"><span data-stu-id="b0b46-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="b0b46-139">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b0b46-139">-Location</span></span>
<span data-ttu-id="b0b46-140">Lokalizacja przechowywania danych wdrożeniowych.</span><span class="sxs-lookup"><span data-stu-id="b0b46-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="b0b46-141">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b0b46-141">-Name</span></span>
<span data-ttu-id="b0b46-142">Nazwa wdrożenia, które zostanie utworzyć.</span><span class="sxs-lookup"><span data-stu-id="b0b46-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="b0b46-143">W przypadku, gdy plik szablonu jest podany, domyślnie jest określana jego nazwa domyślna. domyślnie jest to bieżąca godzina, gdy obiekt szablonu jest podany, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="b0b46-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="b0b46-144">— Przed</span><span class="sxs-lookup"><span data-stu-id="b0b46-144">-Pre</span></span>
<span data-ttu-id="b0b46-145">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b0b46-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b0b46-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="b0b46-146">-ResultFormat</span></span>
<span data-ttu-id="b0b46-147">Format What-If wynik.</span><span class="sxs-lookup"><span data-stu-id="b0b46-147">The What-If result format.</span></span>

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

### <span data-ttu-id="b0b46-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="b0b46-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="b0b46-149">Pomija dynamiczne przetwarzanie parametrów programu PowerShell, które sprawdza, czy podany parametr szablonu zawiera wszystkie niezbędne parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="b0b46-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="b0b46-150">To sprawdzenie spowoduje monitowanie użytkownika o podanie wartości dla brakujących parametrów, ale podanie parametru -SkipTemplateParameterPrompt spowoduje natychmiastowe zignorowanie tego monitu i błędu, jeśli znaleziono, że parametr nie jest powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="b0b46-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="b0b46-151">W przypadku skryptów nieinterakcyjnych można udostępnić komunikat "SkipTemplateParameterPrompt" w celu zapewnienia lepszego komunikatu o błędzie w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="b0b46-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="b0b46-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b0b46-152">-TemplateFile</span></span>
<span data-ttu-id="b0b46-153">Ścieżka lokalna do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="b0b46-153">Local path to the template file.</span></span>

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

### <span data-ttu-id="b0b46-154">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="b0b46-154">-TemplateObject</span></span>
<span data-ttu-id="b0b46-155">Tabela skrótów reprezentująca szablon.</span><span class="sxs-lookup"><span data-stu-id="b0b46-155">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="b0b46-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b0b46-156">-TemplateParameterFile</span></span>
<span data-ttu-id="b0b46-157">Plik z parametrami szablonu.</span><span class="sxs-lookup"><span data-stu-id="b0b46-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="b0b46-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b0b46-158">-TemplateParameterObject</span></span>
<span data-ttu-id="b0b46-159">Tabela skrótów reprezentująca parametry.</span><span class="sxs-lookup"><span data-stu-id="b0b46-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="b0b46-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b0b46-160">-TemplateParameterUri</span></span>
<span data-ttu-id="b0b46-161">Uri do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="b0b46-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="b0b46-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b0b46-162">-TemplateUri</span></span>
<span data-ttu-id="b0b46-163">Uri do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="b0b46-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="b0b46-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b46-164">CommonParameters</span></span>
<span data-ttu-id="b0b46-165">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b46-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b46-166">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0b46-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b46-167">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0b46-167">INPUTS</span></span>

### <span data-ttu-id="b0b46-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b0b46-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b0b46-169">System.String</span><span class="sxs-lookup"><span data-stu-id="b0b46-169">System.String</span></span>

## <span data-ttu-id="b0b46-170">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0b46-170">OUTPUTS</span></span>

### <span data-ttu-id="b0b46-171">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="b0b46-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="b0b46-172">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b0b46-172">NOTES</span></span>

## <span data-ttu-id="b0b46-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0b46-173">RELATED LINKS</span></span>
