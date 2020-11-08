---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 2cd572266656cf194e1d0ff73770f2d2e617009d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053423"
---
# <span data-ttu-id="22eb1-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="22eb1-101">New-AzDeployment</span></span>

## <span data-ttu-id="22eb1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="22eb1-103">Tworzenie wdrożenia</span><span class="sxs-lookup"><span data-stu-id="22eb1-103">Create a deployment</span></span>

## <span data-ttu-id="22eb1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22eb1-104">SYNTAX</span></span>

### <span data-ttu-id="22eb1-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="22eb1-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22eb1-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="22eb1-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22eb1-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="22eb1-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22eb1-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="22eb1-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22eb1-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="22eb1-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22eb1-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="22eb1-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22eb1-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="22eb1-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22eb1-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="22eb1-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22eb1-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="22eb1-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22eb1-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="22eb1-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22eb1-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="22eb1-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22eb1-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="22eb1-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22eb1-117">Opis</span><span class="sxs-lookup"><span data-stu-id="22eb1-117">DESCRIPTION</span></span>
<span data-ttu-id="22eb1-118">Polecenie cmdlet **New-AzDeployment** umożliwia dodanie wdrożenia w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="22eb1-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="22eb1-119">Dotyczy to zasobów, których wdrożenie wymaga.</span><span class="sxs-lookup"><span data-stu-id="22eb1-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="22eb1-120">Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure.</span><span class="sxs-lookup"><span data-stu-id="22eb1-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="22eb1-121">Zasób może być aktywny w grupie zasobów, takiej jak serwer bazy danych, baza danych, witryna sieci Web, maszyna wirtualna lub konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="22eb1-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="22eb1-122">Może to też być zasób poziomu abonamentu, na przykład definicja roli, definicja zasad itd.</span><span class="sxs-lookup"><span data-stu-id="22eb1-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="22eb1-123">Aby dodać zasoby do grupy zasobów, użyj **nowego-AzResourceGroupDeployment** , który tworzy wdrożenie w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="22eb1-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="22eb1-124">Polecenie cmdlet **New-AzDeployment** tworzy wdrożenie w bieżącym zakresie subskrypcji, co powoduje wdrożenie zasobów poziomu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="22eb1-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="22eb1-125">Aby dodać wdrożenie w subskrypcji, określ lokalizację i szablon.</span><span class="sxs-lookup"><span data-stu-id="22eb1-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="22eb1-126">Lokalizacja informuje Menedżera zasobów platformy Azure, gdzie mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="22eb1-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="22eb1-127">Szablon jest ciągiem JSON zawierającym poszczególne zasoby do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="22eb1-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="22eb1-128">Szablon zawiera symbole zastępcze parametru dla wymaganych zasobów i wartości właściwości konfigurowalnych, takich jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="22eb1-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="22eb1-129">Aby użyć szablonu niestandardowego do wdrożenia, określ parametr *TemplateFile* lub *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="22eb1-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="22eb1-130">Każdy szablon zawiera parametry konfigurowalnych właściwości.</span><span class="sxs-lookup"><span data-stu-id="22eb1-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="22eb1-131">Aby określić wartości parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="22eb1-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="22eb1-132">Możesz też użyć parametrów szablonu, które są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="22eb1-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="22eb1-133">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-), aby wskazać parametr, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="22eb1-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="22eb1-134">Wartości parametrów szablonu wprowadzone w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="22eb1-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="22eb1-135">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22eb1-135">EXAMPLES</span></span>

### <span data-ttu-id="22eb1-136">Przykład 1: korzystanie z szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="22eb1-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="22eb1-137">To polecenie tworzy nowe wdrożenie w bieżącym zakresie subskrypcji przy użyciu szablonu niestandardowego i pliku szablonu na dysku.</span><span class="sxs-lookup"><span data-stu-id="22eb1-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="22eb1-138">W poleceniu użyto parametru *TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="22eb1-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="22eb1-139">Używa parametru *TemplateVersion* w celu określenia wersji szablonu.</span><span class="sxs-lookup"><span data-stu-id="22eb1-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="22eb1-140">Przykład 2: Używanie obiektu szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="22eb1-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="22eb1-141">To polecenie tworzy nowe wdrożenie w bieżącym zakresie subskrypcji przy użyciu szablonu niestandardowego i pliku szablonu na dysku, który został przekonwertowany na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="22eb1-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="22eb1-142">Pierwsze dwa polecenia czytają tekst pliku szablonu na dysku i konwertują go na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="22eb1-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="22eb1-143">W ostatnim poleceniu użyto parametru *templateobject* w celu określenia tej obiektu Hashtable i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="22eb1-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="22eb1-144">Używa parametru *TemplateVersion* w celu określenia wersji szablonu.</span><span class="sxs-lookup"><span data-stu-id="22eb1-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="22eb1-145">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22eb1-145">PARAMETERS</span></span>

### <span data-ttu-id="22eb1-146">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="22eb1-146">-ApiVersion</span></span>
<span data-ttu-id="22eb1-147">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="22eb1-147">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="22eb1-148">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="22eb1-148">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="22eb1-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22eb1-149">-AsJob</span></span>
<span data-ttu-id="22eb1-150">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="22eb1-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22eb1-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22eb1-151">-DefaultProfile</span></span>
<span data-ttu-id="22eb1-152">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22eb1-152">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22eb1-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="22eb1-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="22eb1-154">Poziom dziennika debugowania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="22eb1-154">The deployment debug log level.</span></span>

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

### <span data-ttu-id="22eb1-155">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="22eb1-155">-Location</span></span>
<span data-ttu-id="22eb1-156">Lokalizacja przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="22eb1-156">The location to store deployment data.</span></span>

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

### <span data-ttu-id="22eb1-157">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="22eb1-157">-Name</span></span>
<span data-ttu-id="22eb1-158">Nazwa wdrożenia, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="22eb1-158">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="22eb1-159">Ważne tylko w przypadku używania szablonu.</span><span class="sxs-lookup"><span data-stu-id="22eb1-159">Only valid when a template is used.</span></span>
<span data-ttu-id="22eb1-160">Jeśli jest używany szablon, jeśli użytkownik nie określi nazwy wdrożenia, Użyj bieżącej godziny, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="22eb1-160">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

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

### <span data-ttu-id="22eb1-161">-Pre</span><span class="sxs-lookup"><span data-stu-id="22eb1-161">-Pre</span></span>
<span data-ttu-id="22eb1-162">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="22eb1-162">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="22eb1-163">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="22eb1-163">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="22eb1-164">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="22eb1-164">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="22eb1-165">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="22eb1-165">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="22eb1-166">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="22eb1-166">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="22eb1-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="22eb1-167">-TemplateFile</span></span>
<span data-ttu-id="22eb1-168">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="22eb1-168">Local path to the template file.</span></span>

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

### <span data-ttu-id="22eb1-169">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="22eb1-169">-TemplateObject</span></span>
<span data-ttu-id="22eb1-170">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="22eb1-170">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="22eb1-171">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="22eb1-171">-TemplateParameterFile</span></span>
<span data-ttu-id="22eb1-172">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="22eb1-172">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="22eb1-173">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="22eb1-173">-TemplateParameterObject</span></span>
<span data-ttu-id="22eb1-174">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="22eb1-174">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="22eb1-175">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="22eb1-175">-TemplateParameterUri</span></span>
<span data-ttu-id="22eb1-176">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="22eb1-176">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="22eb1-177">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="22eb1-177">-TemplateUri</span></span>
<span data-ttu-id="22eb1-178">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="22eb1-178">Uri to the template file.</span></span>

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

### <span data-ttu-id="22eb1-179">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22eb1-179">-Confirm</span></span>
<span data-ttu-id="22eb1-180">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22eb1-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22eb1-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22eb1-181">-WhatIf</span></span>
<span data-ttu-id="22eb1-182">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22eb1-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22eb1-183">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="22eb1-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22eb1-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22eb1-184">CommonParameters</span></span>
<span data-ttu-id="22eb1-185">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22eb1-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22eb1-186">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22eb1-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22eb1-187">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22eb1-187">INPUTS</span></span>

### <span data-ttu-id="22eb1-188">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="22eb1-188">System.Collections.Hashtable</span></span>

### <span data-ttu-id="22eb1-189">System. String</span><span class="sxs-lookup"><span data-stu-id="22eb1-189">System.String</span></span>

## <span data-ttu-id="22eb1-190">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22eb1-190">OUTPUTS</span></span>

### <span data-ttu-id="22eb1-191">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="22eb1-191">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="22eb1-192">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22eb1-192">NOTES</span></span>

## <span data-ttu-id="22eb1-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22eb1-193">RELATED LINKS</span></span>
