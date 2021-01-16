---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: 8135dc4c4bdb6eb21761dbf5cb7ecea216a81593
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353734"
---
# <span data-ttu-id="08566-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="08566-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="08566-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08566-102">SYNOPSIS</span></span>
<span data-ttu-id="08566-103">Tworzenie wdrożenia w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="08566-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="08566-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08566-104">SYNTAX</span></span>

### <span data-ttu-id="08566-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="08566-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08566-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="08566-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08566-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="08566-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08566-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="08566-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08566-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="08566-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08566-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="08566-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08566-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="08566-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08566-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="08566-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08566-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="08566-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08566-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="08566-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08566-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="08566-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08566-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="08566-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08566-117">Opis</span><span class="sxs-lookup"><span data-stu-id="08566-117">DESCRIPTION</span></span>
<span data-ttu-id="08566-118">Polecenie cmdlet **New-AzTenantDeployment** umożliwia dodanie wdrożenia w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="08566-118">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="08566-119">Aby dodać wdrożenie w zakresie dzierżawy, określ lokalizację i szablon.</span><span class="sxs-lookup"><span data-stu-id="08566-119">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="08566-120">Lokalizacja informuje Menedżera zasobów platformy Azure, gdzie mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="08566-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="08566-121">Szablon jest ciągiem JSON zawierającym poszczególne zasoby do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="08566-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="08566-122">Szablon zawiera symbole zastępcze parametru dla wymaganych zasobów i wartości właściwości konfigurowalnych, takich jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="08566-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="08566-123">Aby użyć szablonu niestandardowego do wdrożenia, określ parametr *TemplateFile* lub *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="08566-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="08566-124">Każdy szablon zawiera parametry konfigurowalnych właściwości.</span><span class="sxs-lookup"><span data-stu-id="08566-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="08566-125">Aby określić wartości parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="08566-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="08566-126">Możesz też użyć parametrów szablonu, które są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="08566-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="08566-127">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-), aby wskazać parametr, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="08566-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="08566-128">Wartości parametrów szablonu wprowadzone w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="08566-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="08566-129">Aby dodać zasoby do grupy zasobów, użyj **nowego-AzResourceGroupDeployment** , który tworzy wdrożenie w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="08566-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="08566-130">Aby dodać zasoby do subskrypcji, użyj **nowego-AzSubscriptionDeployment** , który tworzy wdrożenie w zakresie subskrypcji, co powoduje wdrożenie zasobów poziomu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="08566-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="08566-131">Aby dodać zasoby w grupie zarządzania, użyj **nowego-AzManagementGroupDeployment** , który tworzy wdrożenie w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="08566-131">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="08566-132">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08566-132">EXAMPLES</span></span>

### <span data-ttu-id="08566-133">Przykład 1: korzystanie z szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="08566-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="08566-134">To polecenie tworzy nowe wdrożenie w bieżącym zakresie dzierżawy przy użyciu szablonu niestandardowego i pliku szablonu na dysku z parametrem defined Tags.</span><span class="sxs-lookup"><span data-stu-id="08566-134">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="08566-135">W poleceniu użyto parametru *TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="08566-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="08566-136">Przykład 2: Używanie obiektu szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="08566-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="08566-137">To polecenie tworzy nowe wdrożenie w bieżącej dzierżawie przy użyciu szablonu niestandardowego i pliku szablonu na dysku, który został przekonwertowany na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="08566-137">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="08566-138">Pierwsze dwa polecenia czytają tekst pliku szablonu na dysku i konwertują go na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="08566-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="08566-139">W ostatnim poleceniu użyto parametru *templateobject* w celu określenia tej obiektu Hashtable i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="08566-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="08566-140">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08566-140">PARAMETERS</span></span>

### <span data-ttu-id="08566-141">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08566-141">-AsJob</span></span>
<span data-ttu-id="08566-142">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="08566-142">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08566-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08566-143">-DefaultProfile</span></span>
<span data-ttu-id="08566-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08566-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08566-145">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="08566-145">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="08566-146">Poziom dziennika debugowania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="08566-146">The deployment debug log level.</span></span>

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

### <span data-ttu-id="08566-147">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="08566-147">-Location</span></span>
<span data-ttu-id="08566-148">Lokalizacja przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="08566-148">The location to store deployment data.</span></span>

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

### <span data-ttu-id="08566-149">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="08566-149">-Name</span></span>
<span data-ttu-id="08566-150">Nazwa wdrożenia, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="08566-150">The name of the deployment it's going to create.</span></span> <span data-ttu-id="08566-151">Jeśli ten parametr nie jest określony, domyślnie jest określana nazwa pliku szablonu, gdy jest dostarczany plik szablonu; Domyślnie jest to bieżąca godzina, w której jest dostarczany obiekt szablonu, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="08566-151">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="08566-152">-Pre</span><span class="sxs-lookup"><span data-stu-id="08566-152">-Pre</span></span>
<span data-ttu-id="08566-153">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="08566-153">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="08566-154">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="08566-154">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="08566-155">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="08566-155">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="08566-156">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="08566-156">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="08566-157">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="08566-157">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="08566-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="08566-158">-Tag</span></span>
<span data-ttu-id="08566-159">Tagi, które mają zostać wprowadzone do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="08566-159">The tags to put on the deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08566-160">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="08566-160">-TemplateFile</span></span>
<span data-ttu-id="08566-161">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="08566-161">Local path to the template file.</span></span>

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

### <span data-ttu-id="08566-162">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="08566-162">-TemplateObject</span></span>
<span data-ttu-id="08566-163">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="08566-163">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="08566-164">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="08566-164">-TemplateParameterFile</span></span>
<span data-ttu-id="08566-165">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="08566-165">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="08566-166">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="08566-166">-TemplateParameterObject</span></span>
<span data-ttu-id="08566-167">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="08566-167">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="08566-168">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="08566-168">-TemplateParameterUri</span></span>
<span data-ttu-id="08566-169">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="08566-169">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="08566-170">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="08566-170">-TemplateUri</span></span>
<span data-ttu-id="08566-171">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="08566-171">Uri to the template file.</span></span>

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

### <span data-ttu-id="08566-172">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="08566-172">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="08566-173">Typy zmian zasobów rozdzielanych przecinkami, które mają być wykluczone z wyników What-If.</span><span class="sxs-lookup"><span data-stu-id="08566-173">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="08566-174">Obowiązuje po ustawieniu przełącznika-WhatIf lub-Confirm.</span><span class="sxs-lookup"><span data-stu-id="08566-174">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="08566-175">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="08566-175">-WhatIfResultFormat</span></span>
<span data-ttu-id="08566-176">What-If format wyników.</span><span class="sxs-lookup"><span data-stu-id="08566-176">The What-If result format.</span></span> <span data-ttu-id="08566-177">Obowiązuje po ustawieniu przełącznika-WhatIf lub-Confirm.</span><span class="sxs-lookup"><span data-stu-id="08566-177">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="08566-178">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08566-178">-Confirm</span></span>
<span data-ttu-id="08566-179">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08566-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08566-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08566-180">-WhatIf</span></span>
<span data-ttu-id="08566-181">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08566-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08566-182">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08566-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08566-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08566-183">CommonParameters</span></span>
<span data-ttu-id="08566-184">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08566-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08566-185">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08566-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08566-186">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08566-186">INPUTS</span></span>

### <span data-ttu-id="08566-187">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="08566-187">System.Collections.Hashtable</span></span>

### <span data-ttu-id="08566-188">System. String</span><span class="sxs-lookup"><span data-stu-id="08566-188">System.String</span></span>

## <span data-ttu-id="08566-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08566-189">OUTPUTS</span></span>

### <span data-ttu-id="08566-190">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="08566-190">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="08566-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08566-191">NOTES</span></span>

## <span data-ttu-id="08566-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08566-192">RELATED LINKS</span></span>
