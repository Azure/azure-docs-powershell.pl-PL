---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502780"
---
# <span data-ttu-id="25f32-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="25f32-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="25f32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25f32-102">SYNOPSIS</span></span>
<span data-ttu-id="25f32-103">Ponownie uruchom określone węzły z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="25f32-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="25f32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25f32-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25f32-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25f32-105">DESCRIPTION</span></span>
<span data-ttu-id="25f32-106">Ponownie uruchom określone węzły z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="25f32-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="25f32-107">Przed ponownym uruchomieniem maszyn wirtualnych zostaną wyłączone węzły usługi Fabric.</span><span class="sxs-lookup"><span data-stu-id="25f32-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="25f32-108">W przypadku wykonania tej czynności w głównych typach węzłów może to zająć trochę czasu, ponieważ może to nie być ponowne uruchomienie wszystkich węzłów w tym samym czasie.</span><span class="sxs-lookup"><span data-stu-id="25f32-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="25f32-109">Użyj funkcji-ForceRestart Wymuś operację, nawet jeśli program Service Fabric nie jest w stanie wyłączyć węzłów, ale z zachowaniem ostrożności, ponieważ może to spowodować utratę danych, jeśli w węźle działa stanowe obciążenie.</span><span class="sxs-lookup"><span data-stu-id="25f32-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="25f32-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25f32-110">EXAMPLES</span></span>

### <span data-ttu-id="25f32-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25f32-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="25f32-112">Uruchom ponownie węzły 0 i 3 w obszarze Typ węzła.</span><span class="sxs-lookup"><span data-stu-id="25f32-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="25f32-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25f32-113">PARAMETERS</span></span>

### <span data-ttu-id="25f32-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25f32-114">-AsJob</span></span>
<span data-ttu-id="25f32-115">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="25f32-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="25f32-116">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="25f32-116">-ClusterName</span></span>
<span data-ttu-id="25f32-117">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="25f32-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="25f32-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f32-118">-DefaultProfile</span></span>
<span data-ttu-id="25f32-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="25f32-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25f32-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="25f32-120">-ForceRestart</span></span>
<span data-ttu-id="25f32-121">Użycie tej flagi spowoduje wymuszenie ponownego uruchomienia węzła, nawet jeśli program Service Fabric nie będzie mógł wyłączyć węzłów.</span><span class="sxs-lookup"><span data-stu-id="25f32-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="25f32-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="25f32-122">-Name</span></span>
<span data-ttu-id="25f32-123">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="25f32-123">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="25f32-124">-Nodename</span><span class="sxs-lookup"><span data-stu-id="25f32-124">-NodeName</span></span>
<span data-ttu-id="25f32-125">Lista nazw węzłów dla operacji.</span><span class="sxs-lookup"><span data-stu-id="25f32-125">List of node names for the operation.</span></span>

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

### <span data-ttu-id="25f32-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25f32-126">-PassThru</span></span>
<span data-ttu-id="25f32-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="25f32-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="25f32-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25f32-128">-ResourceGroupName</span></span>
<span data-ttu-id="25f32-129">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25f32-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="25f32-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25f32-130">-Confirm</span></span>
<span data-ttu-id="25f32-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25f32-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25f32-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25f32-132">-WhatIf</span></span>
<span data-ttu-id="25f32-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25f32-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25f32-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25f32-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25f32-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f32-135">CommonParameters</span></span>
<span data-ttu-id="25f32-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25f32-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f32-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25f32-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f32-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25f32-138">INPUTS</span></span>

### <span data-ttu-id="25f32-139">System. String</span><span class="sxs-lookup"><span data-stu-id="25f32-139">System.String</span></span>

## <span data-ttu-id="25f32-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25f32-140">OUTPUTS</span></span>

### <span data-ttu-id="25f32-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25f32-141">System.Boolean</span></span>

## <span data-ttu-id="25f32-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25f32-142">NOTES</span></span>

## <span data-ttu-id="25f32-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25f32-143">RELATED LINKS</span></span>
