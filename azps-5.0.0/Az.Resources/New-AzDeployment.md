---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: ad5979d65565107ac071bcaac94bc178b8c36d1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224859"
---
# <span data-ttu-id="2511d-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="2511d-101">New-AzDeployment</span></span>

## <span data-ttu-id="2511d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2511d-102">SYNOPSIS</span></span>
<span data-ttu-id="2511d-103">Tworzenie wdrożenia</span><span class="sxs-lookup"><span data-stu-id="2511d-103">Create a deployment</span></span>

## <span data-ttu-id="2511d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2511d-104">SYNTAX</span></span>

### <span data-ttu-id="2511d-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2511d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2511d-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2511d-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2511d-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2511d-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2511d-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2511d-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2511d-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2511d-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2511d-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2511d-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2511d-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2511d-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2511d-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2511d-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2511d-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2511d-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2511d-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2511d-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2511d-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2511d-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2511d-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2511d-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2511d-117">Opis</span><span class="sxs-lookup"><span data-stu-id="2511d-117">DESCRIPTION</span></span>
<span data-ttu-id="2511d-118">Polecenie cmdlet **New-AzDeployment** umożliwia dodanie wdrożenia w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2511d-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="2511d-119">Dotyczy to zasobów, których wdrożenie wymaga.</span><span class="sxs-lookup"><span data-stu-id="2511d-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="2511d-120">Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure.</span><span class="sxs-lookup"><span data-stu-id="2511d-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="2511d-121">Zasób może być aktywny w grupie zasobów, takiej jak serwer bazy danych, baza danych, witryna sieci Web, maszyna wirtualna lub konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="2511d-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="2511d-122">Może to też być zasób poziomu abonamentu, na przykład definicja roli, definicja zasad itd.</span><span class="sxs-lookup"><span data-stu-id="2511d-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="2511d-123">Aby dodać zasoby do grupy zasobów, użyj **nowego-AzResourceGroupDeployment** , który tworzy wdrożenie w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="2511d-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="2511d-124">Polecenie cmdlet **New-AzDeployment** tworzy wdrożenie w bieżącym zakresie subskrypcji, co powoduje wdrożenie zasobów poziomu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2511d-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="2511d-125">Aby dodać wdrożenie w subskrypcji, określ lokalizację i szablon.</span><span class="sxs-lookup"><span data-stu-id="2511d-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="2511d-126">Lokalizacja informuje Menedżera zasobów platformy Azure, gdzie mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="2511d-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="2511d-127">Szablon jest ciągiem JSON zawierającym poszczególne zasoby do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="2511d-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="2511d-128">Szablon zawiera symbole zastępcze parametru dla wymaganych zasobów i wartości właściwości konfigurowalnych, takich jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="2511d-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="2511d-129">Aby użyć szablonu niestandardowego do wdrożenia, określ parametr *TemplateFile* lub *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="2511d-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="2511d-130">Każdy szablon zawiera parametry konfigurowalnych właściwości.</span><span class="sxs-lookup"><span data-stu-id="2511d-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="2511d-131">Aby określić wartości parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="2511d-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="2511d-132">Możesz też użyć parametrów szablonu, które są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="2511d-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="2511d-133">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-), aby wskazać parametr, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="2511d-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="2511d-134">Wartości parametrów szablonu wprowadzone w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="2511d-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="2511d-135">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2511d-135">EXAMPLES</span></span>

### <span data-ttu-id="2511d-136">Przykład 1: korzystanie z szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="2511d-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="2511d-137">To polecenie tworzy nowe wdrożenie w bieżącym zakresie subskrypcji przy użyciu szablonu niestandardowego i pliku szablonu na dysku z parametrem defined Tags.</span><span class="sxs-lookup"><span data-stu-id="2511d-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="2511d-138">W poleceniu użyto parametru *TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="2511d-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="2511d-139">Używa parametru *TemplateVersion* w celu określenia wersji szablonu.</span><span class="sxs-lookup"><span data-stu-id="2511d-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="2511d-140">Przykład 2: Używanie obiektu szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="2511d-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="2511d-141">To polecenie tworzy nowe wdrożenie w bieżącym zakresie subskrypcji przy użyciu szablonu niestandardowego i pliku szablonu na dysku, który został przekonwertowany na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="2511d-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="2511d-142">Pierwsze dwa polecenia czytają tekst pliku szablonu na dysku i konwertują go na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="2511d-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="2511d-143">W ostatnim poleceniu użyto parametru *templateobject* w celu określenia tej obiektu Hashtable i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="2511d-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="2511d-144">Używa parametru *TemplateVersion* w celu określenia wersji szablonu.</span><span class="sxs-lookup"><span data-stu-id="2511d-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="2511d-145">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2511d-145">PARAMETERS</span></span>

### <span data-ttu-id="2511d-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2511d-146">-AsJob</span></span>
<span data-ttu-id="2511d-147">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2511d-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2511d-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2511d-148">-DefaultProfile</span></span>
<span data-ttu-id="2511d-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2511d-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2511d-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="2511d-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="2511d-151">Poziom dziennika debugowania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="2511d-151">The deployment debug log level.</span></span>

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

### <span data-ttu-id="2511d-152">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2511d-152">-Location</span></span>
<span data-ttu-id="2511d-153">Lokalizacja przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="2511d-153">The location to store deployment data.</span></span>

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

### <span data-ttu-id="2511d-154">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2511d-154">-Name</span></span>
<span data-ttu-id="2511d-155">Nazwa wdrożenia, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="2511d-155">The name of the deployment it's going to create.</span></span> <span data-ttu-id="2511d-156">Jeśli ten parametr nie jest określony, domyślnie jest określana nazwa pliku szablonu, gdy jest dostarczany plik szablonu; Domyślnie jest to bieżąca godzina, w której jest dostarczany obiekt szablonu, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="2511d-156">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="2511d-157">-Pre</span><span class="sxs-lookup"><span data-stu-id="2511d-157">-Pre</span></span>
<span data-ttu-id="2511d-158">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="2511d-158">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2511d-159">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="2511d-159">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="2511d-160">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="2511d-160">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="2511d-161">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="2511d-161">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="2511d-162">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="2511d-162">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="2511d-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="2511d-163">-Tag</span></span>
<span data-ttu-id="2511d-164">Tagi, które mają zostać wprowadzone do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="2511d-164">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="2511d-165">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2511d-165">-TemplateFile</span></span>
<span data-ttu-id="2511d-166">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="2511d-166">Local path to the template file.</span></span>

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

### <span data-ttu-id="2511d-167">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="2511d-167">-TemplateObject</span></span>
<span data-ttu-id="2511d-168">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="2511d-168">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="2511d-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2511d-169">-TemplateParameterFile</span></span>
<span data-ttu-id="2511d-170">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="2511d-170">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="2511d-171">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2511d-171">-TemplateParameterObject</span></span>
<span data-ttu-id="2511d-172">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="2511d-172">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="2511d-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2511d-173">-TemplateParameterUri</span></span>
<span data-ttu-id="2511d-174">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="2511d-174">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="2511d-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2511d-175">-TemplateUri</span></span>
<span data-ttu-id="2511d-176">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="2511d-176">Uri to the template file.</span></span>

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

### <span data-ttu-id="2511d-177">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="2511d-177">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="2511d-178">Typy zmian zasobów rozdzielanych przecinkami, które mają być wykluczone z wyników What-If.</span><span class="sxs-lookup"><span data-stu-id="2511d-178">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="2511d-179">Obowiązuje po ustawieniu przełącznika-WhatIf lub-Confirm.</span><span class="sxs-lookup"><span data-stu-id="2511d-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="2511d-180">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="2511d-180">-WhatIfResultFormat</span></span>
<span data-ttu-id="2511d-181">What-If format wyników.</span><span class="sxs-lookup"><span data-stu-id="2511d-181">The What-If result format.</span></span>

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

### <span data-ttu-id="2511d-182">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2511d-182">-Confirm</span></span>
<span data-ttu-id="2511d-183">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2511d-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2511d-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2511d-184">-WhatIf</span></span>
<span data-ttu-id="2511d-185">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2511d-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2511d-186">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2511d-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2511d-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2511d-187">CommonParameters</span></span>
<span data-ttu-id="2511d-188">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2511d-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2511d-189">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2511d-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2511d-190">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2511d-190">INPUTS</span></span>

### <span data-ttu-id="2511d-191">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2511d-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2511d-192">System. String</span><span class="sxs-lookup"><span data-stu-id="2511d-192">System.String</span></span>

## <span data-ttu-id="2511d-193">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2511d-193">OUTPUTS</span></span>

### <span data-ttu-id="2511d-194">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="2511d-194">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="2511d-195">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2511d-195">NOTES</span></span>

## <span data-ttu-id="2511d-196">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2511d-196">RELATED LINKS</span></span>
