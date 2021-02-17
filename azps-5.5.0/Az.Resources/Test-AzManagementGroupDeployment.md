---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178746"
---
# <span data-ttu-id="24883-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="24883-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="24883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24883-102">SYNOPSIS</span></span>
<span data-ttu-id="24883-103">Sprawdza poprawność wdrożenia w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="24883-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="24883-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="24883-104">SYNTAX</span></span>

### <span data-ttu-id="24883-105">ByTemplateFileWithNoParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="24883-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24883-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="24883-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24883-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="24883-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24883-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="24883-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24883-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="24883-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24883-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="24883-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24883-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="24883-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24883-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="24883-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24883-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="24883-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24883-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="24883-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24883-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="24883-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24883-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="24883-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24883-117">OPIS</span><span class="sxs-lookup"><span data-stu-id="24883-117">DESCRIPTION</span></span>
<span data-ttu-id="24883-118">Polecenie cmdlet **Test-AzManagementGroupDeployment** określa, czy szablon wdrożenia i jego wartości parametrów są prawidłowe w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="24883-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="24883-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="24883-119">EXAMPLES</span></span>

### <span data-ttu-id="24883-120">Przykład 1. Testowanie wdrożenia za pomocą szablonu niestandardowego i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="24883-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="24883-121">To polecenie sprawdza wdrożenie w grupie zarządzania "myMG" przy użyciu danego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="24883-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="24883-122">Przykład 2. Testowanie wdrożenia z niestandardowym obiektem szablonu i plikiem parametrów</span><span class="sxs-lookup"><span data-stu-id="24883-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="24883-123">To polecenie służy do testowania wdrożenia w grupie zarządzania "myMG" przy użyciu skrótu w pamięci utworzonego na podstawie pliku danego szablonu i pliku parametru.</span><span class="sxs-lookup"><span data-stu-id="24883-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="24883-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24883-124">PARAMETERS</span></span>

### <span data-ttu-id="24883-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24883-125">-DefaultProfile</span></span>
<span data-ttu-id="24883-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="24883-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24883-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="24883-127">-Location</span></span>
<span data-ttu-id="24883-128">Lokalizacja przechowywania danych wdrożeniowych.</span><span class="sxs-lookup"><span data-stu-id="24883-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="24883-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="24883-129">-ManagementGroupId</span></span>
<span data-ttu-id="24883-130">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="24883-130">The management group id.</span></span>

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

### <span data-ttu-id="24883-131">— Przed</span><span class="sxs-lookup"><span data-stu-id="24883-131">-Pre</span></span>
<span data-ttu-id="24883-132">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="24883-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="24883-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="24883-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="24883-134">Pomija dynamiczne przetwarzanie parametrów programu PowerShell, które sprawdza, czy podany parametr szablonu zawiera wszystkie niezbędne parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="24883-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="24883-135">To sprawdzenie spowoduje monitowanie użytkownika o podanie wartości dla brakujących parametrów, ale podanie parametru -SkipTemplateParameterPrompt spowoduje natychmiastowe zignorowanie tego monitu i błędu, jeśli nie zostanie znaleziony parametr powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="24883-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="24883-136">W przypadku skryptów nieinterakcyjnych można udostępnić komunikat "SkipTemplateParameterPrompt" w celu zapewnienia lepszego komunikatu o błędzie w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="24883-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="24883-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="24883-137">-TemplateFile</span></span>
<span data-ttu-id="24883-138">Ścieżka lokalna do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="24883-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="24883-139">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="24883-139">-TemplateObject</span></span>
<span data-ttu-id="24883-140">Tabela skrótów reprezentująca szablon.</span><span class="sxs-lookup"><span data-stu-id="24883-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="24883-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="24883-141">-TemplateParameterFile</span></span>
<span data-ttu-id="24883-142">Plik z parametrami szablonu.</span><span class="sxs-lookup"><span data-stu-id="24883-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="24883-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="24883-143">-TemplateParameterObject</span></span>
<span data-ttu-id="24883-144">Tabela skrótów reprezentująca parametry.</span><span class="sxs-lookup"><span data-stu-id="24883-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="24883-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="24883-145">-TemplateParameterUri</span></span>
<span data-ttu-id="24883-146">Uri do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="24883-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="24883-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="24883-147">-TemplateUri</span></span>
<span data-ttu-id="24883-148">Uri do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="24883-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="24883-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24883-149">CommonParameters</span></span>
<span data-ttu-id="24883-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24883-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24883-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24883-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24883-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24883-152">INPUTS</span></span>

### <span data-ttu-id="24883-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="24883-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="24883-154">System.String</span><span class="sxs-lookup"><span data-stu-id="24883-154">System.String</span></span>

## <span data-ttu-id="24883-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="24883-155">OUTPUTS</span></span>

### <span data-ttu-id="24883-156">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="24883-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="24883-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="24883-157">NOTES</span></span>

## <span data-ttu-id="24883-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24883-158">RELATED LINKS</span></span>
