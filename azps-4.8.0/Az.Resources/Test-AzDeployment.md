---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: d6222c0e1ecd6eee39b65ac65e74707d1d64ef17
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219887"
---
# <span data-ttu-id="d93fd-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d93fd-101">Test-AzDeployment</span></span>

## <span data-ttu-id="d93fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d93fd-102">SYNOPSIS</span></span>
<span data-ttu-id="d93fd-103">Sprawdza poprawność wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d93fd-103">Validates a deployment.</span></span>

## <span data-ttu-id="d93fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d93fd-104">SYNTAX</span></span>

### <span data-ttu-id="d93fd-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d93fd-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d93fd-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d93fd-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d93fd-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d93fd-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d93fd-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="d93fd-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d93fd-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d93fd-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d93fd-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d93fd-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d93fd-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="d93fd-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d93fd-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d93fd-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d93fd-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d93fd-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d93fd-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="d93fd-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d93fd-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d93fd-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d93fd-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="d93fd-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d93fd-117">Opis</span><span class="sxs-lookup"><span data-stu-id="d93fd-117">DESCRIPTION</span></span>
<span data-ttu-id="d93fd-118">Polecenie cmdlet **test-AzDeployment** określa, czy szablon wdrożenia i jego wartości parametrów są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="d93fd-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="d93fd-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d93fd-119">EXAMPLES</span></span>

### <span data-ttu-id="d93fd-120">Przykład 1: Testowanie wdrożenia za pomocą szablonu niestandardowego i pliku parametrów</span><span class="sxs-lookup"><span data-stu-id="d93fd-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="d93fd-121">To polecenie testuje wdrożenie w bieżącym zakresie subskrypcji przy użyciu danego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="d93fd-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="d93fd-122">Przykład 2: Testowanie wdrożenia za pomocą obiektu szablonu niestandardowego i pliku parametrów</span><span class="sxs-lookup"><span data-stu-id="d93fd-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="d93fd-123">To polecenie testuje wdrożenie w bieżącym zakresie subskrypcji przy użyciu obiektu Hashtable w pamięci utworzonej z danego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="d93fd-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="d93fd-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d93fd-124">PARAMETERS</span></span>

### <span data-ttu-id="d93fd-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d93fd-125">-ApiVersion</span></span>
<span data-ttu-id="d93fd-126">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="d93fd-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d93fd-127">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="d93fd-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d93fd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d93fd-128">-DefaultProfile</span></span>
<span data-ttu-id="d93fd-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d93fd-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d93fd-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d93fd-130">-Location</span></span>
<span data-ttu-id="d93fd-131">Lokalizacja przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d93fd-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="d93fd-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="d93fd-132">-Pre</span></span>
<span data-ttu-id="d93fd-133">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="d93fd-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d93fd-134">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="d93fd-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="d93fd-135">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="d93fd-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="d93fd-136">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="d93fd-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="d93fd-137">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="d93fd-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="d93fd-138">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d93fd-138">-TemplateFile</span></span>
<span data-ttu-id="d93fd-139">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="d93fd-139">Local path to the template file.</span></span>

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

### <span data-ttu-id="d93fd-140">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="d93fd-140">-TemplateObject</span></span>
<span data-ttu-id="d93fd-141">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="d93fd-141">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="d93fd-142">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="d93fd-142">-TemplateParameterFile</span></span>
<span data-ttu-id="d93fd-143">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="d93fd-143">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="d93fd-144">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="d93fd-144">-TemplateParameterObject</span></span>
<span data-ttu-id="d93fd-145">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="d93fd-145">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="d93fd-146">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="d93fd-146">-TemplateParameterUri</span></span>
<span data-ttu-id="d93fd-147">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="d93fd-147">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="d93fd-148">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="d93fd-148">-TemplateUri</span></span>
<span data-ttu-id="d93fd-149">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="d93fd-149">Uri to the template file.</span></span>

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

### <span data-ttu-id="d93fd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d93fd-150">CommonParameters</span></span>
<span data-ttu-id="d93fd-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d93fd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d93fd-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d93fd-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d93fd-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d93fd-153">INPUTS</span></span>

### <span data-ttu-id="d93fd-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d93fd-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d93fd-155">System. String</span><span class="sxs-lookup"><span data-stu-id="d93fd-155">System.String</span></span>

## <span data-ttu-id="d93fd-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d93fd-156">OUTPUTS</span></span>

### <span data-ttu-id="d93fd-157">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="d93fd-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="d93fd-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d93fd-158">NOTES</span></span>

## <span data-ttu-id="d93fd-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d93fd-159">RELATED LINKS</span></span>
