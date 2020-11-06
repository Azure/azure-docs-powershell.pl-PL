---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: 1fe6476836622445337ea0b4741b361504a57302
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553839"
---
# <span data-ttu-id="5776f-101">New-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="5776f-101">New-AzureRmMlWebService</span></span>

## <span data-ttu-id="5776f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5776f-102">SYNOPSIS</span></span>
<span data-ttu-id="5776f-103">Tworzy nową usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5776f-103">Creates a new web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5776f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5776f-104">SYNTAX</span></span>

### <span data-ttu-id="5776f-105">Utwórz nową usługę sieci Web usługi Azure ML z pliku Definiton JSON.</span><span class="sxs-lookup"><span data-stu-id="5776f-105">Create a new Azure ML webservice from a JSON definiton file.</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5776f-106">Utwórz nową usługę sieci Web Azure ML z definicji wystąpienia usługi WebService.</span><span class="sxs-lookup"><span data-stu-id="5776f-106">Create a new Azure ML webservice from a WebService instance definition.</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5776f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5776f-107">DESCRIPTION</span></span>
<span data-ttu-id="5776f-108">Tworzy usługę sieci Web Azure Machine Learning w istniejącej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="5776f-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="5776f-109">Jeśli w grupie zasobów istnieje usługa sieci Web o tej samej nazwie, to połączenie działa jako operacja aktualizacji, a istniejąca usługa sieci Web zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="5776f-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="5776f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5776f-110">EXAMPLES</span></span>

### <span data-ttu-id="5776f-111">--------------------------Przykład 1: Tworzenie nowej usługi na podstawie definicji pliku JSON--------------------------</span><span class="sxs-lookup"><span data-stu-id="5776f-111">--------------------------  Example 1: Create a new service from a Json file based definition  --------------------------</span></span>
<span data-ttu-id="5776f-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="5776f-112">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="5776f-113">Tworzy nową usługę sieci Web Azure Machine Learning o nazwie "" w grupie "Moja zasobów" i w Południowo-środkowe region w Stanach Zjednoczonych na podstawie definicji obecnej w pliku JSON odwołania.</span><span class="sxs-lookup"><span data-stu-id="5776f-113">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="5776f-114">--------------------------Przykład 2: Tworzenie nowej usługi z wystąpienia obiektu--------------------------</span><span class="sxs-lookup"><span data-stu-id="5776f-114">--------------------------  Example 2: Create a new service from an object instance  --------------------------</span></span>
<span data-ttu-id="5776f-115">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="5776f-115">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="5776f-116">Za pomocą polecenia cmdlet Import-AzureRmMlWebService można uzyskać wystąpienie obiektu usługi sieci Web w celu dostosowania przed opublikowaniem jako zasobu.</span><span class="sxs-lookup"><span data-stu-id="5776f-116">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="5776f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5776f-117">PARAMETERS</span></span>

### <span data-ttu-id="5776f-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="5776f-118">-DefinitionFile</span></span>
<span data-ttu-id="5776f-119">Specifes ścieżkę do pliku zawierającego definicję formatu JSON usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5776f-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="5776f-120">Najnowszą specyfikację definicji usługi sieci Web można znaleźć w specyfikacji struktury Swagger w obszarze https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="5776f-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: Create a new Azure ML webservice from a JSON definiton file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5776f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5776f-121">-Force</span></span>
<span data-ttu-id="5776f-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5776f-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5776f-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5776f-123">-Location</span></span>
<span data-ttu-id="5776f-124">Region usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5776f-124">The region of the web service.</span></span>
<span data-ttu-id="5776f-125">Wprowadź region centrum danych platformy Azure, na przykład "zachodni USA" lub "Południowo-Wschodnia".</span><span class="sxs-lookup"><span data-stu-id="5776f-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="5776f-126">Usługę sieci Web można umieścić w dowolnym regionie obsługującym zasoby tego typu.</span><span class="sxs-lookup"><span data-stu-id="5776f-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="5776f-127">Usługa sieci Web nie musi znajdować się w tym samym regionie subskrypcji platformy Azure ani w tym samym regionie co grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="5776f-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="5776f-128">Grupy zasobów mogą zawierać usługi sieci Web z różnych regionów.</span><span class="sxs-lookup"><span data-stu-id="5776f-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="5776f-129">Aby określić, które regiony obsługują poszczególne typy zasobów, użyj Get-AzureRmResourceProvider za pomocą polecenia cmdlet parametru ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="5776f-129">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="5776f-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5776f-130">-Name</span></span>
<span data-ttu-id="5776f-131">Nazwa usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5776f-131">The name for the web service.</span></span>
<span data-ttu-id="5776f-132">Nazwa musi być unikatowa w grupie zasób.</span><span class="sxs-lookup"><span data-stu-id="5776f-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="5776f-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="5776f-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="5776f-134">Definicja nowej usługi sieci Web zawierająca wszystkie właściwości, które tworzą usługę.</span><span class="sxs-lookup"><span data-stu-id="5776f-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="5776f-135">Ten parametr jest wymagany i reprezentuje wystąpienie klasy Microsoft. Azure. Management. MachineLearning. WebServices. models. WebService.</span><span class="sxs-lookup"><span data-stu-id="5776f-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="5776f-136">Najnowszą specyfikację definicji usługi sieci Web można znaleźć w specyfikacji struktury Swagger w obszarze https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="5776f-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5776f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5776f-137">-ResourceGroupName</span></span>
<span data-ttu-id="5776f-138">Grupa zasobów, w której ma zostać umieszczona usługa sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5776f-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="5776f-139">Wprowadź region centrum danych platformy Azure, na przykład "zachodni USA" lub "Południowo-Wschodnia".</span><span class="sxs-lookup"><span data-stu-id="5776f-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="5776f-140">Usługę sieci Web można umieścić w dowolnym regionie obsługującym zasoby tego typu.</span><span class="sxs-lookup"><span data-stu-id="5776f-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="5776f-141">Usługa sieci Web nie musi znajdować się w tym samym regionie subskrypcji platformy Azure ani w tym samym regionie co grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="5776f-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="5776f-142">Grupy zasobów mogą zawierać usługi sieci Web z różnych regionów.</span><span class="sxs-lookup"><span data-stu-id="5776f-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="5776f-143">Aby określić, które regiony obsługują poszczególne typy zasobów, użyj Get-AzureRmResourceProvider za pomocą polecenia cmdlet parametru ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="5776f-143">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="5776f-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5776f-144">-Confirm</span></span>
<span data-ttu-id="5776f-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5776f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5776f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5776f-146">-WhatIf</span></span>
<span data-ttu-id="5776f-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5776f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5776f-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5776f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5776f-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5776f-149">-DefaultProfile</span></span>
<span data-ttu-id="5776f-150">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5776f-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5776f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5776f-151">CommonParameters</span></span>
<span data-ttu-id="5776f-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5776f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5776f-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5776f-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5776f-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5776f-154">INPUTS</span></span>

### <span data-ttu-id="5776f-155">Usług</span><span class="sxs-lookup"><span data-stu-id="5776f-155">WebService</span></span>
<span data-ttu-id="5776f-156">Parametr "NewWebServiceDefinition" akceptuje wartość typu "WebService" z procesu</span><span class="sxs-lookup"><span data-stu-id="5776f-156">Parameter 'NewWebServiceDefinition' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="5776f-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5776f-157">OUTPUTS</span></span>

### <span data-ttu-id="5776f-158">Microsoft. Azure. Management. MachineLearning. WebServices. modele. WebService</span><span class="sxs-lookup"><span data-stu-id="5776f-158">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="5776f-159">Skrócony opis usługi sieci Web Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="5776f-159">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="5776f-160">Podobny do opisu zwróconego przez wywołanie polecenia cmdlet Get-AzureRmMlWebService w istniejącej usłudze sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5776f-160">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="5776f-161">Ten opis nie zawiera poufnych właściwości, takich jak poświadczenia konta magazynu i klucze dostępu usługi.</span><span class="sxs-lookup"><span data-stu-id="5776f-161">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="5776f-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5776f-162">NOTES</span></span>
<span data-ttu-id="5776f-163">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure</span><span class="sxs-lookup"><span data-stu-id="5776f-163">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5776f-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5776f-164">RELATED LINKS</span></span>

