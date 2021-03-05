---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5cb0e5bf8dce38a8552514835d2e16d19c3cc833
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005473"
---
# <span data-ttu-id="593bf-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="593bf-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="593bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="593bf-102">SYNOPSIS</span></span>
<span data-ttu-id="593bf-103">Usuń typ węzła lub określone węzły w obrębie typu węzła.</span><span class="sxs-lookup"><span data-stu-id="593bf-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="593bf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="593bf-104">SYNTAX</span></span>

### <span data-ttu-id="593bf-105">DeleteNodeTypeByObj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="593bf-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="593bf-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="593bf-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="593bf-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="593bf-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="593bf-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="593bf-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="593bf-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="593bf-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="593bf-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="593bf-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="593bf-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="593bf-111">DESCRIPTION</span></span>
<span data-ttu-id="593bf-112">Usuń typ węzła lub określone węzły w obrębie typu węzła.</span><span class="sxs-lookup"><span data-stu-id="593bf-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="593bf-113">Jeśli paremter -NodeName jest używany, zostaną usunięte tylko określone węzły.</span><span class="sxs-lookup"><span data-stu-id="593bf-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="593bf-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="593bf-114">EXAMPLES</span></span>

### <span data-ttu-id="593bf-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="593bf-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="593bf-116">Usuń typ węzła.</span><span class="sxs-lookup"><span data-stu-id="593bf-116">Remove node type.</span></span>

### <span data-ttu-id="593bf-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="593bf-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="593bf-118">Usuwanie typu węzła za pomocą rur.</span><span class="sxs-lookup"><span data-stu-id="593bf-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="593bf-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="593bf-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="593bf-120">Usuń 2 węzły z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="593bf-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="593bf-121">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="593bf-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="593bf-122">Usuń 2 węzły z typu węzła za pomocą rur.</span><span class="sxs-lookup"><span data-stu-id="593bf-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="593bf-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="593bf-123">PARAMETERS</span></span>

### <span data-ttu-id="593bf-124">— AsJob</span><span class="sxs-lookup"><span data-stu-id="593bf-124">-AsJob</span></span>
<span data-ttu-id="593bf-125">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="593bf-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="593bf-126">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="593bf-126">-ClusterName</span></span>
<span data-ttu-id="593bf-127">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="593bf-127">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="593bf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="593bf-128">-DefaultProfile</span></span>
<span data-ttu-id="593bf-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="593bf-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="593bf-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="593bf-130">-ForceRemoveNode</span></span>
<span data-ttu-id="593bf-131">Użycie tej flagi wymusi usunięcie nawet wtedy, gdy sieć szkieletowa usługi nie może wyłączyć węzłów.</span><span class="sxs-lookup"><span data-stu-id="593bf-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="593bf-132">Należy zachować ostrożność, ponieważ może to spowodować utratę danych, jeśli w węzłach są uruchomione obciążenia pracą o stanie lub jeśli po zakończeniu procesu grupowania nie ma wystarczającej ilości węzłów inicjalacji.</span><span class="sxs-lookup"><span data-stu-id="593bf-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="593bf-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="593bf-133">-InputObject</span></span>
<span data-ttu-id="593bf-134">Zasób typu węzła</span><span class="sxs-lookup"><span data-stu-id="593bf-134">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: DeleteNodeTypeByObj, DeleteNodeByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="593bf-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="593bf-135">-Name</span></span>
<span data-ttu-id="593bf-136">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="593bf-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="593bf-137">-NodeName</span><span class="sxs-lookup"><span data-stu-id="593bf-137">-NodeName</span></span>
<span data-ttu-id="593bf-138">Lista nazw węzła dla operacji.</span><span class="sxs-lookup"><span data-stu-id="593bf-138">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="593bf-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="593bf-139">-PassThru</span></span>
<span data-ttu-id="593bf-140">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="593bf-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="593bf-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="593bf-141">-ResourceGroupName</span></span>
<span data-ttu-id="593bf-142">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="593bf-142">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="593bf-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="593bf-143">-ResourceId</span></span>
<span data-ttu-id="593bf-144">Identyfikator zasobu typu węzła</span><span class="sxs-lookup"><span data-stu-id="593bf-144">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeById, DeleteNodeById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="593bf-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="593bf-145">-Confirm</span></span>
<span data-ttu-id="593bf-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="593bf-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="593bf-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="593bf-147">-WhatIf</span></span>
<span data-ttu-id="593bf-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="593bf-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="593bf-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="593bf-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="593bf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="593bf-150">CommonParameters</span></span>
<span data-ttu-id="593bf-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="593bf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="593bf-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="593bf-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="593bf-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="593bf-153">INPUTS</span></span>

### <span data-ttu-id="593bf-154">System.String</span><span class="sxs-lookup"><span data-stu-id="593bf-154">System.String</span></span>

## <span data-ttu-id="593bf-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="593bf-155">OUTPUTS</span></span>

### <span data-ttu-id="593bf-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="593bf-156">System.Boolean</span></span>

## <span data-ttu-id="593bf-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="593bf-157">NOTES</span></span>

## <span data-ttu-id="593bf-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="593bf-158">RELATED LINKS</span></span>
