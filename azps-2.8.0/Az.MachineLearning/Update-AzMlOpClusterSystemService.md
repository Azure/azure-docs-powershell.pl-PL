---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
ms.openlocfilehash: 0e673cd74d87cee990130c1fd58b9049eec9ff15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704917"
---
# <span data-ttu-id="9daf9-101">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="9daf9-101">Update-AzMlOpClusterSystemService</span></span>

## <span data-ttu-id="9daf9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9daf9-102">SYNOPSIS</span></span>
<span data-ttu-id="9daf9-103">Rozpoczyna aktualizację usług systemowych klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="9daf9-103">Starts an update on the operationalization cluster's system services.</span></span>

## <span data-ttu-id="9daf9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9daf9-104">SYNTAX</span></span>

### <span data-ttu-id="9daf9-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9daf9-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9daf9-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="9daf9-106">StartUpdateWithInputObject</span></span>
```
Update-AzMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9daf9-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="9daf9-107">StartUpdateWithResourceId</span></span>
```
Update-AzMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9daf9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9daf9-108">DESCRIPTION</span></span>
<span data-ttu-id="9daf9-109">Usługi systemowe można aktualizować niezależnie od klastra programu operationalization.</span><span class="sxs-lookup"><span data-stu-id="9daf9-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="9daf9-110">Aby rozpocząć aktualizację usług systemowych, użyj tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9daf9-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="9daf9-111">Jeśli żadna aktualizacja nie jest dostępna, aktualizacja będzie nadal uruchamiana i zostanie pomyślnie przywrócona.</span><span class="sxs-lookup"><span data-stu-id="9daf9-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="9daf9-112">Po zakończeniu aktualizacji raporty są zgłaszane po jej uruchomieniu, zakończeniu i po poprawnym utworzeniu.</span><span class="sxs-lookup"><span data-stu-id="9daf9-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="9daf9-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9daf9-113">EXAMPLES</span></span>

### <span data-ttu-id="9daf9-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9daf9-114">Example 1</span></span>
```
PS C:\> Update-AzMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="9daf9-115">Rozpoczyna aktualizację usług systemowych w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="9daf9-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="9daf9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9daf9-116">PARAMETERS</span></span>

### <span data-ttu-id="9daf9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9daf9-117">-DefaultProfile</span></span>
<span data-ttu-id="9daf9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9daf9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9daf9-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9daf9-119">-InputObject</span></span>
<span data-ttu-id="9daf9-120">Obiekt klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="9daf9-120">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9daf9-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9daf9-121">-Name</span></span>
<span data-ttu-id="9daf9-122">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="9daf9-122">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9daf9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9daf9-123">-ResourceGroupName</span></span>
<span data-ttu-id="9daf9-124">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="9daf9-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9daf9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9daf9-125">-ResourceId</span></span>
<span data-ttu-id="9daf9-126">Identyfikator zasobu platformy Azure dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="9daf9-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9daf9-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9daf9-127">-Confirm</span></span>
<span data-ttu-id="9daf9-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9daf9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9daf9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9daf9-129">-WhatIf</span></span>
<span data-ttu-id="9daf9-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9daf9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9daf9-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9daf9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9daf9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9daf9-132">CommonParameters</span></span>
<span data-ttu-id="9daf9-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9daf9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9daf9-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9daf9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9daf9-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9daf9-135">INPUTS</span></span>

### <span data-ttu-id="9daf9-136">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="9daf9-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="9daf9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9daf9-137">System.String</span></span>

## <span data-ttu-id="9daf9-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9daf9-138">OUTPUTS</span></span>

### <span data-ttu-id="9daf9-139">Microsoft. Azure. Commands. MachineLearningCompute. models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="9daf9-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="9daf9-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9daf9-140">NOTES</span></span>

## <span data-ttu-id="9daf9-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9daf9-141">RELATED LINKS</span></span>
