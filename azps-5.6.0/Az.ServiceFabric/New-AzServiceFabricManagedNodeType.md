---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 065885f4ae8f6d2ac51cb87cb0e697f4f22245f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995891"
---
# <span data-ttu-id="176b6-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="176b6-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="176b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="176b6-102">SYNOPSIS</span></span>
<span data-ttu-id="176b6-103">Tworzenie nowego zasobu typu węzła.</span><span class="sxs-lookup"><span data-stu-id="176b6-103">Create new node type resource.</span></span>

## <span data-ttu-id="176b6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="176b6-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="176b6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="176b6-105">DESCRIPTION</span></span>
<span data-ttu-id="176b6-106">Utwórz nowy zasób typu węzła dla określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="176b6-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="176b6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="176b6-107">EXAMPLES</span></span>

### <span data-ttu-id="176b6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="176b6-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="176b6-109">Utwórz podstawowy typ węzła z 3 węzłami.</span><span class="sxs-lookup"><span data-stu-id="176b6-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="176b6-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="176b6-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="176b6-111">Utwórz podstawowy typ węzła z 5 węzłami i określanie właściwości położenia, zastosowań, aplikacji i portów pierwotnych.</span><span class="sxs-lookup"><span data-stu-id="176b6-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="176b6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="176b6-112">PARAMETERS</span></span>

### <span data-ttu-id="176b6-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="176b6-113">-ApplicationEndPort</span></span>
<span data-ttu-id="176b6-114">Port końca aplikacji zakresu portów.</span><span class="sxs-lookup"><span data-stu-id="176b6-114">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="176b6-115">-ApplicationStartPort</span></span>
<span data-ttu-id="176b6-116">Port uruchamiania aplikacji dla zakresu portów.</span><span class="sxs-lookup"><span data-stu-id="176b6-116">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="176b6-117">-AsJob</span></span>
<span data-ttu-id="176b6-118">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="176b6-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="176b6-119">— Pojemność</span><span class="sxs-lookup"><span data-stu-id="176b6-119">-Capacity</span></span>
<span data-ttu-id="176b6-120">Tagi wydajności zastosowane do węzłów typu węzła jako pary klucz/wartość są używane przez menedżera zasobów klastrów do zrozumienia, ile zasobu ma węzeł.</span><span class="sxs-lookup"><span data-stu-id="176b6-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="176b6-121">Aktualizacja spowoduje zastąpienie bieżących wartości.</span><span class="sxs-lookup"><span data-stu-id="176b6-121">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-122">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="176b6-122">-ClusterName</span></span>
<span data-ttu-id="176b6-123">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="176b6-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="176b6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176b6-124">-DefaultProfile</span></span>
<span data-ttu-id="176b6-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="176b6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="176b6-126">- DiskSize</span><span class="sxs-lookup"><span data-stu-id="176b6-126">-DiskSize</span></span>
<span data-ttu-id="176b6-127">Rozmiar dysku każdej maszyny wirtualnej typu węzła w kb/s.</span><span class="sxs-lookup"><span data-stu-id="176b6-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="176b6-128">Domyślna wartość 100.</span><span class="sxs-lookup"><span data-stu-id="176b6-128">Default 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="176b6-129">-EphemeralEndPort</span></span>
<span data-ttu-id="176b6-130">Ephemeral end port of a range of ports.</span><span class="sxs-lookup"><span data-stu-id="176b6-130">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="176b6-131">-EphemeralStartPort</span></span>
<span data-ttu-id="176b6-132">Ephemeral start port of a range of ports.</span><span class="sxs-lookup"><span data-stu-id="176b6-132">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="176b6-133">-InstanceCount</span></span>
<span data-ttu-id="176b6-134">Liczba węzłów typu węzła.</span><span class="sxs-lookup"><span data-stu-id="176b6-134">The number of nodes in the node type.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="176b6-135">-Name</span></span>
<span data-ttu-id="176b6-136">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="176b6-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="176b6-137">-PlacementProperty</span></span>
<span data-ttu-id="176b6-138">Tagi położenia stosowane do węzłów typu węzła jako pary klucz/wartość, których można używać do wskazywania miejsc, w których mają być uruchamiane określone usługi (obciążenie pracą).</span><span class="sxs-lookup"><span data-stu-id="176b6-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="176b6-139">Aktualizacja spowoduje zastąpienie bieżących wartości.</span><span class="sxs-lookup"><span data-stu-id="176b6-139">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-140">— podstawowy</span><span class="sxs-lookup"><span data-stu-id="176b6-140">-Primary</span></span>
<span data-ttu-id="176b6-141">Określ, czy typ węzła jest podstawowy.</span><span class="sxs-lookup"><span data-stu-id="176b6-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="176b6-142">W tym typie węzła będą uruchamiane usługi systemowe.</span><span class="sxs-lookup"><span data-stu-id="176b6-142">On this node type will run system services.</span></span>
<span data-ttu-id="176b6-143">Tylko jeden typ węzła powinien być oznaczony jako podstawowy.</span><span class="sxs-lookup"><span data-stu-id="176b6-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="176b6-144">Podstawowy typ węzła nie może być usuwany ani zmieniany dla istniejących klastrów.</span><span class="sxs-lookup"><span data-stu-id="176b6-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="176b6-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="176b6-145">-ResourceGroupName</span></span>
<span data-ttu-id="176b6-146">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="176b6-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="176b6-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="176b6-147">-VmImageOffer</span></span>
<span data-ttu-id="176b6-148">Typ oferty portalu Azure Virtual Machines Marketplace.</span><span class="sxs-lookup"><span data-stu-id="176b6-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="176b6-149">Domyślne: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="176b6-149">Default: WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "WindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="176b6-150">-VmImagePublisher</span></span>
<span data-ttu-id="176b6-151">Obraz wydawcy witryny Azure Virtual Machines Marketplace.</span><span class="sxs-lookup"><span data-stu-id="176b6-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="176b6-152">Domyślne: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="176b6-152">Default: MicrosoftWindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "MicrosoftWindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="176b6-153">-VmImageSku</span></span>
<span data-ttu-id="176b6-154">The SKU of the Azure Virtual Machines Marketplace image.</span><span class="sxs-lookup"><span data-stu-id="176b6-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="176b6-155">Domyślne: 2019-Datacenter.</span><span class="sxs-lookup"><span data-stu-id="176b6-155">Default: 2019-Datacenter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "2019-Datacenter"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="176b6-156">-VmImageVersion</span></span>
<span data-ttu-id="176b6-157">Obraz wersji witryny Azure Virtual Machines Marketplace.</span><span class="sxs-lookup"><span data-stu-id="176b6-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="176b6-158">Domyślne: najnowsze.</span><span class="sxs-lookup"><span data-stu-id="176b6-158">Default: latest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "latest"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="176b6-159">-VmSize</span></span>
<span data-ttu-id="176b6-160">Rozmiar maszyn wirtualnych w puli.</span><span class="sxs-lookup"><span data-stu-id="176b6-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="176b6-161">Wszystkie maszyny wirtualne w puli mają ten sam rozmiar.</span><span class="sxs-lookup"><span data-stu-id="176b6-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="176b6-162">Domyślne: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="176b6-162">Default: Standard_D2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "Standard_D2"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176b6-163">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="176b6-163">-Confirm</span></span>
<span data-ttu-id="176b6-164">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="176b6-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176b6-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176b6-165">-WhatIf</span></span>
<span data-ttu-id="176b6-166">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="176b6-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="176b6-167">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="176b6-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="176b6-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176b6-168">CommonParameters</span></span>
<span data-ttu-id="176b6-169">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176b6-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176b6-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="176b6-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176b6-171">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="176b6-171">INPUTS</span></span>

### <span data-ttu-id="176b6-172">System.String</span><span class="sxs-lookup"><span data-stu-id="176b6-172">System.String</span></span>

## <span data-ttu-id="176b6-173">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="176b6-173">OUTPUTS</span></span>

### <span data-ttu-id="176b6-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="176b6-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="176b6-175">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="176b6-175">NOTES</span></span>

## <span data-ttu-id="176b6-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="176b6-176">RELATED LINKS</span></span>
