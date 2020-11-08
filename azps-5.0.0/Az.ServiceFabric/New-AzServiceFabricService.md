---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: 930d86e457bef446d282db95d4289913bdcf10b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234270"
---
# <span data-ttu-id="3e2f8-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3e2f8-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="3e2f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e2f8-102">SYNOPSIS</span></span>
<span data-ttu-id="3e2f8-103">Tworzenie nowej usługi programu Fabric Service w ramach określonej aplikacji i klastra.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="3e2f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e2f8-104">SYNTAX</span></span>

### <span data-ttu-id="3e2f8-105">Stateless-Singleton (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3e2f8-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e2f8-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="3e2f8-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e2f8-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="3e2f8-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e2f8-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="3e2f8-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e2f8-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="3e2f8-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e2f8-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="3e2f8-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e2f8-111">Opis</span><span class="sxs-lookup"><span data-stu-id="3e2f8-111">DESCRIPTION</span></span>
<span data-ttu-id="3e2f8-112">To polecenie cmdlet umożliwia tworzenie usług bezstanowych i stanowych w ramach określonej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="3e2f8-113">Usługa powinna zostać zamknięta w manifeście aplikacji, a typ musi być taki sam jak w manifeście.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="3e2f8-114">Nazwa aplikacji powinna być prefiksem nazwy usługi.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="3e2f8-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e2f8-115">EXAMPLES</span></span>

### <span data-ttu-id="3e2f8-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3e2f8-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="3e2f8-117">W tym przykładzie zostanie utworzona nowa usługa bezstanowa "testApp ~ testService1" z liczbą wystąpień-1 (na wszystkich węzłach).</span><span class="sxs-lookup"><span data-stu-id="3e2f8-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="3e2f8-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3e2f8-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="3e2f8-119">W tym przykładzie zostanie utworzona nowa usługa stanowa "testApp ~ testService2" z elementem docelowym 5 węzłów.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="3e2f8-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e2f8-120">PARAMETERS</span></span>

### <span data-ttu-id="3e2f8-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="3e2f8-121">-ApplicationName</span></span>
<span data-ttu-id="3e2f8-122">Określ nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-123">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="3e2f8-123">-ClusterName</span></span>
<span data-ttu-id="3e2f8-124">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-124">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="3e2f8-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="3e2f8-125">-DefaultMoveCost</span></span>
<span data-ttu-id="3e2f8-126">Określ domyślny koszt przeniesienia.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="3e2f8-127">Większe koszty sprawiają, że Menedżer zasobów klastra przeniesie replikę podczas próby zrównoważenia klastra</span><span class="sxs-lookup"><span data-stu-id="3e2f8-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.MoveCostEnum
Parameter Sets: (All)
Aliases:
Accepted values: Zero, Low, Medium, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e2f8-128">-DefaultProfile</span></span>
<span data-ttu-id="3e2f8-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e2f8-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="3e2f8-130">-InstanceCount</span></span>
<span data-ttu-id="3e2f8-131">Określanie liczby wystąpień dla usługi</span><span class="sxs-lookup"><span data-stu-id="3e2f8-131">Specify the instance count for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="3e2f8-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="3e2f8-133">Określanie minimalnego rozmiaru zestawu replik dla usługi</span><span class="sxs-lookup"><span data-stu-id="3e2f8-133">Specify the min replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e2f8-134">-Name</span></span>
<span data-ttu-id="3e2f8-135">Określ nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-135">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="3e2f8-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="3e2f8-137">Wskazuje, że usługa korzysta ze schematu partycji nazwanej.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="3e2f8-138">Usługi korzystające z tego modelu zazwyczaj mają dane, które można przetworzyć w ramach ograniczonego zestawu.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="3e2f8-139">Do typowych przykładów pól danych używanych jako klucze partycji nazwanych są regiony, kody pocztowe, grupy klientów lub inne granice biznesowe.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Named, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-140">-PartitionSchemeSingleton</span><span class="sxs-lookup"><span data-stu-id="3e2f8-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="3e2f8-141">Wskazuje, że usługa używa schematu partycji singleton.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="3e2f8-142">Partycje pojedyncze są zazwyczaj używane, gdy usługa nie wymaga żadnych dodatkowych tras routingu.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateful-Singleton
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="3e2f8-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="3e2f8-144">Wskazuje, że usługa używa schematu partycji UniformInt64.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="3e2f8-145">Oznacza to, że każda partycja należy do zakresu kluczy Int64.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-145">This means that each partition owns a range of int64 keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-UniformInt64Range, Stateful-UniformInt64Range
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-146">-QuorumLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="3e2f8-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="3e2f8-147">Określanie czasu oczekiwania na utratę kworum dla usługi</span><span class="sxs-lookup"><span data-stu-id="3e2f8-147">Specify the quorum loss wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="3e2f8-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="3e2f8-149">Określanie czasu oczekiwania na ponowne uruchomienie repliki dla usługi</span><span class="sxs-lookup"><span data-stu-id="3e2f8-149">Specify the replica restart wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e2f8-150">-ResourceGroupName</span></span>
<span data-ttu-id="3e2f8-151">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-151">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="3e2f8-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="3e2f8-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="3e2f8-153">Określanie czasu trwania repliki dla usługi</span><span class="sxs-lookup"><span data-stu-id="3e2f8-153">Specify the stand by replica duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-154">-Stanowy</span><span class="sxs-lookup"><span data-stu-id="3e2f8-154">-Stateful</span></span>
<span data-ttu-id="3e2f8-155">Korzystanie z usługi akumulującej stan</span><span class="sxs-lookup"><span data-stu-id="3e2f8-155">Use for stateful service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-156">-Bez Stanów</span><span class="sxs-lookup"><span data-stu-id="3e2f8-156">-Stateless</span></span>
<span data-ttu-id="3e2f8-157">Korzystanie z usługi bezstanowej</span><span class="sxs-lookup"><span data-stu-id="3e2f8-157">Use for stateless service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="3e2f8-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="3e2f8-159">Określanie docelowego rozmiaru zestawu replik dla usługi</span><span class="sxs-lookup"><span data-stu-id="3e2f8-159">Specify the target replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-160">-Type</span><span class="sxs-lookup"><span data-stu-id="3e2f8-160">-Type</span></span>
<span data-ttu-id="3e2f8-161">Określ nazwę typu usługi aplikacji, która powinna znajdować się w manifeście aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2f8-162">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e2f8-162">-Confirm</span></span>
<span data-ttu-id="3e2f8-163">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e2f8-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e2f8-164">-WhatIf</span></span>
<span data-ttu-id="3e2f8-165">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e2f8-166">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e2f8-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e2f8-167">CommonParameters</span></span>
<span data-ttu-id="3e2f8-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e2f8-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e2f8-169">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e2f8-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e2f8-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e2f8-170">INPUTS</span></span>

### <span data-ttu-id="3e2f8-171">System. String</span><span class="sxs-lookup"><span data-stu-id="3e2f8-171">System.String</span></span>

## <span data-ttu-id="3e2f8-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e2f8-172">OUTPUTS</span></span>

### <span data-ttu-id="3e2f8-173">Microsoft. Azure. Commands. servicefabric. MODELES. PSService</span><span class="sxs-lookup"><span data-stu-id="3e2f8-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="3e2f8-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e2f8-174">NOTES</span></span>

## <span data-ttu-id="3e2f8-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e2f8-175">RELATED LINKS</span></span>
