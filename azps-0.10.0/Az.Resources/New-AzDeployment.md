---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 97d6b11a4993ced62b84de24c501a2c438173141
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892505"
---
# <span data-ttu-id="8929a-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8929a-101">New-AzDeployment</span></span>

## <span data-ttu-id="8929a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8929a-102">SYNOPSIS</span></span>
<span data-ttu-id="8929a-103">Tworzenie wdrożenia</span><span class="sxs-lookup"><span data-stu-id="8929a-103">Creat a deployment</span></span>

## <span data-ttu-id="8929a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8929a-104">SYNTAX</span></span>

### <span data-ttu-id="8929a-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8929a-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8929a-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8929a-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8929a-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8929a-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8929a-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8929a-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8929a-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8929a-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8929a-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8929a-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8929a-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8929a-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8929a-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8929a-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8929a-113">Opis</span><span class="sxs-lookup"><span data-stu-id="8929a-113">DESCRIPTION</span></span>
<span data-ttu-id="8929a-114">Polecenie cmdlet **New-AzDeployment** umożliwia dodanie wdrożenia w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8929a-114">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="8929a-115">Dotyczy to zasobów, których wdrożenie wymaga.</span><span class="sxs-lookup"><span data-stu-id="8929a-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="8929a-116">Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure.</span><span class="sxs-lookup"><span data-stu-id="8929a-116">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="8929a-117">Zasób może być aktywny w grupie zasobów, takiej jak serwer bazy danych, baza danych, witryna sieci Web, maszyna wirtualna lub konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="8929a-117">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span> <span data-ttu-id="8929a-118">Może to też być zasób poziomu abonamentu, na przykład definicja roli, definicja zasad itd.</span><span class="sxs-lookup"><span data-stu-id="8929a-118">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="8929a-119">Aby dodać zasoby do grupy zasobów, użyj **nowego-AzDeployment** , który tworzy wdrożenie w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="8929a-119">To add resources to a resource group, use the **New-AzDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="8929a-120">Polecenie cmdlet **New-AzDeployment** tworzy wdrożenie w bieżącym zakresie subskrypcji, co powoduje wdrożenie zasobów poziomu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8929a-120">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span> 

<span data-ttu-id="8929a-121">Aby dodać wdrożenie w subskrypcji, określ lokalizację i szablon.</span><span class="sxs-lookup"><span data-stu-id="8929a-121">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="8929a-122">Lokalizacja informuje Menedżera zasobów platformy Azure, gdzie mają być przechowywane dane wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="8929a-122">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="8929a-123">Szablon jest ciągiem JSON zawierającym poszczególne zasoby do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="8929a-123">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="8929a-124">Szablon zawiera symbole zastępcze parametru dla wymaganych zasobów i wartości właściwości konfigurowalnych, takich jak nazwy i rozmiary.</span><span class="sxs-lookup"><span data-stu-id="8929a-124">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="8929a-125">Aby użyć szablonu niestandardowego do wdrożenia, określ parametr *TemplateFile* lub *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="8929a-125">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="8929a-126">Każdy szablon zawiera parametry konfigurowalnych właściwości.</span><span class="sxs-lookup"><span data-stu-id="8929a-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="8929a-127">Aby określić wartości parametrów szablonu, określ parametr *TemplateParameterFile* lub parametr *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="8929a-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="8929a-128">Możesz też użyć parametrów szablonu, które są dodawane dynamicznie do polecenia podczas określania szablonu.</span><span class="sxs-lookup"><span data-stu-id="8929a-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="8929a-129">Aby użyć parametrów dynamicznych, wpisz je w wierszu polecenia lub wpisz znak minus (-), aby wskazać parametr, a następnie użyj klawisza Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="8929a-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="8929a-130">Wartości parametrów szablonu wprowadzone w wierszu polecenia mają pierwszeństwo przed wartościami w obiekcie lub pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="8929a-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="8929a-131">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8929a-131">EXAMPLES</span></span>

### <span data-ttu-id="8929a-132">Przykład 1: korzystanie z szablonu niestandardowego i pliku parametrów w celu utworzenia wdrożenia</span><span class="sxs-lookup"><span data-stu-id="8929a-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="8929a-133">To polecenie tworzy nowe wdrożenie w bieżącym zakresie subskrypcji przy użyciu szablonu niestandardowego i pliku szablonu na dysku.</span><span class="sxs-lookup"><span data-stu-id="8929a-133">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="8929a-134">W poleceniu użyto parametru *TemplateFile* w celu określenia szablonu i parametru *TemplateParameterFile* w celu określenia pliku zawierającego parametry i wartości parametrów.</span><span class="sxs-lookup"><span data-stu-id="8929a-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="8929a-135">Używa parametru *TemplateVersion* w celu określenia wersji szablonu.</span><span class="sxs-lookup"><span data-stu-id="8929a-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="8929a-136">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8929a-136">PARAMETERS</span></span>

### <span data-ttu-id="8929a-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8929a-137">-ApiVersion</span></span>
<span data-ttu-id="8929a-138">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="8929a-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8929a-139">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="8929a-139">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8929a-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8929a-140">-AsJob</span></span>
<span data-ttu-id="8929a-141">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8929a-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8929a-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8929a-142">-DefaultProfile</span></span>
<span data-ttu-id="8929a-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8929a-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8929a-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="8929a-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="8929a-145">Poziom dziennika debugowania wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="8929a-145">The deployment debug log level.</span></span>

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

### <span data-ttu-id="8929a-146">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8929a-146">-Location</span></span>
<span data-ttu-id="8929a-147">Lokalizacja przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="8929a-147">The location to store deployment data.</span></span>

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

### <span data-ttu-id="8929a-148">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8929a-148">-Name</span></span>
<span data-ttu-id="8929a-149">Nazwa wdrożenia, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="8929a-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="8929a-150">Ważne tylko w przypadku używania szablonu.</span><span class="sxs-lookup"><span data-stu-id="8929a-150">Only valid when a template is used.</span></span>
<span data-ttu-id="8929a-151">Jeśli jest używany szablon, jeśli użytkownik nie określi nazwy wdrożenia, Użyj bieżącej godziny, na przykład "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="8929a-151">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8929a-152">-Pre</span><span class="sxs-lookup"><span data-stu-id="8929a-152">-Pre</span></span>
<span data-ttu-id="8929a-153">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="8929a-153">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8929a-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8929a-154">-TemplateFile</span></span>
<span data-ttu-id="8929a-155">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="8929a-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="8929a-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8929a-156">-TemplateParameterFile</span></span>
<span data-ttu-id="8929a-157">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="8929a-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="8929a-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="8929a-158">-TemplateParameterObject</span></span>
<span data-ttu-id="8929a-159">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="8929a-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="8929a-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="8929a-160">-TemplateParameterUri</span></span>
<span data-ttu-id="8929a-161">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="8929a-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="8929a-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="8929a-162">-TemplateUri</span></span>
<span data-ttu-id="8929a-163">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="8929a-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="8929a-164">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8929a-164">-Confirm</span></span>
<span data-ttu-id="8929a-165">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8929a-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8929a-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8929a-166">-WhatIf</span></span>
<span data-ttu-id="8929a-167">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8929a-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8929a-168">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8929a-168">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8929a-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8929a-169">CommonParameters</span></span>
<span data-ttu-id="8929a-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8929a-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8929a-171">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8929a-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8929a-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8929a-172">INPUTS</span></span>

### <span data-ttu-id="8929a-173">System. String</span><span class="sxs-lookup"><span data-stu-id="8929a-173">System.String</span></span>
<span data-ttu-id="8929a-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8929a-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8929a-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8929a-175">OUTPUTS</span></span>

### <span data-ttu-id="8929a-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="8929a-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="8929a-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8929a-177">NOTES</span></span>

## <span data-ttu-id="8929a-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8929a-178">RELATED LINKS</span></span>
