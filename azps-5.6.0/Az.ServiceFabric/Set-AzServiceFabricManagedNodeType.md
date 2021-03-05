---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3f3f19f88ffdd37cbad009950c064e672e186b34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976337"
---
# <span data-ttu-id="fc01e-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="fc01e-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="fc01e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc01e-102">SYNOPSIS</span></span>
<span data-ttu-id="fc01e-103">Ustawia właściwości zasobu typu węzła lub uruchamiaj akcje ponownego projektu dla określonych ndes typu węzła za pomocą parametru -Reimage.</span><span class="sxs-lookup"><span data-stu-id="fc01e-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="fc01e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fc01e-104">SYNTAX</span></span>

### <span data-ttu-id="fc01e-105">ByObj (Domyślnie)</span><span class="sxs-lookup"><span data-stu-id="fc01e-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc01e-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="fc01e-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc01e-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="fc01e-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc01e-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="fc01e-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc01e-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="fc01e-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc01e-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="fc01e-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc01e-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="fc01e-111">DESCRIPTION</span></span>
<span data-ttu-id="fc01e-112">Ustawia właściwości zasobu typu węzła lub uruchamiaj akcje ponownego projektu dla określonych ndes typu węzła za pomocą parametru -Reimage.</span><span class="sxs-lookup"><span data-stu-id="fc01e-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="fc01e-113">Podczas operacji ponownego tworzenia klienta węzły szkieletów usług zostaną wyłączone przed ponownego zaimportowania maszyny wirtualnej i ponownie włączono je po ich powrocie.</span><span class="sxs-lookup"><span data-stu-id="fc01e-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="fc01e-114">Jeśli to zrobisz w przypadku typów węzła podstawowego, może to zająć trochę czasu, ponieważ może nie zostać ponownie zaimportowane wszystkie węzły w tym samym czasie.</span><span class="sxs-lookup"><span data-stu-id="fc01e-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="fc01e-115">Użycie funkcji -ForceReimage wymusza operację, nawet jeśli sieć szkielet usług nie może wyłączyć węzłów, ale należy zachować ostrożność, ponieważ może to spowodować utratę danych, jeśli w węźle są uruchomione obciążenia pracą o stanach.</span><span class="sxs-lookup"><span data-stu-id="fc01e-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="fc01e-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fc01e-116">EXAMPLES</span></span>

### <span data-ttu-id="fc01e-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fc01e-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="fc01e-118">Aktualizowanie liczby wystąpień typu węzła.</span><span class="sxs-lookup"><span data-stu-id="fc01e-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="fc01e-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fc01e-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="fc01e-120">Zaktualizuj położenie odpowiednich węzłów typu węzła.</span><span class="sxs-lookup"><span data-stu-id="fc01e-120">Update placement properites of the node type.</span></span> <span data-ttu-id="fc01e-121">Spowoduje to zastąpienie starszych miejsc, w których są wyty już istniejące.</span><span class="sxs-lookup"><span data-stu-id="fc01e-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="fc01e-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="fc01e-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="fc01e-123">Ponownie przeprojektuj węzeł 0 i 3 w typie węzła.</span><span class="sxs-lookup"><span data-stu-id="fc01e-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="fc01e-124">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="fc01e-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="fc01e-125">Zaktualizuj liczbę wystąpień typu węzła za pomocą rur.</span><span class="sxs-lookup"><span data-stu-id="fc01e-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="fc01e-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc01e-126">PARAMETERS</span></span>

### <span data-ttu-id="fc01e-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="fc01e-127">-ApplicationEndPort</span></span>
<span data-ttu-id="fc01e-128">Port końca aplikacji zakresu portów.</span><span class="sxs-lookup"><span data-stu-id="fc01e-128">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="fc01e-129">-ApplicationStartPort</span></span>
<span data-ttu-id="fc01e-130">Port uruchamiania aplikacji dla zakresu portów.</span><span class="sxs-lookup"><span data-stu-id="fc01e-130">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-131">— AsJob</span><span class="sxs-lookup"><span data-stu-id="fc01e-131">-AsJob</span></span>
<span data-ttu-id="fc01e-132">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="fc01e-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fc01e-133">— Pojemność</span><span class="sxs-lookup"><span data-stu-id="fc01e-133">-Capacity</span></span>
<span data-ttu-id="fc01e-134">Tagi wydajności zastosowane do węzłów typu węzła jako pary klucz/wartość są używane przez menedżera zasobów klastrów do zrozumienia, ile zasobu ma węzeł.</span><span class="sxs-lookup"><span data-stu-id="fc01e-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="fc01e-135">Aktualizacja spowoduje zastąpienie bieżących wartości.</span><span class="sxs-lookup"><span data-stu-id="fc01e-135">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-136">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fc01e-136">-ClusterName</span></span>
<span data-ttu-id="fc01e-137">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="fc01e-137">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc01e-138">-DefaultProfile</span></span>
<span data-ttu-id="fc01e-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc01e-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc01e-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="fc01e-140">-EphemeralEndPort</span></span>
<span data-ttu-id="fc01e-141">Ephemeral end port of a range of ports.</span><span class="sxs-lookup"><span data-stu-id="fc01e-141">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="fc01e-142">-EphemeralStartPort</span></span>
<span data-ttu-id="fc01e-143">Ephemeral start port of a range of ports.</span><span class="sxs-lookup"><span data-stu-id="fc01e-143">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="fc01e-144">-ForceReimage</span></span>
<span data-ttu-id="fc01e-145">Użycie tej flagi wymusi usunięcie nawet wtedy, gdy sieć szkieletowa usługi nie może wyłączyć węzłów.</span><span class="sxs-lookup"><span data-stu-id="fc01e-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="fc01e-146">Należy zachować ostrożność, ponieważ może to spowodować utratę danych, jeśli w węźle są uruchomione obciążenia pracą o stanie.</span><span class="sxs-lookup"><span data-stu-id="fc01e-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc01e-147">-InputObject</span></span>
<span data-ttu-id="fc01e-148">Zasób typu węzła</span><span class="sxs-lookup"><span data-stu-id="fc01e-148">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj, ReimageByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="fc01e-149">-InstanceCount</span></span>
<span data-ttu-id="fc01e-150">Liczba węzłów typu węzła.</span><span class="sxs-lookup"><span data-stu-id="fc01e-150">The number of nodes in the node type.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-151">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fc01e-151">-Name</span></span>
<span data-ttu-id="fc01e-152">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="fc01e-152">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-153">-NodeName</span><span class="sxs-lookup"><span data-stu-id="fc01e-153">-NodeName</span></span>
<span data-ttu-id="fc01e-154">Lista nazw węzła dla operacji.</span><span class="sxs-lookup"><span data-stu-id="fc01e-154">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc01e-155">-PassThru</span></span>
<span data-ttu-id="fc01e-156">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="fc01e-156">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="fc01e-157">-PlacementProperty</span></span>
<span data-ttu-id="fc01e-158">Tagi położenia stosowane do węzłów typu węzła jako pary klucz/wartość, których można używać do wskazywania miejsc, w których mają być uruchamiane określone usługi (obciążenie pracą).</span><span class="sxs-lookup"><span data-stu-id="fc01e-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="fc01e-159">Aktualizacja spowoduje zastąpienie bieżących wartości.</span><span class="sxs-lookup"><span data-stu-id="fc01e-159">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-160">-Reimage</span><span class="sxs-lookup"><span data-stu-id="fc01e-160">-Reimage</span></span>
<span data-ttu-id="fc01e-161">Określ, aby ponownie zaimportować węzły typu węzła.</span><span class="sxs-lookup"><span data-stu-id="fc01e-161">Specify to reimage nodes on the node type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc01e-162">-ResourceGroupName</span></span>
<span data-ttu-id="fc01e-163">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc01e-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc01e-164">-ResourceId</span></span>
<span data-ttu-id="fc01e-165">Identyfikator zasobu typu węzła</span><span class="sxs-lookup"><span data-stu-id="fc01e-165">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsById, ReimageById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc01e-166">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc01e-166">-Confirm</span></span>
<span data-ttu-id="fc01e-167">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fc01e-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc01e-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc01e-168">-WhatIf</span></span>
<span data-ttu-id="fc01e-169">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc01e-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc01e-170">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fc01e-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc01e-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc01e-171">CommonParameters</span></span>
<span data-ttu-id="fc01e-172">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc01e-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc01e-173">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc01e-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc01e-174">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc01e-174">INPUTS</span></span>

### <span data-ttu-id="fc01e-175">System.String</span><span class="sxs-lookup"><span data-stu-id="fc01e-175">System.String</span></span>

## <span data-ttu-id="fc01e-176">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc01e-176">OUTPUTS</span></span>

### <span data-ttu-id="fc01e-177">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fc01e-177">System.Boolean</span></span>

## <span data-ttu-id="fc01e-178">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fc01e-178">NOTES</span></span>

## <span data-ttu-id="fc01e-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc01e-179">RELATED LINKS</span></span>
