---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 514d1257d917dc1bbf20f93d05236af9f36bd832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542343"
---
# <span data-ttu-id="5fcc4-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5fcc4-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="5fcc4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5fcc4-102">SYNOPSIS</span></span>
<span data-ttu-id="5fcc4-103">Umożliwia dodanie wdrożenia platformy Azure do grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fcc4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5fcc4-104">SYNTAX</span></span>

### <span data-ttu-id="5fcc4-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5fcc4-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fcc4-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5fcc4-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fcc4-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5fcc4-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fcc4-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5fcc4-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fcc4-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5fcc4-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fcc4-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5fcc4-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fcc4-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5fcc4-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fcc4-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5fcc4-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fcc4-113">Opis</span><span class="sxs-lookup"><span data-stu-id="5fcc4-113">DESCRIPTION</span></span>
<span data-ttu-id="5fcc4-114">Polecenie cmdlet **New-AzureRmResourceGroupDeployment** umożliwia dodanie wdrożenia do istniejącej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="5fcc4-115">Dotyczy to zasobów, których wdrożenie wymaga.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="5fcc4-116">Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure, taką jak serwer bazy danych, baza danych, witryna sieci Web, maszyna wirtualna lub konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="5fcc4-117">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka, takich jak witryna sieci Web, serwer bazy danych i bazy danych wymagane dla finansowej witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="5fcc4-118">Wdrożenie grupy zasobów umożliwia dodanie zasobów do grupy zasobów i opublikowanie ich w celu udostępnienia ich na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="5fcc4-119">Aby dodać zasoby do grupy zasobów bez użycia szablonu, użyj polecenia cmdlet New-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="5fcc4-120">Aby dodać wdrożenie grupy zasobów, określ nazwę istniejącej grupy zasobów i szablonu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="5fcc4-121">Szablon Grupa zasobów to ciąg JSON reprezentujący grupę zasobów dla skomplikowanej usługi opartej na chmurze, na przykład portalu sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="5fcc4-122">Szablon zawiera symbole zastępcze parametru dla wymaganych zasobów i wartości właściwości konfigurowalnych, takich jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="5fcc4-123">Wiele szablonów można znaleźć w galerii szablonów platformy Azure lub można utworzyć własne szablony.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="5fcc4-124">Za pomocą polecenia cmdlet **Get-AzureRmResourceGroupGalleryTemplate** można znaleźć szablon w galerii.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="5fcc4-125">Aby utworzyć grupę zasobów przy użyciu szablonu niestandardowego, określ parametr *TemplateFile* lub parametr *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="5fcc4-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="5fcc4-126">Każdy szablon zawiera parametry konfigurowalnych właściwości.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="5fcc4-127">Aby określić wartości parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="5fcc4-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="5fcc4-128">Możesz też użyć parametrów szablonu, które są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="5fcc4-129">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-), aby wskazać parametr, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="5fcc4-130">Wartości parametrów szablonu wprowadzone w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="5fcc4-131">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5fcc4-131">EXAMPLES</span></span>

### <span data-ttu-id="5fcc4-132">Przykład 1: korzystanie z szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="5fcc4-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="5fcc4-133">To polecenie tworzy nowe wdrożenie przy użyciu szablonu niestandardowego i pliku szablonu na dysku.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="5fcc4-134">W poleceniu użyto parametru *TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="5fcc4-135">Używa parametru *TemplateVersion* w celu określenia wersji szablonu.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="5fcc4-136">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5fcc4-136">PARAMETERS</span></span>

### <span data-ttu-id="5fcc4-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5fcc4-137">-ApiVersion</span></span>
<span data-ttu-id="5fcc4-138">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5fcc4-139">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-139">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="5fcc4-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fcc4-140">-AsJob</span></span>
<span data-ttu-id="5fcc4-141">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5fcc4-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fcc4-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fcc4-142">-DefaultProfile</span></span>
<span data-ttu-id="5fcc4-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5fcc4-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fcc4-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="5fcc4-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="5fcc4-145">Określa poziom dziennika debugowania.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-145">Specifies a debug log level.</span></span>
<span data-ttu-id="5fcc4-146">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5fcc4-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5fcc4-147">RequestContent</span><span class="sxs-lookup"><span data-stu-id="5fcc4-147">RequestContent</span></span>
- <span data-ttu-id="5fcc4-148">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="5fcc4-148">ResponseContent</span></span>
- <span data-ttu-id="5fcc4-149">Cały</span><span class="sxs-lookup"><span data-stu-id="5fcc4-149">All</span></span>
- <span data-ttu-id="5fcc4-150">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5fcc4-150">None</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcc4-151">-Force</span><span class="sxs-lookup"><span data-stu-id="5fcc4-151">-Force</span></span>
<span data-ttu-id="5fcc4-152">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-152">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5fcc4-153">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="5fcc4-153">-Mode</span></span>
<span data-ttu-id="5fcc4-154">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-154">Specifies the deployment mode.</span></span> <span data-ttu-id="5fcc4-155">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5fcc4-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5fcc4-156">Pełni</span><span class="sxs-lookup"><span data-stu-id="5fcc4-156">Complete</span></span>
- <span data-ttu-id="5fcc4-157">Dodatkowe</span><span class="sxs-lookup"><span data-stu-id="5fcc4-157">Incremental</span></span>

<span data-ttu-id="5fcc4-158">W trybie Complete Menedżer zasobów usuwa zasoby istniejące w grupie zasobów, ale nie są określone w szablonie.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-158">In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="5fcc4-159">W trybie przyrostowym Menedżer zasobów pozostawia niezmienione zasoby, które znajdują się w grupie zasobów, ale nie są określone w szablonie.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-159">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcc4-160">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5fcc4-160">-Name</span></span>
<span data-ttu-id="5fcc4-161">Określa nazwę wdrożenia grupy zasobów do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-161">Specifies the name of the resource group deployment to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcc4-162">-Pre</span><span class="sxs-lookup"><span data-stu-id="5fcc4-162">-Pre</span></span>
<span data-ttu-id="5fcc4-163">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-163">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5fcc4-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fcc4-164">-ResourceGroupName</span></span>
<span data-ttu-id="5fcc4-165">Określa nazwę grupy zasobów do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-165">Specifies the name of the resource group to deploy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcc4-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="5fcc4-166">-TemplateFile</span></span>
<span data-ttu-id="5fcc4-167">Określa pełną ścieżkę pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-167">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="5fcc4-168">Może to być szablon niestandardowy lub szablon galerii zapisany jako plik JSON, taki jak utworzony za pomocą polecenia cmdlet **Save-AzureRmResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="5fcc4-168">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="5fcc4-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="5fcc4-169">-TemplateParameterFile</span></span>
<span data-ttu-id="5fcc4-170">Określa pełną ścieżkę pliku JSON zawierającego nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-170">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="5fcc4-171">Jeśli szablon zawiera parametry, należy określić wartości parametrów za pomocą parametru *TemplateParameterFile* lub parametru *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="5fcc4-171">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="5fcc4-172">Parametry szablonu są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="5fcc4-173">Aby użyć parametrów dynamicznych, wpisz znak minus (-), aby wskazać nazwę parametru, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-173">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcc4-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="5fcc4-174">-TemplateParameterObject</span></span>
<span data-ttu-id="5fcc4-175">Określa tabelę skrótów zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-175">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="5fcc4-176">Aby uzyskać pomoc dotyczącą tabel skrótów w programie Windows PowerShell, wpisz polecenie `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="5fcc4-176">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="5fcc4-177">Jeśli szablon zawiera parametry, należy określić wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-177">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="5fcc4-178">Parametry szablonu są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-178">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcc4-179">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="5fcc4-179">-TemplateParameterUri</span></span>
<span data-ttu-id="5fcc4-180">Określa identyfikator URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-180">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcc4-181">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="5fcc4-181">-TemplateUri</span></span>
<span data-ttu-id="5fcc4-182">Określa identyfikator URI pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-182">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="5fcc4-183">Ten plik może być szablonem niestandardowym lub szablonem galerii zapisanym jako plik JSON, na przykład przy użyciu polecenia **Save-AzureRmResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-183">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="5fcc4-184">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5fcc4-184">-Confirm</span></span>
<span data-ttu-id="5fcc4-185">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-185">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fcc4-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fcc4-186">-WhatIf</span></span>
<span data-ttu-id="5fcc4-187">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fcc4-188">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-188">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fcc4-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fcc4-189">CommonParameters</span></span>
<span data-ttu-id="5fcc4-190">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fcc4-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fcc4-191">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fcc4-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fcc4-192">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fcc4-192">INPUTS</span></span>

### <span data-ttu-id="5fcc4-193">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5fcc4-193">None</span></span>

## <span data-ttu-id="5fcc4-194">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5fcc4-194">OUTPUTS</span></span>

### <span data-ttu-id="5fcc4-195">Microsoft. Azure. Commands. ResourceManager. modele. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5fcc4-195">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="5fcc4-196">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5fcc4-196">NOTES</span></span>

## <span data-ttu-id="5fcc4-197">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fcc4-197">RELATED LINKS</span></span>

[<span data-ttu-id="5fcc4-198">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5fcc4-198">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="5fcc4-199">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="5fcc4-199">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="5fcc4-200">Nowe — AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5fcc4-200">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="5fcc4-201">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5fcc4-201">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="5fcc4-202">Zatrzymaj — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5fcc4-202">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="5fcc4-203">Test — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5fcc4-203">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


