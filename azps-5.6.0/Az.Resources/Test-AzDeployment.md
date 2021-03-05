---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 5a7bb411c5b2881361c1f9dfe7e675450f76e318
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962641"
---
# <span data-ttu-id="8892d-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8892d-101">Test-AzDeployment</span></span>

## <span data-ttu-id="8892d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8892d-102">SYNOPSIS</span></span>
<span data-ttu-id="8892d-103">Sprawdza poprawność wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="8892d-103">Validates a deployment.</span></span>

## <span data-ttu-id="8892d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8892d-104">SYNTAX</span></span>

### <span data-ttu-id="8892d-105">ByTemplateFileWithNoParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8892d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8892d-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8892d-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8892d-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8892d-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8892d-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8892d-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8892d-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8892d-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8892d-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8892d-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8892d-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8892d-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8892d-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="8892d-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8892d-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8892d-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8892d-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8892d-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8892d-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8892d-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8892d-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="8892d-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8892d-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8892d-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8892d-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8892d-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8892d-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="8892d-119">ByTemplateSpecResourceId</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8892d-120">OPIS</span><span class="sxs-lookup"><span data-stu-id="8892d-120">DESCRIPTION</span></span>
<span data-ttu-id="8892d-121">Polecenie **cmdlet Test-AzDeployment** określa, czy szablon wdrożenia i jego wartości parametrów są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="8892d-121">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="8892d-122">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8892d-122">EXAMPLES</span></span>

### <span data-ttu-id="8892d-123">Przykład 1. Testowanie wdrożenia za pomocą szablonu niestandardowego i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="8892d-123">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="8892d-124">To polecenie sprawdza wdrożenie w bieżącym zakresie subskrypcji przy użyciu danego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="8892d-124">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="8892d-125">Przykład 2. Testowanie wdrożenia z niestandardowym obiektem szablonu i plikiem parametrów</span><span class="sxs-lookup"><span data-stu-id="8892d-125">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="8892d-126">To polecenie służy do testowania wdrożenia w bieżącym zakresie subskrypcji przy użyciu skrótu w pamięci utworzonego na podstawie pliku danego szablonu i pliku parametru.</span><span class="sxs-lookup"><span data-stu-id="8892d-126">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="8892d-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8892d-127">PARAMETERS</span></span>

### <span data-ttu-id="8892d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8892d-128">-DefaultProfile</span></span>
<span data-ttu-id="8892d-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8892d-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8892d-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8892d-130">-Location</span></span>
<span data-ttu-id="8892d-131">Lokalizacja przechowywania danych wdrożeniowych.</span><span class="sxs-lookup"><span data-stu-id="8892d-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="8892d-132">— Przed</span><span class="sxs-lookup"><span data-stu-id="8892d-132">-Pre</span></span>
<span data-ttu-id="8892d-133">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8892d-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8892d-134">-QueryString</span><span class="sxs-lookup"><span data-stu-id="8892d-134">-QueryString</span></span>
<span data-ttu-id="8892d-135">Ciąg zapytania (na przykład token SAS) używany z parametrem TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="8892d-135">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="8892d-136">Czy będzie używana w przypadku szablonów połączonych</span><span class="sxs-lookup"><span data-stu-id="8892d-136">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="8892d-137">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="8892d-137">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="8892d-138">Pomija dynamiczne przetwarzanie parametrów programu PowerShell, które sprawdza, czy podany parametr szablonu zawiera wszystkie niezbędne parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="8892d-138">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="8892d-139">To sprawdzenie spowoduje monitowanie użytkownika o podanie wartości dla brakujących parametrów, ale podanie parametru -SkipTemplateParameterPrompt spowoduje natychmiastowe zignorowanie tego monitu i błędu, jeśli znaleziono, że parametr nie jest powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="8892d-139">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="8892d-140">W przypadku skryptów nieinterakcyjnych można udostępnić komunikat -SkipTemplateParameterPrompt w celu zapewnienia lepszego komunikatu o błędzie w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="8892d-140">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="8892d-141">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8892d-141">-TemplateFile</span></span>
<span data-ttu-id="8892d-142">Ścieżka lokalna do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="8892d-142">Local path to the template file.</span></span> <span data-ttu-id="8892d-143">Obsługiwany typ pliku szablonu: json i biceps.</span><span class="sxs-lookup"><span data-stu-id="8892d-143">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="8892d-144">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="8892d-144">-TemplateObject</span></span>
<span data-ttu-id="8892d-145">Tabela skrótów reprezentująca szablon.</span><span class="sxs-lookup"><span data-stu-id="8892d-145">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="8892d-146">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8892d-146">-TemplateParameterFile</span></span>
<span data-ttu-id="8892d-147">Plik z parametrami szablonu.</span><span class="sxs-lookup"><span data-stu-id="8892d-147">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="8892d-148">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="8892d-148">-TemplateParameterObject</span></span>
<span data-ttu-id="8892d-149">Tabela skrótów reprezentująca parametry.</span><span class="sxs-lookup"><span data-stu-id="8892d-149">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="8892d-150">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="8892d-150">-TemplateParameterUri</span></span>
<span data-ttu-id="8892d-151">Uri do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="8892d-151">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="8892d-152">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="8892d-152">-TemplateSpecId</span></span>
<span data-ttu-id="8892d-153">Identyfikator zasobu szablonuOkreślony, który ma zostać wdrożony.</span><span class="sxs-lookup"><span data-stu-id="8892d-153">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="8892d-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="8892d-154">-TemplateUri</span></span>
<span data-ttu-id="8892d-155">Uri do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="8892d-155">Uri to the template file.</span></span>

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

### <span data-ttu-id="8892d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8892d-156">CommonParameters</span></span>
<span data-ttu-id="8892d-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8892d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8892d-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8892d-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8892d-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8892d-159">INPUTS</span></span>

### <span data-ttu-id="8892d-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8892d-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8892d-161">System.String</span><span class="sxs-lookup"><span data-stu-id="8892d-161">System.String</span></span>

## <span data-ttu-id="8892d-162">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8892d-162">OUTPUTS</span></span>

### <span data-ttu-id="8892d-163">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="8892d-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="8892d-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8892d-164">NOTES</span></span>

## <span data-ttu-id="8892d-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8892d-165">RELATED LINKS</span></span>
