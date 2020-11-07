---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 182cf4d60cf2b81f5a465f9ffad5d862b09e3787
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708264"
---
# <span data-ttu-id="4aa5c-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="4aa5c-101">Test-AzDeployment</span></span>

## <span data-ttu-id="4aa5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4aa5c-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa5c-103">Sprawdza poprawność wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-103">Validates a deployment.</span></span>

## <span data-ttu-id="4aa5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4aa5c-104">SYNTAX</span></span>

### <span data-ttu-id="4aa5c-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4aa5c-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aa5c-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4aa5c-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4aa5c-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4aa5c-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4aa5c-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4aa5c-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4aa5c-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4aa5c-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4aa5c-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4aa5c-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4aa5c-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4aa5c-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4aa5c-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4aa5c-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4aa5c-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4aa5c-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4aa5c-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4aa5c-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4aa5c-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4aa5c-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aa5c-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4aa5c-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aa5c-117">Opis</span><span class="sxs-lookup"><span data-stu-id="4aa5c-117">DESCRIPTION</span></span>
<span data-ttu-id="4aa5c-118">Polecenie cmdlet **test-AzDeployment** określa, czy szablon wdrożenia i jego wartości parametrów są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="4aa5c-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4aa5c-119">EXAMPLES</span></span>

### <span data-ttu-id="4aa5c-120">Przykład 1: Testowanie wdrożenia za pomocą szablonu niestandardowego i pliku parametrów</span><span class="sxs-lookup"><span data-stu-id="4aa5c-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="4aa5c-121">To polecenie testuje wdrożenie w bieżącym zakresie subskrypcji przy użyciu danego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="4aa5c-122">Przykład 2: Testowanie wdrożenia za pomocą obiektu szablonu niestandardowego i pliku parametrów</span><span class="sxs-lookup"><span data-stu-id="4aa5c-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="4aa5c-123">To polecenie testuje wdrożenie w bieżącym zakresie subskrypcji przy użyciu obiektu Hashtable w pamięci utworzonej z danego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="4aa5c-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4aa5c-124">PARAMETERS</span></span>

### <span data-ttu-id="4aa5c-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4aa5c-125">-ApiVersion</span></span>
<span data-ttu-id="4aa5c-126">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4aa5c-127">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4aa5c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa5c-128">-DefaultProfile</span></span>
<span data-ttu-id="4aa5c-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aa5c-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4aa5c-130">-Location</span></span>
<span data-ttu-id="4aa5c-131">Lokalizacja przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="4aa5c-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="4aa5c-132">-Pre</span></span>
<span data-ttu-id="4aa5c-133">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4aa5c-134">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="4aa5c-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="4aa5c-135">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="4aa5c-136">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="4aa5c-137">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="4aa5c-138">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4aa5c-138">-TemplateFile</span></span>
<span data-ttu-id="4aa5c-139">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-139">Local path to the template file.</span></span>

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

### <span data-ttu-id="4aa5c-140">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="4aa5c-140">-TemplateObject</span></span>
<span data-ttu-id="4aa5c-141">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-141">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="4aa5c-142">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4aa5c-142">-TemplateParameterFile</span></span>
<span data-ttu-id="4aa5c-143">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-143">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="4aa5c-144">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4aa5c-144">-TemplateParameterObject</span></span>
<span data-ttu-id="4aa5c-145">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-145">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="4aa5c-146">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4aa5c-146">-TemplateParameterUri</span></span>
<span data-ttu-id="4aa5c-147">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-147">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="4aa5c-148">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4aa5c-148">-TemplateUri</span></span>
<span data-ttu-id="4aa5c-149">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-149">Uri to the template file.</span></span>

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

### <span data-ttu-id="4aa5c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa5c-150">CommonParameters</span></span>
<span data-ttu-id="4aa5c-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aa5c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa5c-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aa5c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa5c-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4aa5c-153">INPUTS</span></span>

### <span data-ttu-id="4aa5c-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4aa5c-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4aa5c-155">System. String</span><span class="sxs-lookup"><span data-stu-id="4aa5c-155">System.String</span></span>

## <span data-ttu-id="4aa5c-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4aa5c-156">OUTPUTS</span></span>

### <span data-ttu-id="4aa5c-157">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="4aa5c-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="4aa5c-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4aa5c-158">NOTES</span></span>

## <span data-ttu-id="4aa5c-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4aa5c-159">RELATED LINKS</span></span>
