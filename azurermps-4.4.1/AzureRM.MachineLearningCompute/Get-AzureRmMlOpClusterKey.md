---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550931"
---
# <span data-ttu-id="d0fa8-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="d0fa8-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="d0fa8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="d0fa8-103">Pobiera klucze dostępu skojarzone z klastrem usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="d0fa8-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0fa8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0fa8-104">SYNTAX</span></span>

### <span data-ttu-id="d0fa8-105">Pobierz klucze klastra operationalization z parametrów wejściowych polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0fa8-105">Get operationalization cluster's keys from cmdlet input parameters.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="d0fa8-106">Pobierz klucze klastra operationalization z definicji wystąpienia OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="d0fa8-106">Get operationalization cluster's keys from an OperationalizationCluster instance definition.</span></span>
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### <span data-ttu-id="d0fa8-107">Pobierz klucze klastra operationalization z identyfikatora zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0fa8-107">Get operationalization cluster's keys from an Azure resource id.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## <span data-ttu-id="d0fa8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d0fa8-108">DESCRIPTION</span></span>
<span data-ttu-id="d0fa8-109">Klucze dla konta magazynu, rejestru kontenera i innych usług skojarzonych z klastrem operationalization nie są zwracane podczas uzyskiwania właściwości klastra.</span><span class="sxs-lookup"><span data-stu-id="d0fa8-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="d0fa8-110">Należy wprowadzić określone połączenie, aby pobrać klucze, ponieważ są to informacje poufne.</span><span class="sxs-lookup"><span data-stu-id="d0fa8-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="d0fa8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0fa8-111">EXAMPLES</span></span>

### <span data-ttu-id="d0fa8-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d0fa8-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="d0fa8-113">Zwraca klucze tajne dla usług skojarzonych z klastrem operationalization.</span><span class="sxs-lookup"><span data-stu-id="d0fa8-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="d0fa8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0fa8-114">PARAMETERS</span></span>

### <span data-ttu-id="d0fa8-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d0fa8-115">-InputObject</span></span>
<span data-ttu-id="d0fa8-116">Obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="d0fa8-116">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0fa8-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0fa8-117">-Name</span></span>
<span data-ttu-id="d0fa8-118">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="d0fa8-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0fa8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0fa8-119">-ResourceGroupName</span></span>
<span data-ttu-id="d0fa8-120">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="d0fa8-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0fa8-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0fa8-121">-ResourceId</span></span>
<span data-ttu-id="d0fa8-122">Identyfikator zasobu platformy Azure dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="d0fa8-122">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="d0fa8-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0fa8-123">INPUTS</span></span>

### <span data-ttu-id="d0fa8-124">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="d0fa8-124">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="d0fa8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d0fa8-125">System.String</span></span>


## <span data-ttu-id="d0fa8-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0fa8-126">OUTPUTS</span></span>

### <span data-ttu-id="d0fa8-127">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationClusterCredentials</span><span class="sxs-lookup"><span data-stu-id="d0fa8-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>


## <span data-ttu-id="d0fa8-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0fa8-128">NOTES</span></span>

## <span data-ttu-id="d0fa8-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0fa8-129">RELATED LINKS</span></span>

