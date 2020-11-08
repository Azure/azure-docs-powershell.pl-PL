---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233399"
---
# <span data-ttu-id="48ea0-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="48ea0-101">New-AzMlWebService</span></span>

## <span data-ttu-id="48ea0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48ea0-102">SYNOPSIS</span></span>
<span data-ttu-id="48ea0-103">Tworzy nową usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="48ea0-103">Creates a new web service.</span></span>

## <span data-ttu-id="48ea0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48ea0-104">SYNTAX</span></span>

### <span data-ttu-id="48ea0-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="48ea0-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48ea0-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="48ea0-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48ea0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="48ea0-107">DESCRIPTION</span></span>
<span data-ttu-id="48ea0-108">Tworzy usługę sieci Web Azure Machine Learning w istniejącej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="48ea0-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="48ea0-109">Jeśli w grupie zasobów istnieje usługa sieci Web o tej samej nazwie, to połączenie działa jako operacja aktualizacji, a istniejąca usługa sieci Web zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="48ea0-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="48ea0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48ea0-110">EXAMPLES</span></span>

### <span data-ttu-id="48ea0-111">Przykład 1. Tworzenie nowej usługi z definicji opartej na pliku JSON</span><span class="sxs-lookup"><span data-stu-id="48ea0-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="48ea0-112">Tworzy nową usługę sieci Web Azure Machine Learning o nazwie "" w grupie "Moja zasobów" i w Południowo-środkowe region w Stanach Zjednoczonych na podstawie definicji obecnej w pliku JSON odwołania.</span><span class="sxs-lookup"><span data-stu-id="48ea0-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="48ea0-113">Przykład 2: Tworzenie nowej usługi z wystąpienia obiektu</span><span class="sxs-lookup"><span data-stu-id="48ea0-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="48ea0-114">Za pomocą polecenia cmdlet Import-AzMlWebService można uzyskać wystąpienie obiektu usługi sieci Web w celu dostosowania przed opublikowaniem jako zasobu.</span><span class="sxs-lookup"><span data-stu-id="48ea0-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="48ea0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48ea0-115">PARAMETERS</span></span>

### <span data-ttu-id="48ea0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ea0-116">-DefaultProfile</span></span>
<span data-ttu-id="48ea0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="48ea0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48ea0-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="48ea0-118">-DefinitionFile</span></span>
<span data-ttu-id="48ea0-119">Określa ścieżkę do pliku zawierającego definicję formatu JSON usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="48ea0-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="48ea0-120">Najnowszą specyfikację definicji usługi sieci Web można znaleźć w specyfikacji struktury Swagger w obszarze https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="48ea0-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48ea0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="48ea0-121">-Force</span></span>
<span data-ttu-id="48ea0-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="48ea0-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="48ea0-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="48ea0-123">-Location</span></span>
<span data-ttu-id="48ea0-124">Region usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="48ea0-124">The region of the web service.</span></span>
<span data-ttu-id="48ea0-125">Wprowadź region centrum danych platformy Azure, na przykład "zachodni USA" lub "Południowo-Wschodnia".</span><span class="sxs-lookup"><span data-stu-id="48ea0-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="48ea0-126">Usługę sieci Web można umieścić w dowolnym regionie obsługującym zasoby tego typu.</span><span class="sxs-lookup"><span data-stu-id="48ea0-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="48ea0-127">Usługa sieci Web nie musi znajdować się w tym samym regionie subskrypcji platformy Azure ani w tym samym regionie co grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="48ea0-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="48ea0-128">Grupy zasobów mogą zawierać usługi sieci Web z różnych regionów.</span><span class="sxs-lookup"><span data-stu-id="48ea0-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="48ea0-129">Aby określić, które regiony obsługują poszczególne typy zasobów, użyj Get-AzResourceProvider za pomocą polecenia cmdlet parametru ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="48ea0-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="48ea0-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="48ea0-130">-Name</span></span>
<span data-ttu-id="48ea0-131">Nazwa usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="48ea0-131">The name for the web service.</span></span>
<span data-ttu-id="48ea0-132">Nazwa musi być unikatowa w grupie zasób.</span><span class="sxs-lookup"><span data-stu-id="48ea0-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="48ea0-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="48ea0-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="48ea0-134">Definicja nowej usługi sieci Web zawierająca wszystkie właściwości, które tworzą usługę.</span><span class="sxs-lookup"><span data-stu-id="48ea0-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="48ea0-135">Ten parametr jest wymagany i reprezentuje wystąpienie klasy Microsoft. Azure. Management. MachineLearning. WebServices. models. WebService.</span><span class="sxs-lookup"><span data-stu-id="48ea0-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="48ea0-136">Najnowszą specyfikację definicji usługi sieci Web można znaleźć w specyfikacji struktury Swagger w obszarze https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="48ea0-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48ea0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48ea0-137">-ResourceGroupName</span></span>
<span data-ttu-id="48ea0-138">Grupa zasobów, w której ma zostać umieszczona usługa sieci Web.</span><span class="sxs-lookup"><span data-stu-id="48ea0-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="48ea0-139">Wprowadź region centrum danych platformy Azure, na przykład "zachodni USA" lub "Południowo-Wschodnia".</span><span class="sxs-lookup"><span data-stu-id="48ea0-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="48ea0-140">Usługę sieci Web można umieścić w dowolnym regionie obsługującym zasoby tego typu.</span><span class="sxs-lookup"><span data-stu-id="48ea0-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="48ea0-141">Usługa sieci Web nie musi znajdować się w tym samym regionie subskrypcji platformy Azure ani w tym samym regionie co grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="48ea0-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="48ea0-142">Grupy zasobów mogą zawierać usługi sieci Web z różnych regionów.</span><span class="sxs-lookup"><span data-stu-id="48ea0-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="48ea0-143">Aby określić, które regiony obsługują poszczególne typy zasobów, użyj Get-AzResourceProvider za pomocą polecenia cmdlet parametru ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="48ea0-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="48ea0-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48ea0-144">-Confirm</span></span>
<span data-ttu-id="48ea0-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48ea0-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48ea0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48ea0-146">-WhatIf</span></span>
<span data-ttu-id="48ea0-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48ea0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48ea0-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="48ea0-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48ea0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ea0-149">CommonParameters</span></span>
<span data-ttu-id="48ea0-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48ea0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ea0-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48ea0-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ea0-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48ea0-152">INPUTS</span></span>

### <span data-ttu-id="48ea0-153">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="48ea0-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="48ea0-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48ea0-154">OUTPUTS</span></span>

### <span data-ttu-id="48ea0-155">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="48ea0-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="48ea0-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48ea0-156">NOTES</span></span>
<span data-ttu-id="48ea0-157">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="48ea0-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="48ea0-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48ea0-158">RELATED LINKS</span></span>
