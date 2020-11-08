---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 97a16dcebe2730fef1d770fe8cbbf54d5488b49a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050669"
---
# <span data-ttu-id="7f4ad-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7f4ad-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="7f4ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f4ad-102">SYNOPSIS</span></span>
<span data-ttu-id="7f4ad-103">Sprawdza poprawność wdrożenia grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="7f4ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f4ad-104">SYNTAX</span></span>

### <span data-ttu-id="7f4ad-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7f4ad-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f4ad-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7f4ad-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4ad-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7f4ad-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4ad-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="7f4ad-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4ad-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7f4ad-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4ad-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7f4ad-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4ad-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="7f4ad-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4ad-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7f4ad-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4ad-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7f4ad-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4ad-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="7f4ad-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f4ad-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7f4ad-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f4ad-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="7f4ad-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f4ad-117">Opis</span><span class="sxs-lookup"><span data-stu-id="7f4ad-117">DESCRIPTION</span></span>
<span data-ttu-id="7f4ad-118">Polecenie cmdlet **test-AzResourceGroupDeployment** określa, czy szablon wdrożenia grup zasobów platformy Azure i jego wartości parametrów są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="7f4ad-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f4ad-119">EXAMPLES</span></span>

### <span data-ttu-id="7f4ad-120">Przykład 1: Testowanie wdrożenia za pomocą obiektu szablonu niestandardowego i pliku parametrów</span><span class="sxs-lookup"><span data-stu-id="7f4ad-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="7f4ad-121">To polecenie testuje wdrożenie w danej grupie zasobów przy użyciu obiektu Hashtable w pamięci utworzonej z danego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="7f4ad-122">Przykład 2: Testowanie wdrożenia za pośrednictwem obiektu szablonu i pliku parametrów</span><span class="sxs-lookup"><span data-stu-id="7f4ad-122">Example 2: Test deployment via template file and parameter object</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name testDeployment1 -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="7f4ad-123">To polecenie testuje wdrożenie w danej grupie zasobów i zasobie przy użyciu podanego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="7f4ad-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f4ad-124">PARAMETERS</span></span>

### <span data-ttu-id="7f4ad-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7f4ad-125">-ApiVersion</span></span>
<span data-ttu-id="7f4ad-126">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="7f4ad-127">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="7f4ad-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f4ad-128">-DefaultProfile</span></span>
<span data-ttu-id="7f4ad-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7f4ad-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f4ad-130">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="7f4ad-130">-Mode</span></span>
<span data-ttu-id="7f4ad-131">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="7f4ad-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7f4ad-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f4ad-133">Dodatkowe</span><span class="sxs-lookup"><span data-stu-id="7f4ad-133">Incremental</span></span>
- <span data-ttu-id="7f4ad-134">Pełni</span><span class="sxs-lookup"><span data-stu-id="7f4ad-134">Complete</span></span>

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

### <span data-ttu-id="7f4ad-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="7f4ad-135">-Pre</span></span>
<span data-ttu-id="7f4ad-136">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7f4ad-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f4ad-137">-ResourceGroupName</span></span>
<span data-ttu-id="7f4ad-138">Określa nazwę grupy zasobów do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-138">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="7f4ad-139">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="7f4ad-139">-RollBackDeploymentName</span></span>
<span data-ttu-id="7f4ad-140">Wycofanie do poprawnego wdrożenia o podanej nazwie w grupie zasobów nie powinno być używane, jeśli jest używana funkcja-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-140">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="7f4ad-141">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="7f4ad-141">-RollbackToLastDeployment</span></span>
<span data-ttu-id="7f4ad-142">Wycofanie do ostatniego poprawnego wdrożenia w grupie zasobów nie powinno być dostępne, jeśli jest używana funkcja-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-142">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="7f4ad-143">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="7f4ad-143">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="7f4ad-144">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-144">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="7f4ad-145">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-145">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="7f4ad-146">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-146">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="7f4ad-147">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="7f4ad-147">-TemplateFile</span></span>
<span data-ttu-id="7f4ad-148">Określa pełną ścieżkę pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-148">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="7f4ad-149">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="7f4ad-149">-TemplateObject</span></span>
<span data-ttu-id="7f4ad-150">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-150">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="7f4ad-151">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="7f4ad-151">-TemplateParameterFile</span></span>
<span data-ttu-id="7f4ad-152">Określa pełną ścieżkę pliku JSON zawierającego nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-152">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="7f4ad-153">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="7f4ad-153">-TemplateParameterObject</span></span>
<span data-ttu-id="7f4ad-154">Określa tabelę skrótów zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-154">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="7f4ad-155">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="7f4ad-155">-TemplateParameterUri</span></span>
<span data-ttu-id="7f4ad-156">Określa identyfikator URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-156">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="7f4ad-157">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="7f4ad-157">-TemplateUri</span></span>
<span data-ttu-id="7f4ad-158">Określa identyfikator URI pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-158">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="7f4ad-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f4ad-159">CommonParameters</span></span>
<span data-ttu-id="7f4ad-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f4ad-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f4ad-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f4ad-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f4ad-162">INPUTS</span></span>

### <span data-ttu-id="7f4ad-163">System. String</span><span class="sxs-lookup"><span data-stu-id="7f4ad-163">System.String</span></span>

### <span data-ttu-id="7f4ad-164">Microsoft. Azure. Management. ResourceManager. modele. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="7f4ad-164">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="7f4ad-165">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7f4ad-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7f4ad-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f4ad-166">OUTPUTS</span></span>

### <span data-ttu-id="7f4ad-167">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="7f4ad-167">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="7f4ad-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f4ad-168">NOTES</span></span>

## <span data-ttu-id="7f4ad-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f4ad-169">RELATED LINKS</span></span>

[<span data-ttu-id="7f4ad-170">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7f4ad-170">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="7f4ad-171">Nowe — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7f4ad-171">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="7f4ad-172">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7f4ad-172">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="7f4ad-173">Zatrzymaj — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7f4ad-173">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


