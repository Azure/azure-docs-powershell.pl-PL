---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 97fbda90b27cbfabca8cbfd21c5bf375b86f7adb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898606"
---
# <span data-ttu-id="2e8f6-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2e8f6-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="2e8f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="2e8f6-103">Sprawdza poprawność wdrożenia grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e8f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e8f6-104">SYNTAX</span></span>

### <span data-ttu-id="2e8f6-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2e8f6-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e8f6-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2e8f6-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e8f6-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2e8f6-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e8f6-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2e8f6-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e8f6-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2e8f6-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e8f6-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2e8f6-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e8f6-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2e8f6-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e8f6-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2e8f6-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e8f6-113">Opis</span><span class="sxs-lookup"><span data-stu-id="2e8f6-113">DESCRIPTION</span></span>
<span data-ttu-id="2e8f6-114">Polecenie cmdlet **test-AzureRmResourceGroupDeployment** określa, czy szablon wdrożenia grup zasobów platformy Azure i jego wartości parametrów są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="2e8f6-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e8f6-115">EXAMPLES</span></span>

## <span data-ttu-id="2e8f6-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e8f6-116">PARAMETERS</span></span>

### <span data-ttu-id="2e8f6-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2e8f6-117">-ApiVersion</span></span>
<span data-ttu-id="2e8f6-118">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2e8f6-119">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="2e8f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e8f6-120">-DefaultProfile</span></span>
<span data-ttu-id="2e8f6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2e8f6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e8f6-122">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="2e8f6-122">-Mode</span></span>
<span data-ttu-id="2e8f6-123">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="2e8f6-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2e8f6-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2e8f6-125">Dodatkowe</span><span class="sxs-lookup"><span data-stu-id="2e8f6-125">Incremental</span></span>
- <span data-ttu-id="2e8f6-126">Pełni</span><span class="sxs-lookup"><span data-stu-id="2e8f6-126">Complete</span></span>

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

### <span data-ttu-id="2e8f6-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="2e8f6-127">-Pre</span></span>
<span data-ttu-id="2e8f6-128">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2e8f6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e8f6-129">-ResourceGroupName</span></span>
<span data-ttu-id="2e8f6-130">Określa nazwę grupy zasobów do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="2e8f6-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="2e8f6-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="2e8f6-132">Wycofanie do poprawnego wdrożenia o podanej nazwie w grupie zasobów nie powinno być używane, jeśli jest używana funkcja-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="2e8f6-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="2e8f6-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="2e8f6-134">Wycofanie do ostatniego poprawnego wdrożenia w grupie zasobów nie powinno być dostępne, jeśli jest używana funkcja-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="2e8f6-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2e8f6-135">-TemplateFile</span></span>
<span data-ttu-id="2e8f6-136">Określa pełną ścieżkę pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-136">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="2e8f6-137">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2e8f6-137">-TemplateParameterFile</span></span>
<span data-ttu-id="2e8f6-138">Określa pełną ścieżkę pliku JSON zawierającego nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="2e8f6-139">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2e8f6-139">-TemplateParameterObject</span></span>
<span data-ttu-id="2e8f6-140">Określa tabelę skrótów zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-140">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="2e8f6-141">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2e8f6-141">-TemplateParameterUri</span></span>
<span data-ttu-id="2e8f6-142">Określa identyfikator URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-142">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="2e8f6-143">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2e8f6-143">-TemplateUri</span></span>
<span data-ttu-id="2e8f6-144">Określa identyfikator URI pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-144">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="2e8f6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e8f6-145">CommonParameters</span></span>
<span data-ttu-id="2e8f6-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e8f6-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e8f6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e8f6-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e8f6-148">INPUTS</span></span>

### <span data-ttu-id="2e8f6-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2e8f6-149">None</span></span>

## <span data-ttu-id="2e8f6-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e8f6-150">OUTPUTS</span></span>

### <span data-ttu-id="2e8f6-151">Microsoft. Azure. Commands. ResourceManager. modele. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="2e8f6-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="2e8f6-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e8f6-152">NOTES</span></span>

## <span data-ttu-id="2e8f6-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e8f6-153">RELATED LINKS</span></span>

[<span data-ttu-id="2e8f6-154">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2e8f6-154">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2e8f6-155">Nowe — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2e8f6-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2e8f6-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2e8f6-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2e8f6-157">Zatrzymaj — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2e8f6-157">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


