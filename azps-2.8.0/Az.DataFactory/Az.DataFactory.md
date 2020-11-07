---
Module Name: Az.DataFactory
Module Guid: e3c0f6bc-fe96-41a0-88f4-5e490a91f05d
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datafactory
Help Version: 0.5.3.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Az.DataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Az.DataFactory.md
ms.openlocfilehash: 8fccc742860bf66016470826b2e837747306514a
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/15/2019
ms.locfileid: "93704448"
---
# <span data-ttu-id="a7405-101">AZ. moduł DataFactory</span><span class="sxs-lookup"><span data-stu-id="a7405-101">Az.DataFactory Module</span></span>
## <span data-ttu-id="a7405-102">Opis</span><span class="sxs-lookup"><span data-stu-id="a7405-102">Description</span></span>
<span data-ttu-id="a7405-103">Usługa Azure Data Factory V2 to platforma integracji danych, która nie obejmuje usługi Azure Data Factory V1's Orchestration i przetwarzania wsadowego danych dziennika serii czasowej, dzięki modelowi aplikacji ogólnego przeznaczenia obsługującym nowoczesne wzorce i scenariusze magazynowania danych, program SSIS + Shift oraz aplikacje SaaS oparte na danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-103">Azure Data Factory V2 is the data integration platform that goes beyond Azure Data Factory V1's orchestration and batch-processing of time-series log data, with a general purpose app model supporting modern data warehousing patterns and scenarios, lift-and-shift SSIS, and data-driven SaaS applications.</span></span> <span data-ttu-id="a7405-104">Tworzenie i zarządzanie wiarygodnymi i bezpiecznymi przepływami pracy integracji danych w skali.</span><span class="sxs-lookup"><span data-stu-id="a7405-104">Compose and manage reliable and secure data integration workflows at scale.</span></span> <span data-ttu-id="a7405-105">Używaj natywnych łączników danych ADF i środowisk uruchomieniowych integracji do przenoszenia i przekształcania danych w chmurze i lokalnie, które mogą być bez struktury, mają strukturę hierarchiczną i mają strukturę usługi Hadoop, Azure Data Lake, Spark, SQL Server, Cosmos DB i wiele innych platform danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-105">Use native ADF data connectors and Integration Runtimes to move and transform cloud and on-premises data that can be unstructured, semi-structured, and structured with Hadoop, Azure Data Lake, Spark, SQL Server, Cosmos DB and many other data platforms.</span></span>

## <span data-ttu-id="a7405-106">AZ. polecenia cmdlet DataFactory</span><span class="sxs-lookup"><span data-stu-id="a7405-106">Az.DataFactory Cmdlets</span></span>
### [<span data-ttu-id="a7405-107">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a7405-107">Get-AzDataFactory</span></span>](Get-AzDataFactory.md)
<span data-ttu-id="a7405-108">Pobiera informacje na temat fabryk danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-108">Gets information about Data Factories.</span></span>

### [<span data-ttu-id="a7405-109">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="a7405-109">Get-AzDataFactoryActivityWindow</span></span>](Get-AzDataFactoryActivityWindow.md)
<span data-ttu-id="a7405-110">Pobiera informacje o oknach działań skojarzonych z fabryką danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-110">Gets information about activity windows associated with a data factory.</span></span>

### [<span data-ttu-id="a7405-111">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="a7405-111">Get-AzDataFactoryDataset</span></span>](Get-AzDataFactoryDataset.md)
<span data-ttu-id="a7405-112">Pobiera informacje o zestawach danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-112">Gets information about datasets in Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-113">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a7405-113">Get-AzDataFactoryGateway</span></span>](Get-AzDataFactoryGateway.md)
<span data-ttu-id="a7405-114">Pobiera informacje o bramach logicznych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-114">Gets information about logical gateways in Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-115">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="a7405-115">Get-AzDataFactoryGatewayAuthKey</span></span>](Get-AzDataFactoryGatewayAuthKey.md)
<span data-ttu-id="a7405-116">Pobiera klucz uwierzytelniania bramy dla fabryki danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7405-116">Gets gateway auth key for an Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-117">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="a7405-117">Get-AzDataFactoryHub</span></span>](Get-AzDataFactoryHub.md)
<span data-ttu-id="a7405-118">Pobiera informacje o koncentratorach w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-118">Gets information about hubs in Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-119">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="a7405-119">Get-AzDataFactoryLinkedService</span></span>](Get-AzDataFactoryLinkedService.md)
<span data-ttu-id="a7405-120">Pobiera informacje o usługach połączonych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-120">Gets information about linked services in Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-121">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a7405-121">Get-AzDataFactoryPipeline</span></span>](Get-AzDataFactoryPipeline.md)
<span data-ttu-id="a7405-122">Pobiera informacje o rurociągach w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-122">Gets information about pipelines in Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-123">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="a7405-123">Get-AzDataFactoryRun</span></span>](Get-AzDataFactoryRun.md)
<span data-ttu-id="a7405-124">Powoduje uruchomienie wycinka danych zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-124">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-125">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="a7405-125">Get-AzDataFactorySlice</span></span>](Get-AzDataFactorySlice.md)
<span data-ttu-id="a7405-126">Pobiera wycinków danych dla zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-126">Gets data slices for a dataset in Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-127">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7405-127">Get-AzDataFactoryV2</span></span>](Get-AzDataFactoryV2.md)
<span data-ttu-id="a7405-128">Pobiera informacje o fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-128">Gets information about Data Factory.</span></span>

### [<span data-ttu-id="a7405-129">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="a7405-129">Get-AzDataFactoryV2ActivityRun</span></span>](Get-AzDataFactoryV2ActivityRun.md)
<span data-ttu-id="a7405-130">Pobiera informacje o działaniach dotyczących uruchamiania rurociągu.</span><span class="sxs-lookup"><span data-stu-id="a7405-130">Gets information about activity runs for a pipeline run.</span></span>

### [<span data-ttu-id="a7405-131">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="a7405-131">Get-AzDataFactoryV2Dataset</span></span>](Get-AzDataFactoryV2Dataset.md)
<span data-ttu-id="a7405-132">Pobiera informacje o zestawach danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-132">Gets information about datasets in Data Factory.</span></span>

### [<span data-ttu-id="a7405-133">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a7405-133">Get-AzDataFactoryV2IntegrationRuntime</span></span>](Get-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="a7405-134">Pobiera informacje o zasobach w czasie wykonywania integracji.</span><span class="sxs-lookup"><span data-stu-id="a7405-134">Gets information about integration runtime resources.</span></span>

### [<span data-ttu-id="a7405-135">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="a7405-135">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>](Get-AzDataFactoryV2IntegrationRuntimeKey.md)
<span data-ttu-id="a7405-136">Pobiera klucze dla środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="a7405-136">Gets keys for a self-hosted integration runtime.</span></span>

### [<span data-ttu-id="a7405-137">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="a7405-137">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>](Get-AzDataFactoryV2IntegrationRuntimeMetric.md)
<span data-ttu-id="a7405-138">Pobiera dane metryczne dla środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="a7405-138">Gets metric data for an integration runtime.</span></span> 

### [<span data-ttu-id="a7405-139">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a7405-139">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>](Get-AzDataFactoryV2IntegrationRuntimeNode.md)
<span data-ttu-id="a7405-140">Pobiera informacje o węźle środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="a7405-140">Gets an integration runtime node information.</span></span>

### [<span data-ttu-id="a7405-141">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a7405-141">Get-AzDataFactoryV2LinkedService</span></span>](Get-AzDataFactoryV2LinkedService.md)
<span data-ttu-id="a7405-142">Pobiera informacje o usługach połączonych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-142">Gets information about linked services in Data Factory.</span></span>

### [<span data-ttu-id="a7405-143">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a7405-143">Get-AzDataFactoryV2Pipeline</span></span>](Get-AzDataFactoryV2Pipeline.md)
<span data-ttu-id="a7405-144">Pobiera informacje o rurociągach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-144">Gets information about pipelines in Data Factory.</span></span>

### [<span data-ttu-id="a7405-145">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="a7405-145">Get-AzDataFactoryV2PipelineRun</span></span>](Get-AzDataFactoryV2PipelineRun.md)
<span data-ttu-id="a7405-146">Pobiera informacje o przebiegach potokowych.</span><span class="sxs-lookup"><span data-stu-id="a7405-146">Gets information about pipeline runs.</span></span>

### [<span data-ttu-id="a7405-147">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a7405-147">Get-AzDataFactoryV2Trigger</span></span>](Get-AzDataFactoryV2Trigger.md)
<span data-ttu-id="a7405-148">Pobiera informacje o wyzwalaczach w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-148">Gets information about triggers in a data factory.</span></span>

### [<span data-ttu-id="a7405-149">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="a7405-149">Get-AzDataFactoryV2TriggerRun</span></span>](Get-AzDataFactoryV2TriggerRun.md)
<span data-ttu-id="a7405-150">Zwraca informacje o uruchomionych wyzwalaczach.</span><span class="sxs-lookup"><span data-stu-id="a7405-150">Returns information about trigger runs.</span></span>

### [<span data-ttu-id="a7405-151">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="a7405-151">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>](Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md)
<span data-ttu-id="a7405-152">Uaktualnia środowisko uruchomieniowe integracji na samym własnym poziomie.</span><span class="sxs-lookup"><span data-stu-id="a7405-152">Upgrades self-hosted integration runtime.</span></span>

### [<span data-ttu-id="a7405-153">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a7405-153">Invoke-AzDataFactoryV2Pipeline</span></span>](Invoke-AzDataFactoryV2Pipeline.md)
  <span data-ttu-id="a7405-154">Wywołuje potok w celu uruchomienia go.</span><span class="sxs-lookup"><span data-stu-id="a7405-154">Invokes a pipeline to start a run for it.</span></span>

### [<span data-ttu-id="a7405-155">Nowe — AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a7405-155">New-AzDataFactory</span></span>](New-AzDataFactory.md)
<span data-ttu-id="a7405-156">Tworzy fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-156">Creates a data factory.</span></span>

### [<span data-ttu-id="a7405-157">Nowe — AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="a7405-157">New-AzDataFactoryDataset</span></span>](New-AzDataFactoryDataset.md)
<span data-ttu-id="a7405-158">Tworzy zestaw danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-158">Creates a dataset in Data Factory.</span></span>

### [<span data-ttu-id="a7405-159">Nowe — AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="a7405-159">New-AzDataFactoryEncryptValue</span></span>](New-AzDataFactoryEncryptValue.md)
<span data-ttu-id="a7405-160">Szyfruje dane poufne.</span><span class="sxs-lookup"><span data-stu-id="a7405-160">Encrypts sensitive data.</span></span>

### [<span data-ttu-id="a7405-161">Nowe — AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a7405-161">New-AzDataFactoryGateway</span></span>](New-AzDataFactoryGateway.md)
<span data-ttu-id="a7405-162">Tworzy bramę dla fabryki danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7405-162">Creates a gateway for an Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-163">Nowe — AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="a7405-163">New-AzDataFactoryGatewayAuthKey</span></span>](New-AzDataFactoryGatewayAuthKey.md)
<span data-ttu-id="a7405-164">Tworzy klucz uwierzytelniania dla bramy usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-164">Creates auth key for an Azure Data Factory Gateway.</span></span>

### [<span data-ttu-id="a7405-165">Nowe — AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="a7405-165">New-AzDataFactoryHub</span></span>](New-AzDataFactoryHub.md)
<span data-ttu-id="a7405-166">Tworzy centrum dla fabryki danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7405-166">Creates a hub for an Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-167">Nowe — AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="a7405-167">New-AzDataFactoryLinkedService</span></span>](New-AzDataFactoryLinkedService.md)
<span data-ttu-id="a7405-168">Łączy magazyn danych lub usługę w chmurze z fabryką danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a7405-168">Links a data store or a cloud service to an Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-169">Nowe — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a7405-169">New-AzDataFactoryPipeline</span></span>](New-AzDataFactoryPipeline.md)
<span data-ttu-id="a7405-170">Tworzy potok w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-170">Creates a pipeline in Data Factory.</span></span>

### [<span data-ttu-id="a7405-171">Nowe — AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="a7405-171">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>](New-AzDataFactoryV2IntegrationRuntimeKey.md)
<span data-ttu-id="a7405-172">Ponowne generowanie klucza środowiska uruchomieniowego w ramach samodzielnej integracji.</span><span class="sxs-lookup"><span data-stu-id="a7405-172">Regenerate self-hosted integration runtime key.</span></span>

### [<span data-ttu-id="a7405-173">Nowe — AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="a7405-173">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>](New-AzDataFactoryV2LinkedServiceEncryptedCredential.md)
<span data-ttu-id="a7405-174">Szyfruj poświadczenia w połączonej usłudze za pomocą określonego środowiska obsługi integracji.</span><span class="sxs-lookup"><span data-stu-id="a7405-174">Encrypt credential in linked service with specified integration runtime.</span></span>

### [<span data-ttu-id="a7405-175">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a7405-175">Remove-AzDataFactory</span></span>](Remove-AzDataFactory.md)
<span data-ttu-id="a7405-176">Usuwa fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-176">Removes a data factory.</span></span>

### [<span data-ttu-id="a7405-177">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="a7405-177">Remove-AzDataFactoryDataset</span></span>](Remove-AzDataFactoryDataset.md)
<span data-ttu-id="a7405-178">Usuwa zestaw danych z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-178">Removes a dataset from Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-179">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a7405-179">Remove-AzDataFactoryGateway</span></span>](Remove-AzDataFactoryGateway.md)
<span data-ttu-id="a7405-180">Usuwa bramę z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-180">Removes a gateway from Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-181">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="a7405-181">Remove-AzDataFactoryHub</span></span>](Remove-AzDataFactoryHub.md)
<span data-ttu-id="a7405-182">Usuwa centrum z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-182">Removes a hub from Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-183">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="a7405-183">Remove-AzDataFactoryLinkedService</span></span>](Remove-AzDataFactoryLinkedService.md)
<span data-ttu-id="a7405-184">Usuwa połączoną usługę z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-184">Removes a linked service from Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-185">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a7405-185">Remove-AzDataFactoryPipeline</span></span>](Remove-AzDataFactoryPipeline.md)
<span data-ttu-id="a7405-186">Usuwa potok z usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-186">Removes a pipeline from Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-187">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7405-187">Remove-AzDataFactoryV2</span></span>](Remove-AzDataFactoryV2.md)
<span data-ttu-id="a7405-188">Usuwa fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-188">Removes a data factory.</span></span>

### [<span data-ttu-id="a7405-189">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="a7405-189">Remove-AzDataFactoryV2Dataset</span></span>](Remove-AzDataFactoryV2Dataset.md)
<span data-ttu-id="a7405-190">Umożliwia usunięcie zestawu danych z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-190">Removes a dataset from Data Factory.</span></span>

### [<span data-ttu-id="a7405-191">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a7405-191">Remove-AzDataFactoryV2IntegrationRuntime</span></span>](Remove-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="a7405-192">Usuwa środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="a7405-192">Removes an integration runtime.</span></span>

### [<span data-ttu-id="a7405-193">Remove-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a7405-193">Remove-AzDataFactoryV2IntegrationRuntimeNode</span></span>](Remove-AzDataFactoryV2IntegrationRuntimeNode.md)
<span data-ttu-id="a7405-194">Usuwanie węzła o podanej nazwie w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="a7405-194">Remove a node with the given name on an integration runtime.</span></span>

### [<span data-ttu-id="a7405-195">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a7405-195">Remove-AzDataFactoryV2LinkedService</span></span>](Remove-AzDataFactoryV2LinkedService.md)
<span data-ttu-id="a7405-196">Usuwa połączoną usługę z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-196">Removes a linked service from Data Factory.</span></span>

### [<span data-ttu-id="a7405-197">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a7405-197">Remove-AzDataFactoryV2Pipeline</span></span>](Remove-AzDataFactoryV2Pipeline.md)
<span data-ttu-id="a7405-198">Usuwa potok z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-198">Removes a pipeline from Data Factory.</span></span>

### [<span data-ttu-id="a7405-199">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a7405-199">Remove-AzDataFactoryV2Trigger</span></span>](Remove-AzDataFactoryV2Trigger.md)
<span data-ttu-id="a7405-200">Usuwa wyzwalacz z fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-200">Removes a trigger from a data factory.</span></span>

### [<span data-ttu-id="a7405-201">Życiorys — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a7405-201">Resume-AzDataFactoryPipeline</span></span>](Resume-AzDataFactoryPipeline.md)
<span data-ttu-id="a7405-202">Wznawia zawieszoną rurociąg w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-202">Resumes a suspended pipeline in Data Factory.</span></span>

### [<span data-ttu-id="a7405-203">Zapisz — AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="a7405-203">Save-AzDataFactoryLog</span></span>](Save-AzDataFactoryLog.md)
<span data-ttu-id="a7405-204">Pobiera pliki dziennika z przetwarzania usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a7405-204">Downloads log files from Azure HDInsight processing.</span></span>

### [<span data-ttu-id="a7405-205">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a7405-205">Set-AzDataFactoryGateway</span></span>](Set-AzDataFactoryGateway.md)
<span data-ttu-id="a7405-206">Ustawia opis bramy w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-206">Sets the description for a gateway in Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-207">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="a7405-207">Set-AzDataFactoryPipelineActivePeriod</span></span>](Set-AzDataFactoryPipelineActivePeriod.md)
<span data-ttu-id="a7405-208">Umożliwia skonfigurowanie aktywnego okresu wycinków danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-208">Configures the active period for data slices.</span></span>

### [<span data-ttu-id="a7405-209">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="a7405-209">Set-AzDataFactorySliceStatus</span></span>](Set-AzDataFactorySliceStatus.md)
<span data-ttu-id="a7405-210">Ustawia stan wycinków dla zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-210">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-211">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7405-211">Set-AzDataFactoryV2</span></span>](Set-AzDataFactoryV2.md)
<span data-ttu-id="a7405-212">Tworzy fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-212">Creates a data factory.</span></span>

### [<span data-ttu-id="a7405-213">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="a7405-213">Set-AzDataFactoryV2Dataset</span></span>](Set-AzDataFactoryV2Dataset.md)
<span data-ttu-id="a7405-214">Tworzy zestaw danych w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-214">Creates a dataset in Data Factory.</span></span>

### [<span data-ttu-id="a7405-215">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a7405-215">Set-AzDataFactoryV2IntegrationRuntime</span></span>](Set-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="a7405-216">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="a7405-216">Updates an integration runtime.</span></span>

### [<span data-ttu-id="a7405-217">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="a7405-217">Set-AzDataFactoryV2LinkedService</span></span>](Set-AzDataFactoryV2LinkedService.md)
<span data-ttu-id="a7405-218">Łączy magazyn danych lub usługę w chmurze z fabryką danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-218">Links a data store or a cloud service to Data Factory.</span></span>

### [<span data-ttu-id="a7405-219">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a7405-219">Set-AzDataFactoryV2Pipeline</span></span>](Set-AzDataFactoryV2Pipeline.md)
<span data-ttu-id="a7405-220">Tworzy potok w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-220">Creates a pipeline in Data Factory.</span></span>

### [<span data-ttu-id="a7405-221">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a7405-221">Set-AzDataFactoryV2Trigger</span></span>](Set-AzDataFactoryV2Trigger.md)
<span data-ttu-id="a7405-222">Tworzy wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-222">Creates a trigger in a data factory.</span></span>

### [<span data-ttu-id="a7405-223">Start — AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a7405-223">Start-AzDataFactoryV2IntegrationRuntime</span></span>](Start-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="a7405-224">Rozpoczyna zarządzany dedykowany środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="a7405-224">Starts a managed dedicated integration runtime.</span></span>

### [<span data-ttu-id="a7405-225">Start — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a7405-225">Start-AzDataFactoryV2Trigger</span></span>](Start-AzDataFactoryV2Trigger.md)
<span data-ttu-id="a7405-226">Uruchamia wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-226">Starts a trigger in a data factory.</span></span>

### [<span data-ttu-id="a7405-227">Zatrzymaj — AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a7405-227">Stop-AzDataFactoryV2IntegrationRuntime</span></span>](Stop-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="a7405-228">Zatrzymuje zarządzane dedykowane środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="a7405-228">Stops a managed dedicated integration runtime.</span></span>

### [<span data-ttu-id="a7405-229">Zatrzymaj — AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="a7405-229">Stop-AzDataFactoryV2PipelineRun</span></span>](Stop-AzDataFactoryV2PipelineRun.md)
<span data-ttu-id="a7405-230">Zatrzymuje działanie rurociągu w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-230">Stops a pipeline run in a data factory.</span></span>

### [<span data-ttu-id="a7405-231">Zatrzymaj — AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a7405-231">Stop-AzDataFactoryV2Trigger</span></span>](Stop-AzDataFactoryV2Trigger.md)
<span data-ttu-id="a7405-232">Zatrzymuje wyzwalacz w fabryce danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-232">Stops a trigger in a data factory.</span></span>

### [<span data-ttu-id="a7405-233">Suspend — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="a7405-233">Suspend-AzDataFactoryPipeline</span></span>](Suspend-AzDataFactoryPipeline.md)
<span data-ttu-id="a7405-234">Wstrzymuje rurociąg w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a7405-234">Suspends a pipeline in Azure Data Factory.</span></span>

### [<span data-ttu-id="a7405-235">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="a7405-235">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>](Sync-AzDataFactoryV2IntegrationRuntimeCredential.md)
<span data-ttu-id="a7405-236">Synchronizuje poświadczenia między węzłami w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="a7405-236">Synchronizes credentials among integration runtime nodes.</span></span>

### [<span data-ttu-id="a7405-237">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a7405-237">Update-AzDataFactoryV2</span></span>](Update-AzDataFactoryV2.md)
<span data-ttu-id="a7405-238">Aktualizuje właściwości fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="a7405-238">Updates the properties of a data factory.</span></span>

### [<span data-ttu-id="a7405-239">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a7405-239">Update-AzDataFactoryV2IntegrationRuntime</span></span>](Update-AzDataFactoryV2IntegrationRuntime.md)
<span data-ttu-id="a7405-240">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="a7405-240">Updates an integration runtime.</span></span>

### [<span data-ttu-id="a7405-241">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a7405-241">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>](Update-AzDataFactoryV2IntegrationRuntimeNode.md)
<span data-ttu-id="a7405-242">Umożliwia zaktualizowanie węzła środowiska uruchomieniowego integracji na samym własnym poziomie.</span><span class="sxs-lookup"><span data-stu-id="a7405-242">Updates self-hosted integration runtime node.</span></span>

