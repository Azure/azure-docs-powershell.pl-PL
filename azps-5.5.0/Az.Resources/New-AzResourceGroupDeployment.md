---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 3e704885c4ce2df0aee2a9b890f768983f93d7bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186402"
---
# <span data-ttu-id="631fd-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="631fd-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="631fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="631fd-102">SYNOPSIS</span></span>
<span data-ttu-id="631fd-103">Dodaje wdrożenie platformy Azure do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="631fd-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="631fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="631fd-104">SYNTAX</span></span>

### <span data-ttu-id="631fd-105">ByTemplateFileWithNoParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="631fd-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631fd-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="631fd-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="631fd-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="631fd-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="631fd-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="631fd-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="631fd-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="631fd-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="631fd-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="631fd-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="631fd-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="631fd-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="631fd-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="631fd-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="631fd-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="631fd-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="631fd-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="631fd-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="631fd-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="631fd-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="631fd-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="631fd-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="631fd-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="631fd-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631fd-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="631fd-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="631fd-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="631fd-119">ByTemplateSpecResourceId</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="631fd-120">OPIS</span><span class="sxs-lookup"><span data-stu-id="631fd-120">DESCRIPTION</span></span>
<span data-ttu-id="631fd-121">Polecenie **cmdlet New-AzResourceGroupDeployment** dodaje wdrożenie do istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="631fd-121">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="631fd-122">Obejmuje to zasoby wymagane przez wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="631fd-122">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="631fd-123">Zasób platformy Azure to jednostka platformy Azure zarządzana przez użytkownika, taka jak serwer bazy danych, baza danych, witryna internetowa, maszyny wirtualnej lub konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="631fd-123">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="631fd-124">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostki, takich jak witryna internetowa, serwer bazy danych i bazy danych, które są wymagane dla finansowej witryny internetowej.</span><span class="sxs-lookup"><span data-stu-id="631fd-124">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="631fd-125">Wdrożenie grupy zasobów używa szablonu do dodawania zasobów do grupy zasobów i publikuje je, aby były dostępne na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="631fd-125">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="631fd-126">Aby dodać zasoby do grupy zasobów bez użycia szablonu, użyj New-AzResource cmdlet.</span><span class="sxs-lookup"><span data-stu-id="631fd-126">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="631fd-127">Aby dodać wdrożenie grupy zasobów, określ nazwę istniejącej grupy zasobów i szablon grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="631fd-127">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="631fd-128">Szablon grupy zasobów to ciąg JSON reprezentujący grupę zasobów dla złożonej usługi opartej na chmurze, takiej jak portal sieci Web.</span><span class="sxs-lookup"><span data-stu-id="631fd-128">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="631fd-129">Szablon zawiera symbole zastępcze parametrów dla wymaganych zasobów i konfigurowalne wartości właściwości, takie jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="631fd-129">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="631fd-130">W galerii szablonów platformy Azure możesz znaleźć wiele szablonów lub utworzyć własne szablony.</span><span class="sxs-lookup"><span data-stu-id="631fd-130">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="631fd-131">Aby utworzyć grupę zasobów przy użyciu szablonu niestandardowego, określ parametr *TemplateFile* lub *parametr TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="631fd-131">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="631fd-132">Każdy szablon zawiera parametry dotyczące właściwości, które można konfigurować.</span><span class="sxs-lookup"><span data-stu-id="631fd-132">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="631fd-133">Aby określić wartości dla parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="631fd-133">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="631fd-134">Możesz również użyć parametrów szablonu, które są dynamicznie dodawane do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="631fd-134">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="631fd-135">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-) w celu wskazania parametru i użyj klawisza Tab do cyklicznego używania dostępnych parametrów.</span><span class="sxs-lookup"><span data-stu-id="631fd-135">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="631fd-136">Wartości parametrów szablonu w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="631fd-136">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="631fd-137">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="631fd-137">EXAMPLES</span></span>

### <span data-ttu-id="631fd-138">Przykład 1. Tworzenie wdrożenia przy użyciu szablonu niestandardowego i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="631fd-138">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="631fd-139">To polecenie tworzy nowe wdrożenie przy użyciu szablonu niestandardowego i pliku szablonu na dysku z parametrem zdefiniowanych tagów.</span><span class="sxs-lookup"><span data-stu-id="631fd-139">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="631fd-140">To polecenie używa *parametru TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="631fd-140">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="631fd-141">Przykład 2. Tworzenie wdrożenia przy użyciu niestandardowego obiektu szablonu i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="631fd-141">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="631fd-142">To polecenie tworzy nowe wdrożenie przy użyciu pliku niestandardowego i szablonu na dysku, który został przekonwertowany na skrót w pamięci.</span><span class="sxs-lookup"><span data-stu-id="631fd-142">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="631fd-143">Pierwsze dwa polecenia odczytają tekst pliku szablonu na dysku i konwertują go na skrót w pamięci.</span><span class="sxs-lookup"><span data-stu-id="631fd-143">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="631fd-144">Ostatnie polecenie używa *parametru TemplateObject* w celu określenia tabeli skrótów i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="631fd-144">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="631fd-145">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="631fd-145">Example 3</span></span>

<span data-ttu-id="631fd-146">Dodaje wdrożenie platformy Azure do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="631fd-146">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="631fd-147">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="631fd-147">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

### <span data-ttu-id="631fd-148">Przykład 4. Wdrażanie szablonu przechowywanego na koncie magazynu publicznego przy użyciu tokenu uri i SAS</span><span class="sxs-lookup"><span data-stu-id="631fd-148">Example 4: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "RGName" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="631fd-149">To polecenie tworzy nowe wdrożenie przy użyciu szablonu w szablonie TemplateUri, który nie jest publiczny i wymaga parametru tokenu w celu uzyskania dostępu, który zostanie dostarczony przy użyciu parametru QueryString.</span><span class="sxs-lookup"><span data-stu-id="631fd-149">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="631fd-150">Uruchomienie tego polecenia w praktyce uzyskuje dostęp do szablonu przy użyciu adresu https://example.com/example.json?foo URL.</span><span class="sxs-lookup"><span data-stu-id="631fd-150">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="631fd-151">Tej funkcji można użyć, jeśli chcesz użyć szablonu na koncie magazynu, podając token SAS jako zapytanie QueryString</span><span class="sxs-lookup"><span data-stu-id="631fd-151">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>
## <span data-ttu-id="631fd-152">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="631fd-152">PARAMETERS</span></span>

### <span data-ttu-id="631fd-153">— AsJob</span><span class="sxs-lookup"><span data-stu-id="631fd-153">-AsJob</span></span>
<span data-ttu-id="631fd-154">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="631fd-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="631fd-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631fd-155">-DefaultProfile</span></span>
<span data-ttu-id="631fd-156">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="631fd-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="631fd-157">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="631fd-157">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="631fd-158">Określa poziom dziennika debugowania.</span><span class="sxs-lookup"><span data-stu-id="631fd-158">Specifies a debug log level.</span></span>
<span data-ttu-id="631fd-159">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="631fd-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="631fd-160">RequestContent</span><span class="sxs-lookup"><span data-stu-id="631fd-160">RequestContent</span></span>
- <span data-ttu-id="631fd-161">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="631fd-161">ResponseContent</span></span>
- <span data-ttu-id="631fd-162">Wszystkie</span><span class="sxs-lookup"><span data-stu-id="631fd-162">All</span></span>
- <span data-ttu-id="631fd-163">Brak</span><span class="sxs-lookup"><span data-stu-id="631fd-163">None</span></span>

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

### <span data-ttu-id="631fd-164">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="631fd-164">-Force</span></span>
<span data-ttu-id="631fd-165">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="631fd-165">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="631fd-166">— tryb</span><span class="sxs-lookup"><span data-stu-id="631fd-166">-Mode</span></span>
<span data-ttu-id="631fd-167">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="631fd-167">Specifies the deployment mode.</span></span> <span data-ttu-id="631fd-168">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="631fd-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="631fd-169">Ukończono: W trybie ukończonym Menedżer zasobów usuwa zasoby istniejące w grupie zasobów, ale nie są określone w szablonie.</span><span class="sxs-lookup"><span data-stu-id="631fd-169">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="631fd-170">Przyrostowe: W trybie przyrostowym Menedżer zasobów pozostawia zasoby bez zmian istniejące w grupie zasobów, ale nie są określone w szablonie.</span><span class="sxs-lookup"><span data-stu-id="631fd-170">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="631fd-171">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="631fd-171">-Name</span></span>
<span data-ttu-id="631fd-172">Nazwa wdrożenia, które zostanie utworzyć.</span><span class="sxs-lookup"><span data-stu-id="631fd-172">The name of the deployment it's going to create.</span></span> <span data-ttu-id="631fd-173">W przypadku, gdy plik szablonu jest podany, domyślnie jest określana jego nazwa domyślna. domyślnie jest to bieżąca godzina, gdy obiekt szablonu jest podany, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="631fd-173">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="631fd-174">— Przed</span><span class="sxs-lookup"><span data-stu-id="631fd-174">-Pre</span></span>
<span data-ttu-id="631fd-175">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="631fd-175">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="631fd-176">-QueryString</span><span class="sxs-lookup"><span data-stu-id="631fd-176">-QueryString</span></span>
<span data-ttu-id="631fd-177">Ciąg zapytania (na przykład token SAS) używany z parametrem TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="631fd-177">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="631fd-178">Czy będzie używana w przypadku szablonów połączonych</span><span class="sxs-lookup"><span data-stu-id="631fd-178">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="631fd-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="631fd-179">-ResourceGroupName</span></span>
<span data-ttu-id="631fd-180">Określa nazwę grupy zasobów do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="631fd-180">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="631fd-181">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="631fd-181">-RollBackDeploymentName</span></span>
<span data-ttu-id="631fd-182">Nie należy stosować wycofywania do pomyślnego wdrożenia z podaną nazwą w grupie zasobów, jeśli jest używany typ -RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="631fd-182">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="631fd-183">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="631fd-183">-RollbackToLastDeployment</span></span>
<span data-ttu-id="631fd-184">W przypadku użycia parametru -RollBackDeploymentName nie należy stosować wycofywania do ostatniego pomyślnego wdrożenia w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="631fd-184">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="631fd-185">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="631fd-185">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="631fd-186">Pomija dynamiczne przetwarzanie parametrów programu PowerShell, które sprawdza, czy podany parametr szablonu zawiera wszystkie niezbędne parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="631fd-186">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="631fd-187">To sprawdzenie spowoduje monitowanie użytkownika o podanie wartości dla brakujących parametrów, ale podanie parametru -SkipTemplateParameterPrompt spowoduje natychmiastowe zignorowanie tego monitu i błędu, jeśli znaleziono, że parametr nie jest powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="631fd-187">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="631fd-188">W przypadku skryptów nieinterakcyjnych można udostępnić komunikat -SkipTemplateParameterPrompt w celu zapewnienia lepszego komunikatu o błędzie w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="631fd-188">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="631fd-189">— Tag</span><span class="sxs-lookup"><span data-stu-id="631fd-189">-Tag</span></span>
<span data-ttu-id="631fd-190">Tagi do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="631fd-190">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="631fd-191">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="631fd-191">-TemplateFile</span></span>
<span data-ttu-id="631fd-192">Określa pełną ścieżkę pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="631fd-192">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="631fd-193">Może to być szablon niestandardowy lub szablon galerii, który jest zapisywany jako plik JSON, na przykład utworzony za pomocą polecenia cmdlet **Save-AzResourceGroupGalleryTemplate.**</span><span class="sxs-lookup"><span data-stu-id="631fd-193">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="631fd-194">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="631fd-194">-TemplateObject</span></span>
<span data-ttu-id="631fd-195">Tabela skrótów reprezentująca szablon.</span><span class="sxs-lookup"><span data-stu-id="631fd-195">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="631fd-196">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="631fd-196">-TemplateParameterFile</span></span>
<span data-ttu-id="631fd-197">Określa pełną ścieżkę pliku JSON zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="631fd-197">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="631fd-198">Jeśli szablon zawiera parametry, musisz określić wartości parametrów za pomocą parametru *TemplateParameterFile* lub *parametru TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="631fd-198">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="631fd-199">Parametry szablonu są dynamicznie dodawane do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="631fd-199">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="631fd-200">Aby użyć parametrów dynamicznych, wpisz znak minus (-) w celu wskazania nazwy parametru, a następnie użyj klawisza Tab do cyklicznego używania dostępnych parametrów.</span><span class="sxs-lookup"><span data-stu-id="631fd-200">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile, ByTemplateSpecResourceIdAndParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="631fd-201">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="631fd-201">-TemplateParameterObject</span></span>
<span data-ttu-id="631fd-202">Określa tabelę skrótów z nazwami i wartościami parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="631fd-202">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="631fd-203">Aby uzyskać pomoc na stronie skrótów tabel w programie Windows PowerShell, wpisz `Get-Help about_Hash_Tables` tekst.</span><span class="sxs-lookup"><span data-stu-id="631fd-203">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="631fd-204">Jeśli szablon zawiera parametry, musisz określić wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="631fd-204">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="631fd-205">Parametry szablonu są dynamicznie dodawane do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="631fd-205">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="631fd-206">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="631fd-206">-TemplateParameterUri</span></span>
<span data-ttu-id="631fd-207">Określa URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="631fd-207">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri, ByTemplateSpecResourceIdAndParamsUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="631fd-208">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="631fd-208">-TemplateSpecId</span></span>
<span data-ttu-id="631fd-209">Identyfikator zasobu szablonuOkreślony, który ma zostać wdrożony.</span><span class="sxs-lookup"><span data-stu-id="631fd-209">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="631fd-210">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="631fd-210">-TemplateUri</span></span>
<span data-ttu-id="631fd-211">Określa URI pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="631fd-211">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="631fd-212">Ten plik może być szablonem niestandardowym lub szablonem galerii, który jest zapisywany jako plik JSON, na przykład przy użyciu narzędzia **Save-AzResourceGroupGalleryTemplate.**</span><span class="sxs-lookup"><span data-stu-id="631fd-212">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="631fd-213">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="631fd-213">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="631fd-214">Typy zmian zasobów rozdzielanych przecinkami, które mają być wykluczone What-If wyników.</span><span class="sxs-lookup"><span data-stu-id="631fd-214">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="631fd-215">Ma zastosowanie, gdy jest ustawiony przełącznik -WhatIf lub -Confirm.</span><span class="sxs-lookup"><span data-stu-id="631fd-215">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="631fd-216">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="631fd-216">-WhatIfResultFormat</span></span>
<span data-ttu-id="631fd-217">Format What-If wynik.</span><span class="sxs-lookup"><span data-stu-id="631fd-217">The What-If result format.</span></span>

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

### <span data-ttu-id="631fd-218">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="631fd-218">-Confirm</span></span>
<span data-ttu-id="631fd-219">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="631fd-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="631fd-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="631fd-220">-WhatIf</span></span>
<span data-ttu-id="631fd-221">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="631fd-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="631fd-222">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="631fd-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="631fd-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631fd-223">CommonParameters</span></span>
<span data-ttu-id="631fd-224">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="631fd-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631fd-225">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="631fd-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631fd-226">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="631fd-226">INPUTS</span></span>

### <span data-ttu-id="631fd-227">System.String</span><span class="sxs-lookup"><span data-stu-id="631fd-227">System.String</span></span>

### <span data-ttu-id="631fd-228">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="631fd-228">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="631fd-229">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="631fd-229">System.Collections.Hashtable</span></span>

## <span data-ttu-id="631fd-230">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="631fd-230">OUTPUTS</span></span>

### <span data-ttu-id="631fd-231">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="631fd-231">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="631fd-232">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="631fd-232">NOTES</span></span>

## <span data-ttu-id="631fd-233">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="631fd-233">RELATED LINKS</span></span>

[<span data-ttu-id="631fd-234">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="631fd-234">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="631fd-235">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="631fd-235">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="631fd-236">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="631fd-236">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="631fd-237">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="631fd-237">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="631fd-238">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="631fd-238">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="631fd-239">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="631fd-239">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)