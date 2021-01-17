---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367339"
---
# <span data-ttu-id="ea717-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ea717-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="ea717-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea717-102">SYNOPSIS</span></span>
<span data-ttu-id="ea717-103">Sprawdza poprawność wdrożenia w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="ea717-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="ea717-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea717-104">SYNTAX</span></span>

### <span data-ttu-id="ea717-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea717-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea717-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ea717-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea717-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ea717-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea717-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ea717-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea717-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ea717-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea717-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ea717-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea717-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ea717-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea717-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ea717-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea717-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ea717-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea717-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ea717-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea717-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ea717-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea717-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ea717-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea717-117">Opis</span><span class="sxs-lookup"><span data-stu-id="ea717-117">DESCRIPTION</span></span>
<span data-ttu-id="ea717-118">Polecenie cmdlet **test-AzManagementGroupDeployment** określa, czy szablon wdrożenia i jego wartości parametrów są prawidłowe w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="ea717-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="ea717-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea717-119">EXAMPLES</span></span>

### <span data-ttu-id="ea717-120">Przykład 1: Testowanie wdrożenia za pomocą szablonu niestandardowego i pliku parametrów</span><span class="sxs-lookup"><span data-stu-id="ea717-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="ea717-121">To polecenie testuje wdrożenie w grupie zarządzania "myMG" przy użyciu danego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="ea717-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="ea717-122">Przykład 2: Testowanie wdrożenia za pomocą obiektu szablonu niestandardowego i pliku parametrów</span><span class="sxs-lookup"><span data-stu-id="ea717-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="ea717-123">To polecenie testuje wdrożenie w grupie zarządzania "myMG" przy użyciu obiektu Hashtable znajdującego się w pamięci, utworzonego z danego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="ea717-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="ea717-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea717-124">PARAMETERS</span></span>

### <span data-ttu-id="ea717-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea717-125">-DefaultProfile</span></span>
<span data-ttu-id="ea717-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea717-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea717-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ea717-127">-Location</span></span>
<span data-ttu-id="ea717-128">Lokalizacja przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ea717-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="ea717-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ea717-129">-ManagementGroupId</span></span>
<span data-ttu-id="ea717-130">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="ea717-130">The management group id.</span></span>

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

### <span data-ttu-id="ea717-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="ea717-131">-Pre</span></span>
<span data-ttu-id="ea717-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="ea717-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ea717-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="ea717-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="ea717-134">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="ea717-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="ea717-135">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="ea717-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="ea717-136">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="ea717-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="ea717-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="ea717-137">-TemplateFile</span></span>
<span data-ttu-id="ea717-138">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="ea717-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="ea717-139">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="ea717-139">-TemplateObject</span></span>
<span data-ttu-id="ea717-140">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="ea717-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="ea717-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="ea717-141">-TemplateParameterFile</span></span>
<span data-ttu-id="ea717-142">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="ea717-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="ea717-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="ea717-143">-TemplateParameterObject</span></span>
<span data-ttu-id="ea717-144">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="ea717-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="ea717-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="ea717-145">-TemplateParameterUri</span></span>
<span data-ttu-id="ea717-146">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="ea717-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="ea717-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="ea717-147">-TemplateUri</span></span>
<span data-ttu-id="ea717-148">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="ea717-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="ea717-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea717-149">CommonParameters</span></span>
<span data-ttu-id="ea717-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea717-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea717-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea717-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea717-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea717-152">INPUTS</span></span>

### <span data-ttu-id="ea717-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ea717-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ea717-154">System. String</span><span class="sxs-lookup"><span data-stu-id="ea717-154">System.String</span></span>

## <span data-ttu-id="ea717-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea717-155">OUTPUTS</span></span>

### <span data-ttu-id="ea717-156">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="ea717-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="ea717-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea717-157">NOTES</span></span>

## <span data-ttu-id="ea717-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea717-158">RELATED LINKS</span></span>
