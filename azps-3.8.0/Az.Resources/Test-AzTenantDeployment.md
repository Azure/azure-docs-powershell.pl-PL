---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 60db8b7b544b63e29b4834676da946ebbf6c39c3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050666"
---
# <span data-ttu-id="e6744-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e6744-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="e6744-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6744-102">SYNOPSIS</span></span>
<span data-ttu-id="e6744-103">Sprawdza poprawność wdrożenia w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e6744-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="e6744-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6744-104">SYNTAX</span></span>

### <span data-ttu-id="e6744-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e6744-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6744-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e6744-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6744-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e6744-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6744-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e6744-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6744-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e6744-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6744-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e6744-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6744-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e6744-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6744-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e6744-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6744-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e6744-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6744-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e6744-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6744-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e6744-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6744-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e6744-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6744-117">Opis</span><span class="sxs-lookup"><span data-stu-id="e6744-117">DESCRIPTION</span></span>
<span data-ttu-id="e6744-118">Polecenie cmdlet **test-AzTenantDeployment** określa, czy szablon wdrożenia i jego wartości parametrów są prawidłowe w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e6744-118">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="e6744-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6744-119">EXAMPLES</span></span>

### <span data-ttu-id="e6744-120">Przykład 1: Testowanie wdrożenia za pomocą szablonu niestandardowego i pliku parametrów</span><span class="sxs-lookup"><span data-stu-id="e6744-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="e6744-121">To polecenie testuje wdrożenie w bieżącym zakresie dzierżawy przy użyciu danego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="e6744-121">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="e6744-122">Przykład 2: Testowanie wdrożenia za pomocą obiektu szablonu niestandardowego i pliku parametrów</span><span class="sxs-lookup"><span data-stu-id="e6744-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="e6744-123">To polecenie testuje wdrożenie w bieżącym zakresie, korzystając z elementu Hashtable znajdującego się w pamięci, utworzonego z danego pliku szablonu i pliku parametru.</span><span class="sxs-lookup"><span data-stu-id="e6744-123">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="e6744-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6744-124">PARAMETERS</span></span>

### <span data-ttu-id="e6744-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e6744-125">-ApiVersion</span></span>
<span data-ttu-id="e6744-126">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="e6744-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e6744-127">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="e6744-127">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6744-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6744-128">-DefaultProfile</span></span>
<span data-ttu-id="e6744-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6744-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6744-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e6744-130">-Location</span></span>
<span data-ttu-id="e6744-131">Lokalizacja przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e6744-131">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6744-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="e6744-132">-Pre</span></span>
<span data-ttu-id="e6744-133">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="e6744-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6744-134">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="e6744-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="e6744-135">Pomija przetwarzanie parametrów dynamicznych programu PowerShell, które sprawdzają, czy podany parametr szablonu zawiera wszystkie wymagane parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="e6744-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="e6744-136">Ten test spowoduje wyświetlenie monitu o podanie wartości dla brakujących parametrów, ale podanie parametru-SkipTemplateParameterPrompt zignoruje ten monit i natychmiast przeprowadzi komunikat o błędzie, jeśli znaleziono parametr, który nie ma być powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="e6744-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="e6744-137">W przypadku skryptów nieinterakcyjnych można zapewnić lepsze komunikaty o błędach w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="e6744-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6744-138">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e6744-138">-TemplateFile</span></span>
<span data-ttu-id="e6744-139">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="e6744-139">Local path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6744-140">-Templateobject</span><span class="sxs-lookup"><span data-stu-id="e6744-140">-TemplateObject</span></span>
<span data-ttu-id="e6744-141">Tabela skrótów, która reprezentuje szablon.</span><span class="sxs-lookup"><span data-stu-id="e6744-141">A hash table which represents the template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6744-142">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e6744-142">-TemplateParameterFile</span></span>
<span data-ttu-id="e6744-143">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="e6744-143">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6744-144">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e6744-144">-TemplateParameterObject</span></span>
<span data-ttu-id="e6744-145">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="e6744-145">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6744-146">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e6744-146">-TemplateParameterUri</span></span>
<span data-ttu-id="e6744-147">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="e6744-147">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6744-148">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e6744-148">-TemplateUri</span></span>
<span data-ttu-id="e6744-149">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="e6744-149">Uri to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6744-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6744-150">CommonParameters</span></span>
<span data-ttu-id="e6744-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6744-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6744-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6744-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6744-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6744-153">INPUTS</span></span>

### <span data-ttu-id="e6744-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6744-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e6744-155">System. String</span><span class="sxs-lookup"><span data-stu-id="e6744-155">System.String</span></span>

## <span data-ttu-id="e6744-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6744-156">OUTPUTS</span></span>

### <span data-ttu-id="e6744-157">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="e6744-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="e6744-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6744-158">NOTES</span></span>

## <span data-ttu-id="e6744-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6744-159">RELATED LINKS</span></span>
