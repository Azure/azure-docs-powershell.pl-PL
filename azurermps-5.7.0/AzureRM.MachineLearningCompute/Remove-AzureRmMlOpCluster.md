---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/remove-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 9836856ffd663939de8ca0e28635d81785c9c898
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/21/2020
ms.locfileid: "93719678"
---
# <span data-ttu-id="41097-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="41097-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="41097-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41097-102">SYNOPSIS</span></span>
<span data-ttu-id="41097-103">Usuwa klaster operationalization.</span><span class="sxs-lookup"><span data-stu-id="41097-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41097-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41097-104">SYNTAX</span></span>

### <span data-ttu-id="41097-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="41097-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41097-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="41097-106">RemoveByInputObject</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41097-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="41097-107">RemoveByResourceId</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeAllResources] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41097-108">Opis</span><span class="sxs-lookup"><span data-stu-id="41097-108">DESCRIPTION</span></span>
<span data-ttu-id="41097-109">Usuwa klaster operationalization.</span><span class="sxs-lookup"><span data-stu-id="41097-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="41097-110">Niektóre zasoby skojarzone z klastrem mogą nie być usuwane.</span><span class="sxs-lookup"><span data-stu-id="41097-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="41097-111">Na przykład usługa kontenera platformy Azure zostanie usunięta, ale skojarzone z nią maszyny wirtualne nie zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="41097-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="41097-112">Konta magazynu, rejestru kontenera i usługi Application Insights nie są usuwane w celu uzyskania informacji diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="41097-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="41097-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41097-113">EXAMPLES</span></span>

### <span data-ttu-id="41097-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="41097-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="41097-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="41097-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster
```

## <span data-ttu-id="41097-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41097-116">PARAMETERS</span></span>

### <span data-ttu-id="41097-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41097-117">-DefaultProfile</span></span>
<span data-ttu-id="41097-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41097-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41097-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="41097-119">-IncludeAllResources</span></span>
<span data-ttu-id="41097-120">Usuwa wszystkie zasoby, które zostały utworzone w klastrze.</span><span class="sxs-lookup"><span data-stu-id="41097-120">Removes all resources that were created with the cluster.</span></span>

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

### <span data-ttu-id="41097-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="41097-121">-InputObject</span></span>
<span data-ttu-id="41097-122">Obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="41097-122">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41097-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41097-123">-Name</span></span>
<span data-ttu-id="41097-124">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="41097-124">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41097-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41097-125">-ResourceGroupName</span></span>
<span data-ttu-id="41097-126">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="41097-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41097-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41097-127">-ResourceId</span></span>
<span data-ttu-id="41097-128">Identyfikator zasobu platformy Azure dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="41097-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41097-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41097-129">-Confirm</span></span>
<span data-ttu-id="41097-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41097-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41097-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41097-131">-WhatIf</span></span>
<span data-ttu-id="41097-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41097-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41097-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41097-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41097-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41097-134">CommonParameters</span></span>
<span data-ttu-id="41097-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41097-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41097-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41097-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41097-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41097-137">INPUTS</span></span>

### <span data-ttu-id="41097-138">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="41097-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="41097-139">System. String</span><span class="sxs-lookup"><span data-stu-id="41097-139">System.String</span></span>

## <span data-ttu-id="41097-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41097-140">OUTPUTS</span></span>

### <span data-ttu-id="41097-141">System. void</span><span class="sxs-lookup"><span data-stu-id="41097-141">System.Void</span></span>

## <span data-ttu-id="41097-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41097-142">NOTES</span></span>

## <span data-ttu-id="41097-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41097-143">RELATED LINKS</span></span>

