---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183426"
---
# <span data-ttu-id="37baf-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="37baf-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="37baf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37baf-102">SYNOPSIS</span></span>
<span data-ttu-id="37baf-103">Ponowne uruchamianie określonych węzłów z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="37baf-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="37baf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="37baf-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37baf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="37baf-105">DESCRIPTION</span></span>
<span data-ttu-id="37baf-106">Ponowne uruchamianie określonych węzłów z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="37baf-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="37baf-107">Węzły szkieletów usług zostaną wyłączone przed ponownym uruchomieniem maszyny wirtualnej i ponownie włączono je po powrocie.</span><span class="sxs-lookup"><span data-stu-id="37baf-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="37baf-108">Jeśli to zrobisz w przypadku typów węzła podstawowego, może to zająć trochę czasu, ponieważ może to nie spowodować ponownego uruchomienia wszystkich węzłów jednocześnie.</span><span class="sxs-lookup"><span data-stu-id="37baf-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="37baf-109">Użycie funkcji -ForceRestart wymusza operację, nawet jeśli sieć szkielet usług nie może wyłączyć węzłów, ale używaj z zachowaniem ostrożności, ponieważ może to spowodować utratę danych, jeśli w węźle są uruchomione obciążenia pracą o stanach.</span><span class="sxs-lookup"><span data-stu-id="37baf-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="37baf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="37baf-110">EXAMPLES</span></span>

### <span data-ttu-id="37baf-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37baf-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="37baf-112">Uruchom ponownie węzeł 0 i 3 w typie węzła.</span><span class="sxs-lookup"><span data-stu-id="37baf-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="37baf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37baf-113">PARAMETERS</span></span>

### <span data-ttu-id="37baf-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="37baf-114">-AsJob</span></span>
<span data-ttu-id="37baf-115">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="37baf-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="37baf-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="37baf-116">-ClusterName</span></span>
<span data-ttu-id="37baf-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="37baf-117">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37baf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37baf-118">-DefaultProfile</span></span>
<span data-ttu-id="37baf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="37baf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37baf-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="37baf-120">-ForceRestart</span></span>
<span data-ttu-id="37baf-121">Użycie tej flagi wymusi ponowne uruchomienie węzła, nawet jeśli sieć szkieletowa usługi nie może wyłączyć węzłów.</span><span class="sxs-lookup"><span data-stu-id="37baf-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="37baf-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="37baf-122">-Name</span></span>
<span data-ttu-id="37baf-123">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="37baf-123">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37baf-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="37baf-124">-NodeName</span></span>
<span data-ttu-id="37baf-125">Lista nazw węzła dla operacji.</span><span class="sxs-lookup"><span data-stu-id="37baf-125">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37baf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37baf-126">-PassThru</span></span>
<span data-ttu-id="37baf-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="37baf-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="37baf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37baf-128">-ResourceGroupName</span></span>
<span data-ttu-id="37baf-129">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="37baf-129">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37baf-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37baf-130">-Confirm</span></span>
<span data-ttu-id="37baf-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="37baf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37baf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37baf-132">-WhatIf</span></span>
<span data-ttu-id="37baf-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37baf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37baf-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="37baf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37baf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37baf-135">CommonParameters</span></span>
<span data-ttu-id="37baf-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37baf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37baf-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37baf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37baf-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37baf-138">INPUTS</span></span>

### <span data-ttu-id="37baf-139">System.String</span><span class="sxs-lookup"><span data-stu-id="37baf-139">System.String</span></span>

## <span data-ttu-id="37baf-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37baf-140">OUTPUTS</span></span>

### <span data-ttu-id="37baf-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37baf-141">System.Boolean</span></span>

## <span data-ttu-id="37baf-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="37baf-142">NOTES</span></span>

## <span data-ttu-id="37baf-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37baf-143">RELATED LINKS</span></span>
