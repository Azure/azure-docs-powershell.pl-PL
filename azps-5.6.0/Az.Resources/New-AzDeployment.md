---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 42f68065fb5a1785d0f9a243d0165bc72125743d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953082"
---
# <span data-ttu-id="ff686-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="ff686-101">New-AzDeployment</span></span>

## <span data-ttu-id="ff686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff686-102">SYNOPSIS</span></span>
<span data-ttu-id="ff686-103">Tworzenie wdrożenia</span><span class="sxs-lookup"><span data-stu-id="ff686-103">Create a deployment</span></span>

## <span data-ttu-id="ff686-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ff686-104">SYNTAX</span></span>

### <span data-ttu-id="ff686-105">ByTemplateFileWithNoParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ff686-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff686-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ff686-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff686-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ff686-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff686-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ff686-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff686-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="ff686-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff686-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ff686-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff686-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ff686-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff686-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ff686-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff686-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="ff686-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff686-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ff686-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff686-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ff686-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff686-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ff686-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff686-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="ff686-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff686-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ff686-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff686-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ff686-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff686-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="ff686-120">ByTemplateSpecResourceId</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff686-121">OPIS</span><span class="sxs-lookup"><span data-stu-id="ff686-121">DESCRIPTION</span></span>
<span data-ttu-id="ff686-122">Polecenie **cmdlet New-AzDeployment** dodaje wdrożenie w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ff686-122">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="ff686-123">Obejmuje to zasoby wymagane przez wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="ff686-123">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="ff686-124">Zasób platformy Azure jest jednostką platformy Azure zarządzaną przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ff686-124">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="ff686-125">Zasób może mieszkać w grupie zasobów, na przykład w bazie danych, na serwerze bazy danych, w witrynie internetowej, na komputerze wirtualnym lub na koncie magazynu.</span><span class="sxs-lookup"><span data-stu-id="ff686-125">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="ff686-126">Może też być zasobem na poziomie subskrypcji, na przykład definicją ról, definicją zasad itp.</span><span class="sxs-lookup"><span data-stu-id="ff686-126">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="ff686-127">Aby dodać zasoby do grupy zasobów, użyj funkcji **New-AzResourceGroupDeployment,** która tworzy wdrożenie w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ff686-127">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="ff686-128">Polecenie **cmdlet New-AzDeployment** tworzy wdrożenie w bieżącym zakresie subskrypcji, które wdraża zasoby na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ff686-128">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="ff686-129">Aby dodać wdrożenie w subskrypcji, określ lokalizację i szablon.</span><span class="sxs-lookup"><span data-stu-id="ff686-129">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="ff686-130">Ta lokalizacja wskazuje usłudze Azure Resource Manager, gdzie mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ff686-130">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="ff686-131">Szablon to ciąg JSON zawierający poszczególne zasoby do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ff686-131">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="ff686-132">Szablon zawiera symbole zastępcze parametrów dla wymaganych zasobów i konfigurowane wartości właściwości, takie jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="ff686-132">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="ff686-133">Aby użyć szablonu niestandardowego dla wdrożenia, określ parametr *TemplateFile* lub *parametr TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="ff686-133">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="ff686-134">Każdy szablon zawiera parametry dotyczące właściwości, które można konfigurować.</span><span class="sxs-lookup"><span data-stu-id="ff686-134">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="ff686-135">Aby określić wartości dla parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="ff686-135">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="ff686-136">Możesz również użyć parametrów szablonu, które są dynamicznie dodawane do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="ff686-136">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="ff686-137">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-) w celu wskazania parametru i użyj klawisza Tab do cyklicznego używania dostępnych parametrów.</span><span class="sxs-lookup"><span data-stu-id="ff686-137">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="ff686-138">Wartości parametrów szablonu w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="ff686-138">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="ff686-139">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ff686-139">EXAMPLES</span></span>

### <span data-ttu-id="ff686-140">Przykład 1. Tworzenie wdrożenia przy użyciu szablonu niestandardowego i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="ff686-140">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="ff686-141">To polecenie tworzy nowe wdrożenie w bieżącym zakresie subskrypcji przy użyciu szablonu niestandardowego i pliku szablonu na dysku z parametrem zdefiniowanych tagów.</span><span class="sxs-lookup"><span data-stu-id="ff686-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="ff686-142">To polecenie używa *parametru TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="ff686-142">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="ff686-143">Używa ona *parametru TemplateVersion* do określenia wersji szablonu.</span><span class="sxs-lookup"><span data-stu-id="ff686-143">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="ff686-144">Przykład 2. Wdrażanie szablonu przechowywanego na koncie magazynu publicznego przy użyciu tokenu uri i SAS</span><span class="sxs-lookup"><span data-stu-id="ff686-144">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```

<span data-ttu-id="ff686-145">To polecenie tworzy nowe wdrożenie przy użyciu szablonu w szablonie TemplateUri, który nie jest publiczny i wymaga parametru tokenu w celu uzyskania dostępu, który zostanie dostarczony przy użyciu parametru QueryString.</span><span class="sxs-lookup"><span data-stu-id="ff686-145">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="ff686-146">Uruchomienie tego polecenia w praktyce uzyskuje dostęp do szablonu przy użyciu adresu https://example.com/example.json?foo URL.</span><span class="sxs-lookup"><span data-stu-id="ff686-146">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="ff686-147">Tej funkcji można użyć, jeśli chcesz użyć szablonu na koncie magazynu, podając token SAS jako zapytanie QueryString</span><span class="sxs-lookup"><span data-stu-id="ff686-147">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="ff686-148">Przykład 3. Tworzenie wdrożenia przy użyciu niestandardowego obiektu szablonu i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="ff686-148">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="ff686-149">To polecenie tworzy nowe wdrożenie w bieżącym zakresie subskrypcji przy użyciu szablonu niestandardowego i pliku szablonu na dysku, który został przekonwertowany na skrót w pamięci.</span><span class="sxs-lookup"><span data-stu-id="ff686-149">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="ff686-150">Pierwsze dwa polecenia odczytają tekst pliku szablonu na dysku i konwertują go na skrót w pamięci.</span><span class="sxs-lookup"><span data-stu-id="ff686-150">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="ff686-151">Ostatnie polecenie używa *parametru TemplateObject* do określenia tej tabeli skrótów i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="ff686-151">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="ff686-152">Używa ona *parametru TemplateVersion* do określenia wersji szablonu.</span><span class="sxs-lookup"><span data-stu-id="ff686-152">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="ff686-153">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff686-153">PARAMETERS</span></span>

### <span data-ttu-id="ff686-154">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ff686-154">-AsJob</span></span>
<span data-ttu-id="ff686-155">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ff686-155">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ff686-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff686-156">-DefaultProfile</span></span>
<span data-ttu-id="ff686-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff686-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff686-158">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="ff686-158">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="ff686-159">Poziom dziennika debugowania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ff686-159">The deployment debug log level.</span></span>

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

### <span data-ttu-id="ff686-160">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ff686-160">-Location</span></span>
<span data-ttu-id="ff686-161">Lokalizacja przechowywania danych wdrożeniowych.</span><span class="sxs-lookup"><span data-stu-id="ff686-161">The location to store deployment data.</span></span>

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

### <span data-ttu-id="ff686-162">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ff686-162">-Name</span></span>
<span data-ttu-id="ff686-163">Nazwa wdrożenia, które zostanie utworzyć.</span><span class="sxs-lookup"><span data-stu-id="ff686-163">The name of the deployment it's going to create.</span></span> <span data-ttu-id="ff686-164">W przypadku, gdy plik szablonu jest podany, domyślnie jest określana jego nazwa domyślna. domyślnie jest to bieżąca godzina, gdy obiekt szablonu jest podany, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="ff686-164">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="ff686-165">— Przed</span><span class="sxs-lookup"><span data-stu-id="ff686-165">-Pre</span></span>
<span data-ttu-id="ff686-166">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ff686-166">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ff686-167">-QueryString</span><span class="sxs-lookup"><span data-stu-id="ff686-167">-QueryString</span></span>
<span data-ttu-id="ff686-168">Ciąg zapytania (na przykład token SAS) używany z parametrem TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="ff686-168">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="ff686-169">Czy będzie używana w przypadku szablonów połączonych</span><span class="sxs-lookup"><span data-stu-id="ff686-169">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="ff686-170">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="ff686-170">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="ff686-171">Pomija dynamiczne przetwarzanie parametrów programu PowerShell, które sprawdza, czy podany parametr szablonu zawiera wszystkie niezbędne parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="ff686-171">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="ff686-172">To sprawdzenie spowoduje monitowanie użytkownika o podanie wartości dla brakujących parametrów, ale podanie parametru -SkipTemplateParameterPrompt spowoduje natychmiastowe zignorowanie tego monitu i błędu, jeśli znaleziono, że parametr nie jest powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="ff686-172">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="ff686-173">W przypadku skryptów nieinterakcyjnych można udostępnić komunikat -SkipTemplateParameterPrompt w celu zapewnienia lepszego komunikatu o błędzie w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="ff686-173">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="ff686-174">— Tag</span><span class="sxs-lookup"><span data-stu-id="ff686-174">-Tag</span></span>
<span data-ttu-id="ff686-175">Tagi do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ff686-175">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="ff686-176">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="ff686-176">-TemplateFile</span></span>
<span data-ttu-id="ff686-177">Ścieżka lokalna do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="ff686-177">Local path to the template file.</span></span> <span data-ttu-id="ff686-178">Obsługiwany typ pliku szablonu: json i biceps.</span><span class="sxs-lookup"><span data-stu-id="ff686-178">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="ff686-179">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="ff686-179">-TemplateObject</span></span>
<span data-ttu-id="ff686-180">Tabela skrótów reprezentująca szablon.</span><span class="sxs-lookup"><span data-stu-id="ff686-180">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="ff686-181">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="ff686-181">-TemplateParameterFile</span></span>
<span data-ttu-id="ff686-182">Plik z parametrami szablonu.</span><span class="sxs-lookup"><span data-stu-id="ff686-182">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="ff686-183">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="ff686-183">-TemplateParameterObject</span></span>
<span data-ttu-id="ff686-184">Tabela skrótów reprezentująca parametry.</span><span class="sxs-lookup"><span data-stu-id="ff686-184">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="ff686-185">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="ff686-185">-TemplateParameterUri</span></span>
<span data-ttu-id="ff686-186">Uri do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="ff686-186">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="ff686-187">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="ff686-187">-TemplateSpecId</span></span>
<span data-ttu-id="ff686-188">Identyfikator zasobu szablonuOkreślony, który ma zostać wdrożony.</span><span class="sxs-lookup"><span data-stu-id="ff686-188">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="ff686-189">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="ff686-189">-TemplateUri</span></span>
<span data-ttu-id="ff686-190">Uri do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="ff686-190">Uri to the template file.</span></span>

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

### <span data-ttu-id="ff686-191">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="ff686-191">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="ff686-192">Typy zmian zasobów rozdzielane przecinkami, które mają być wykluczone What-If wyników.</span><span class="sxs-lookup"><span data-stu-id="ff686-192">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="ff686-193">Ma zastosowanie, gdy jest ustawiony przełącznik -WhatIf lub -Confirm.</span><span class="sxs-lookup"><span data-stu-id="ff686-193">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="ff686-194">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="ff686-194">-WhatIfResultFormat</span></span>
<span data-ttu-id="ff686-195">Format What-If wynik.</span><span class="sxs-lookup"><span data-stu-id="ff686-195">The What-If result format.</span></span>

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

### <span data-ttu-id="ff686-196">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ff686-196">-Confirm</span></span>
<span data-ttu-id="ff686-197">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ff686-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff686-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff686-198">-WhatIf</span></span>
<span data-ttu-id="ff686-199">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff686-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff686-200">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ff686-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff686-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff686-201">CommonParameters</span></span>
<span data-ttu-id="ff686-202">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff686-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff686-203">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff686-203">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff686-204">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff686-204">INPUTS</span></span>

### <span data-ttu-id="ff686-205">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ff686-205">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ff686-206">System.String</span><span class="sxs-lookup"><span data-stu-id="ff686-206">System.String</span></span>

## <span data-ttu-id="ff686-207">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff686-207">OUTPUTS</span></span>

### <span data-ttu-id="ff686-208">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ff686-208">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ff686-209">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ff686-209">NOTES</span></span>

## <span data-ttu-id="ff686-210">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff686-210">RELATED LINKS</span></span>
