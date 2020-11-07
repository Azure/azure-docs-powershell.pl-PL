---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: f1109e61c2ea1f8c4d2f20aec7927cc550f95249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718763"
---
# <span data-ttu-id="0907c-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0907c-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="0907c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0907c-102">SYNOPSIS</span></span>
<span data-ttu-id="0907c-103">Sprawdza poprawność wdrożenia grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0907c-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0907c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0907c-104">SYNTAX</span></span>

### <span data-ttu-id="0907c-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0907c-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0907c-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0907c-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0907c-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0907c-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0907c-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0907c-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0907c-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0907c-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0907c-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0907c-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0907c-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0907c-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0907c-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0907c-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0907c-113">Opis</span><span class="sxs-lookup"><span data-stu-id="0907c-113">DESCRIPTION</span></span>
<span data-ttu-id="0907c-114">Polecenie cmdlet **test-AzureRmResourceGroupDeployment** określa, czy szablon wdrożenia grup zasobów platformy Azure i jego wartości parametrów są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="0907c-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="0907c-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0907c-115">EXAMPLES</span></span>

## <span data-ttu-id="0907c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0907c-116">PARAMETERS</span></span>

### <span data-ttu-id="0907c-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0907c-117">-ApiVersion</span></span>
<span data-ttu-id="0907c-118">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="0907c-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0907c-119">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="0907c-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0907c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0907c-120">-DefaultProfile</span></span>
<span data-ttu-id="0907c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0907c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0907c-122">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="0907c-122">-Mode</span></span>
<span data-ttu-id="0907c-123">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="0907c-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="0907c-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0907c-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0907c-125">Dodatkowe</span><span class="sxs-lookup"><span data-stu-id="0907c-125">Incremental</span></span>
- <span data-ttu-id="0907c-126">Pełni</span><span class="sxs-lookup"><span data-stu-id="0907c-126">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0907c-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="0907c-127">-Pre</span></span>
<span data-ttu-id="0907c-128">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="0907c-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0907c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0907c-129">-ResourceGroupName</span></span>
<span data-ttu-id="0907c-130">Określa nazwę grupy zasobów do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="0907c-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="0907c-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="0907c-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="0907c-132">Wycofanie do poprawnego wdrożenia o podanej nazwie w grupie zasobów nie powinno być używane, jeśli jest używana funkcja-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="0907c-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="0907c-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="0907c-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="0907c-134">Wycofanie do ostatniego poprawnego wdrożenia w grupie zasobów nie powinno być dostępne, jeśli jest używana funkcja-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="0907c-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="0907c-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="0907c-135">-TemplateFile</span></span>
<span data-ttu-id="0907c-136">Określa pełną ścieżkę pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="0907c-136">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="0907c-137">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="0907c-137">-TemplateParameterFile</span></span>
<span data-ttu-id="0907c-138">Określa pełną ścieżkę pliku JSON zawierającego nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="0907c-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="0907c-139">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="0907c-139">-TemplateParameterObject</span></span>
<span data-ttu-id="0907c-140">Określa tabelę skrótów zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="0907c-140">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="0907c-141">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="0907c-141">-TemplateParameterUri</span></span>
<span data-ttu-id="0907c-142">Określa identyfikator URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="0907c-142">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="0907c-143">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="0907c-143">-TemplateUri</span></span>
<span data-ttu-id="0907c-144">Określa identyfikator URI pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="0907c-144">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="0907c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0907c-145">CommonParameters</span></span>
<span data-ttu-id="0907c-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0907c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0907c-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0907c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0907c-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0907c-148">INPUTS</span></span>

### <span data-ttu-id="0907c-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0907c-149">None</span></span>

## <span data-ttu-id="0907c-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0907c-150">OUTPUTS</span></span>

### <span data-ttu-id="0907c-151">Microsoft. Azure. Commands. ResourceManager. modele. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="0907c-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="0907c-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0907c-152">NOTES</span></span>

## <span data-ttu-id="0907c-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0907c-153">RELATED LINKS</span></span>

[<span data-ttu-id="0907c-154">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0907c-154">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="0907c-155">Nowe — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0907c-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="0907c-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0907c-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="0907c-157">Zatrzymaj — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0907c-157">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


