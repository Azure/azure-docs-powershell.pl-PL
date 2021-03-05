---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 6ecdf53ecd762c0c3b8ef378b1e8bc78b301a012
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985594"
---
# <span data-ttu-id="aed71-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="aed71-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="aed71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aed71-102">SYNOPSIS</span></span>
<span data-ttu-id="aed71-103">Sprawdza poprawność wdrożenia w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="aed71-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="aed71-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aed71-104">SYNTAX</span></span>

### <span data-ttu-id="aed71-105">ByTemplateFileWithNoParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="aed71-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aed71-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="aed71-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed71-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="aed71-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed71-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="aed71-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed71-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="aed71-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed71-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="aed71-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed71-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="aed71-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed71-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="aed71-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterFile <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed71-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="aed71-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed71-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="aed71-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed71-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="aed71-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed71-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="aed71-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed71-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="aed71-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aed71-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="aed71-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aed71-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="aed71-119">ByTemplateSpecResourceId</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> [-QueryString <String>]
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aed71-120">OPIS</span><span class="sxs-lookup"><span data-stu-id="aed71-120">DESCRIPTION</span></span>
<span data-ttu-id="aed71-121">Polecenie cmdlet **Test-AzManagementGroupDeployment** określa, czy szablon wdrożenia i jego wartości parametrów są prawidłowe w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="aed71-121">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="aed71-122">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aed71-122">EXAMPLES</span></span>

### <span data-ttu-id="aed71-123">Przykład 1. Testowanie wdrożenia za pomocą szablonu niestandardowego i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="aed71-123">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="aed71-124">To polecenie sprawdza wdrożenie w grupie zarządzania "myMG" przy użyciu danego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="aed71-124">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="aed71-125">Przykład 2. Testowanie wdrożenia z niestandardowym obiektem szablonu i plikiem parametrów</span><span class="sxs-lookup"><span data-stu-id="aed71-125">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="aed71-126">To polecenie służy do testowania wdrożenia w grupie zarządzania "myMG" przy użyciu skrótu w pamięci utworzonego na podstawie pliku danego szablonu i pliku parametru.</span><span class="sxs-lookup"><span data-stu-id="aed71-126">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="aed71-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aed71-127">PARAMETERS</span></span>

### <span data-ttu-id="aed71-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed71-128">-DefaultProfile</span></span>
<span data-ttu-id="aed71-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aed71-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aed71-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="aed71-130">-Location</span></span>
<span data-ttu-id="aed71-131">Lokalizacja przechowywania danych wdrożeniowych.</span><span class="sxs-lookup"><span data-stu-id="aed71-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="aed71-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="aed71-132">-ManagementGroupId</span></span>
<span data-ttu-id="aed71-133">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="aed71-133">The management group id.</span></span>

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

### <span data-ttu-id="aed71-134">— Przed</span><span class="sxs-lookup"><span data-stu-id="aed71-134">-Pre</span></span>
<span data-ttu-id="aed71-135">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="aed71-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="aed71-136">-QueryString</span><span class="sxs-lookup"><span data-stu-id="aed71-136">-QueryString</span></span>
<span data-ttu-id="aed71-137">Ciąg zapytania (na przykład token SAS) używany z parametrem TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="aed71-137">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="aed71-138">Czy będzie używana w przypadku szablonów połączonych</span><span class="sxs-lookup"><span data-stu-id="aed71-138">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="aed71-139">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="aed71-139">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="aed71-140">Pomija dynamiczne przetwarzanie parametrów programu PowerShell, które sprawdza, czy podany parametr szablonu zawiera wszystkie niezbędne parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="aed71-140">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="aed71-141">To sprawdzenie spowoduje monitowanie użytkownika o podanie wartości dla brakujących parametrów, ale podanie parametru -SkipTemplateParameterPrompt spowoduje natychmiastowe zignorowanie tego monitu i błędu, jeśli znaleziono, że parametr nie jest powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="aed71-141">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="aed71-142">W przypadku skryptów nieinterakcyjnych można udostępnić komunikat -SkipTemplateParameterPrompt w celu zapewnienia lepszego komunikatu o błędzie w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="aed71-142">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="aed71-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="aed71-143">-TemplateFile</span></span>
<span data-ttu-id="aed71-144">Ścieżka lokalna do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="aed71-144">Local path to the template file.</span></span> <span data-ttu-id="aed71-145">Obsługiwany typ pliku szablonu: json i biceps.</span><span class="sxs-lookup"><span data-stu-id="aed71-145">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="aed71-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="aed71-146">-TemplateObject</span></span>
<span data-ttu-id="aed71-147">Tabela skrótów reprezentująca szablon.</span><span class="sxs-lookup"><span data-stu-id="aed71-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="aed71-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="aed71-148">-TemplateParameterFile</span></span>
<span data-ttu-id="aed71-149">Plik z parametrami szablonu.</span><span class="sxs-lookup"><span data-stu-id="aed71-149">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="aed71-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="aed71-150">-TemplateParameterObject</span></span>
<span data-ttu-id="aed71-151">Tabela skrótów reprezentująca parametry.</span><span class="sxs-lookup"><span data-stu-id="aed71-151">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="aed71-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="aed71-152">-TemplateParameterUri</span></span>
<span data-ttu-id="aed71-153">Uri do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="aed71-153">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="aed71-154">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="aed71-154">-TemplateSpecId</span></span>
<span data-ttu-id="aed71-155">Identyfikator zasobu szablonuOkreślony, który ma zostać wdrożony.</span><span class="sxs-lookup"><span data-stu-id="aed71-155">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="aed71-156">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="aed71-156">-TemplateUri</span></span>
<span data-ttu-id="aed71-157">Uri do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="aed71-157">Uri to the template file.</span></span>

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

### <span data-ttu-id="aed71-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed71-158">CommonParameters</span></span>
<span data-ttu-id="aed71-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aed71-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed71-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aed71-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed71-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aed71-161">INPUTS</span></span>

### <span data-ttu-id="aed71-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="aed71-162">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aed71-163">System.String</span><span class="sxs-lookup"><span data-stu-id="aed71-163">System.String</span></span>

## <span data-ttu-id="aed71-164">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aed71-164">OUTPUTS</span></span>

### <span data-ttu-id="aed71-165">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="aed71-165">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="aed71-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aed71-166">NOTES</span></span>

## <span data-ttu-id="aed71-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aed71-167">RELATED LINKS</span></span>
