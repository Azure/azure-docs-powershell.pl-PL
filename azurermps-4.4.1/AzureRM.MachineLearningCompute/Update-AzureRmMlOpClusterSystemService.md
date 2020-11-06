---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: fc89ff40c36fc444eec23089288849aa5ffe592c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553838"
---
# <span data-ttu-id="232ee-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="232ee-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="232ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="232ee-102">SYNOPSIS</span></span>
<span data-ttu-id="232ee-103">Rozpoczyna aktualizację usług systemowych klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="232ee-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="232ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="232ee-104">SYNTAX</span></span>

### <span data-ttu-id="232ee-105">Uruchom aktualizację usług systemowych z parametrów wejściowych polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="232ee-105">Start a system services update from cmdlet input parameters.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="232ee-106">Uruchom aktualizację usług systemowych z definicji wystąpienia PSOperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="232ee-106">Start a system services update from an PSOperationalizationCluster instance definition.</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="232ee-107">Uruchom aktualizację usług systemowych na podstawie identyfikatora usługi Azure Resouce.</span><span class="sxs-lookup"><span data-stu-id="232ee-107">Start a system services update from an Azure resouce id.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="232ee-108">Opis</span><span class="sxs-lookup"><span data-stu-id="232ee-108">DESCRIPTION</span></span>
<span data-ttu-id="232ee-109">Usługi systemowe można aktualizować niezależnie od klastra programu operationalization.</span><span class="sxs-lookup"><span data-stu-id="232ee-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="232ee-110">Aby rozpocząć aktualizację usług systemowych, użyj tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="232ee-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="232ee-111">Jeśli żadna aktualizacja nie jest dostępna, aktualizacja będzie nadal uruchamiana i zostanie pomyślnie przywrócona.</span><span class="sxs-lookup"><span data-stu-id="232ee-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="232ee-112">Po zakończeniu aktualizacji raporty są zgłaszane po jej uruchomieniu, zakończeniu i po poprawnym utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="232ee-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="232ee-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="232ee-113">EXAMPLES</span></span>

### <span data-ttu-id="232ee-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="232ee-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="232ee-115">Rozpoczyna aktualizację usług systemowych w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="232ee-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="232ee-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="232ee-116">PARAMETERS</span></span>

### <span data-ttu-id="232ee-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="232ee-117">-InputObject</span></span>
<span data-ttu-id="232ee-118">Obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="232ee-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Start a system services update from an PSOperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="232ee-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="232ee-119">-Confirm</span></span>
<span data-ttu-id="232ee-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="232ee-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="232ee-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="232ee-121">-Name</span></span>
<span data-ttu-id="232ee-122">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="232ee-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232ee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="232ee-123">-ResourceGroupName</span></span>
<span data-ttu-id="232ee-124">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="232ee-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232ee-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="232ee-125">-ResourceId</span></span>
<span data-ttu-id="232ee-126">Identyfikator zasobu platformy Azure dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="232ee-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232ee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="232ee-127">-WhatIf</span></span>
<span data-ttu-id="232ee-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="232ee-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="232ee-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="232ee-129">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="232ee-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="232ee-130">INPUTS</span></span>

### <span data-ttu-id="232ee-131">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="232ee-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="232ee-132">System. String</span><span class="sxs-lookup"><span data-stu-id="232ee-132">System.String</span></span>


## <span data-ttu-id="232ee-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="232ee-133">OUTPUTS</span></span>

### <span data-ttu-id="232ee-134">Microsoft. Azure. Commands. MachineLearningCompute. models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="232ee-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>


## <span data-ttu-id="232ee-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="232ee-135">NOTES</span></span>

## <span data-ttu-id="232ee-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="232ee-136">RELATED LINKS</span></span>

