---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: df6392e339063ccb2cc60411b77f73936071ab3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554138"
---
# <span data-ttu-id="f49db-101">New-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="f49db-101">New-AzureRmMlWebService</span></span>

## <span data-ttu-id="f49db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f49db-102">SYNOPSIS</span></span>
<span data-ttu-id="f49db-103">Tworzy nową usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f49db-103">Creates a new web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f49db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f49db-104">SYNTAX</span></span>

### <span data-ttu-id="f49db-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="f49db-105">CreateFromFile</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f49db-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="f49db-106">CreateFromInstance</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f49db-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f49db-107">DESCRIPTION</span></span>
<span data-ttu-id="f49db-108">Tworzy usługę sieci Web Azure Machine Learning w istniejącej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="f49db-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="f49db-109">Jeśli w grupie zasobów istnieje usługa sieci Web o tej samej nazwie, to połączenie działa jako operacja aktualizacji, a istniejąca usługa sieci Web zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="f49db-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="f49db-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f49db-110">EXAMPLES</span></span>

### <span data-ttu-id="f49db-111">--------------------------Przykład 1: Tworzenie nowej usługi na podstawie definicji pliku JSON--------------------------</span><span class="sxs-lookup"><span data-stu-id="f49db-111">--------------------------  Example 1: Create a new service from a Json file based definition  --------------------------</span></span>
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="f49db-112">Tworzy nową usługę sieci Web Azure Machine Learning o nazwie "" w grupie "Moja zasobów" i w Południowo-środkowe region w Stanach Zjednoczonych na podstawie definicji obecnej w pliku JSON odwołania.</span><span class="sxs-lookup"><span data-stu-id="f49db-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="f49db-113">--------------------------Przykład 2: Tworzenie nowej usługi z wystąpienia obiektu--------------------------</span><span class="sxs-lookup"><span data-stu-id="f49db-113">--------------------------  Example 2: Create a new service from an object instance  --------------------------</span></span>
```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="f49db-114">Za pomocą polecenia cmdlet Import-AzureRmMlWebService można uzyskać wystąpienie obiektu usługi sieci Web w celu dostosowania przed opublikowaniem jako zasobu.</span><span class="sxs-lookup"><span data-stu-id="f49db-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="f49db-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f49db-115">PARAMETERS</span></span>

### <span data-ttu-id="f49db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f49db-116">-DefaultProfile</span></span>
<span data-ttu-id="f49db-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f49db-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f49db-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="f49db-118">-DefinitionFile</span></span>
<span data-ttu-id="f49db-119">Specifes ścieżkę do pliku zawierającego definicję formatu JSON usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f49db-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="f49db-120">Najnowszą specyfikację definicji usługi sieci Web można znaleźć w specyfikacji struktury Swagger w obszarze https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="f49db-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: String
Parameter Sets: CreateFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f49db-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f49db-121">-Force</span></span>
<span data-ttu-id="f49db-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f49db-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f49db-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f49db-123">-Location</span></span>
<span data-ttu-id="f49db-124">Region usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f49db-124">The region of the web service.</span></span>
<span data-ttu-id="f49db-125">Wprowadź region centrum danych platformy Azure, na przykład "zachodni USA" lub "Południowo-Wschodnia".</span><span class="sxs-lookup"><span data-stu-id="f49db-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="f49db-126">Usługę sieci Web można umieścić w dowolnym regionie obsługującym zasoby tego typu.</span><span class="sxs-lookup"><span data-stu-id="f49db-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="f49db-127">Usługa sieci Web nie musi znajdować się w tym samym regionie subskrypcji platformy Azure ani w tym samym regionie co grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="f49db-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="f49db-128">Grupy zasobów mogą zawierać usługi sieci Web z różnych regionów.</span><span class="sxs-lookup"><span data-stu-id="f49db-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="f49db-129">Aby określić, które regiony obsługują poszczególne typy zasobów, użyj Get-AzureRmResourceProvider za pomocą polecenia cmdlet parametru ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="f49db-129">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="f49db-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f49db-130">-Name</span></span>
<span data-ttu-id="f49db-131">Nazwa usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f49db-131">The name for the web service.</span></span>
<span data-ttu-id="f49db-132">Nazwa musi być unikatowa w grupie zasób.</span><span class="sxs-lookup"><span data-stu-id="f49db-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="f49db-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="f49db-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="f49db-134">Definicja nowej usługi sieci Web zawierająca wszystkie właściwości, które tworzą usługę.</span><span class="sxs-lookup"><span data-stu-id="f49db-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="f49db-135">Ten parametr jest wymagany i reprezentuje wystąpienie klasy Microsoft. Azure. Management. MachineLearning. WebServices. models. WebService.</span><span class="sxs-lookup"><span data-stu-id="f49db-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="f49db-136">Najnowszą specyfikację definicji usługi sieci Web można znaleźć w specyfikacji struktury Swagger w obszarze https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="f49db-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: WebService
Parameter Sets: CreateFromInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f49db-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f49db-137">-ResourceGroupName</span></span>
<span data-ttu-id="f49db-138">Grupa zasobów, w której ma zostać umieszczona usługa sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f49db-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="f49db-139">Wprowadź region centrum danych platformy Azure, na przykład "zachodni USA" lub "Południowo-Wschodnia".</span><span class="sxs-lookup"><span data-stu-id="f49db-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="f49db-140">Usługę sieci Web można umieścić w dowolnym regionie obsługującym zasoby tego typu.</span><span class="sxs-lookup"><span data-stu-id="f49db-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="f49db-141">Usługa sieci Web nie musi znajdować się w tym samym regionie subskrypcji platformy Azure ani w tym samym regionie co grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="f49db-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="f49db-142">Grupy zasobów mogą zawierać usługi sieci Web z różnych regionów.</span><span class="sxs-lookup"><span data-stu-id="f49db-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="f49db-143">Aby określić, które regiony obsługują poszczególne typy zasobów, użyj Get-AzureRmResourceProvider za pomocą polecenia cmdlet parametru ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="f49db-143">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="f49db-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f49db-144">-Confirm</span></span>
<span data-ttu-id="f49db-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f49db-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f49db-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f49db-146">-WhatIf</span></span>
<span data-ttu-id="f49db-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f49db-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f49db-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f49db-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f49db-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49db-149">CommonParameters</span></span>
<span data-ttu-id="f49db-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f49db-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49db-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f49db-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49db-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f49db-152">INPUTS</span></span>

### <span data-ttu-id="f49db-153">Usług</span><span class="sxs-lookup"><span data-stu-id="f49db-153">WebService</span></span>
<span data-ttu-id="f49db-154">Parametr "NewWebServiceDefinition" akceptuje wartość typu "WebService" z procesu</span><span class="sxs-lookup"><span data-stu-id="f49db-154">Parameter 'NewWebServiceDefinition' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="f49db-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f49db-155">OUTPUTS</span></span>

### <span data-ttu-id="f49db-156">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="f49db-156">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="f49db-157">Skrócony opis usługi sieci Web Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="f49db-157">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="f49db-158">Podobny do opisu zwróconego przez wywołanie polecenia cmdlet Get-AzureRmMlWebService w istniejącej usłudze sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f49db-158">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="f49db-159">Ten opis nie zawiera poufnych właściwości, takich jak poświadczenia konta magazynu i klucze dostępu usługi.</span><span class="sxs-lookup"><span data-stu-id="f49db-159">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="f49db-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f49db-160">NOTES</span></span>
<span data-ttu-id="f49db-161">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="f49db-161">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f49db-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f49db-162">RELATED LINKS</span></span>

