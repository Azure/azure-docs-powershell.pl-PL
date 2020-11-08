---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222272"
---
# <span data-ttu-id="72dd6-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="72dd6-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="72dd6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="72dd6-103">Usuwanie typu węzła lub określonych węzłów w obrębie typu węzła.</span><span class="sxs-lookup"><span data-stu-id="72dd6-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="72dd6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72dd6-104">SYNTAX</span></span>

### <span data-ttu-id="72dd6-105">DeleteNodeTypeByObj (domyślny)</span><span class="sxs-lookup"><span data-stu-id="72dd6-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72dd6-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="72dd6-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72dd6-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="72dd6-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72dd6-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="72dd6-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72dd6-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="72dd6-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72dd6-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="72dd6-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72dd6-111">Opis</span><span class="sxs-lookup"><span data-stu-id="72dd6-111">DESCRIPTION</span></span>
<span data-ttu-id="72dd6-112">Usuwanie typu węzła lub określonych węzłów w obrębie typu węzła.</span><span class="sxs-lookup"><span data-stu-id="72dd6-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="72dd6-113">Jeśli jest używana paremter-nodename, zostaną usunięte tylko określone węzły.</span><span class="sxs-lookup"><span data-stu-id="72dd6-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="72dd6-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72dd6-114">EXAMPLES</span></span>

### <span data-ttu-id="72dd6-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="72dd6-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="72dd6-116">Usuń typ węzła.</span><span class="sxs-lookup"><span data-stu-id="72dd6-116">Remove node type.</span></span>

### <span data-ttu-id="72dd6-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="72dd6-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="72dd6-118">Usuwanie typu węzła za pomocą połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="72dd6-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="72dd6-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="72dd6-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="72dd6-120">Usuń 2 węzły z typu węzła.</span><span class="sxs-lookup"><span data-stu-id="72dd6-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="72dd6-121">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="72dd6-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="72dd6-122">Usuwanie dwóch węzłów z typu węzła za pomocą połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="72dd6-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="72dd6-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72dd6-123">PARAMETERS</span></span>

### <span data-ttu-id="72dd6-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72dd6-124">-AsJob</span></span>
<span data-ttu-id="72dd6-125">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="72dd6-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="72dd6-126">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="72dd6-126">-ClusterName</span></span>
<span data-ttu-id="72dd6-127">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="72dd6-127">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="72dd6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72dd6-128">-DefaultProfile</span></span>
<span data-ttu-id="72dd6-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72dd6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72dd6-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="72dd6-130">-ForceRemoveNode</span></span>
<span data-ttu-id="72dd6-131">Użycie tej flagi spowoduje wymuszenie usunięcia, nawet jeśli program Service Fabric nie będzie w stanie wyłączyć węzłów.</span><span class="sxs-lookup"><span data-stu-id="72dd6-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="72dd6-132">W razie potrzeby należy skorzystać z ostrożności, ponieważ może to spowodować utratę danych, jeśli w węzłach są uruchomione stanowe obciążenia, lub może dojść do działania klastra, jeśli po opearion nie ma wystarczającej liczby węzłów.</span><span class="sxs-lookup"><span data-stu-id="72dd6-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

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

### <span data-ttu-id="72dd6-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="72dd6-133">-InputObject</span></span>
<span data-ttu-id="72dd6-134">Zasób typu węzła</span><span class="sxs-lookup"><span data-stu-id="72dd6-134">Node type resource</span></span>

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

### <span data-ttu-id="72dd6-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72dd6-135">-Name</span></span>
<span data-ttu-id="72dd6-136">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="72dd6-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="72dd6-137">-Nodename</span><span class="sxs-lookup"><span data-stu-id="72dd6-137">-NodeName</span></span>
<span data-ttu-id="72dd6-138">Lista nazw węzłów dla operacji.</span><span class="sxs-lookup"><span data-stu-id="72dd6-138">List of node names for the operation.</span></span>

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

### <span data-ttu-id="72dd6-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72dd6-139">-PassThru</span></span>
<span data-ttu-id="72dd6-140">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="72dd6-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="72dd6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72dd6-141">-ResourceGroupName</span></span>
<span data-ttu-id="72dd6-142">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="72dd6-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="72dd6-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72dd6-143">-ResourceId</span></span>
<span data-ttu-id="72dd6-144">Identyfikator zasobu typu węzła</span><span class="sxs-lookup"><span data-stu-id="72dd6-144">Node type resource id</span></span>

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

### <span data-ttu-id="72dd6-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72dd6-145">-Confirm</span></span>
<span data-ttu-id="72dd6-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72dd6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72dd6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72dd6-147">-WhatIf</span></span>
<span data-ttu-id="72dd6-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72dd6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72dd6-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72dd6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72dd6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72dd6-150">CommonParameters</span></span>
<span data-ttu-id="72dd6-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72dd6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72dd6-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72dd6-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72dd6-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72dd6-153">INPUTS</span></span>

### <span data-ttu-id="72dd6-154">System. String</span><span class="sxs-lookup"><span data-stu-id="72dd6-154">System.String</span></span>

## <span data-ttu-id="72dd6-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72dd6-155">OUTPUTS</span></span>

### <span data-ttu-id="72dd6-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72dd6-156">System.Boolean</span></span>

## <span data-ttu-id="72dd6-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72dd6-157">NOTES</span></span>

## <span data-ttu-id="72dd6-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72dd6-158">RELATED LINKS</span></span>
