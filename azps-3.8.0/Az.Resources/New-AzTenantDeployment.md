---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: 38f46b8805b8e259b086e5c5a78e929112dca83a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895026"
---
# <span data-ttu-id="94df3-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="94df3-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="94df3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94df3-102">SYNOPSIS</span></span>
<span data-ttu-id="94df3-103">Tworzenie wdrożenia w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="94df3-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="94df3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94df3-104">SYNTAX</span></span>

### <span data-ttu-id="94df3-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="94df3-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94df3-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="94df3-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94df3-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="94df3-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94df3-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="94df3-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94df3-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="94df3-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94df3-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="94df3-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94df3-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="94df3-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94df3-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="94df3-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94df3-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="94df3-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94df3-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="94df3-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94df3-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="94df3-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94df3-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="94df3-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94df3-117">Opis</span><span class="sxs-lookup"><span data-stu-id="94df3-117">DESCRIPTION</span></span>
<span data-ttu-id="94df3-118">Polecenie cmdlet **New-AzTenantDeployment** umożliwia dodanie wdrożenia w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="94df3-118">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="94df3-119">Aby dodać wdrożenie w zakresie dzierżawy, określ lokalizację i szablon.</span><span class="sxs-lookup"><span data-stu-id="94df3-119">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="94df3-120">Lokalizacja informuje Menedżera zasobów platformy Azure, gdzie mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="94df3-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="94df3-121">Szablon jest ciągiem JSON zawierającym poszczególne zasoby do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="94df3-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="94df3-122">Szablon zawiera symbole zastępcze parametru dla wymaganych zasobów i wartości właściwości konfigurowalnych, takich jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="94df3-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="94df3-123">Aby użyć szablonu niestandardowego do wdrożenia, określ parametr *TemplateFile* lub *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="94df3-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="94df3-124">Każdy szablon zawiera parametry konfigurowalnych właściwości.</span><span class="sxs-lookup"><span data-stu-id="94df3-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="94df3-125">Aby określić wartości parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="94df3-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="94df3-126">Możesz też użyć parametrów szablonu, które są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="94df3-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="94df3-127">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-), aby wskazać parametr, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="94df3-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="94df3-128">Wartości parametrów szablonu wprowadzone w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="94df3-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="94df3-129">Aby dodać zasoby do grupy zasobów, użyj **nowego-AzResourceGroupDeployment** , który tworzy wdrożenie w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="94df3-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="94df3-130">Aby dodać zasoby do subskrypcji, użyj **nowego-AzSubscriptionDeployment** , który tworzy wdrożenie w zakresie subskrypcji, co powoduje wdrożenie zasobów poziomu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="94df3-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="94df3-131">Aby dodać zasoby w grupie zarządzania, użyj **nowego-AzManagementGroupDeployment** , który tworzy wdrożenie w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="94df3-131">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="94df3-132">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94df3-132">EXAMPLES</span></span>

### <span data-ttu-id="94df3-133">Przykład 1: korzystanie z szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="94df3-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="94df3-134">To polecenie tworzy nowe wdrożenie w bieżącym zakresie dzierżawy przy użyciu szablonu niestandardowego i pliku szablonu na dysku.</span><span class="sxs-lookup"><span data-stu-id="94df3-134">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="94df3-135">W poleceniu użyto parametru *TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="94df3-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="94df3-136">Przykład 2: Używanie obiektu szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="94df3-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="94df3-137">To polecenie tworzy nowe wdrożenie w bieżącej dzierżawie przy użyciu szablonu niestandardowego i pliku szablonu na dysku, który został przekonwertowany na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="94df3-137">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="94df3-138">Pierwsze dwa polecenia czytają tekst pliku szablonu na dysku i konwertują go na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="94df3-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="94df3-139">W ostatnim poleceniu użyto parametru *templateobject* w celu określenia tej obiektu Hashtable i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="94df3-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="94df3-140">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94df3-140">PARAMETERS</span></span>

### <span data-ttu-id="94df3-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="94df3-141">-ApiVersion</span></span>
<span data-ttu-id="94df3-142">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="94df3-142">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="94df3-143">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="94df3-143">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94df3-144">-AsJob</span></span>
<span data-ttu-id="94df3-145">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="94df3-145">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94df3-146">-DefaultProfile</span></span>
<span data-ttu-id="94df3-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94df3-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="94df3-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="94df3-149">Poziom dziennika debugowania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="94df3-149">The deployment debug log level.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-150">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="94df3-150">-Location</span></span>
<span data-ttu-id="94df3-151">Lokalizacja przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="94df3-151">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-152">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="94df3-152">-Name</span></span>
<span data-ttu-id="94df3-153">Nazwa wdrożenia, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="94df3-153">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="94df3-154">Ważne tylko w przypadku używania szablonu.</span><span class="sxs-lookup"><span data-stu-id="94df3-154">Only valid when a template is used.</span></span>
<span data-ttu-id="94df3-155">Jeśli jest używany szablon, jeśli użytkownik nie określi nazwy wdrożenia, Użyj bieżącej godziny, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="94df3-155">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="94df3-156">-Pre</span></span>
<span data-ttu-id="94df3-157">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="94df3-157">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-158">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="94df3-158">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="94df3-159">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="94df3-159">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="94df3-160">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="94df3-160">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="94df3-161">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="94df3-161">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-162">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="94df3-162">-TemplateFile</span></span>
<span data-ttu-id="94df3-163">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="94df3-163">Local path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-164">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="94df3-164">-TemplateObject</span></span>
<span data-ttu-id="94df3-165">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="94df3-165">A hash table which represents the template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-166">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="94df3-166">-TemplateParameterFile</span></span>
<span data-ttu-id="94df3-167">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="94df3-167">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="94df3-168">-TemplateParameterObject</span></span>
<span data-ttu-id="94df3-169">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="94df3-169">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-170">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="94df3-170">-TemplateParameterUri</span></span>
<span data-ttu-id="94df3-171">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="94df3-171">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-172">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="94df3-172">-TemplateUri</span></span>
<span data-ttu-id="94df3-173">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="94df3-173">Uri to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-174">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94df3-174">-Confirm</span></span>
<span data-ttu-id="94df3-175">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94df3-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94df3-176">-WhatIf</span></span>
<span data-ttu-id="94df3-177">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94df3-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94df3-178">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="94df3-178">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df3-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94df3-179">CommonParameters</span></span>
<span data-ttu-id="94df3-180">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94df3-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94df3-181">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94df3-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94df3-182">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94df3-182">INPUTS</span></span>

### <span data-ttu-id="94df3-183">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="94df3-183">System.Collections.Hashtable</span></span>

### <span data-ttu-id="94df3-184">System. String</span><span class="sxs-lookup"><span data-stu-id="94df3-184">System.String</span></span>

## <span data-ttu-id="94df3-185">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94df3-185">OUTPUTS</span></span>

### <span data-ttu-id="94df3-186">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="94df3-186">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="94df3-187">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94df3-187">NOTES</span></span>

## <span data-ttu-id="94df3-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94df3-188">RELATED LINKS</span></span>
