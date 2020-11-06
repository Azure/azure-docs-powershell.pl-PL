---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: b357215bf2c4ba032ca44e37cc445e12606aeffe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546079"
---
# <span data-ttu-id="1df21-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1df21-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="1df21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1df21-102">SYNOPSIS</span></span>
<span data-ttu-id="1df21-103">Sprawdza poprawność wdrożenia grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1df21-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1df21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1df21-104">SYNTAX</span></span>

### <span data-ttu-id="1df21-105">Wdrożenie za pośrednictwem pliku szablonu bez parametrów (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1df21-105">Deployment via template file without parameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1df21-106">Obiekt wdrażania za pośrednictwem szablonu plik i parametry szablonu</span><span class="sxs-lookup"><span data-stu-id="1df21-106">Deployment via template file and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1df21-107">Wdrażanie za pośrednictwem obiektu identyfikator URI szablonu i parametry szablonu</span><span class="sxs-lookup"><span data-stu-id="1df21-107">Deployment via template uri and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1df21-108">Wdrażanie za pośrednictwem pliku szablonu i pliku parametrów szablonu</span><span class="sxs-lookup"><span data-stu-id="1df21-108">Deployment via template file and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1df21-109">Wdrożenie przy użyciu identyfikatora URI szablonu i pliku parametrów szablonu</span><span class="sxs-lookup"><span data-stu-id="1df21-109">Deployment via template uri and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1df21-110">Wdrażanie za pośrednictwem szablonu pliku szablonu o identyfikatorze URI</span><span class="sxs-lookup"><span data-stu-id="1df21-110">Deployment via template file template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1df21-111">Wdrażanie za pośrednictwem identyfikatora URI szablonu i parametrów szablonu URI</span><span class="sxs-lookup"><span data-stu-id="1df21-111">Deployment via template uri and template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1df21-112">Wdrożenie za pośrednictwem identyfikatora URI szablonu bez parametrów</span><span class="sxs-lookup"><span data-stu-id="1df21-112">Deployment via template uri without parameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1df21-113">Opis</span><span class="sxs-lookup"><span data-stu-id="1df21-113">DESCRIPTION</span></span>
<span data-ttu-id="1df21-114">Polecenie cmdlet **test-AzureRmResourceGroupDeployment** określa, czy szablon wdrożenia grup zasobów platformy Azure i jego wartości parametrów są prawidłowe.</span><span class="sxs-lookup"><span data-stu-id="1df21-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="1df21-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1df21-115">EXAMPLES</span></span>

## <span data-ttu-id="1df21-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1df21-116">PARAMETERS</span></span>

### <span data-ttu-id="1df21-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1df21-117">-ApiVersion</span></span>
<span data-ttu-id="1df21-118">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="1df21-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="1df21-119">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="1df21-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="1df21-120">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="1df21-120">-Mode</span></span>
<span data-ttu-id="1df21-121">Określa tryb wdrażania.</span><span class="sxs-lookup"><span data-stu-id="1df21-121">Specifies the deployment mode.</span></span>
<span data-ttu-id="1df21-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1df21-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1df21-123">Dodatkowe</span><span class="sxs-lookup"><span data-stu-id="1df21-123">Incremental</span></span>
- <span data-ttu-id="1df21-124">Pełni</span><span class="sxs-lookup"><span data-stu-id="1df21-124">Complete</span></span>

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

### <span data-ttu-id="1df21-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="1df21-125">-Pre</span></span>
<span data-ttu-id="1df21-126">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="1df21-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1df21-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1df21-127">-ResourceGroupName</span></span>
<span data-ttu-id="1df21-128">Określa nazwę grupy zasobów do przetestowania.</span><span class="sxs-lookup"><span data-stu-id="1df21-128">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="1df21-129">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="1df21-129">-TemplateFile</span></span>
<span data-ttu-id="1df21-130">Określa pełną ścieżkę pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="1df21-130">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1df21-131">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="1df21-131">-TemplateParameterFile</span></span>
<span data-ttu-id="1df21-132">Określa pełną ścieżkę pliku JSON zawierającego nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="1df21-132">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1df21-133">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="1df21-133">-TemplateParameterObject</span></span>
<span data-ttu-id="1df21-134">Określa tabelę skrótów zawierającą nazwy i wartości parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="1df21-134">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1df21-135">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="1df21-135">-TemplateParameterUri</span></span>
<span data-ttu-id="1df21-136">Określa identyfikator URI pliku parametrów szablonu.</span><span class="sxs-lookup"><span data-stu-id="1df21-136">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1df21-137">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="1df21-137">-TemplateUri</span></span>
<span data-ttu-id="1df21-138">Określa identyfikator URI pliku szablonu JSON.</span><span class="sxs-lookup"><span data-stu-id="1df21-138">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1df21-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1df21-139">-DefaultProfile</span></span>
<span data-ttu-id="1df21-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1df21-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1df21-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df21-141">CommonParameters</span></span>
<span data-ttu-id="1df21-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1df21-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df21-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1df21-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df21-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1df21-144">INPUTS</span></span>

## <span data-ttu-id="1df21-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1df21-145">OUTPUTS</span></span>

### <span data-ttu-id="1df21-146">System. Collections. Generic. list "1 [Microsoft. Azure. Commands.</span><span class="sxs-lookup"><span data-stu-id="1df21-146">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="1df21-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1df21-147">NOTES</span></span>

## <span data-ttu-id="1df21-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1df21-148">RELATED LINKS</span></span>

[<span data-ttu-id="1df21-149">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1df21-149">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="1df21-150">Nowe — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1df21-150">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="1df21-151">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1df21-151">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="1df21-152">Zatrzymaj — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1df21-152">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


