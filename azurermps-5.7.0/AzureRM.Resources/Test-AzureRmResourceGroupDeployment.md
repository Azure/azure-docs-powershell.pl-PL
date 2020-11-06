---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 0caf541aeadcbf2617ae5d31d0dfaf69e432e888
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551604"
---
# <span data-ttu-id="af311-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="af311-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="af311-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af311-102">SYNOPSIS</span></span>
<span data-ttu-id="af311-103">Sprawdza poprawność wdrożenia grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="af311-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af311-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af311-104">SYNTAX</span></span>

### <span data-ttu-id="af311-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="af311-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af311-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="af311-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af311-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="af311-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af311-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="af311-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af311-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="af311-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af311-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="af311-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af311-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="af311-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af311-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="af311-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af311-113">Opis</span><span class="sxs-lookup"><span data-stu-id="af311-113">DESCRIPTION</span></span>
<span data-ttu-id="af311-114">Polecenie cmdlet **test-AzureRmResourceGroupDeployment** określa, czy szablon wdrożenia grup zasobów platformy Azure i jego wartości parametrów są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="af311-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="af311-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af311-115">EXAMPLES</span></span>

## <span data-ttu-id="af311-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af311-116">PARAMETERS</span></span>

### <span data-ttu-id="af311-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="af311-117">-ApiVersion</span></span>
<span data-ttu-id="af311-118">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="af311-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="af311-119">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="af311-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="af311-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af311-120">-DefaultProfile</span></span>
<span data-ttu-id="af311-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="af311-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af311-122">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="af311-122">-Mode</span></span>
<span data-ttu-id="af311-123">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="af311-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="af311-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="af311-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="af311-125">Dodatkowe</span><span class="sxs-lookup"><span data-stu-id="af311-125">Incremental</span></span>
- <span data-ttu-id="af311-126">Pełni</span><span class="sxs-lookup"><span data-stu-id="af311-126">Complete</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af311-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="af311-127">-Pre</span></span>
<span data-ttu-id="af311-128">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="af311-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="af311-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af311-129">-ResourceGroupName</span></span>
<span data-ttu-id="af311-130">Określa nazwę grupy zasobów do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="af311-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="af311-131">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="af311-131">-TemplateFile</span></span>
<span data-ttu-id="af311-132">Określa pełną ścieżkę pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="af311-132">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="af311-133">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="af311-133">-TemplateParameterFile</span></span>
<span data-ttu-id="af311-134">Określa pełną ścieżkę pliku JSON zawierającego nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="af311-134">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="af311-135">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="af311-135">-TemplateParameterObject</span></span>
<span data-ttu-id="af311-136">Określa tabelę skrótów zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="af311-136">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="af311-137">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="af311-137">-TemplateParameterUri</span></span>
<span data-ttu-id="af311-138">Określa identyfikator URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="af311-138">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="af311-139">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="af311-139">-TemplateUri</span></span>
<span data-ttu-id="af311-140">Określa identyfikator URI pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="af311-140">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="af311-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af311-141">CommonParameters</span></span>
<span data-ttu-id="af311-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af311-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af311-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af311-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af311-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af311-144">INPUTS</span></span>

### <span data-ttu-id="af311-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="af311-145">None</span></span>
<span data-ttu-id="af311-146">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="af311-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af311-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af311-147">OUTPUTS</span></span>

### <span data-ttu-id="af311-148">System. Collections. Generic. list "1 [Microsoft. Azure. Commands.</span><span class="sxs-lookup"><span data-stu-id="af311-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="af311-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af311-149">NOTES</span></span>

## <span data-ttu-id="af311-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af311-150">RELATED LINKS</span></span>

[<span data-ttu-id="af311-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="af311-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="af311-152">Nowe — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="af311-152">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="af311-153">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="af311-153">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="af311-154">Zatrzymaj — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="af311-154">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


