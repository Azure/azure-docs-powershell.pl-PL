---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356545"
---
# <span data-ttu-id="8ca4a-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="8ca4a-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="8ca4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ca4a-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca4a-103">Ustawia właściwości zasobu typu węzła lub uruchamia akcje ponownego tworzenia obrazów dla konkretnej usługi NDES typu węzła z parametrem-Reimage.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="8ca4a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ca4a-104">SYNTAX</span></span>

### <span data-ttu-id="8ca4a-105">ByObj (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8ca4a-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ca4a-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="8ca4a-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ca4a-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="8ca4a-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ca4a-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="8ca4a-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ca4a-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="8ca4a-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ca4a-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="8ca4a-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ca4a-111">Opis</span><span class="sxs-lookup"><span data-stu-id="8ca4a-111">DESCRIPTION</span></span>
<span data-ttu-id="8ca4a-112">Ustawia właściwości zasobu typu węzła lub uruchamia akcje ponownego tworzenia obrazów dla konkretnej usługi NDES typu węzła z parametrem-Reimage.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="8ca4a-113">W przypadku działania reimgae węzły usługi Fabric są wyłączone przed ponownym przetwarzaniem maszyn wirtualnych i ponowne włączenie ich po zakończeniu odtwarzania.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="8ca4a-114">W przypadku wykonania tej czynności w głównych typach węzłów może to zająć trochę czasu, ponieważ może to spowodować, że nie będzie można ponownie wykonać obrazu we wszystkich węzłach.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="8ca4a-115">Użyj funkcji-ForceReimage Wymuś operację, nawet jeśli program Service Fabric nie jest w stanie wyłączyć węzłów, ale z zachowaniem ostrożności, ponieważ może to spowodować utratę danych, jeśli w węźle działa stanowe obciążenie.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="8ca4a-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ca4a-116">EXAMPLES</span></span>

### <span data-ttu-id="8ca4a-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ca4a-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="8ca4a-118">Aktualizowanie liczby wystąpień typu węzła.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="8ca4a-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8ca4a-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="8ca4a-120">Aktualizowanie properites umieszczania typu węzła.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-120">Update placement properites of the node type.</span></span> <span data-ttu-id="8ca4a-121">Spowoduje to zastąpienie starszych properites dotyczących położenia.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="8ca4a-122">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8ca4a-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="8ca4a-123">Odobrazowanie węzła 0 i 3 w obszarze Typ węzła.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="8ca4a-124">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="8ca4a-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="8ca4a-125">Aktualizowanie liczby wystąpień typu węzła za pomocą połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="8ca4a-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ca4a-126">PARAMETERS</span></span>

### <span data-ttu-id="8ca4a-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="8ca4a-127">-ApplicationEndPort</span></span>
<span data-ttu-id="8ca4a-128">Port końcowy aplikacji zakresu portów.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-128">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="8ca4a-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="8ca4a-129">-ApplicationStartPort</span></span>
<span data-ttu-id="8ca4a-130">Port startowy zakresu portów.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-130">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="8ca4a-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ca4a-131">-AsJob</span></span>
<span data-ttu-id="8ca4a-132">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8ca4a-133">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="8ca4a-133">-Capacity</span></span>
<span data-ttu-id="8ca4a-134">Znaczniki pojemności zastosowane do węzłów w typie węzła jako pary klucz/wartość, Menedżer zasobów klastra używa tych znaczników w celu zrozumienia, ile zasobów zawiera węzeł.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="8ca4a-135">Zaktualizowanie tego ustawienia spowoduje zastąpienie bieżących wartości.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-135">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="8ca4a-136">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="8ca4a-136">-ClusterName</span></span>
<span data-ttu-id="8ca4a-137">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-137">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8ca4a-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca4a-138">-DefaultProfile</span></span>
<span data-ttu-id="8ca4a-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ca4a-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="8ca4a-140">-EphemeralEndPort</span></span>
<span data-ttu-id="8ca4a-141">Tymczasowych portów końcowych zakresu portów.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-141">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="8ca4a-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="8ca4a-142">-EphemeralStartPort</span></span>
<span data-ttu-id="8ca4a-143">Tymczasowych portów startowych zakresu portów.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-143">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="8ca4a-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="8ca4a-144">-ForceReimage</span></span>
<span data-ttu-id="8ca4a-145">Użycie tej flagi spowoduje wymuszenie usunięcia, nawet jeśli program Service Fabric nie będzie w stanie wyłączyć węzłów.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="8ca4a-146">Z tego powodu może dojść do utraty danych, jeśli w węźle działają stanowe obciążenia.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

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

### <span data-ttu-id="8ca4a-147">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8ca4a-147">-InputObject</span></span>
<span data-ttu-id="8ca4a-148">Zasób typu węzła</span><span class="sxs-lookup"><span data-stu-id="8ca4a-148">Node type resource</span></span>

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

### <span data-ttu-id="8ca4a-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="8ca4a-149">-InstanceCount</span></span>
<span data-ttu-id="8ca4a-150">Liczba węzłów w typie węzła.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-150">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="8ca4a-151">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ca4a-151">-Name</span></span>
<span data-ttu-id="8ca4a-152">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-152">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="8ca4a-153">-Nodename</span><span class="sxs-lookup"><span data-stu-id="8ca4a-153">-NodeName</span></span>
<span data-ttu-id="8ca4a-154">Lista nazw węzłów dla operacji.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-154">List of node names for the operation.</span></span>

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

### <span data-ttu-id="8ca4a-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ca4a-155">-PassThru</span></span>
<span data-ttu-id="8ca4a-156">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8ca4a-156">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="8ca4a-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="8ca4a-157">-PlacementProperty</span></span>
<span data-ttu-id="8ca4a-158">Znaczniki umieszczania zastosowane do węzłów w typie węzła jako pary klucz/wartość, które mogą być używane do wskazywania miejsca uruchomienia określonych usług (obciążenia).</span><span class="sxs-lookup"><span data-stu-id="8ca4a-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="8ca4a-159">Zaktualizowanie tego ustawienia spowoduje zastąpienie bieżących wartości.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-159">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="8ca4a-160">-Reimage</span><span class="sxs-lookup"><span data-stu-id="8ca4a-160">-Reimage</span></span>
<span data-ttu-id="8ca4a-161">Określ, czy węzły mają być ponownie podobrazami w typie węzła.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-161">Specify to reimage nodes on the node type.</span></span>

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

### <span data-ttu-id="8ca4a-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ca4a-162">-ResourceGroupName</span></span>
<span data-ttu-id="8ca4a-163">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8ca4a-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ca4a-164">-ResourceId</span></span>
<span data-ttu-id="8ca4a-165">Identyfikator zasobu typu węzła</span><span class="sxs-lookup"><span data-stu-id="8ca4a-165">Node type resource id</span></span>

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

### <span data-ttu-id="8ca4a-166">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8ca4a-166">-Confirm</span></span>
<span data-ttu-id="8ca4a-167">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ca4a-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ca4a-168">-WhatIf</span></span>
<span data-ttu-id="8ca4a-169">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ca4a-170">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ca4a-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca4a-171">CommonParameters</span></span>
<span data-ttu-id="8ca4a-172">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ca4a-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ca4a-173">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ca4a-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca4a-174">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ca4a-174">INPUTS</span></span>

### <span data-ttu-id="8ca4a-175">System. String</span><span class="sxs-lookup"><span data-stu-id="8ca4a-175">System.String</span></span>

## <span data-ttu-id="8ca4a-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ca4a-176">OUTPUTS</span></span>

### <span data-ttu-id="8ca4a-177">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ca4a-177">System.Boolean</span></span>

## <span data-ttu-id="8ca4a-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ca4a-178">NOTES</span></span>

## <span data-ttu-id="8ca4a-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ca4a-179">RELATED LINKS</span></span>
