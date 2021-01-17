---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 916e2fea0e88a1409bc2586ab8b2e80b11ec1a70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490378"
---
# <span data-ttu-id="4dc34-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4dc34-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="4dc34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4dc34-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc34-103">Umożliwia dodanie wdrożenia platformy Azure do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4dc34-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="4dc34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4dc34-104">SYNTAX</span></span>

### <span data-ttu-id="4dc34-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4dc34-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc34-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4dc34-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc34-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4dc34-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc34-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4dc34-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc34-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4dc34-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc34-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4dc34-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc34-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4dc34-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc34-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4dc34-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc34-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4dc34-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc34-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4dc34-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc34-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4dc34-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc34-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4dc34-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dc34-117">Opis</span><span class="sxs-lookup"><span data-stu-id="4dc34-117">DESCRIPTION</span></span>
<span data-ttu-id="4dc34-118">Polecenie cmdlet **New-AzResourceGroupDeployment** umożliwia dodanie wdrożenia do istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4dc34-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="4dc34-119">Dotyczy to zasobów, których wdrożenie wymaga.</span><span class="sxs-lookup"><span data-stu-id="4dc34-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="4dc34-120">Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure, taką jak serwer bazy danych, baza danych, witryna sieci Web, maszyna wirtualna lub konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="4dc34-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="4dc34-121">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka, takich jak witryna sieci Web, serwer bazy danych i bazy danych wymagane dla finansowej witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="4dc34-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="4dc34-122">Wdrożenie grupy zasobów umożliwia dodanie zasobów do grupy zasobów i opublikowanie ich w celu udostępnienia ich na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="4dc34-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="4dc34-123">Aby dodać zasoby do grupy zasobów bez użycia szablonu, użyj polecenia cmdlet New-AzResource.</span><span class="sxs-lookup"><span data-stu-id="4dc34-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="4dc34-124">Aby dodać wdrożenie grupy zasobów, określ nazwę istniejącej grupy zasobów i szablonu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4dc34-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="4dc34-125">Szablon Grupa zasobów to ciąg JSON reprezentujący grupę zasobów dla skomplikowanej usługi opartej na chmurze, na przykład portalu sieci Web.</span><span class="sxs-lookup"><span data-stu-id="4dc34-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="4dc34-126">Szablon zawiera symbole zastępcze parametru dla wymaganych zasobów i wartości właściwości konfigurowalnych, takich jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="4dc34-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="4dc34-127">Wiele szablonów można znaleźć w galerii szablonów platformy Azure lub można utworzyć własne szablony.</span><span class="sxs-lookup"><span data-stu-id="4dc34-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="4dc34-128">Aby utworzyć grupę zasobów przy użyciu szablonu niestandardowego, określ parametr *TemplateFile* lub parametr *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="4dc34-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="4dc34-129">Każdy szablon zawiera parametry konfigurowalnych właściwości.</span><span class="sxs-lookup"><span data-stu-id="4dc34-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="4dc34-130">Aby określić wartości parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="4dc34-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="4dc34-131">Możesz też użyć parametrów szablonu, które są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="4dc34-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="4dc34-132">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-), aby wskazać parametr, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="4dc34-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="4dc34-133">Wartości parametrów szablonu wprowadzone w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="4dc34-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="4dc34-134">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4dc34-134">EXAMPLES</span></span>

### <span data-ttu-id="4dc34-135">Przykład 1: korzystanie z szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="4dc34-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="4dc34-136">To polecenie tworzy nowe wdrożenie przy użyciu szablonu niestandardowego i pliku szablonu na dysku z parametrem zdefiniowane znaczniki.</span><span class="sxs-lookup"><span data-stu-id="4dc34-136">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="4dc34-137">W poleceniu użyto parametru *TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="4dc34-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="4dc34-138">Przykład 2: Używanie obiektu szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="4dc34-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="4dc34-139">To polecenie tworzy nowe wdrożenie przy użyciu pliku niestandardowego i szablonu na dysku, który został przekonwertowany na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="4dc34-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="4dc34-140">Pierwsze dwa polecenia czytają tekst pliku szablonu na dysku i konwertują go na obiekt Hashtable znajdujący się w pamięci.</span><span class="sxs-lookup"><span data-stu-id="4dc34-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="4dc34-141">W ostatnim poleceniu użyto parametru *templateobject* w celu określenia pliku Hashtable i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="4dc34-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="4dc34-142">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4dc34-142">Example 3</span></span>

<span data-ttu-id="4dc34-143">Umożliwia dodanie wdrożenia platformy Azure do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4dc34-143">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="4dc34-144">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="4dc34-144">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

## <span data-ttu-id="4dc34-145">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4dc34-145">PARAMETERS</span></span>

### <span data-ttu-id="4dc34-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4dc34-146">-AsJob</span></span>
<span data-ttu-id="4dc34-147">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4dc34-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4dc34-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc34-148">-DefaultProfile</span></span>
<span data-ttu-id="4dc34-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4dc34-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4dc34-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="4dc34-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="4dc34-151">Określa poziom dziennika debugowania.</span><span class="sxs-lookup"><span data-stu-id="4dc34-151">Specifies a debug log level.</span></span>
<span data-ttu-id="4dc34-152">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4dc34-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4dc34-153">RequestContent</span><span class="sxs-lookup"><span data-stu-id="4dc34-153">RequestContent</span></span>
- <span data-ttu-id="4dc34-154">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="4dc34-154">ResponseContent</span></span>
- <span data-ttu-id="4dc34-155">Cały</span><span class="sxs-lookup"><span data-stu-id="4dc34-155">All</span></span>
- <span data-ttu-id="4dc34-156">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4dc34-156">None</span></span>

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

### <span data-ttu-id="4dc34-157">-Force</span><span class="sxs-lookup"><span data-stu-id="4dc34-157">-Force</span></span>
<span data-ttu-id="4dc34-158">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4dc34-158">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4dc34-159">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="4dc34-159">-Mode</span></span>
<span data-ttu-id="4dc34-160">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="4dc34-160">Specifies the deployment mode.</span></span> <span data-ttu-id="4dc34-161">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4dc34-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4dc34-162">Ukończone: w trybie Complete Menedżer zasobów usuwa zasoby istniejące w grupie zasobów, ale nie są określone w szablonie.</span><span class="sxs-lookup"><span data-stu-id="4dc34-162">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="4dc34-163">Przyrostowe: w trybie przyrostowym Menedżer zasobów pozostawia niezmienione zasoby, które znajdują się w grupie zasobów, ale nie są określone w szablonie.</span><span class="sxs-lookup"><span data-stu-id="4dc34-163">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="4dc34-164">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4dc34-164">-Name</span></span>
<span data-ttu-id="4dc34-165">Nazwa wdrożenia, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="4dc34-165">The name of the deployment it's going to create.</span></span> <span data-ttu-id="4dc34-166">Jeśli ten parametr nie jest określony, domyślnie jest określana nazwa pliku szablonu, gdy jest dostarczany plik szablonu; Domyślnie jest to bieżąca godzina, w której jest dostarczany obiekt szablonu, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="4dc34-166">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="4dc34-167">-Pre</span><span class="sxs-lookup"><span data-stu-id="4dc34-167">-Pre</span></span>
<span data-ttu-id="4dc34-168">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="4dc34-168">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4dc34-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dc34-169">-ResourceGroupName</span></span>
<span data-ttu-id="4dc34-170">Określa nazwę grupy zasobów do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="4dc34-170">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="4dc34-171">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="4dc34-171">-RollBackDeploymentName</span></span>
<span data-ttu-id="4dc34-172">Wycofanie do poprawnego wdrożenia o podanej nazwie w grupie zasobów nie powinno być używane, jeśli jest używana funkcja-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="4dc34-172">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="4dc34-173">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="4dc34-173">-RollbackToLastDeployment</span></span>
<span data-ttu-id="4dc34-174">Wycofanie do ostatniego poprawnego wdrożenia w grupie zasobów nie powinno być dostępne, jeśli jest używana funkcja-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="4dc34-174">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="4dc34-175">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="4dc34-175">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="4dc34-176">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="4dc34-176">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="4dc34-177">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="4dc34-177">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="4dc34-178">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="4dc34-178">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="4dc34-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="4dc34-179">-Tag</span></span>
<span data-ttu-id="4dc34-180">Tagi, które mają zostać wprowadzone do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="4dc34-180">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="4dc34-181">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4dc34-181">-TemplateFile</span></span>
<span data-ttu-id="4dc34-182">Określa pełną ścieżkę pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="4dc34-182">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="4dc34-183">Może to być szablon niestandardowy lub szablon galerii zapisany jako plik JSON, taki jak utworzony za pomocą polecenia cmdlet **Save-AzResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="4dc34-183">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="4dc34-184">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="4dc34-184">-TemplateObject</span></span>
<span data-ttu-id="4dc34-185">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="4dc34-185">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="4dc34-186">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4dc34-186">-TemplateParameterFile</span></span>
<span data-ttu-id="4dc34-187">Określa pełną ścieżkę pliku JSON zawierającego nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="4dc34-187">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="4dc34-188">Jeśli szablon zawiera parametry, należy określić wartości parametrów za pomocą parametru *TemplateParameterFile* lub parametru *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="4dc34-188">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="4dc34-189">Parametry szablonu są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="4dc34-189">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="4dc34-190">Aby użyć parametrów dynamicznych, wpisz znak minus (-), aby wskazać nazwę parametru, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="4dc34-190">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="4dc34-191">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4dc34-191">-TemplateParameterObject</span></span>
<span data-ttu-id="4dc34-192">Określa tabelę skrótów zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="4dc34-192">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="4dc34-193">Aby uzyskać pomoc dotyczącą tabel skrótów w programie Windows PowerShell, wpisz polecenie `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="4dc34-193">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="4dc34-194">Jeśli szablon zawiera parametry, należy określić wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="4dc34-194">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="4dc34-195">Parametry szablonu są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="4dc34-195">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="4dc34-196">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4dc34-196">-TemplateParameterUri</span></span>
<span data-ttu-id="4dc34-197">Określa identyfikator URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="4dc34-197">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="4dc34-198">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4dc34-198">-TemplateUri</span></span>
<span data-ttu-id="4dc34-199">Określa identyfikator URI pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="4dc34-199">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="4dc34-200">Ten plik może być szablonem niestandardowym lub szablonem galerii zapisanym jako plik JSON, na przykład przy użyciu polecenia **Save-AzResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="4dc34-200">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="4dc34-201">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="4dc34-201">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="4dc34-202">Typy zmian zasobów rozdzielanych przecinkami, które mają być wykluczone z wyników What-If.</span><span class="sxs-lookup"><span data-stu-id="4dc34-202">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="4dc34-203">Obowiązuje po ustawieniu przełącznika-WhatIf lub-Confirm.</span><span class="sxs-lookup"><span data-stu-id="4dc34-203">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="4dc34-204">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="4dc34-204">-WhatIfResultFormat</span></span>
<span data-ttu-id="4dc34-205">What-If format wyników.</span><span class="sxs-lookup"><span data-stu-id="4dc34-205">The What-If result format.</span></span>

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

### <span data-ttu-id="4dc34-206">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4dc34-206">-Confirm</span></span>
<span data-ttu-id="4dc34-207">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dc34-207">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dc34-208">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dc34-208">-WhatIf</span></span>
<span data-ttu-id="4dc34-209">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dc34-209">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dc34-210">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4dc34-210">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dc34-211">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc34-211">CommonParameters</span></span>
<span data-ttu-id="4dc34-212">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dc34-212">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc34-213">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dc34-213">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc34-214">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4dc34-214">INPUTS</span></span>

### <span data-ttu-id="4dc34-215">System. String</span><span class="sxs-lookup"><span data-stu-id="4dc34-215">System.String</span></span>

### <span data-ttu-id="4dc34-216">Microsoft. Azure. Management. ResourceManager. modele. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="4dc34-216">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="4dc34-217">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4dc34-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4dc34-218">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4dc34-218">OUTPUTS</span></span>

### <span data-ttu-id="4dc34-219">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4dc34-219">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="4dc34-220">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4dc34-220">NOTES</span></span>

## <span data-ttu-id="4dc34-221">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4dc34-221">RELATED LINKS</span></span>

[<span data-ttu-id="4dc34-222">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4dc34-222">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="4dc34-223">Nowe — AzResource</span><span class="sxs-lookup"><span data-stu-id="4dc34-223">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="4dc34-224">Nowe — AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4dc34-224">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="4dc34-225">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4dc34-225">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="4dc34-226">Zatrzymaj — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4dc34-226">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="4dc34-227">Test — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4dc34-227">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)