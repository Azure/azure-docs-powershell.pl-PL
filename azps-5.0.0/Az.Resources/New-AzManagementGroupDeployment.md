---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: a04c19df84626fd08968e1950074306dfd7cf1ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307962"
---
# <span data-ttu-id="b482c-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b482c-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="b482c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b482c-102">SYNOPSIS</span></span>
<span data-ttu-id="b482c-103">Tworzenie wdrożenia w grupie zarządzania</span><span class="sxs-lookup"><span data-stu-id="b482c-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="b482c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b482c-104">SYNTAX</span></span>

### <span data-ttu-id="b482c-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b482c-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b482c-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b482c-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b482c-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b482c-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b482c-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b482c-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b482c-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b482c-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b482c-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b482c-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b482c-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b482c-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b482c-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b482c-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b482c-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b482c-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b482c-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b482c-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b482c-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b482c-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b482c-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b482c-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b482c-117">Opis</span><span class="sxs-lookup"><span data-stu-id="b482c-117">DESCRIPTION</span></span>
<span data-ttu-id="b482c-118">Polecenie cmdlet **New-AzManagementGroupDeployment** umożliwia dodanie wdrożenia w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="b482c-118">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="b482c-119">Aby dodać wdrożenie w grupie zarządzania, określ grupę zarządzania, lokalizację i szablon.</span><span class="sxs-lookup"><span data-stu-id="b482c-119">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="b482c-120">Lokalizacja informuje Menedżera zasobów platformy Azure, gdzie mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b482c-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="b482c-121">Szablon jest ciągiem JSON zawierającym poszczególne zasoby do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b482c-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="b482c-122">Szablon zawiera symbole zastępcze parametru dla wymaganych zasobów i wartości właściwości konfigurowalnych, takich jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="b482c-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="b482c-123">Aby użyć szablonu niestandardowego do wdrożenia, określ parametr *TemplateFile* lub *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="b482c-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="b482c-124">Każdy szablon zawiera parametry konfigurowalnych właściwości.</span><span class="sxs-lookup"><span data-stu-id="b482c-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="b482c-125">Aby określić wartości parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="b482c-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="b482c-126">Możesz też użyć parametrów szablonu, które są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="b482c-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="b482c-127">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-), aby wskazać parametr, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="b482c-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="b482c-128">Wartości parametrów szablonu wprowadzone w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="b482c-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="b482c-129">Aby dodać zasoby do grupy zasobów, użyj **nowego-AzResourceGroupDeployment** , który tworzy wdrożenie w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b482c-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="b482c-130">Aby dodać zasoby do subskrypcji, użyj **nowego-AzSubscriptionDeployment** , który tworzy wdrożenie w zakresie subskrypcji, co powoduje wdrożenie zasobów poziomu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b482c-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="b482c-131">Aby dodać zasoby w zakresie dzierżawy, użyj **nowego-AzTenantDeployment** , który tworzy wdrożenie w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="b482c-131">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="b482c-132">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b482c-132">EXAMPLES</span></span>

### <span data-ttu-id="b482c-133">Przykład 1: korzystanie z szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="b482c-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="b482c-134">To polecenie tworzy nowe wdrożenie w grupie zarządzania "myMG" przy użyciu szablonu niestandardowego i pliku szablonu na dysku z parametrem defined Tags.</span><span class="sxs-lookup"><span data-stu-id="b482c-134">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="b482c-135">W poleceniu użyto parametru *TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="b482c-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="b482c-136">Przykład 2: Używanie obiektu szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="b482c-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="b482c-137">To polecenie tworzy nowe wdrożenie w grupie zarządzania "myMG" przy użyciu szablonu niestandardowego i pliku szablonu na dysku, który został przekonwertowany na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="b482c-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="b482c-138">Pierwsze dwa polecenia czytają tekst pliku szablonu na dysku i konwertują go na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="b482c-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="b482c-139">W ostatnim poleceniu użyto parametru *templateobject* w celu określenia tej obiektu Hashtable i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="b482c-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="b482c-140">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b482c-140">PARAMETERS</span></span>

### <span data-ttu-id="b482c-141">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b482c-141">-AsJob</span></span>
<span data-ttu-id="b482c-142">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b482c-142">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b482c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b482c-143">-DefaultProfile</span></span>
<span data-ttu-id="b482c-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b482c-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b482c-145">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="b482c-145">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="b482c-146">Poziom dziennika debugowania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b482c-146">The deployment debug log level.</span></span>

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

### <span data-ttu-id="b482c-147">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b482c-147">-Location</span></span>
<span data-ttu-id="b482c-148">Lokalizacja przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b482c-148">The location to store deployment data.</span></span>

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

### <span data-ttu-id="b482c-149">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b482c-149">-ManagementGroupId</span></span>
<span data-ttu-id="b482c-150">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="b482c-150">The management group ID.</span></span>

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

### <span data-ttu-id="b482c-151">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b482c-151">-Name</span></span>
<span data-ttu-id="b482c-152">Nazwa wdrożenia, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="b482c-152">The name of the deployment it's going to create.</span></span> <span data-ttu-id="b482c-153">Jeśli ten parametr nie jest określony, domyślnie jest określana nazwa pliku szablonu, gdy jest dostarczany plik szablonu; Domyślnie jest to bieżąca godzina, w której jest dostarczany obiekt szablonu, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="b482c-153">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="b482c-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="b482c-154">-Pre</span></span>
<span data-ttu-id="b482c-155">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="b482c-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b482c-156">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="b482c-156">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="b482c-157">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="b482c-157">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="b482c-158">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="b482c-158">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="b482c-159">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="b482c-159">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="b482c-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="b482c-160">-Tag</span></span>
<span data-ttu-id="b482c-161">Tagi, które mają zostać wprowadzone do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b482c-161">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="b482c-162">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b482c-162">-TemplateFile</span></span>
<span data-ttu-id="b482c-163">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="b482c-163">Local path to the template file.</span></span>

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

### <span data-ttu-id="b482c-164">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="b482c-164">-TemplateObject</span></span>
<span data-ttu-id="b482c-165">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="b482c-165">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="b482c-166">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b482c-166">-TemplateParameterFile</span></span>
<span data-ttu-id="b482c-167">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="b482c-167">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="b482c-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b482c-168">-TemplateParameterObject</span></span>
<span data-ttu-id="b482c-169">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="b482c-169">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="b482c-170">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b482c-170">-TemplateParameterUri</span></span>
<span data-ttu-id="b482c-171">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="b482c-171">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="b482c-172">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b482c-172">-TemplateUri</span></span>
<span data-ttu-id="b482c-173">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="b482c-173">Uri to the template file.</span></span>

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

### <span data-ttu-id="b482c-174">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="b482c-174">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="b482c-175">Typy zmian zasobów rozdzielanych przecinkami, które mają być wykluczone z wyników What-If.</span><span class="sxs-lookup"><span data-stu-id="b482c-175">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="b482c-176">Obowiązuje po ustawieniu przełącznika-WhatIf lub-Confirm.</span><span class="sxs-lookup"><span data-stu-id="b482c-176">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="b482c-177">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="b482c-177">-WhatIfResultFormat</span></span>
<span data-ttu-id="b482c-178">What-If format wyników.</span><span class="sxs-lookup"><span data-stu-id="b482c-178">The What-If result format.</span></span> <span data-ttu-id="b482c-179">Obowiązuje po ustawieniu przełącznika-WhatIf lub-Confirm.</span><span class="sxs-lookup"><span data-stu-id="b482c-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="b482c-180">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b482c-180">-Confirm</span></span>
<span data-ttu-id="b482c-181">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b482c-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b482c-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b482c-182">-WhatIf</span></span>
<span data-ttu-id="b482c-183">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b482c-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b482c-184">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b482c-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b482c-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b482c-185">CommonParameters</span></span>
<span data-ttu-id="b482c-186">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b482c-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b482c-187">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b482c-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b482c-188">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b482c-188">INPUTS</span></span>

### <span data-ttu-id="b482c-189">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b482c-189">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b482c-190">System. String</span><span class="sxs-lookup"><span data-stu-id="b482c-190">System.String</span></span>

## <span data-ttu-id="b482c-191">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b482c-191">OUTPUTS</span></span>

### <span data-ttu-id="b482c-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="b482c-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b482c-193">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b482c-193">NOTES</span></span>

## <span data-ttu-id="b482c-194">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b482c-194">RELATED LINKS</span></span>
