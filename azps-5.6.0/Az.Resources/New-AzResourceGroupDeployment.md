---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 3403900fafae1615f8253b4d5671e497a1d507f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978154"
---
# <span data-ttu-id="36dec-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="36dec-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="36dec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36dec-102">SYNOPSIS</span></span>
<span data-ttu-id="36dec-103">Dodaje wdrożenie platformy Azure do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36dec-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="36dec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36dec-104">SYNTAX</span></span>

### <span data-ttu-id="36dec-105">ByTemplateFileWithNoParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="36dec-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36dec-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="36dec-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36dec-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="36dec-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36dec-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="36dec-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36dec-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="36dec-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36dec-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="36dec-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36dec-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="36dec-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36dec-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="36dec-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36dec-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="36dec-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36dec-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="36dec-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36dec-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="36dec-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36dec-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="36dec-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36dec-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="36dec-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36dec-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="36dec-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36dec-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="36dec-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36dec-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="36dec-120">ByTemplateSpecResourceId</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36dec-121">OPIS</span><span class="sxs-lookup"><span data-stu-id="36dec-121">DESCRIPTION</span></span>
<span data-ttu-id="36dec-122">Polecenie **cmdlet New-AzResourceGroupDeployment** dodaje wdrożenie do istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36dec-122">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="36dec-123">Obejmuje to zasoby wymagane przez wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="36dec-123">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="36dec-124">Zasób platformy Azure to jednostka platformy Azure zarządzana przez użytkownika, taka jak serwer bazy danych, baza danych, witryna internetowa, maszyny wirtualnej lub konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="36dec-124">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="36dec-125">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostki, takich jak witryna internetowa, serwer bazy danych i bazy danych, które są wymagane dla finansowej witryny internetowej.</span><span class="sxs-lookup"><span data-stu-id="36dec-125">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="36dec-126">Wdrożenie grupy zasobów używa szablonu do dodawania zasobów do grupy zasobów i publikuje je, aby były dostępne na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="36dec-126">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="36dec-127">Aby dodać zasoby do grupy zasobów bez użycia szablonu, użyj New-AzResource cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36dec-127">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="36dec-128">Aby dodać wdrożenie grupy zasobów, określ nazwę istniejącej grupy zasobów i szablon grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36dec-128">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="36dec-129">Szablon grupy zasobów to ciąg JSON reprezentujący grupę zasobów dla złożonej usługi opartej na chmurze, takiej jak portal sieci Web.</span><span class="sxs-lookup"><span data-stu-id="36dec-129">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="36dec-130">Szablon zawiera symbole zastępcze parametrów dla wymaganych zasobów i konfigurowane wartości właściwości, takie jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="36dec-130">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="36dec-131">W galerii szablonów platformy Azure możesz znaleźć wiele szablonów lub utworzyć własne szablony.</span><span class="sxs-lookup"><span data-stu-id="36dec-131">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="36dec-132">Aby utworzyć grupę zasobów przy użyciu szablonu niestandardowego, określ parametr *TemplateFile* lub *parametr TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="36dec-132">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="36dec-133">Każdy szablon zawiera parametry dotyczące właściwości, które można konfigurować.</span><span class="sxs-lookup"><span data-stu-id="36dec-133">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="36dec-134">Aby określić wartości dla parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="36dec-134">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="36dec-135">Możesz również użyć parametrów szablonu, które są dynamicznie dodawane do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="36dec-135">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="36dec-136">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-) w celu wskazania parametru i użyj klawisza Tab do cyklicznego używania dostępnych parametrów.</span><span class="sxs-lookup"><span data-stu-id="36dec-136">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="36dec-137">Wartości parametrów szablonu w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="36dec-137">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="36dec-138">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36dec-138">EXAMPLES</span></span>

### <span data-ttu-id="36dec-139">Przykład 1. Tworzenie wdrożenia przy użyciu szablonu niestandardowego i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="36dec-139">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="36dec-140">To polecenie służy do tworzenia nowego wdrożenia przy użyciu szablonu niestandardowego i pliku szablonu na dysku z parametrem zdefiniowanych tagów.</span><span class="sxs-lookup"><span data-stu-id="36dec-140">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="36dec-141">To polecenie używa *parametru TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="36dec-141">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="36dec-142">Przykład 2. Tworzenie wdrożenia przy użyciu niestandardowego obiektu szablonu i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="36dec-142">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="36dec-143">To polecenie tworzy nowe wdrożenie przy użyciu pliku niestandardowego i szablonu na dysku, który został przekonwertowany na skrót w pamięci.</span><span class="sxs-lookup"><span data-stu-id="36dec-143">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="36dec-144">Pierwsze dwa polecenia odczytają tekst pliku szablonu na dysku i konwertują go na skrót w pamięci.</span><span class="sxs-lookup"><span data-stu-id="36dec-144">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="36dec-145">Ostatnie polecenie używa *parametru TemplateObject* w celu określenia tabeli skrótów i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="36dec-145">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="36dec-146">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="36dec-146">Example 3</span></span>

<span data-ttu-id="36dec-147">Dodaje wdrożenie platformy Azure do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36dec-147">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="36dec-148">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="36dec-148">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

### <span data-ttu-id="36dec-149">Przykład 4. Wdrażanie szablonu przechowywanego na koncie magazynu nieudostępniania publicznego przy użyciu tokenu uri i SAS</span><span class="sxs-lookup"><span data-stu-id="36dec-149">Example 4: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "RGName" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```

<span data-ttu-id="36dec-150">To polecenie tworzy nowe wdrożenie przy użyciu szablonu w szablonie TemplateUri, który nie jest publiczny i wymaga parametru tokenu w celu uzyskania dostępu, który zostanie dostarczony przy użyciu parametru QueryString.</span><span class="sxs-lookup"><span data-stu-id="36dec-150">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="36dec-151">Uruchomienie tego polecenia w praktyce uzyskuje dostęp do szablonu przy użyciu adresu https://example.com/example.json?foo URL.</span><span class="sxs-lookup"><span data-stu-id="36dec-151">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="36dec-152">Tej funkcji można użyć, jeśli chcesz użyć szablonu na koncie magazynu, podając token SAS jako zapytanie QueryString</span><span class="sxs-lookup"><span data-stu-id="36dec-152">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

## <span data-ttu-id="36dec-153">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36dec-153">PARAMETERS</span></span>

### <span data-ttu-id="36dec-154">— AsJob</span><span class="sxs-lookup"><span data-stu-id="36dec-154">-AsJob</span></span>
<span data-ttu-id="36dec-155">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="36dec-155">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36dec-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36dec-156">-DefaultProfile</span></span>
<span data-ttu-id="36dec-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="36dec-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36dec-158">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="36dec-158">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="36dec-159">Określa poziom dziennika debugowania.</span><span class="sxs-lookup"><span data-stu-id="36dec-159">Specifies a debug log level.</span></span>
<span data-ttu-id="36dec-160">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="36dec-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="36dec-161">RequestContent</span><span class="sxs-lookup"><span data-stu-id="36dec-161">RequestContent</span></span>
- <span data-ttu-id="36dec-162">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="36dec-162">ResponseContent</span></span>
- <span data-ttu-id="36dec-163">Wszystkie</span><span class="sxs-lookup"><span data-stu-id="36dec-163">All</span></span>
- <span data-ttu-id="36dec-164">Brak</span><span class="sxs-lookup"><span data-stu-id="36dec-164">None</span></span>

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

### <span data-ttu-id="36dec-165">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="36dec-165">-Force</span></span>
<span data-ttu-id="36dec-166">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="36dec-166">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="36dec-167">— tryb</span><span class="sxs-lookup"><span data-stu-id="36dec-167">-Mode</span></span>
<span data-ttu-id="36dec-168">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="36dec-168">Specifies the deployment mode.</span></span> <span data-ttu-id="36dec-169">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="36dec-169">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="36dec-170">Ukończono: W trybie ukończonym Menedżer zasobów usuwa zasoby istniejące w grupie zasobów, ale nie są określone w szablonie.</span><span class="sxs-lookup"><span data-stu-id="36dec-170">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="36dec-171">Przyrostowe: W trybie przyrostowym Menedżer zasobów pozostawia zasoby bez zmian istniejące w grupie zasobów, ale nie są określone w szablonie.</span><span class="sxs-lookup"><span data-stu-id="36dec-171">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="36dec-172">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="36dec-172">-Name</span></span>
<span data-ttu-id="36dec-173">Nazwa wdrożenia, które zostanie utworzyć.</span><span class="sxs-lookup"><span data-stu-id="36dec-173">The name of the deployment it's going to create.</span></span> <span data-ttu-id="36dec-174">W przypadku, gdy plik szablonu jest podany, domyślnie jest określana jego nazwa domyślna. domyślnie jest to bieżąca godzina, gdy obiekt szablonu jest podany, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="36dec-174">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="36dec-175">— Przed</span><span class="sxs-lookup"><span data-stu-id="36dec-175">-Pre</span></span>
<span data-ttu-id="36dec-176">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="36dec-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="36dec-177">-QueryString</span><span class="sxs-lookup"><span data-stu-id="36dec-177">-QueryString</span></span>
<span data-ttu-id="36dec-178">Ciąg zapytania (na przykład token SAS) używany z parametrem TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="36dec-178">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="36dec-179">Czy będzie używana w przypadku szablonów połączonych</span><span class="sxs-lookup"><span data-stu-id="36dec-179">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="36dec-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36dec-180">-ResourceGroupName</span></span>
<span data-ttu-id="36dec-181">Określa nazwę grupy zasobów do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="36dec-181">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="36dec-182">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="36dec-182">-RollBackDeploymentName</span></span>
<span data-ttu-id="36dec-183">Nie należy stosować wycofywania do pomyślnego wdrożenia z podaną nazwą w grupie zasobów, jeśli jest używany typ -RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="36dec-183">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="36dec-184">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="36dec-184">-RollbackToLastDeployment</span></span>
<span data-ttu-id="36dec-185">W przypadku użycia parametru -RollBackDeploymentName nie należy stosować wycofywania do ostatniego pomyślnego wdrożenia w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="36dec-185">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="36dec-186">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="36dec-186">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="36dec-187">Pomija dynamiczne przetwarzanie parametrów programu PowerShell, które sprawdza, czy podany parametr szablonu zawiera wszystkie niezbędne parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="36dec-187">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="36dec-188">To sprawdzenie spowoduje monitowanie użytkownika o podanie wartości dla brakujących parametrów, ale podanie parametru -SkipTemplateParameterPrompt spowoduje natychmiastowe zignorowanie tego monitu i błędu, jeśli znaleziono, że parametr nie jest powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="36dec-188">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="36dec-189">W przypadku skryptów nieinterakcyjnych można udostępnić komunikat -SkipTemplateParameterPrompt w celu zapewnienia lepszego komunikatu o błędzie w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="36dec-189">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="36dec-190">— Tag</span><span class="sxs-lookup"><span data-stu-id="36dec-190">-Tag</span></span>
<span data-ttu-id="36dec-191">Tagi do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="36dec-191">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="36dec-192">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="36dec-192">-TemplateFile</span></span>
<span data-ttu-id="36dec-193">Określa pełną ścieżkę pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="36dec-193">Specifies the full path of a template file.</span></span> <span data-ttu-id="36dec-194">Obsługiwany typ pliku szablonu: json i biceps.</span><span class="sxs-lookup"><span data-stu-id="36dec-194">Supported template file type: json and bicep.</span></span>
<span data-ttu-id="36dec-195">Może to być szablon niestandardowy lub szablon galerii, który jest zapisywany jako plik JSON, na przykład utworzony za pomocą polecenia cmdlet **Save-AzResourceGroupGalleryTemplate.**</span><span class="sxs-lookup"><span data-stu-id="36dec-195">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="36dec-196">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="36dec-196">-TemplateObject</span></span>
<span data-ttu-id="36dec-197">Tabela skrótów reprezentująca szablon.</span><span class="sxs-lookup"><span data-stu-id="36dec-197">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="36dec-198">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="36dec-198">-TemplateParameterFile</span></span>
<span data-ttu-id="36dec-199">Określa pełną ścieżkę pliku JSON zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="36dec-199">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="36dec-200">Jeśli szablon zawiera parametry, musisz określić wartości parametrów za pomocą parametru *TemplateParameterFile* lub *parametru TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="36dec-200">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="36dec-201">Parametry szablonu są dynamicznie dodawane do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="36dec-201">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="36dec-202">Aby użyć parametrów dynamicznych, wpisz znak minus (-) w celu wskazania nazwy parametru, a następnie użyj klawisza Tab do cyklicznego używania dostępnych parametrów.</span><span class="sxs-lookup"><span data-stu-id="36dec-202">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="36dec-203">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="36dec-203">-TemplateParameterObject</span></span>
<span data-ttu-id="36dec-204">Określa tabelę skrótów z nazwami i wartościami parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="36dec-204">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="36dec-205">Aby uzyskać pomoc na stronie skrótów tabel w programie Windows PowerShell, wpisz `Get-Help about_Hash_Tables` tekst.</span><span class="sxs-lookup"><span data-stu-id="36dec-205">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="36dec-206">Jeśli szablon zawiera parametry, musisz określić wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="36dec-206">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="36dec-207">Parametry szablonu są dynamicznie dodawane do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="36dec-207">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject, ByTemplateSpecResourceIdAndParamsObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36dec-208">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="36dec-208">-TemplateParameterUri</span></span>
<span data-ttu-id="36dec-209">Określa URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="36dec-209">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="36dec-210">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="36dec-210">-TemplateSpecId</span></span>
<span data-ttu-id="36dec-211">Identyfikator zasobu szablonuOkreślony, który ma zostać wdrożony.</span><span class="sxs-lookup"><span data-stu-id="36dec-211">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParamsObject, ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36dec-212">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="36dec-212">-TemplateUri</span></span>
<span data-ttu-id="36dec-213">Określa URI pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="36dec-213">Specifies the URI of a template file.</span></span>
<span data-ttu-id="36dec-214">Ten plik może być szablonem niestandardowym lub szablonem galerii, który jest zapisywany jako plik JSON, na przykład przy użyciu narzędzia **Save-AzResourceGroupGalleryTemplate.**</span><span class="sxs-lookup"><span data-stu-id="36dec-214">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="36dec-215">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="36dec-215">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="36dec-216">Typy zmian zasobów rozdzielane przecinkami, które mają być wykluczone What-If wyników.</span><span class="sxs-lookup"><span data-stu-id="36dec-216">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="36dec-217">Ma zastosowanie, gdy jest ustawiony przełącznik -WhatIf lub -Confirm.</span><span class="sxs-lookup"><span data-stu-id="36dec-217">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="36dec-218">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="36dec-218">-WhatIfResultFormat</span></span>
<span data-ttu-id="36dec-219">Format What-If wynik.</span><span class="sxs-lookup"><span data-stu-id="36dec-219">The What-If result format.</span></span>

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

### <span data-ttu-id="36dec-220">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36dec-220">-Confirm</span></span>
<span data-ttu-id="36dec-221">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36dec-221">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36dec-222">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36dec-222">-WhatIf</span></span>
<span data-ttu-id="36dec-223">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36dec-223">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36dec-224">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="36dec-224">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36dec-225">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36dec-225">CommonParameters</span></span>
<span data-ttu-id="36dec-226">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36dec-226">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36dec-227">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36dec-227">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36dec-228">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36dec-228">INPUTS</span></span>

### <span data-ttu-id="36dec-229">System.String</span><span class="sxs-lookup"><span data-stu-id="36dec-229">System.String</span></span>

### <span data-ttu-id="36dec-230">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="36dec-230">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="36dec-231">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="36dec-231">System.Collections.Hashtable</span></span>

## <span data-ttu-id="36dec-232">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36dec-232">OUTPUTS</span></span>

### <span data-ttu-id="36dec-233">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="36dec-233">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="36dec-234">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36dec-234">NOTES</span></span>

## <span data-ttu-id="36dec-235">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36dec-235">RELATED LINKS</span></span>

[<span data-ttu-id="36dec-236">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="36dec-236">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="36dec-237">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="36dec-237">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="36dec-238">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36dec-238">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="36dec-239">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="36dec-239">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="36dec-240">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="36dec-240">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="36dec-241">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="36dec-241">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)