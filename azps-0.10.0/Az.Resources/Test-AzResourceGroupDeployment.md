---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 59bbe7c5309764c41f22aaa99dbb4d47a23f1ba8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892322"
---
# <span data-ttu-id="db468-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db468-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="db468-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db468-102">SYNOPSIS</span></span>
<span data-ttu-id="db468-103">Sprawdza poprawność wdrożenia grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="db468-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="db468-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db468-104">SYNTAX</span></span>

### <span data-ttu-id="db468-105">ByTemplateFileWithNoParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="db468-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db468-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="db468-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db468-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="db468-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db468-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="db468-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db468-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="db468-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db468-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="db468-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db468-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="db468-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db468-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="db468-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db468-113">Opis</span><span class="sxs-lookup"><span data-stu-id="db468-113">DESCRIPTION</span></span>
<span data-ttu-id="db468-114">Polecenie cmdlet **test-AzResourceGroupDeployment** określa, czy szablon wdrożenia grup zasobów platformy Azure i jego wartości parametrów są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="db468-114">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="db468-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db468-115">EXAMPLES</span></span>

## <span data-ttu-id="db468-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db468-116">PARAMETERS</span></span>

### <span data-ttu-id="db468-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="db468-117">-ApiVersion</span></span>
<span data-ttu-id="db468-118">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="db468-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="db468-119">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="db468-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="db468-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db468-120">-DefaultProfile</span></span>
<span data-ttu-id="db468-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="db468-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db468-122">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="db468-122">-Mode</span></span>
<span data-ttu-id="db468-123">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="db468-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="db468-124">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="db468-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db468-125">Dodatkowe</span><span class="sxs-lookup"><span data-stu-id="db468-125">Incremental</span></span>
- <span data-ttu-id="db468-126">Pełni</span><span class="sxs-lookup"><span data-stu-id="db468-126">Complete</span></span>

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

### <span data-ttu-id="db468-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="db468-127">-Pre</span></span>
<span data-ttu-id="db468-128">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="db468-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="db468-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db468-129">-ResourceGroupName</span></span>
<span data-ttu-id="db468-130">Określa nazwę grupy zasobów do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="db468-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="db468-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="db468-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="db468-132">Wycofanie do poprawnego wdrożenia o podanej nazwie w grupie zasobów nie powinno być używane, jeśli jest używana funkcja-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="db468-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="db468-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="db468-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="db468-134">Wycofanie do ostatniego poprawnego wdrożenia w grupie zasobów nie powinno być dostępne, jeśli jest używana funkcja-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="db468-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="db468-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="db468-135">-TemplateFile</span></span>
<span data-ttu-id="db468-136">Określa pełną ścieżkę pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="db468-136">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="db468-137">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="db468-137">-TemplateParameterFile</span></span>
<span data-ttu-id="db468-138">Określa pełną ścieżkę pliku JSON zawierającego nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="db468-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="db468-139">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="db468-139">-TemplateParameterObject</span></span>
<span data-ttu-id="db468-140">Określa tabelę skrótów zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="db468-140">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="db468-141">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="db468-141">-TemplateParameterUri</span></span>
<span data-ttu-id="db468-142">Określa identyfikator URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="db468-142">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="db468-143">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="db468-143">-TemplateUri</span></span>
<span data-ttu-id="db468-144">Określa identyfikator URI pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="db468-144">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="db468-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db468-145">CommonParameters</span></span>
<span data-ttu-id="db468-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db468-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db468-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db468-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db468-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db468-148">INPUTS</span></span>

### <span data-ttu-id="db468-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="db468-149">None</span></span>

## <span data-ttu-id="db468-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db468-150">OUTPUTS</span></span>

### <span data-ttu-id="db468-151">Microsoft. Azure. Commands. ResourceManager. modele. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="db468-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="db468-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db468-152">NOTES</span></span>

## <span data-ttu-id="db468-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db468-153">RELATED LINKS</span></span>

[<span data-ttu-id="db468-154">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db468-154">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="db468-155">Nowe — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db468-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="db468-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db468-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="db468-157">Zatrzymaj — AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db468-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


