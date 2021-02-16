---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: 95aa46354fb0ea1f2a1883fe7d319acfda220526
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242538"
---
# <span data-ttu-id="e00db-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e00db-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="e00db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e00db-102">SYNOPSIS</span></span>
<span data-ttu-id="e00db-103">Tworzenie wdrożenia w grupie zarządzania</span><span class="sxs-lookup"><span data-stu-id="e00db-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="e00db-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e00db-104">SYNTAX</span></span>

### <span data-ttu-id="e00db-105">ByTemplateFileWithNoParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e00db-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e00db-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e00db-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e00db-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e00db-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e00db-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e00db-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e00db-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e00db-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e00db-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e00db-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e00db-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e00db-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e00db-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="e00db-112">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e00db-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e00db-113">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e00db-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e00db-114">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e00db-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e00db-115">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e00db-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="e00db-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e00db-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e00db-117">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e00db-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e00db-118">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e00db-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="e00db-119">ByTemplateSpecResourceId</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-QueryString <String>] [-AsJob] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e00db-120">OPIS</span><span class="sxs-lookup"><span data-stu-id="e00db-120">DESCRIPTION</span></span>
<span data-ttu-id="e00db-121">Polecenie **cmdlet New-AzManagementGroupDeployment** dodaje wdrożenie w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e00db-121">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="e00db-122">Aby dodać wdrożenie w grupie zarządzania, określ grupę zarządzania, lokalizację i szablon.</span><span class="sxs-lookup"><span data-stu-id="e00db-122">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="e00db-123">Ta lokalizacja wskazuje usłudze Azure Resource Manager, gdzie mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e00db-123">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="e00db-124">Szablon to ciąg JSON zawierający poszczególne zasoby do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e00db-124">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="e00db-125">Szablon zawiera symbole zastępcze parametrów dla wymaganych zasobów i konfigurowalne wartości właściwości, takie jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="e00db-125">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="e00db-126">Aby użyć szablonu niestandardowego dla wdrożenia, określ parametr *TemplateFile* lub *parametr TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="e00db-126">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="e00db-127">Każdy szablon zawiera parametry dotyczące właściwości, które można konfigurować.</span><span class="sxs-lookup"><span data-stu-id="e00db-127">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="e00db-128">Aby określić wartości dla parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="e00db-128">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="e00db-129">Możesz również użyć parametrów szablonu, które są dynamicznie dodawane do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="e00db-129">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="e00db-130">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-) w celu wskazania parametru i użyj klawisza Tab do cyklicznego używania dostępnych parametrów.</span><span class="sxs-lookup"><span data-stu-id="e00db-130">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="e00db-131">Wartości parametrów szablonu w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="e00db-131">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="e00db-132">Aby dodać zasoby do grupy zasobów, użyj funkcji **New-AzResourceGroupDeployment,** która tworzy wdrożenie w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e00db-132">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="e00db-133">Aby dodać zasoby do subskrypcji, użyj funkcji **New-AzSubscriptionDeployment,** która tworzy wdrożenie w zakresie subskrypcji, które wdraża zasoby na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e00db-133">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="e00db-134">Aby dodać zasoby w zakresie dzierżawy, użyj funkcji **New-AzTenantDeployment,** która tworzy wdrożenie w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e00db-134">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="e00db-135">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e00db-135">EXAMPLES</span></span>

### <span data-ttu-id="e00db-136">Przykład 1. Tworzenie wdrożenia przy użyciu szablonu niestandardowego i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="e00db-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="e00db-137">To polecenie tworzy nowe wdrożenie w grupie zarządzania "myMG" przy użyciu szablonu niestandardowego i pliku szablonu na dysku z parametrem zdefiniowanych tagów.</span><span class="sxs-lookup"><span data-stu-id="e00db-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="e00db-138">To polecenie używa *parametru TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="e00db-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="e00db-139">Przykład 2. Wdrażanie szablonu przechowywanego na koncie magazynu publicznego przy użyciu tokenu uri i SAS</span><span class="sxs-lookup"><span data-stu-id="e00db-139">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```
<span data-ttu-id="e00db-140">To polecenie tworzy nowe wdrożenie przy użyciu szablonu w szablonie TemplateUri, który nie jest publiczny i wymaga parametru tokenu w celu uzyskania dostępu, który zostanie dostarczony przy użyciu parametru QueryString.</span><span class="sxs-lookup"><span data-stu-id="e00db-140">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="e00db-141">Uruchomienie tego polecenia w praktyce uzyskuje dostęp do szablonu przy użyciu adresu https://example.com/example.json?foo URL.</span><span class="sxs-lookup"><span data-stu-id="e00db-141">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="e00db-142">Może to być używane, jeśli chcesz użyć szablonu na koncie magazynu, podając token SAS jako zapytanie QueryString</span><span class="sxs-lookup"><span data-stu-id="e00db-142">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="e00db-143">Przykład 3. Tworzenie wdrożenia przy użyciu niestandardowego obiektu szablonu i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="e00db-143">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="e00db-144">To polecenie tworzy nowe wdrożenie w grupie zarządzania "myMG" przy użyciu szablonu niestandardowego i pliku szablonu na dysku, który został przekonwertowany na skrót w pamięci.</span><span class="sxs-lookup"><span data-stu-id="e00db-144">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="e00db-145">Pierwsze dwa polecenia odczytają tekst pliku szablonu na dysku i konwertują go na skrót w pamięci.</span><span class="sxs-lookup"><span data-stu-id="e00db-145">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="e00db-146">Ostatnie polecenie używa *parametru TemplateObject* do określenia tej tabeli skrótów i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="e00db-146">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="e00db-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e00db-147">PARAMETERS</span></span>

### <span data-ttu-id="e00db-148">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e00db-148">-AsJob</span></span>
<span data-ttu-id="e00db-149">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e00db-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e00db-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e00db-150">-DefaultProfile</span></span>
<span data-ttu-id="e00db-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e00db-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e00db-152">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="e00db-152">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="e00db-153">Poziom dziennika debugowania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e00db-153">The deployment debug log level.</span></span>

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

### <span data-ttu-id="e00db-154">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e00db-154">-Location</span></span>
<span data-ttu-id="e00db-155">Lokalizacja przechowywania danych wdrożeniowych.</span><span class="sxs-lookup"><span data-stu-id="e00db-155">The location to store deployment data.</span></span>

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

### <span data-ttu-id="e00db-156">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="e00db-156">-ManagementGroupId</span></span>
<span data-ttu-id="e00db-157">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="e00db-157">The management group ID.</span></span>

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

### <span data-ttu-id="e00db-158">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e00db-158">-Name</span></span>
<span data-ttu-id="e00db-159">Nazwa wdrożenia, które zostanie utworzyć.</span><span class="sxs-lookup"><span data-stu-id="e00db-159">The name of the deployment it's going to create.</span></span> <span data-ttu-id="e00db-160">Jeśli nie zostanie określony, domyślnie jest określana nazwa pliku szablonu po podano plik szablonu. domyślnie jest to bieżąca godzina, gdy obiekt szablonu jest podany, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="e00db-160">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="e00db-161">— Przed</span><span class="sxs-lookup"><span data-stu-id="e00db-161">-Pre</span></span>
<span data-ttu-id="e00db-162">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e00db-162">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e00db-163">-QueryString</span><span class="sxs-lookup"><span data-stu-id="e00db-163">-QueryString</span></span>
<span data-ttu-id="e00db-164">Ciąg zapytania (na przykład token SAS) używany z parametrem TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="e00db-164">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="e00db-165">Czy będzie używana w przypadku szablonów połączonych</span><span class="sxs-lookup"><span data-stu-id="e00db-165">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="e00db-166">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="e00db-166">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="e00db-167">Pomija dynamiczne przetwarzanie parametrów programu PowerShell, które sprawdza, czy podany parametr szablonu zawiera wszystkie niezbędne parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="e00db-167">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="e00db-168">To sprawdzenie spowoduje monitowanie użytkownika o podanie wartości dla brakujących parametrów, ale podanie parametru -SkipTemplateParameterPrompt spowoduje natychmiastowe zignorowanie tego monitu i błędu, jeśli znaleziono, że parametr nie jest powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="e00db-168">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="e00db-169">W przypadku skryptów nieinterakcyjnych można udostępnić komunikat "SkipTemplateParameterPrompt" w celu zapewnienia lepszego komunikatu o błędzie w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="e00db-169">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="e00db-170">— Tag</span><span class="sxs-lookup"><span data-stu-id="e00db-170">-Tag</span></span>
<span data-ttu-id="e00db-171">Tagi do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e00db-171">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="e00db-172">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e00db-172">-TemplateFile</span></span>
<span data-ttu-id="e00db-173">Ścieżka lokalna do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="e00db-173">Local path to the template file.</span></span>

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

### <span data-ttu-id="e00db-174">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="e00db-174">-TemplateObject</span></span>
<span data-ttu-id="e00db-175">Tabela skrótów reprezentująca szablon.</span><span class="sxs-lookup"><span data-stu-id="e00db-175">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="e00db-176">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e00db-176">-TemplateParameterFile</span></span>
<span data-ttu-id="e00db-177">Plik z parametrami szablonu.</span><span class="sxs-lookup"><span data-stu-id="e00db-177">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="e00db-178">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e00db-178">-TemplateParameterObject</span></span>
<span data-ttu-id="e00db-179">Tabela skrótów reprezentująca parametry.</span><span class="sxs-lookup"><span data-stu-id="e00db-179">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="e00db-180">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e00db-180">-TemplateParameterUri</span></span>
<span data-ttu-id="e00db-181">Uri do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="e00db-181">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="e00db-182">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="e00db-182">-TemplateSpecId</span></span>
<span data-ttu-id="e00db-183">Identyfikator zasobu szablonuSpecyfik do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e00db-183">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="e00db-184">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e00db-184">-TemplateUri</span></span>
<span data-ttu-id="e00db-185">Uri do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="e00db-185">Uri to the template file.</span></span>

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

### <span data-ttu-id="e00db-186">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="e00db-186">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="e00db-187">Typy zmian zasobów rozdzielane przecinkami, które mają być wykluczone What-If wyników.</span><span class="sxs-lookup"><span data-stu-id="e00db-187">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="e00db-188">Ma zastosowanie, gdy jest ustawiony przełącznik -WhatIf lub -Confirm.</span><span class="sxs-lookup"><span data-stu-id="e00db-188">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="e00db-189">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="e00db-189">-WhatIfResultFormat</span></span>
<span data-ttu-id="e00db-190">Format What-If wynik.</span><span class="sxs-lookup"><span data-stu-id="e00db-190">The What-If result format.</span></span> <span data-ttu-id="e00db-191">Ma zastosowanie, gdy jest ustawiony przełącznik -WhatIf lub -Confirm.</span><span class="sxs-lookup"><span data-stu-id="e00db-191">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="e00db-192">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e00db-192">-Confirm</span></span>
<span data-ttu-id="e00db-193">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e00db-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e00db-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e00db-194">-WhatIf</span></span>
<span data-ttu-id="e00db-195">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e00db-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e00db-196">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e00db-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e00db-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e00db-197">CommonParameters</span></span>
<span data-ttu-id="e00db-198">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e00db-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e00db-199">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e00db-199">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e00db-200">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e00db-200">INPUTS</span></span>

### <span data-ttu-id="e00db-201">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e00db-201">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e00db-202">System.String</span><span class="sxs-lookup"><span data-stu-id="e00db-202">System.String</span></span>

## <span data-ttu-id="e00db-203">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e00db-203">OUTPUTS</span></span>

### <span data-ttu-id="e00db-204">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="e00db-204">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="e00db-205">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e00db-205">NOTES</span></span>

## <span data-ttu-id="e00db-206">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e00db-206">RELATED LINKS</span></span>
