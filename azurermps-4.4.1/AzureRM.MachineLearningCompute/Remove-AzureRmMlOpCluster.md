---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 63e401c09a2d224b53d260855990198a409d4846
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717577"
---
# <span data-ttu-id="2c535-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2c535-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="2c535-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c535-102">SYNOPSIS</span></span>
<span data-ttu-id="2c535-103">Usuwa klaster operationalization.</span><span class="sxs-lookup"><span data-stu-id="2c535-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c535-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c535-104">SYNTAX</span></span>

### <span data-ttu-id="2c535-105">Usuń klaster operationalization z parametrów wejściowych polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c535-105">Remove an operationalization cluster from cmdlet input parameters.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2c535-106">Usuwanie klastra operationalization z definicji wystąpienia OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="2c535-106">Remove an operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2c535-107">Usuń klaster operationalization z usługi Azure Resouce ID.</span><span class="sxs-lookup"><span data-stu-id="2c535-107">Remove an operationalization cluster from an Azure resouce id.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="2c535-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2c535-108">DESCRIPTION</span></span>
<span data-ttu-id="2c535-109">Usuwa klaster operationalization.</span><span class="sxs-lookup"><span data-stu-id="2c535-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="2c535-110">Niektóre zasoby skojarzone z klastrem mogą nie być usuwane.</span><span class="sxs-lookup"><span data-stu-id="2c535-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="2c535-111">Na przykład usługa kontenera platformy Azure zostanie usunięta, ale skojarzone z nią maszyny wirtualne nie zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="2c535-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="2c535-112">Konta magazynu, rejestru kontenera i usługi Application Insights nie są usuwane w celu uzyskania informacji diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="2c535-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="2c535-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c535-113">EXAMPLES</span></span>

### <span data-ttu-id="2c535-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2c535-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="2c535-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2c535-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster 
```

## <span data-ttu-id="2c535-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c535-116">PARAMETERS</span></span>

### <span data-ttu-id="2c535-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2c535-117">-InputObject</span></span>
<span data-ttu-id="2c535-118">Obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="2c535-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Remove an operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c535-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c535-119">-Confirm</span></span>
<span data-ttu-id="2c535-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c535-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c535-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c535-121">-Name</span></span>
<span data-ttu-id="2c535-122">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="2c535-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c535-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c535-123">-ResourceGroupName</span></span>
<span data-ttu-id="2c535-124">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="2c535-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c535-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c535-125">-ResourceId</span></span>
<span data-ttu-id="2c535-126">Identyfikator zasobu platformy Azure dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="2c535-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c535-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c535-127">-WhatIf</span></span>
<span data-ttu-id="2c535-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c535-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c535-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2c535-129">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="2c535-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c535-130">INPUTS</span></span>

### <span data-ttu-id="2c535-131">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="2c535-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="2c535-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2c535-132">System.String</span></span>


## <span data-ttu-id="2c535-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c535-133">OUTPUTS</span></span>

### <span data-ttu-id="2c535-134">System. void</span><span class="sxs-lookup"><span data-stu-id="2c535-134">System.Void</span></span>


## <span data-ttu-id="2c535-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c535-135">NOTES</span></span>

## <span data-ttu-id="2c535-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c535-136">RELATED LINKS</span></span>

