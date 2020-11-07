---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 35741c908e57e96fd4d9709ff350ac885f41181d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892481"
---
# <span data-ttu-id="b4afa-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4afa-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="b4afa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4afa-102">SYNOPSIS</span></span>
<span data-ttu-id="b4afa-103">Umożliwia dodanie wdrożenia platformy Azure do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4afa-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="b4afa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4afa-104">SYNTAX</span></span>

### <span data-ttu-id="b4afa-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b4afa-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4afa-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b4afa-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4afa-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b4afa-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4afa-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b4afa-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4afa-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b4afa-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4afa-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b4afa-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4afa-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b4afa-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4afa-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b4afa-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4afa-113">Opis</span><span class="sxs-lookup"><span data-stu-id="b4afa-113">DESCRIPTION</span></span>
<span data-ttu-id="b4afa-114">Polecenie cmdlet **New-AzResourceGroupDeployment** umożliwia dodanie wdrożenia do istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4afa-114">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="b4afa-115">Dotyczy to zasobów, których wdrożenie wymaga.</span><span class="sxs-lookup"><span data-stu-id="b4afa-115">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="b4afa-116">Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure, taką jak serwer bazy danych, baza danych, witryna sieci Web, maszyna wirtualna lub konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="b4afa-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="b4afa-117">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka, takich jak witryna sieci Web, serwer bazy danych i bazy danych wymagane dla finansowej witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b4afa-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="b4afa-118">Wdrożenie grupy zasobów umożliwia dodanie zasobów do grupy zasobów i opublikowanie ich w celu udostępnienia ich na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b4afa-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="b4afa-119">Aby dodać zasoby do grupy zasobów bez użycia szablonu, użyj polecenia cmdlet New-AzResource.</span><span class="sxs-lookup"><span data-stu-id="b4afa-119">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="b4afa-120">Aby dodać wdrożenie grupy zasobów, określ nazwę istniejącej grupy zasobów i szablonu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4afa-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="b4afa-121">Szablon Grupa zasobów to ciąg JSON reprezentujący grupę zasobów dla skomplikowanej usługi opartej na chmurze, na przykład portalu sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b4afa-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="b4afa-122">Szablon zawiera symbole zastępcze parametru dla wymaganych zasobów i wartości właściwości konfigurowalnych, takich jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="b4afa-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="b4afa-123">Wiele szablonów można znaleźć w galerii szablonów platformy Azure lub można utworzyć własne szablony.</span><span class="sxs-lookup"><span data-stu-id="b4afa-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="b4afa-124">Za pomocą polecenia cmdlet **Get-AzResourceGroupGalleryTemplate** można znaleźć szablon w galerii.</span><span class="sxs-lookup"><span data-stu-id="b4afa-124">You can use the **Get-AzResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>
<span data-ttu-id="b4afa-125">Aby utworzyć grupę zasobów przy użyciu szablonu niestandardowego, określ parametr *TemplateFile* lub parametr *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="b4afa-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="b4afa-126">Każdy szablon zawiera parametry konfigurowalnych właściwości.</span><span class="sxs-lookup"><span data-stu-id="b4afa-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="b4afa-127">Aby określić wartości parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="b4afa-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="b4afa-128">Możesz też użyć parametrów szablonu, które są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="b4afa-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="b4afa-129">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-), aby wskazać parametr, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="b4afa-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="b4afa-130">Wartości parametrów szablonu wprowadzone w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="b4afa-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="b4afa-131">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4afa-131">EXAMPLES</span></span>

### <span data-ttu-id="b4afa-132">Przykład 1: korzystanie z szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="b4afa-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="b4afa-133">To polecenie tworzy nowe wdrożenie przy użyciu szablonu niestandardowego i pliku szablonu na dysku.</span><span class="sxs-lookup"><span data-stu-id="b4afa-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="b4afa-134">W poleceniu użyto parametru *TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="b4afa-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="b4afa-135">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4afa-135">PARAMETERS</span></span>

### <span data-ttu-id="b4afa-136">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b4afa-136">-ApiVersion</span></span>
<span data-ttu-id="b4afa-137">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="b4afa-137">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b4afa-138">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="b4afa-138">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b4afa-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4afa-139">-AsJob</span></span>
<span data-ttu-id="b4afa-140">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b4afa-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4afa-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4afa-141">-DefaultProfile</span></span>
<span data-ttu-id="b4afa-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b4afa-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4afa-143">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="b4afa-143">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="b4afa-144">Określa poziom dziennika debugowania.</span><span class="sxs-lookup"><span data-stu-id="b4afa-144">Specifies a debug log level.</span></span>
<span data-ttu-id="b4afa-145">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b4afa-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b4afa-146">RequestContent</span><span class="sxs-lookup"><span data-stu-id="b4afa-146">RequestContent</span></span>
- <span data-ttu-id="b4afa-147">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="b4afa-147">ResponseContent</span></span>
- <span data-ttu-id="b4afa-148">Cały</span><span class="sxs-lookup"><span data-stu-id="b4afa-148">All</span></span>
- <span data-ttu-id="b4afa-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b4afa-149">None</span></span>

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

### <span data-ttu-id="b4afa-150">-Force</span><span class="sxs-lookup"><span data-stu-id="b4afa-150">-Force</span></span>
<span data-ttu-id="b4afa-151">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b4afa-151">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4afa-152">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="b4afa-152">-Mode</span></span>
<span data-ttu-id="b4afa-153">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="b4afa-153">Specifies the deployment mode.</span></span> <span data-ttu-id="b4afa-154">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b4afa-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b4afa-155">Pełni</span><span class="sxs-lookup"><span data-stu-id="b4afa-155">Complete</span></span>
- <span data-ttu-id="b4afa-156">Przyrostowy tryb Complete, Menedżer zasobów usuwa zasoby istniejące w grupie zasobów, ale nie są określone w szablonie.</span><span class="sxs-lookup"><span data-stu-id="b4afa-156">Incremental In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="b4afa-157">W trybie przyrostowym Menedżer zasobów pozostawia niezmienione zasoby, które znajdują się w grupie zasobów, ale nie są określone w szablonie.</span><span class="sxs-lookup"><span data-stu-id="b4afa-157">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4afa-158">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b4afa-158">-Name</span></span>
<span data-ttu-id="b4afa-159">Określa nazwę wdrożenia grupy zasobów do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="b4afa-159">Specifies the name of the resource group deployment to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4afa-160">-Pre</span><span class="sxs-lookup"><span data-stu-id="b4afa-160">-Pre</span></span>
<span data-ttu-id="b4afa-161">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="b4afa-161">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b4afa-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4afa-162">-ResourceGroupName</span></span>
<span data-ttu-id="b4afa-163">Określa nazwę grupy zasobów do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b4afa-163">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="b4afa-164">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="b4afa-164">-RollBackDeploymentName</span></span>
<span data-ttu-id="b4afa-165">Wycofanie do poprawnego wdrożenia o podanej nazwie w grupie zasobów nie powinno być używane, jeśli jest używana funkcja-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="b4afa-165">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="b4afa-166">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="b4afa-166">-RollbackToLastDeployment</span></span>
<span data-ttu-id="b4afa-167">Wycofanie do ostatniego poprawnego wdrożenia w grupie zasobów nie powinno być dostępne, jeśli jest używana funkcja-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="b4afa-167">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="b4afa-168">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b4afa-168">-TemplateFile</span></span>
<span data-ttu-id="b4afa-169">Określa pełną ścieżkę pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="b4afa-169">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="b4afa-170">Może to być szablon niestandardowy lub szablon galerii zapisany jako plik JSON, taki jak utworzony za pomocą polecenia cmdlet **Save-AzResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="b4afa-170">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="b4afa-171">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b4afa-171">-TemplateParameterFile</span></span>
<span data-ttu-id="b4afa-172">Określa pełną ścieżkę pliku JSON zawierającego nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="b4afa-172">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="b4afa-173">Jeśli szablon zawiera parametry, należy określić wartości parametrów za pomocą parametru *TemplateParameterFile* lub parametru *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="b4afa-173">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="b4afa-174">Parametry szablonu są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="b4afa-174">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="b4afa-175">Aby użyć parametrów dynamicznych, wpisz znak minus (-), aby wskazać nazwę parametru, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="b4afa-175">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4afa-176">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b4afa-176">-TemplateParameterObject</span></span>
<span data-ttu-id="b4afa-177">Określa tabelę skrótów zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="b4afa-177">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="b4afa-178">Aby uzyskać pomoc dotyczącą tabel skrótów w programie Windows PowerShell, wpisz polecenie `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="b4afa-178">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="b4afa-179">Jeśli szablon zawiera parametry, należy określić wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="b4afa-179">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="b4afa-180">Parametry szablonu są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="b4afa-180">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4afa-181">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b4afa-181">-TemplateParameterUri</span></span>
<span data-ttu-id="b4afa-182">Określa identyfikator URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="b4afa-182">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4afa-183">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b4afa-183">-TemplateUri</span></span>
<span data-ttu-id="b4afa-184">Określa identyfikator URI pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="b4afa-184">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="b4afa-185">Ten plik może być szablonem niestandardowym lub szablonem galerii zapisanym jako plik JSON, na przykład przy użyciu polecenia **Save-AzResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="b4afa-185">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="b4afa-186">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b4afa-186">-Confirm</span></span>
<span data-ttu-id="b4afa-187">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4afa-187">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4afa-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4afa-188">-WhatIf</span></span>
<span data-ttu-id="b4afa-189">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4afa-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4afa-190">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b4afa-190">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4afa-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4afa-191">CommonParameters</span></span>
<span data-ttu-id="b4afa-192">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4afa-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4afa-193">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4afa-193">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4afa-194">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4afa-194">INPUTS</span></span>

### <span data-ttu-id="b4afa-195">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b4afa-195">None</span></span>

## <span data-ttu-id="b4afa-196">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4afa-196">OUTPUTS</span></span>

### <span data-ttu-id="b4afa-197">Microsoft. Azure. Commands. ResourceManager. modele. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4afa-197">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="b4afa-198">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4afa-198">NOTES</span></span>

## <span data-ttu-id="b4afa-199">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4afa-199">RELATED LINKS</span></span>

[<span data-ttu-id="b4afa-200">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4afa-200">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="b4afa-201">Nowe — AzResource</span><span class="sxs-lookup"><span data-stu-id="b4afa-201">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="b4afa-202">Nowe — AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b4afa-202">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="b4afa-203">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4afa-203">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="b4afa-204">Zatrzymaj — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4afa-204">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="b4afa-205">Test — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b4afa-205">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


