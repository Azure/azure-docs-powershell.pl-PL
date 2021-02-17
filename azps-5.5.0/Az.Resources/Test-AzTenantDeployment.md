---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5144dacb044523c2ad72d0a9c24aa43427f14f99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178738"
---
# <span data-ttu-id="76fb4-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="76fb4-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="76fb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="76fb4-103">Sprawdza poprawność wdrożenia w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="76fb4-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="76fb4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76fb4-104">SYNTAX</span></span>

### <span data-ttu-id="76fb4-105">ByTemplateFileWithNoParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="76fb4-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fb4-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="76fb4-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fb4-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="76fb4-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fb4-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="76fb4-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fb4-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="76fb4-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fb4-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="76fb4-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fb4-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="76fb4-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fb4-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="76fb4-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fb4-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="76fb4-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fb4-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="76fb4-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fb4-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="76fb4-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fb4-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="76fb4-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76fb4-117">OPIS</span><span class="sxs-lookup"><span data-stu-id="76fb4-117">DESCRIPTION</span></span>
<span data-ttu-id="76fb4-118">Polecenie cmdlet **Test-AzTenantDeployment** określa, czy szablon wdrożenia i jego wartości parametrów są prawidłowe w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="76fb4-118">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="76fb4-119">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76fb4-119">EXAMPLES</span></span>

### <span data-ttu-id="76fb4-120">Przykład 1. Testowanie wdrożenia za pomocą szablonu niestandardowego i pliku parametru</span><span class="sxs-lookup"><span data-stu-id="76fb4-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="76fb4-121">To polecenie sprawdza wdrożenie w bieżącym zakresie dzierżawy przy użyciu danego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="76fb4-121">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="76fb4-122">Przykład 2. Testowanie wdrożenia z niestandardowym obiektem szablonu i plikiem parametrów</span><span class="sxs-lookup"><span data-stu-id="76fb4-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="76fb4-123">To polecenie służy do testowania wdrożenia w bieżącym zakresie dzierżawy przy użyciu skrótu w pamięci utworzonego na podstawie pliku danego szablonu i pliku parametru.</span><span class="sxs-lookup"><span data-stu-id="76fb4-123">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="76fb4-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76fb4-124">PARAMETERS</span></span>

### <span data-ttu-id="76fb4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76fb4-125">-DefaultProfile</span></span>
<span data-ttu-id="76fb4-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="76fb4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76fb4-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="76fb4-127">-Location</span></span>
<span data-ttu-id="76fb4-128">Lokalizacja przechowywania danych wdrożeniowych.</span><span class="sxs-lookup"><span data-stu-id="76fb4-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="76fb4-129">— Przed</span><span class="sxs-lookup"><span data-stu-id="76fb4-129">-Pre</span></span>
<span data-ttu-id="76fb4-130">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="76fb4-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="76fb4-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="76fb4-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="76fb4-132">Pomija dynamiczne przetwarzanie parametrów programu PowerShell, które sprawdza, czy podany parametr szablonu zawiera wszystkie niezbędne parametry używane w szablonie.</span><span class="sxs-lookup"><span data-stu-id="76fb4-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="76fb4-133">To sprawdzenie spowoduje monitowanie użytkownika o podanie wartości dla brakujących parametrów, ale podanie parametru -SkipTemplateParameterPrompt spowoduje natychmiastowe zignorowanie tego monitu i błędu, jeśli nie zostanie znaleziony parametr powiązany z szablonem.</span><span class="sxs-lookup"><span data-stu-id="76fb4-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="76fb4-134">W przypadku skryptów nieinterakcyjnych można udostępnić komunikat "SkipTemplateParameterPrompt" w celu zapewnienia lepszego komunikatu o błędzie w przypadku, gdy nie wszystkie wymagane parametry są spełnione.</span><span class="sxs-lookup"><span data-stu-id="76fb4-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="76fb4-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="76fb4-135">-TemplateFile</span></span>
<span data-ttu-id="76fb4-136">Ścieżka lokalna do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="76fb4-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="76fb4-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="76fb4-137">-TemplateObject</span></span>
<span data-ttu-id="76fb4-138">Tabela skrótów reprezentująca szablon.</span><span class="sxs-lookup"><span data-stu-id="76fb4-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="76fb4-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="76fb4-139">-TemplateParameterFile</span></span>
<span data-ttu-id="76fb4-140">Plik z parametrami szablonu.</span><span class="sxs-lookup"><span data-stu-id="76fb4-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="76fb4-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="76fb4-141">-TemplateParameterObject</span></span>
<span data-ttu-id="76fb4-142">Tabela skrótów reprezentująca parametry.</span><span class="sxs-lookup"><span data-stu-id="76fb4-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="76fb4-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="76fb4-143">-TemplateParameterUri</span></span>
<span data-ttu-id="76fb4-144">Uri do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="76fb4-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="76fb4-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="76fb4-145">-TemplateUri</span></span>
<span data-ttu-id="76fb4-146">Uri do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="76fb4-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="76fb4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76fb4-147">CommonParameters</span></span>
<span data-ttu-id="76fb4-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76fb4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76fb4-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76fb4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76fb4-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76fb4-150">INPUTS</span></span>

### <span data-ttu-id="76fb4-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="76fb4-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="76fb4-152">System.String</span><span class="sxs-lookup"><span data-stu-id="76fb4-152">System.String</span></span>

## <span data-ttu-id="76fb4-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76fb4-153">OUTPUTS</span></span>

### <span data-ttu-id="76fb4-154">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="76fb4-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="76fb4-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76fb4-155">NOTES</span></span>

## <span data-ttu-id="76fb4-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76fb4-156">RELATED LINKS</span></span>
