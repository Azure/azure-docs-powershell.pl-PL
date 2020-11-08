---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: cf0b8f4897832d84630c98a8518b3c10eefcf5e7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052461"
---
# <span data-ttu-id="8904b-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8904b-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="8904b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8904b-102">SYNOPSIS</span></span>
<span data-ttu-id="8904b-103">Umożliwia dodanie wdrożenia platformy Azure do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8904b-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="8904b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8904b-104">SYNTAX</span></span>

### <span data-ttu-id="8904b-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8904b-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8904b-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8904b-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8904b-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8904b-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8904b-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8904b-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8904b-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8904b-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8904b-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8904b-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8904b-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8904b-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8904b-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8904b-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8904b-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8904b-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8904b-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8904b-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8904b-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8904b-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8904b-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8904b-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8904b-117">Opis</span><span class="sxs-lookup"><span data-stu-id="8904b-117">DESCRIPTION</span></span>
<span data-ttu-id="8904b-118">Polecenie cmdlet **New-AzResourceGroupDeployment** umożliwia dodanie wdrożenia do istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8904b-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="8904b-119">Dotyczy to zasobów, których wdrożenie wymaga.</span><span class="sxs-lookup"><span data-stu-id="8904b-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="8904b-120">Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure, taką jak serwer bazy danych, baza danych, witryna sieci Web, maszyna wirtualna lub konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="8904b-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="8904b-121">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka, takich jak witryna sieci Web, serwer bazy danych i bazy danych wymagane dla finansowej witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="8904b-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="8904b-122">Wdrożenie grupy zasobów umożliwia dodanie zasobów do grupy zasobów i opublikowanie ich w celu udostępnienia ich na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="8904b-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="8904b-123">Aby dodać zasoby do grupy zasobów bez użycia szablonu, użyj polecenia cmdlet New-AzResource.</span><span class="sxs-lookup"><span data-stu-id="8904b-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="8904b-124">Aby dodać wdrożenie grupy zasobów, określ nazwę istniejącej grupy zasobów i szablonu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8904b-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="8904b-125">Szablon Grupa zasobów to ciąg JSON reprezentujący grupę zasobów dla skomplikowanej usługi opartej na chmurze, na przykład portalu sieci Web.</span><span class="sxs-lookup"><span data-stu-id="8904b-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="8904b-126">Szablon zawiera symbole zastępcze parametru dla wymaganych zasobów i wartości właściwości konfigurowalnych, takich jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="8904b-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="8904b-127">Wiele szablonów można znaleźć w galerii szablonów platformy Azure lub można utworzyć własne szablony.</span><span class="sxs-lookup"><span data-stu-id="8904b-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="8904b-128">Aby utworzyć grupę zasobów przy użyciu szablonu niestandardowego, określ parametr *TemplateFile* lub parametr *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="8904b-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="8904b-129">Każdy szablon zawiera parametry konfigurowalnych właściwości.</span><span class="sxs-lookup"><span data-stu-id="8904b-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="8904b-130">Aby określić wartości parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="8904b-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="8904b-131">Możesz też użyć parametrów szablonu, które są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="8904b-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="8904b-132">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-), aby wskazać parametr, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="8904b-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="8904b-133">Wartości parametrów szablonu wprowadzone w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="8904b-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="8904b-134">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8904b-134">EXAMPLES</span></span>

### <span data-ttu-id="8904b-135">Przykład 1: korzystanie z szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="8904b-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="8904b-136">To polecenie tworzy nowe wdrożenie przy użyciu szablonu niestandardowego i pliku szablonu na dysku.</span><span class="sxs-lookup"><span data-stu-id="8904b-136">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="8904b-137">W poleceniu użyto parametru *TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="8904b-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="8904b-138">Przykład 2: Używanie obiektu szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="8904b-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="8904b-139">To polecenie tworzy nowe wdrożenie przy użyciu pliku niestandardowego i szablonu na dysku, który został przekonwertowany na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="8904b-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="8904b-140">Pierwsze dwa polecenia czytają tekst pliku szablonu na dysku i konwertują go na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="8904b-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="8904b-141">W ostatnim poleceniu użyto parametru *templateobject* w celu określenia pliku Hashtable i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="8904b-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="8904b-142">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8904b-142">PARAMETERS</span></span>

### <span data-ttu-id="8904b-143">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8904b-143">-ApiVersion</span></span>
<span data-ttu-id="8904b-144">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="8904b-144">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8904b-145">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="8904b-145">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8904b-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8904b-146">-AsJob</span></span>
<span data-ttu-id="8904b-147">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8904b-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8904b-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8904b-148">-DefaultProfile</span></span>
<span data-ttu-id="8904b-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8904b-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8904b-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="8904b-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="8904b-151">Określa poziom dziennika debugowania.</span><span class="sxs-lookup"><span data-stu-id="8904b-151">Specifies a debug log level.</span></span>
<span data-ttu-id="8904b-152">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8904b-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8904b-153">RequestContent</span><span class="sxs-lookup"><span data-stu-id="8904b-153">RequestContent</span></span>
- <span data-ttu-id="8904b-154">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="8904b-154">ResponseContent</span></span>
- <span data-ttu-id="8904b-155">Cały</span><span class="sxs-lookup"><span data-stu-id="8904b-155">All</span></span>
- <span data-ttu-id="8904b-156">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8904b-156">None</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestContent, ResponseContent, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8904b-157">-Force</span><span class="sxs-lookup"><span data-stu-id="8904b-157">-Force</span></span>
<span data-ttu-id="8904b-158">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8904b-158">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8904b-159">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="8904b-159">-Mode</span></span>
<span data-ttu-id="8904b-160">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="8904b-160">Specifies the deployment mode.</span></span> <span data-ttu-id="8904b-161">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8904b-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8904b-162">Ukończone: w trybie Complete Menedżer zasobów usuwa zasoby istniejące w grupie zasobów, ale nie są określone w szablonie.</span><span class="sxs-lookup"><span data-stu-id="8904b-162">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="8904b-163">Przyrostowe: w trybie przyrostowym Menedżer zasobów pozostawia niezmienione zasoby, które znajdują się w grupie zasobów, ale nie są określone w szablonie.</span><span class="sxs-lookup"><span data-stu-id="8904b-163">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8904b-164">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8904b-164">-Name</span></span>
<span data-ttu-id="8904b-165">Określa nazwę wdrożenia grupy zasobów do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="8904b-165">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="8904b-166">-Pre</span><span class="sxs-lookup"><span data-stu-id="8904b-166">-Pre</span></span>
<span data-ttu-id="8904b-167">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="8904b-167">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8904b-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8904b-168">-ResourceGroupName</span></span>
<span data-ttu-id="8904b-169">Określa nazwę grupy zasobów do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="8904b-169">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="8904b-170">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="8904b-170">-RollBackDeploymentName</span></span>
<span data-ttu-id="8904b-171">Wycofanie do poprawnego wdrożenia o podanej nazwie w grupie zasobów nie powinno być używane, jeśli jest używana funkcja-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="8904b-171">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8904b-172">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="8904b-172">-RollbackToLastDeployment</span></span>
<span data-ttu-id="8904b-173">Wycofanie do ostatniego poprawnego wdrożenia w grupie zasobów nie powinno być dostępne, jeśli jest używana funkcja-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="8904b-173">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="8904b-174">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="8904b-174">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="8904b-175">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="8904b-175">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="8904b-176">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="8904b-176">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="8904b-177">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="8904b-177">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="8904b-178">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8904b-178">-TemplateFile</span></span>
<span data-ttu-id="8904b-179">Określa pełną ścieżkę pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="8904b-179">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="8904b-180">Może to być szablon niestandardowy lub szablon galerii zapisany jako plik JSON, taki jak utworzony za pomocą polecenia cmdlet **Save-AzResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="8904b-180">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="8904b-181">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="8904b-181">-TemplateObject</span></span>
<span data-ttu-id="8904b-182">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="8904b-182">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="8904b-183">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8904b-183">-TemplateParameterFile</span></span>
<span data-ttu-id="8904b-184">Określa pełną ścieżkę pliku JSON zawierającego nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="8904b-184">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="8904b-185">Jeśli szablon zawiera parametry, należy określić wartości parametrów za pomocą parametru *TemplateParameterFile* lub parametru *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="8904b-185">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="8904b-186">Parametry szablonu są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="8904b-186">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="8904b-187">Aby użyć parametrów dynamicznych, wpisz znak minus (-), aby wskazać nazwę parametru, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="8904b-187">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="8904b-188">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="8904b-188">-TemplateParameterObject</span></span>
<span data-ttu-id="8904b-189">Określa tabelę skrótów zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="8904b-189">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="8904b-190">Aby uzyskać pomoc dotyczącą tabel skrótów w programie Windows PowerShell, wpisz polecenie `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="8904b-190">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="8904b-191">Jeśli szablon zawiera parametry, należy określić wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="8904b-191">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="8904b-192">Parametry szablonu są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="8904b-192">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="8904b-193">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="8904b-193">-TemplateParameterUri</span></span>
<span data-ttu-id="8904b-194">Określa identyfikator URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="8904b-194">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="8904b-195">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="8904b-195">-TemplateUri</span></span>
<span data-ttu-id="8904b-196">Określa identyfikator URI pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="8904b-196">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="8904b-197">Ten plik może być szablonem niestandardowym lub szablonem galerii zapisanym jako plik JSON, na przykład przy użyciu polecenia **Save-AzResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="8904b-197">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="8904b-198">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8904b-198">-Confirm</span></span>
<span data-ttu-id="8904b-199">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8904b-199">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8904b-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8904b-200">-WhatIf</span></span>
<span data-ttu-id="8904b-201">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8904b-201">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8904b-202">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8904b-202">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8904b-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8904b-203">CommonParameters</span></span>
<span data-ttu-id="8904b-204">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8904b-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8904b-205">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8904b-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8904b-206">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8904b-206">INPUTS</span></span>

### <span data-ttu-id="8904b-207">System. String</span><span class="sxs-lookup"><span data-stu-id="8904b-207">System.String</span></span>

### <span data-ttu-id="8904b-208">Microsoft. Azure. Management. ResourceManager. modele. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="8904b-208">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="8904b-209">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8904b-209">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8904b-210">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8904b-210">OUTPUTS</span></span>

### <span data-ttu-id="8904b-211">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8904b-211">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="8904b-212">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8904b-212">NOTES</span></span>

## <span data-ttu-id="8904b-213">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8904b-213">RELATED LINKS</span></span>

[<span data-ttu-id="8904b-214">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8904b-214">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="8904b-215">Nowe — AzResource</span><span class="sxs-lookup"><span data-stu-id="8904b-215">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="8904b-216">Nowe — AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8904b-216">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="8904b-217">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8904b-217">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="8904b-218">Zatrzymaj — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8904b-218">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="8904b-219">Test — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8904b-219">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


