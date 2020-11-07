---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 51d0405ffbedf5ad5a708fdcf9184ef49dc6ecdb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898629"
---
# <span data-ttu-id="4f7c2-101">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="4f7c2-101">Test-AzureRmDeployment</span></span>

## <span data-ttu-id="4f7c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="4f7c2-103">Sprawdza poprawność wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-103">Validates a deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f7c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f7c2-104">SYNTAX</span></span>

### <span data-ttu-id="4f7c2-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4f7c2-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f7c2-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4f7c2-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f7c2-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4f7c2-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f7c2-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4f7c2-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f7c2-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4f7c2-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f7c2-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4f7c2-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f7c2-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4f7c2-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f7c2-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4f7c2-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmDeployment -Location <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f7c2-113">Opis</span><span class="sxs-lookup"><span data-stu-id="4f7c2-113">DESCRIPTION</span></span>
<span data-ttu-id="4f7c2-114">Polecenie cmdlet **test-AzureRmDeployment** określa, czy szablon wdrożenia i jego wartości parametrów są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-114">The **Test-AzureRmDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="4f7c2-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f7c2-115">EXAMPLES</span></span>

### <span data-ttu-id="4f7c2-116">Przykład 1: Testowanie wdrożenia za pomocą szablonu niestandardowego i pliku parametrów</span><span class="sxs-lookup"><span data-stu-id="4f7c2-116">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\>Test-AzureRmDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="4f7c2-117">To polecenie testuje wdrożenie w bieżącym zakresie subskrypcji przy użyciu danego pliku szablonu i pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-117">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

## <span data-ttu-id="4f7c2-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f7c2-118">PARAMETERS</span></span>

### <span data-ttu-id="4f7c2-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4f7c2-119">-ApiVersion</span></span>
<span data-ttu-id="4f7c2-120">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4f7c2-121">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4f7c2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f7c2-122">-DefaultProfile</span></span>
<span data-ttu-id="4f7c2-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f7c2-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4f7c2-124">-Location</span></span>
<span data-ttu-id="4f7c2-125">Lokalizacja przechowywania danych wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-125">The location to store deployment data.</span></span>

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

### <span data-ttu-id="4f7c2-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="4f7c2-126">-Pre</span></span>
<span data-ttu-id="4f7c2-127">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4f7c2-128">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4f7c2-128">-TemplateFile</span></span>
<span data-ttu-id="4f7c2-129">Lokalna ścieżka do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-129">Local path to the template file.</span></span>

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

### <span data-ttu-id="4f7c2-130">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4f7c2-130">-TemplateParameterFile</span></span>
<span data-ttu-id="4f7c2-131">Plik zawierający parametry szablonu.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-131">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="4f7c2-132">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4f7c2-132">-TemplateParameterObject</span></span>
<span data-ttu-id="4f7c2-133">Tabela skrótów, która reprezentuje parametry.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-133">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="4f7c2-134">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4f7c2-134">-TemplateParameterUri</span></span>
<span data-ttu-id="4f7c2-135">URI do pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-135">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="4f7c2-136">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4f7c2-136">-TemplateUri</span></span>
<span data-ttu-id="4f7c2-137">Identyfikator URI do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-137">Uri to the template file.</span></span>

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

### <span data-ttu-id="4f7c2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f7c2-138">CommonParameters</span></span>
<span data-ttu-id="4f7c2-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f7c2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f7c2-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f7c2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f7c2-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f7c2-141">INPUTS</span></span>

### <span data-ttu-id="4f7c2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4f7c2-142">System.String</span></span>
<span data-ttu-id="4f7c2-143">Microsoft. Azure. Management. ResourceManager. modele. DeploymentMode system. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4f7c2-143">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode System.Collections.Hashtable</span></span>

## <span data-ttu-id="4f7c2-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f7c2-144">OUTPUTS</span></span>

### <span data-ttu-id="4f7c2-145">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="4f7c2-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="4f7c2-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f7c2-146">NOTES</span></span>

## <span data-ttu-id="4f7c2-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f7c2-147">RELATED LINKS</span></span>
