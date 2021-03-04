---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: febf0ecb24be1b419353142805c9f91e0c771de5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955617"
---
# <span data-ttu-id="3b3eb-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3b3eb-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="3b3eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b3eb-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3eb-103">Aktualizowanie aplikacji do obsługi szkieletów usług.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-103">Update a service fabric application.</span></span> <span data-ttu-id="3b3eb-104">Pozwala to zaktualizować parametry aplikacji i/lub uaktualnić wersję typu aplikacji, co spowoduje uruchomienie uaktualnienia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="3b3eb-105">Obsługuje tylko ARM wdrożonych aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="3b3eb-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3b3eb-106">SYNTAX</span></span>

### <span data-ttu-id="3b3eb-107">ByResourceGroup (Default)</span><span class="sxs-lookup"><span data-stu-id="3b3eb-107">ByResourceGroup (Default)</span></span>
```
Update-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-ForceRestart] [-UpgradeReplicaSetCheckTimeoutSec <Int32>]
 [-FailureAction <FailureAction>] [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b3eb-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b3eb-108">ByResourceId</span></span>
```
Update-AzServiceFabricApplication [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>]
 [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-ForceRestart]
 [-UpgradeReplicaSetCheckTimeoutSec <Int32>] [-FailureAction <FailureAction>]
 [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b3eb-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3b3eb-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b3eb-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="3b3eb-110">DESCRIPTION</span></span>
<span data-ttu-id="3b3eb-111">To polecenie cmdlet służy do aktualizowania parametrów aplikacji i uaktualniania wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="3b3eb-112">Zaktualizowanie parametru spowoduje zmianę modelu tylko ARM stronie, tylko wtedy, gdy zostanie użyta wersja nowego typu, polecenie spowoduje wyzwolenie uaktualnienia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="3b3eb-113">Określona wersja typu powinna już zostać utworzona w klastrze przy użyciu **czcionki New-AzServiceFabricApplicationTypeVersion.**</span><span class="sxs-lookup"><span data-stu-id="3b3eb-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="3b3eb-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3b3eb-114">EXAMPLES</span></span>

### <span data-ttu-id="3b3eb-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3b3eb-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="3b3eb-116">W tym przykładzie rozpocznie się uaktualnianie aplikacji w celu zaktualizowania wersji typu do wersji "v2", która została utworzona za pomocą **new-azServiceFabricApplicationTypeVersion.**</span><span class="sxs-lookup"><span data-stu-id="3b3eb-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="3b3eb-117">Używane parametry aplikacji powinny być zdefiniowane w pliku manifestu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="3b3eb-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3b3eb-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="3b3eb-119">W tym przykładzie zaktualizuje się ograniczenie minimalnej i maksymalnej liczby węzłów aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="3b3eb-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3b3eb-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="3b3eb-121">W tym przykładzie rozpocznie się uaktualnianie aplikacji w celu zaktualizowania wersji typu do wersji "v2", a także zostaną wprowadzone pewne parametry zasad uaktualniania, które zostaną wprowadzone w bieżącym uaktualnieniu.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="3b3eb-122">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="3b3eb-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="3b3eb-123">Ten przykład aktualizuje parametry aplikacji, ale te zmiany będą obowiązywać tylko do następnego uaktualnienia do aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="3b3eb-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b3eb-124">PARAMETERS</span></span>

### <span data-ttu-id="3b3eb-125">-ApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="3b3eb-125">-ApplicationParameter</span></span>
<span data-ttu-id="3b3eb-126">Określ parametry aplikacji jako pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="3b3eb-127">Te parametry muszą istnieć w pliku manifestu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-127">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3b3eb-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="3b3eb-129">Określanie wersji typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="3b3eb-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-130">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3b3eb-130">-ClusterName</span></span>
<span data-ttu-id="3b3eb-131">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-131">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="3b3eb-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="3b3eb-133">Określa, czy ostrzeżenie dotyczące kondycji ma być potraktowane jako zdarzenie błędu podczas oceny kondycji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3eb-134">-DefaultProfile</span></span>
<span data-ttu-id="3b3eb-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b3eb-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="3b3eb-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="3b3eb-137">Określa maksymalną wartość procentową nieobojętych partycji na usługę dozwoloną przez zasady dotyczące kondycji domyślnego typu usługi do używania na monitorowanym uaktualnieniu.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="3b3eb-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="3b3eb-139">Określa maksymalną wartość procentową niesekonomii replik na usługę dozwoloną przez zasady dotyczące kondycji domyślnego typu usługi, które mają być monitorowane podczas uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="3b3eb-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="3b3eb-141">Określa maksymalną wartość procentową nieskompliowanych usług dozwolonych przez zasady dotyczące kondycji dla domyślnego typu usługi do użytku podczas monitorowanego uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="3b3eb-142">-FailureAction</span></span>
<span data-ttu-id="3b3eb-143">Określa akcję, która ma być podjęcia w przypadku niepowodzenia monitorowanego uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="3b3eb-144">Dopuszczalne wartości dla tego parametru to wycofywanie lub ręczne.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.FailureAction
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:
Accepted values: Rollback, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="3b3eb-145">-ForceRestart</span></span>
<span data-ttu-id="3b3eb-146">Wskazuje, że host usługi jest uruchamiany ponownie, nawet jeśli uaktualnienie dotyczy tylko konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="3b3eb-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="3b3eb-148">Określa czas trwania (w sekundach), po upływie którego usługa Service Fabric ponowne sprawdzi kondycję w przypadku niepowodzenia poprzedniej kontroli kondycji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-149">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="3b3eb-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="3b3eb-150">Określa czas (w sekundach), po których usługa Service Fabric czeka, aby sprawdzić, czy aplikacja jest stabilna, przed przejściem do domeny następnego uaktualnienia lub ukończeniem uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="3b3eb-151">Ten czas oczekiwania zapobiega niezauwazywaniu zmian kondycji bezpośrednio po zakończeniu kontroli kondycji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="3b3eb-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="3b3eb-153">Określa czas (w sekundach), po upływie których usługa Service Fabric będzie przeprowadzać wstępną sprawdzanie kondycji po zakończeniu uaktualniania w domenie uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b3eb-154">-InputObject</span></span>
<span data-ttu-id="3b3eb-155">Zasób aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-155">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="3b3eb-156">-MaximumNodeCount</span></span>
<span data-ttu-id="3b3eb-157">Określa maksymalną liczbę węzłów, w których ma być umieszczana aplikacja.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-157">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="3b3eb-158">-MinimumNodeCount</span></span>
<span data-ttu-id="3b3eb-159">Określa minimalną liczbę węzłów, w których usługa Service Fabric będzie rezerwować pojemność dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-160">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3b3eb-160">-Name</span></span>
<span data-ttu-id="3b3eb-161">Określanie nazwy aplikacji</span><span class="sxs-lookup"><span data-stu-id="3b3eb-161">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b3eb-162">-ResourceGroupName</span></span>
<span data-ttu-id="3b3eb-163">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b3eb-164">-ResourceId</span></span>
<span data-ttu-id="3b3eb-165">Arm ResourceId aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-165">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="3b3eb-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="3b3eb-167">Określa mapę zasad kondycji, które mają być używane dla różnych typów usług jako tabelę skrótów w następującym formacie: @ {"ServiceTypeName": "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="3b3eb-168">Na przykład: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span><span class="sxs-lookup"><span data-stu-id="3b3eb-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-169">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="3b3eb-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="3b3eb-170">Określa maksymalną wartość procentową wystąpień aplikacji wdrożonych w węzłach w klastrze, w przypadku których występuje stan błędu kondycji przed wystąpieniem błędu stanu kondycji aplikacji dla klastra.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="3b3eb-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="3b3eb-172">Określa maksymalny czas (w sekundach), przez który usługa Service Fabric pobiera uaktualnienie jednej domeny uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="3b3eb-173">Po upływie tego okresu uaktualnianie kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-173">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="3b3eb-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="3b3eb-175">Określa maksymalną ilość czasu, przez który usługa Service Fabric czeka na ponowne skonfigurowanie usługi w stanie bezpiecznym, jeśli nie jest jeszcze w stanie awaryjnym, zanim usługa Service Fabric przejdzie po uaktualnieniu.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="3b3eb-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="3b3eb-177">Określa maksymalny czas (w sekundach), przez który sieć Service Fabric zajmuje całe uaktualnienie.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="3b3eb-178">Po upływie tego okresu uaktualnianie kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-178">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3eb-179">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b3eb-179">-Confirm</span></span>
<span data-ttu-id="3b3eb-180">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b3eb-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b3eb-181">-WhatIf</span></span>
<span data-ttu-id="3b3eb-182">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b3eb-183">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b3eb-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3eb-184">CommonParameters</span></span>
<span data-ttu-id="3b3eb-185">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3eb-186">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b3eb-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3eb-187">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b3eb-187">INPUTS</span></span>

### <span data-ttu-id="3b3eb-188">System.String</span><span class="sxs-lookup"><span data-stu-id="3b3eb-188">System.String</span></span>

### <span data-ttu-id="3b3eb-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="3b3eb-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="3b3eb-190">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b3eb-190">OUTPUTS</span></span>

### <span data-ttu-id="3b3eb-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="3b3eb-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="3b3eb-192">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3b3eb-192">NOTES</span></span>

## <span data-ttu-id="3b3eb-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b3eb-193">RELATED LINKS</span></span>
