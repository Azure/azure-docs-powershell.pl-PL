---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 5ee86c91b1dc1354b078b727e3bc9ebfe5a43bfe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178739"
---
# <span data-ttu-id="75d5c-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="75d5c-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="75d5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="75d5c-103">Sprawdza poprawność wdrożenia grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="75d5c-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="75d5c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="75d5c-104">SYNTAX</span></span>

### <span data-ttu-id="75d5c-105">ByTemplateFileWithNoParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="75d5c-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d5c-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="75d5c-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d5c-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="75d5c-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d5c-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="75d5c-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d5c-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="75d5c-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d5c-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="75d5c-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d5c-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="75d5c-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d5c-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="75d5c-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d5c-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="75d5c-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d5c-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="75d5c-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d5c-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="75d5c-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d5c-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="75d5c-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75d5c-117">OPIS</span><span class="sxs-lookup"><span data-stu-id="75d5c-117">DESCRIPTION</span></span>
<span data-ttu-id="75d5c-118">Polecenie cmdlet **Test-AzResourceGroupDeployment** określa, czy szablon wdrażania grupy zasobów platformy Azure i jego wartości parametrów są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="75d5c-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="75d5c-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="75d5c-119">EXAMPLES</span></span>

### <span data-ttu-id="75d5c-120">Przykład 1. Testowanie wdrożenia z niestandardowym obiektem szablonu i plikiem parametrów</span><span class="sxs-lookup"><span data-stu-id="75d5c-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="75d5c-121">To polecenie służy do testowania wdrożenia w danej grupie zasobów przy użyciu skrótu w pamięci utworzonego na podstawie pliku danego szablonu i pliku parametru.</span><span class="sxs-lookup"><span data-stu-id="75d5c-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="75d5c-122">Przykład 2. Testowanie wdrożenia za pośrednictwem pliku szablonu i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="75d5c-122">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="75d5c-123">To polecenie służy do testowania wdrożenia w danej grupie zasobów i zasobie przy użyciu dostarczonego pliku szablonu i pliku parametru.</span><span class="sxs-lookup"><span data-stu-id="75d5c-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="75d5c-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75d5c-124">PARAMETERS</span></span>

### <span data-ttu-id="75d5c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d5c-125">-DefaultProfile</span></span>
<span data-ttu-id="75d5c-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="75d5c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75d5c-127">— tryb</span><span class="sxs-lookup"><span data-stu-id="75d5c-127">-Mode</span></span>
<span data-ttu-id="75d5c-128">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="75d5c-128">Specifies the deployment mode.</span></span>
<span data-ttu-id="75d5c-129">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="75d5c-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75d5c-130">Przyrostowe</span><span class="sxs-lookup"><span data-stu-id="75d5c-130">Incremental</span></span>
- <span data-ttu-id="75d5c-131">Ukończ</span><span class="sxs-lookup"><span data-stu-id="75d5c-131">Complete</span></span>

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

### <span data-ttu-id="75d5c-132">— Przed</span><span class="sxs-lookup"><span data-stu-id="75d5c-132">-Pre</span></span>
<span data-ttu-id="75d5c-133">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="75d5c-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="75d5c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d5c-134">-ResourceGroupName</span></span>
<span data-ttu-id="75d5c-135">Określa nazwę grupy zasobów do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="75d5c-135">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="75d5c-136">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="75d5c-136">-RollBackDeploymentName</span></span>
<span data-ttu-id="75d5c-137">Nie należy stosować wycofywania do pomyślnego wdrożenia z podaną nazwą w grupie zasobów, jeśli jest używany typ -RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="75d5c-137">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="75d5c-138">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="75d5c-138">-RollbackToLastDeployment</span></span>
<span data-ttu-id="75d5c-139">W przypadku użycia parametru -RollBackDeploymentName nie należy stosować wycofywania do ostatniego pomyślnego wdrożenia w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="75d5c-139">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="75d5c-140">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="75d5c-140">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="75d5c-141">Pomija dynamiczne przetwarzanie parametrów programu PowerShell, które sprawdza, czy podany parametr szablonu zawiera wszystkie niezbędne parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="75d5c-141">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="75d5c-142">To sprawdzenie spowoduje monitowanie użytkownika o podanie wartości dla brakujących parametrów, ale podanie parametru -SkipTemplateParameterPrompt spowoduje natychmiastowe zignorowanie tego monitu i błędu, jeśli nie zostanie znaleziony parametr powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="75d5c-142">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="75d5c-143">W przypadku skryptów nieinterakcyjnych można udostępnić komunikat "SkipTemplateParameterPrompt" w celu zapewnienia lepszego komunikatu o błędzie w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="75d5c-143">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="75d5c-144">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="75d5c-144">-TemplateFile</span></span>
<span data-ttu-id="75d5c-145">Określa pełną ścieżkę pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="75d5c-145">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="75d5c-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="75d5c-146">-TemplateObject</span></span>
<span data-ttu-id="75d5c-147">Tabela skrótów reprezentująca szablon.</span><span class="sxs-lookup"><span data-stu-id="75d5c-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="75d5c-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="75d5c-148">-TemplateParameterFile</span></span>
<span data-ttu-id="75d5c-149">Określa pełną ścieżkę pliku JSON zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="75d5c-149">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="75d5c-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="75d5c-150">-TemplateParameterObject</span></span>
<span data-ttu-id="75d5c-151">Określa tabelę skrótów z nazwami i wartościami parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="75d5c-151">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="75d5c-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="75d5c-152">-TemplateParameterUri</span></span>
<span data-ttu-id="75d5c-153">Określa URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="75d5c-153">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="75d5c-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="75d5c-154">-TemplateUri</span></span>
<span data-ttu-id="75d5c-155">Określa URI pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="75d5c-155">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="75d5c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d5c-156">CommonParameters</span></span>
<span data-ttu-id="75d5c-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d5c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d5c-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75d5c-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d5c-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75d5c-159">INPUTS</span></span>

### <span data-ttu-id="75d5c-160">System.String</span><span class="sxs-lookup"><span data-stu-id="75d5c-160">System.String</span></span>

### <span data-ttu-id="75d5c-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="75d5c-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="75d5c-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="75d5c-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="75d5c-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75d5c-163">OUTPUTS</span></span>

### <span data-ttu-id="75d5c-164">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="75d5c-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="75d5c-165">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="75d5c-165">NOTES</span></span>

## <span data-ttu-id="75d5c-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75d5c-166">RELATED LINKS</span></span>

[<span data-ttu-id="75d5c-167">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="75d5c-167">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="75d5c-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="75d5c-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="75d5c-169">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="75d5c-169">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="75d5c-170">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="75d5c-170">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


