---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502810"
---
# <span data-ttu-id="0ebd8-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0ebd8-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="0ebd8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ebd8-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebd8-103">Tworzenie nowego zasobu typu węzeł.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-103">Create new node type resource.</span></span>

## <span data-ttu-id="0ebd8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ebd8-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ebd8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0ebd8-105">DESCRIPTION</span></span>
<span data-ttu-id="0ebd8-106">Tworzenie nowego zasobu typu węzeł dla określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="0ebd8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ebd8-107">EXAMPLES</span></span>

### <span data-ttu-id="0ebd8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0ebd8-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="0ebd8-109">Tworzenie typu węzła podstawowego z trzema węzłami.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="0ebd8-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0ebd8-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="0ebd8-111">Tworzenie podstawowego typu węzła z 5 węzłami i określanie właściwości położenia, pojemności, aplikacji i portów tymczasowych.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="0ebd8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ebd8-112">PARAMETERS</span></span>

### <span data-ttu-id="0ebd8-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="0ebd8-113">-ApplicationEndPort</span></span>
<span data-ttu-id="0ebd8-114">Port końcowy aplikacji zakresu portów.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-114">Application End port of a range of ports.</span></span>

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

### <span data-ttu-id="0ebd8-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="0ebd8-115">-ApplicationStartPort</span></span>
<span data-ttu-id="0ebd8-116">Port startowy zakresu portów.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-116">Application start port of a range of ports.</span></span>

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

### <span data-ttu-id="0ebd8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ebd8-117">-AsJob</span></span>
<span data-ttu-id="0ebd8-118">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0ebd8-119">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="0ebd8-119">-Capacity</span></span>
<span data-ttu-id="0ebd8-120">Znaczniki pojemności zastosowane do węzłów w typie węzła jako pary klucz/wartość, Menedżer zasobów klastra używa tych znaczników w celu zrozumienia, ile zasobów zawiera węzeł.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="0ebd8-121">Zaktualizowanie tego ustawienia spowoduje zastąpienie bieżących wartości.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-121">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="0ebd8-122">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="0ebd8-122">-ClusterName</span></span>
<span data-ttu-id="0ebd8-123">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0ebd8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebd8-124">-DefaultProfile</span></span>
<span data-ttu-id="0ebd8-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ebd8-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="0ebd8-126">-DiskSize</span></span>
<span data-ttu-id="0ebd8-127">Rozmiar dysku dla każdej maszyny wirtualnej w typie węzła w GB.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="0ebd8-128">Domyślna 100.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-128">Default 100.</span></span>

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

### <span data-ttu-id="0ebd8-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="0ebd8-129">-EphemeralEndPort</span></span>
<span data-ttu-id="0ebd8-130">Tymczasowych portów końcowych zakresu portów.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-130">Ephemeral end port of a range of ports.</span></span>

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

### <span data-ttu-id="0ebd8-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="0ebd8-131">-EphemeralStartPort</span></span>
<span data-ttu-id="0ebd8-132">Tymczasowych portów startowych zakresu portów.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-132">Ephemeral start port of a range of ports.</span></span>

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

### <span data-ttu-id="0ebd8-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="0ebd8-133">-InstanceCount</span></span>
<span data-ttu-id="0ebd8-134">Liczba węzłów w typie węzła.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-134">The number of nodes in the node type.</span></span>

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

### <span data-ttu-id="0ebd8-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0ebd8-135">-Name</span></span>
<span data-ttu-id="0ebd8-136">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-136">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="0ebd8-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="0ebd8-137">-PlacementProperty</span></span>
<span data-ttu-id="0ebd8-138">Znaczniki umieszczania zastosowane do węzłów w typie węzła jako pary klucz/wartość, które mogą być używane do wskazywania miejsca uruchomienia określonych usług (obciążenia).</span><span class="sxs-lookup"><span data-stu-id="0ebd8-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="0ebd8-139">Zaktualizowanie tego ustawienia spowoduje zastąpienie bieżących wartości.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-139">Updating this will override the current values.</span></span>

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

### <span data-ttu-id="0ebd8-140">-Primary</span><span class="sxs-lookup"><span data-stu-id="0ebd8-140">-Primary</span></span>
<span data-ttu-id="0ebd8-141">Określ, czy typ węzła to podstawowy.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="0ebd8-142">W tym typie węzła będą uruchamiane usługi systemowe.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-142">On this node type will run system services.</span></span>
<span data-ttu-id="0ebd8-143">Tylko pojedynczy typ węzła powinien być oznaczony jako podstawowy.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="0ebd8-144">Nie można usuwać ani zmieniać typu węzła podstawowego dla istniejących klastrów.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="0ebd8-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ebd8-145">-ResourceGroupName</span></span>
<span data-ttu-id="0ebd8-146">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0ebd8-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="0ebd8-147">-VmImageOffer</span></span>
<span data-ttu-id="0ebd8-148">Typ oferty obrazu witryny Marketplace na platformie Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="0ebd8-149">Wartość domyślna: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-149">Default: WindowsServer.</span></span>

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

### <span data-ttu-id="0ebd8-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0ebd8-150">-VmImagePublisher</span></span>
<span data-ttu-id="0ebd8-151">Wydawca obrazu witryny Moja maszyna wirtualna Azure.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="0ebd8-152">Wartość domyślna: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-152">Default: MicrosoftWindowsServer.</span></span>

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

### <span data-ttu-id="0ebd8-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="0ebd8-153">-VmImageSku</span></span>
<span data-ttu-id="0ebd8-154">Wersja SKU maszyny wirtualnej platformy Azure: obraz witryny Marketplace.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="0ebd8-155">Wartość domyślna: 2019 — Datacenter.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-155">Default: 2019-Datacenter.</span></span>

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

### <span data-ttu-id="0ebd8-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="0ebd8-156">-VmImageVersion</span></span>
<span data-ttu-id="0ebd8-157">Wersja obrazu witryny Marketplace na platformie Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="0ebd8-158">Domyślnie: Najnowsza.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-158">Default: latest.</span></span>

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

### <span data-ttu-id="0ebd8-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="0ebd8-159">-VmSize</span></span>
<span data-ttu-id="0ebd8-160">Rozmiar maszyn wirtualnych w puli.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="0ebd8-161">Wszystkie maszyny wirtualne w puli mają ten sam rozmiar.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="0ebd8-162">Wartość domyślna: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-162">Default: Standard_D2.</span></span>

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

### <span data-ttu-id="0ebd8-163">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ebd8-163">-Confirm</span></span>
<span data-ttu-id="0ebd8-164">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ebd8-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ebd8-165">-WhatIf</span></span>
<span data-ttu-id="0ebd8-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ebd8-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ebd8-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebd8-168">CommonParameters</span></span>
<span data-ttu-id="0ebd8-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebd8-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebd8-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ebd8-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebd8-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ebd8-171">INPUTS</span></span>

### <span data-ttu-id="0ebd8-172">System. String</span><span class="sxs-lookup"><span data-stu-id="0ebd8-172">System.String</span></span>

## <span data-ttu-id="0ebd8-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ebd8-173">OUTPUTS</span></span>

### <span data-ttu-id="0ebd8-174">Microsoft. Azure. Commands. servicefabric. MODELES. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="0ebd8-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="0ebd8-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ebd8-175">NOTES</span></span>

## <span data-ttu-id="0ebd8-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ebd8-176">RELATED LINKS</span></span>
