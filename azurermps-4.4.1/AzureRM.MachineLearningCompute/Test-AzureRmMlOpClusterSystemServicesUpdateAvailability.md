---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 067fdf88b7a7b29007f81ab26590ffaa542ac7e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717830"
---
# <span data-ttu-id="9de3d-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="9de3d-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="9de3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9de3d-102">SYNOPSIS</span></span>
<span data-ttu-id="9de3d-103">Sprawdza, czy są dostępne aktualizacje dla usług systemowych skojarzonych z klastrem usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="9de3d-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9de3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9de3d-104">SYNTAX</span></span>

### <span data-ttu-id="9de3d-105">Przetestuj dostępność aktualizacji za pomocą parametrów wejściowych polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9de3d-105">Test for update availability from cmdlet input parameters.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="9de3d-106">Test dostępności aktualizacji z definicji wystąpienia OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="9de3d-106">Test for update availability from an OperationalizationCluster instance definition.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
```

### <span data-ttu-id="9de3d-107">Przetestuj dostępność aktualizacji na podstawie identyfikatora usługi Azure Resouce.</span><span class="sxs-lookup"><span data-stu-id="9de3d-107">Test for update availability from an Azure resouce id.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
```

## <span data-ttu-id="9de3d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9de3d-108">DESCRIPTION</span></span>
<span data-ttu-id="9de3d-109">Usługi systemowe odbierają aktualizacje niezależnie od klastra programu operationalization.</span><span class="sxs-lookup"><span data-stu-id="9de3d-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="9de3d-110">Użycie tego polecenia cmdlet umożliwi użytkownikowi zapoznanie się z informacją, czy funkcja Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span><span class="sxs-lookup"><span data-stu-id="9de3d-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="9de3d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9de3d-111">EXAMPLES</span></span>

### <span data-ttu-id="9de3d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9de3d-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="9de3d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9de3d-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="9de3d-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9de3d-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="9de3d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9de3d-115">PARAMETERS</span></span>

### <span data-ttu-id="9de3d-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9de3d-116">-InputObject</span></span>
<span data-ttu-id="9de3d-117">Obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="9de3d-117">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Test for update availability from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9de3d-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9de3d-118">-Name</span></span>
<span data-ttu-id="9de3d-119">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="9de3d-119">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9de3d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de3d-120">-ResourceGroupName</span></span>
<span data-ttu-id="9de3d-121">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="9de3d-121">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9de3d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9de3d-122">-ResourceId</span></span>
<span data-ttu-id="9de3d-123">Identyfikator zasobu platformy Azure dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="9de3d-123">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="9de3d-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9de3d-124">INPUTS</span></span>

### <span data-ttu-id="9de3d-125">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="9de3d-125">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="9de3d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9de3d-126">System.String</span></span>


## <span data-ttu-id="9de3d-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9de3d-127">OUTPUTS</span></span>

### <span data-ttu-id="9de3d-128">Microsoft. Azure. Commands. MachineLearningCompute. models. PSCheckSystemServicesUpdatesAvailableResponse</span><span class="sxs-lookup"><span data-stu-id="9de3d-128">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>


## <span data-ttu-id="9de3d-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9de3d-129">NOTES</span></span>

## <span data-ttu-id="9de3d-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9de3d-130">RELATED LINKS</span></span>

