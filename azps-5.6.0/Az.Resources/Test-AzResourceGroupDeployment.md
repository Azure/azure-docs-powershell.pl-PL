---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 0e0d4645901f60f9e290d197a47b133d6bf3db8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976458"
---
# <span data-ttu-id="0e24e-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0e24e-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="0e24e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e24e-102">SYNOPSIS</span></span>
<span data-ttu-id="0e24e-103">Sprawdza poprawność wdrożenia grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e24e-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="0e24e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e24e-104">SYNTAX</span></span>

### <span data-ttu-id="0e24e-105">ByTemplateFileWithNoParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0e24e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e24e-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0e24e-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e24e-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0e24e-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e24e-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0e24e-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e24e-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0e24e-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e24e-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0e24e-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e24e-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0e24e-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e24e-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="0e24e-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e24e-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0e24e-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e24e-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0e24e-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e24e-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0e24e-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e24e-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="0e24e-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0e24e-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0e24e-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e24e-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0e24e-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e24e-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="0e24e-119">ByTemplateSpecResourceId</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e24e-120">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e24e-120">DESCRIPTION</span></span>
<span data-ttu-id="0e24e-121">Polecenie **cmdlet Test-AzResourceGroupDeployment** określa, czy szablon wdrażania grupy zasobów platformy Azure i jego wartości parametrów są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="0e24e-121">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="0e24e-122">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e24e-122">EXAMPLES</span></span>

### <span data-ttu-id="0e24e-123">Przykład 1. Testowanie wdrożenia z niestandardowym obiektem szablonu i plikiem parametrów</span><span class="sxs-lookup"><span data-stu-id="0e24e-123">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="0e24e-124">To polecenie służy do testowania wdrożenia w danej grupie zasobów przy użyciu skrótu w pamięci utworzonego na podstawie pliku danego szablonu i pliku parametru.</span><span class="sxs-lookup"><span data-stu-id="0e24e-124">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="0e24e-125">Przykład 2. Testowanie wdrożenia za pośrednictwem pliku szablonu i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="0e24e-125">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="0e24e-126">To polecenie służy do testowania wdrożenia w danej grupie zasobów i zasobie przy użyciu dostarczonego pliku szablonu i pliku parametru.</span><span class="sxs-lookup"><span data-stu-id="0e24e-126">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="0e24e-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e24e-127">PARAMETERS</span></span>

### <span data-ttu-id="0e24e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e24e-128">-DefaultProfile</span></span>
<span data-ttu-id="0e24e-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0e24e-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e24e-130">— tryb</span><span class="sxs-lookup"><span data-stu-id="0e24e-130">-Mode</span></span>
<span data-ttu-id="0e24e-131">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="0e24e-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="0e24e-132">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0e24e-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0e24e-133">Przyrostowe</span><span class="sxs-lookup"><span data-stu-id="0e24e-133">Incremental</span></span>
- <span data-ttu-id="0e24e-134">Ukończ</span><span class="sxs-lookup"><span data-stu-id="0e24e-134">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e24e-135">— Przed</span><span class="sxs-lookup"><span data-stu-id="0e24e-135">-Pre</span></span>
<span data-ttu-id="0e24e-136">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="0e24e-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0e24e-137">-QueryString</span><span class="sxs-lookup"><span data-stu-id="0e24e-137">-QueryString</span></span>
<span data-ttu-id="0e24e-138">Ciąg zapytania (na przykład token SAS) używany z parametrem TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="0e24e-138">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="0e24e-139">Czy będzie używana w przypadku szablonów połączonych</span><span class="sxs-lookup"><span data-stu-id="0e24e-139">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="0e24e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e24e-140">-ResourceGroupName</span></span>
<span data-ttu-id="0e24e-141">Określa nazwę testowej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e24e-141">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="0e24e-142">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="0e24e-142">-RollBackDeploymentName</span></span>
<span data-ttu-id="0e24e-143">Nie należy stosować wycofywania do pomyślnego wdrożenia z podaną nazwą w grupie zasobów, jeśli jest używany typ -RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="0e24e-143">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="0e24e-144">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="0e24e-144">-RollbackToLastDeployment</span></span>
<span data-ttu-id="0e24e-145">W przypadku użycia parametru -RollBackDeploymentName nie należy stosować wycofywania do ostatniego pomyślnego wdrożenia w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e24e-145">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="0e24e-146">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="0e24e-146">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="0e24e-147">Pomija dynamiczne przetwarzanie parametrów programu PowerShell, które sprawdza, czy podany parametr szablonu zawiera wszystkie niezbędne parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="0e24e-147">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="0e24e-148">To sprawdzenie spowoduje monitowanie użytkownika o podanie wartości dla brakujących parametrów, ale podanie parametru -SkipTemplateParameterPrompt spowoduje natychmiastowe zignorowanie tego monitu i błędu, jeśli znaleziono, że parametr nie jest powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="0e24e-148">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="0e24e-149">W przypadku skryptów nieinterakcyjnych można udostępnić komunikat -SkipTemplateParameterPrompt w celu zapewnienia lepszego komunikatu o błędzie w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="0e24e-149">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="0e24e-150">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="0e24e-150">-TemplateFile</span></span>
<span data-ttu-id="0e24e-151">Określa pełną ścieżkę pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="0e24e-151">Specifies the full path of a template file.</span></span> <span data-ttu-id="0e24e-152">Obsługiwany typ pliku szablonu: json i biceps.</span><span class="sxs-lookup"><span data-stu-id="0e24e-152">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="0e24e-153">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="0e24e-153">-TemplateObject</span></span>
<span data-ttu-id="0e24e-154">Tabela skrótów reprezentująca szablon.</span><span class="sxs-lookup"><span data-stu-id="0e24e-154">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="0e24e-155">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="0e24e-155">-TemplateParameterFile</span></span>
<span data-ttu-id="0e24e-156">Określa pełną ścieżkę pliku JSON zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="0e24e-156">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="0e24e-157">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="0e24e-157">-TemplateParameterObject</span></span>
<span data-ttu-id="0e24e-158">Określa tabelę skrótów z nazwami i wartościami parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="0e24e-158">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="0e24e-159">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="0e24e-159">-TemplateParameterUri</span></span>
<span data-ttu-id="0e24e-160">Określa URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="0e24e-160">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="0e24e-161">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="0e24e-161">-TemplateSpecId</span></span>
<span data-ttu-id="0e24e-162">Identyfikator zasobu szablonuOkreślony, który ma zostać wdrożony.</span><span class="sxs-lookup"><span data-stu-id="0e24e-162">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="0e24e-163">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="0e24e-163">-TemplateUri</span></span>
<span data-ttu-id="0e24e-164">Określa URI pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="0e24e-164">Specifies the URI of a template file.</span></span>

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

### <span data-ttu-id="0e24e-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e24e-165">CommonParameters</span></span>
<span data-ttu-id="0e24e-166">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e24e-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e24e-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e24e-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e24e-168">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e24e-168">INPUTS</span></span>

### <span data-ttu-id="0e24e-169">System.String</span><span class="sxs-lookup"><span data-stu-id="0e24e-169">System.String</span></span>

### <span data-ttu-id="0e24e-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="0e24e-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="0e24e-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0e24e-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0e24e-172">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e24e-172">OUTPUTS</span></span>

### <span data-ttu-id="0e24e-173">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="0e24e-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="0e24e-174">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e24e-174">NOTES</span></span>

## <span data-ttu-id="0e24e-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e24e-175">RELATED LINKS</span></span>

[<span data-ttu-id="0e24e-176">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0e24e-176">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="0e24e-177">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0e24e-177">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="0e24e-178">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0e24e-178">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="0e24e-179">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0e24e-179">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


