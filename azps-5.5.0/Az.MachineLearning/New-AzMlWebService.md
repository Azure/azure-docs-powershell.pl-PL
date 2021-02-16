---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190298"
---
# <span data-ttu-id="e07e2-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="e07e2-101">New-AzMlWebService</span></span>

## <span data-ttu-id="e07e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e07e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e07e2-103">Tworzy nową usługę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e07e2-103">Creates a new web service.</span></span>

## <span data-ttu-id="e07e2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e07e2-104">SYNTAX</span></span>

### <span data-ttu-id="e07e2-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="e07e2-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07e2-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="e07e2-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e07e2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e07e2-107">DESCRIPTION</span></span>
<span data-ttu-id="e07e2-108">Tworzy usługę internetową Azure Machine Learning w istniejącej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e07e2-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="e07e2-109">Jeśli w grupie zasobów istnieje usługa sieci Web o takiej samej nazwie, połączenie działa jako operacja aktualizacji, a istniejąca usługa sieci Web jest zastępowana.</span><span class="sxs-lookup"><span data-stu-id="e07e2-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="e07e2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e07e2-110">EXAMPLES</span></span>

### <span data-ttu-id="e07e2-111">Przykład 1. Tworzenie nowej usługi na podstawie definicji pliku Jsona</span><span class="sxs-lookup"><span data-stu-id="e07e2-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="e07e2-112">Tworzy nową usługę internetową Azure Machine Learning o nazwie "mywebservicename" w grupie "myresourcegroup" i regionie Południowo-środkowych Stanów Zjednoczonych na podstawie definicji z pliku json, do których następuje odwołanie.</span><span class="sxs-lookup"><span data-stu-id="e07e2-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="e07e2-113">Przykład 2. Tworzenie nowej usługi z wystąpienia obiektu</span><span class="sxs-lookup"><span data-stu-id="e07e2-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="e07e2-114">Wystąpienie obiektu usługi sieci Web można uzyskać w celu dostosowania przed opublikowaniem jako zasób za pomocą Import-AzMlWebService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e07e2-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="e07e2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e07e2-115">PARAMETERS</span></span>

### <span data-ttu-id="e07e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07e2-116">-DefaultProfile</span></span>
<span data-ttu-id="e07e2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e07e2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e07e2-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e07e2-118">-DefinitionFile</span></span>
<span data-ttu-id="e07e2-119">Określa ścieżkę do pliku zawierającego definicję formatu JSON usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e07e2-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="e07e2-120">Najnowszą specyfikację definicji usługi sieci Web można znaleźć w specyfikacji swaggera w obszarze https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="e07e2-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

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

### <span data-ttu-id="e07e2-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e07e2-121">-Force</span></span>
<span data-ttu-id="e07e2-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e07e2-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e07e2-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e07e2-123">-Location</span></span>
<span data-ttu-id="e07e2-124">Region usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e07e2-124">The region of the web service.</span></span>
<span data-ttu-id="e07e2-125">Wprowadź region centrum danych platformy Azure, na przykład "Stany Zjednoczone Zachód" lub "Azja Południowo-Wschodnia".</span><span class="sxs-lookup"><span data-stu-id="e07e2-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="e07e2-126">Usługę sieci Web można umieścić w dowolnym regionie, który obsługuje zasoby tego typu.</span><span class="sxs-lookup"><span data-stu-id="e07e2-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="e07e2-127">Usługa sieci Web nie musi być w tym samym regionie, w których jest subskrybowanie platformy Azure, ani w tym samym regionie co grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="e07e2-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="e07e2-128">Grupy zasobów mogą zawierać usługi sieci Web z różnych regionów.</span><span class="sxs-lookup"><span data-stu-id="e07e2-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="e07e2-129">Aby określić, które regiony obsługują poszczególne typy zasobów, użyj Get-AzResourceProvider z poleceniem cmdlet parametru ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="e07e2-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="e07e2-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e07e2-130">-Name</span></span>
<span data-ttu-id="e07e2-131">Nazwa usługi sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e07e2-131">The name for the web service.</span></span>
<span data-ttu-id="e07e2-132">Nazwa musi być unikatowa w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e07e2-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="e07e2-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="e07e2-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="e07e2-134">Definicja nowej usługi sieci Web zawierająca wszystkie właściwości, które ją zawierają.</span><span class="sxs-lookup"><span data-stu-id="e07e2-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="e07e2-135">Ten parametr jest wymagany i reprezentuje wystąpienie klasy Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span><span class="sxs-lookup"><span data-stu-id="e07e2-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="e07e2-136">Najnowszą specyfikację definicji usługi sieci Web można znaleźć w specyfikacji swaggera w obszarze https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="e07e2-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

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

### <span data-ttu-id="e07e2-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e07e2-137">-ResourceGroupName</span></span>
<span data-ttu-id="e07e2-138">Grupa zasobów, w której ma być umieszczana usługa sieci Web.</span><span class="sxs-lookup"><span data-stu-id="e07e2-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="e07e2-139">Wprowadź region centrum danych platformy Azure, na przykład "Stany Zjednoczone Zachód" lub "Azja Południowo-Wschodnia".</span><span class="sxs-lookup"><span data-stu-id="e07e2-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="e07e2-140">Usługę sieci Web można umieścić w dowolnym regionie, który obsługuje zasoby tego typu.</span><span class="sxs-lookup"><span data-stu-id="e07e2-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="e07e2-141">Usługa sieci Web nie musi być w tym samym regionie, w których jest subskrybowanie platformy Azure, ani w tym samym regionie co grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="e07e2-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="e07e2-142">Grupy zasobów mogą zawierać usługi sieci Web z różnych regionów.</span><span class="sxs-lookup"><span data-stu-id="e07e2-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="e07e2-143">Aby określić, które regiony obsługują poszczególne typy zasobów, użyj Get-AzResourceProvider z poleceniem cmdlet parametru ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="e07e2-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="e07e2-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e07e2-144">-Confirm</span></span>
<span data-ttu-id="e07e2-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e07e2-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e07e2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e07e2-146">-WhatIf</span></span>
<span data-ttu-id="e07e2-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e07e2-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e07e2-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e07e2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e07e2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07e2-149">CommonParameters</span></span>
<span data-ttu-id="e07e2-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e07e2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07e2-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e07e2-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07e2-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e07e2-152">INPUTS</span></span>

### <span data-ttu-id="e07e2-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="e07e2-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="e07e2-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e07e2-154">OUTPUTS</span></span>

### <span data-ttu-id="e07e2-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="e07e2-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="e07e2-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e07e2-156">NOTES</span></span>
<span data-ttu-id="e07e2-157">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="e07e2-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e07e2-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e07e2-158">RELATED LINKS</span></span>
