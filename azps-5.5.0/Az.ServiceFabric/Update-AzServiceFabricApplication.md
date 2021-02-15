---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: e53ed405c9a03e7a9ec7a7c3694a44d513a1a1ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189082"
---
# <span data-ttu-id="d9fba-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d9fba-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="d9fba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9fba-102">SYNOPSIS</span></span>
<span data-ttu-id="d9fba-103">Aktualizowanie aplikacji do obsługi szkieletów usług.</span><span class="sxs-lookup"><span data-stu-id="d9fba-103">Update a service fabric application.</span></span> <span data-ttu-id="d9fba-104">Pozwala to zaktualizować parametry aplikacji i/lub uaktualnić wersję typu aplikacji, co spowoduje uruchomienie uaktualnienia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="d9fba-105">Obsługuje tylko ARM wdrożonych aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="d9fba-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9fba-106">SYNTAX</span></span>

### <span data-ttu-id="d9fba-107">ByResourceGroup (Default)</span><span class="sxs-lookup"><span data-stu-id="d9fba-107">ByResourceGroup (Default)</span></span>
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

### <span data-ttu-id="d9fba-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9fba-108">ByResourceId</span></span>
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

### <span data-ttu-id="d9fba-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9fba-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9fba-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9fba-110">DESCRIPTION</span></span>
<span data-ttu-id="d9fba-111">To polecenie cmdlet służy do aktualizowania parametrów aplikacji i uaktualniania wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="d9fba-112">Zaktualizowanie parametru spowoduje tylko zmianę modelu ARM stronie, tylko wtedy, gdy zostanie użyta wersja nowego typu, polecenie spowoduje wyzwolenie uaktualnienia aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="d9fba-113">Określona wersja typu powinna już zostać utworzona w klastrze przy użyciu **czcionki New-AzServiceFabricApplicationTypeVersion.**</span><span class="sxs-lookup"><span data-stu-id="d9fba-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="d9fba-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9fba-114">EXAMPLES</span></span>

### <span data-ttu-id="d9fba-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9fba-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="d9fba-116">W tym przykładzie rozpocznie się uaktualnianie aplikacji w celu zaktualizowania wersji typu do wersji "v2", która została utworzona za pomocą **new-AzServiceFabricApplicationTypeVersion.**</span><span class="sxs-lookup"><span data-stu-id="d9fba-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="d9fba-117">Używane parametry aplikacji powinny być zdefiniowane w pliku manifestu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="d9fba-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d9fba-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="d9fba-119">W tym przykładzie zaktualizuje się ograniczenie minimalnej i maksymalnej liczby węzłów dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="d9fba-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d9fba-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="d9fba-121">W tym przykładzie rozpocznie się uaktualnianie aplikacji w celu zaktualizowania wersji typu do wersji "v2", a także zostaną wprowadzone pewne parametry zasad uaktualniania, które zostaną wprowadzone w bieżącym uaktualnieniu.</span><span class="sxs-lookup"><span data-stu-id="d9fba-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="d9fba-122">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="d9fba-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="d9fba-123">W tym przykładzie parametry aplikacji są aktualizowane, ale te zmiany będą obowiązywać tylko do następnego uaktualnienia do aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="d9fba-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9fba-124">PARAMETERS</span></span>

### <span data-ttu-id="d9fba-125">-ApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="d9fba-125">-ApplicationParameter</span></span>
<span data-ttu-id="d9fba-126">Określ parametry aplikacji jako pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="d9fba-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="d9fba-127">Te parametry muszą istnieć w pliku manifestu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-127">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="d9fba-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d9fba-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="d9fba-129">Określanie wersji typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="d9fba-129">Specify the application type version</span></span>

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

### <span data-ttu-id="d9fba-130">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d9fba-130">-ClusterName</span></span>
<span data-ttu-id="d9fba-131">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d9fba-131">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d9fba-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="d9fba-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="d9fba-133">Określa, czy ostrzeżenie dotyczące kondycji ma być potraktowane jak zdarzenie błędu podczas oceny kondycji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

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

### <span data-ttu-id="d9fba-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9fba-134">-DefaultProfile</span></span>
<span data-ttu-id="d9fba-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9fba-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9fba-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="d9fba-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="d9fba-137">Określa maksymalną wartość procentową nieobojętych partycji na usługę dozwoloną przez zasady dotyczące kondycji domyślnego typu usługi, które mają być monitorowane podczas uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="d9fba-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="d9fba-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="d9fba-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="d9fba-139">Określa maksymalną wartość procentową niesekonomii replik na usługę dozwoloną przez zasady dotyczące kondycji domyślnego typu usługi, które mają być monitorowane podczas uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="d9fba-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="d9fba-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="d9fba-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="d9fba-141">Określa maksymalną wartość procentową nieskompliowanych usług dozwolonych przez zasady dotyczące kondycji dla domyślnego typu usługi do użytku podczas monitorowanego uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="d9fba-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="d9fba-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="d9fba-142">-FailureAction</span></span>
<span data-ttu-id="d9fba-143">Określa akcję, która ma być podjąć w przypadku niepowodzenia monitorowanego uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="d9fba-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="d9fba-144">Dopuszczalne wartości dla tego parametru to wycofywanie lub ręczne.</span><span class="sxs-lookup"><span data-stu-id="d9fba-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

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

### <span data-ttu-id="d9fba-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="d9fba-145">-ForceRestart</span></span>
<span data-ttu-id="d9fba-146">Wskazuje, że host usługi jest uruchamiany ponownie, nawet jeśli uaktualnienie dotyczy tylko konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

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

### <span data-ttu-id="d9fba-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d9fba-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="d9fba-148">Określa czas trwania (w sekundach), po upływie którego usługa Service Fabric ponowne sprawdzi kondycję w przypadku niepowodzenia poprzedniego sprawdzania kondycji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

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

### <span data-ttu-id="d9fba-149">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="d9fba-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="d9fba-150">Określa czas (w sekundach), po których usługa Service Fabric czeka, aby sprawdzić, czy aplikacja jest stabilna, przed przejściem do następnej domeny uaktualnienia lub ukończeniem uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="d9fba-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="d9fba-151">Ten czas oczekiwania zapobiega niezauwazywaniu zmian kondycji bezpośrednio po zakończeniu kontroli kondycji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

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

### <span data-ttu-id="d9fba-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="d9fba-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="d9fba-153">Określa czas (w sekundach), po upływie których usługa Service Fabric będzie przeprowadzać wstępną sprawdzanie kondycji po zakończeniu uaktualniania w domenie uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="d9fba-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

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

### <span data-ttu-id="d9fba-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9fba-154">-InputObject</span></span>
<span data-ttu-id="d9fba-155">Zasób aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-155">The application resource.</span></span>

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

### <span data-ttu-id="d9fba-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="d9fba-156">-MaximumNodeCount</span></span>
<span data-ttu-id="d9fba-157">Określa maksymalną liczbę węzłów, w których ma być umieszczana aplikacja.</span><span class="sxs-lookup"><span data-stu-id="d9fba-157">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="d9fba-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="d9fba-158">-MinimumNodeCount</span></span>
<span data-ttu-id="d9fba-159">Określa minimalną liczbę węzłów, w których usługa Service Fabric będzie rezerwować pojemność dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="d9fba-160">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d9fba-160">-Name</span></span>
<span data-ttu-id="d9fba-161">Określanie nazwy aplikacji</span><span class="sxs-lookup"><span data-stu-id="d9fba-161">Specify the name of the application</span></span>

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

### <span data-ttu-id="d9fba-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9fba-162">-ResourceGroupName</span></span>
<span data-ttu-id="d9fba-163">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9fba-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d9fba-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9fba-164">-ResourceId</span></span>
<span data-ttu-id="d9fba-165">Arm ResourceId aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9fba-165">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="d9fba-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="d9fba-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="d9fba-167">Określa mapę zasad kondycji, które mają być używane dla różnych typów usług jako tabelę skrótów w następującym formacie: @ {"ServiceTypeName": "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="d9fba-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="d9fba-168">Na przykład: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span><span class="sxs-lookup"><span data-stu-id="d9fba-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

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

### <span data-ttu-id="d9fba-169">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="d9fba-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="d9fba-170">Określa maksymalną wartość procentową wystąpień aplikacji wdrożonych w węzłach w klastrze, w przypadku których występuje stan błędu kondycji przed wystąpieniem błędu stanu kondycji aplikacji dla klastra.</span><span class="sxs-lookup"><span data-stu-id="d9fba-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

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

### <span data-ttu-id="d9fba-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d9fba-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="d9fba-172">Określa maksymalny czas (w sekundach), przez który usługa Service Fabric pobiera uaktualnienie jednej domeny uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="d9fba-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="d9fba-173">Po upływie tego okresu uaktualnianie kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d9fba-173">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="d9fba-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d9fba-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="d9fba-175">Określa maksymalną ilość czasu, przez który usługa Service Fabric czeka na ponowne skonfigurowanie usługi do stanu bezpiecznego, jeśli nie jest jeszcze w stanie awaryjnym, zanim usługa Service Fabric przejdzie po uaktualnieniu.</span><span class="sxs-lookup"><span data-stu-id="d9fba-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

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

### <span data-ttu-id="d9fba-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d9fba-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="d9fba-177">Określa maksymalny czas (w sekundach), przez który sieć Service Fabric zajmuje całe uaktualnienie.</span><span class="sxs-lookup"><span data-stu-id="d9fba-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="d9fba-178">Po upływie tego okresu uaktualnianie kończy się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d9fba-178">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="d9fba-179">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9fba-179">-Confirm</span></span>
<span data-ttu-id="d9fba-180">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9fba-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9fba-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9fba-181">-WhatIf</span></span>
<span data-ttu-id="d9fba-182">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9fba-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9fba-183">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d9fba-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9fba-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9fba-184">CommonParameters</span></span>
<span data-ttu-id="d9fba-185">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9fba-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9fba-186">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9fba-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9fba-187">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9fba-187">INPUTS</span></span>

### <span data-ttu-id="d9fba-188">System.String</span><span class="sxs-lookup"><span data-stu-id="d9fba-188">System.String</span></span>

### <span data-ttu-id="d9fba-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="d9fba-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="d9fba-190">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9fba-190">OUTPUTS</span></span>

### <span data-ttu-id="d9fba-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="d9fba-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="d9fba-192">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9fba-192">NOTES</span></span>

## <span data-ttu-id="d9fba-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9fba-193">RELATED LINKS</span></span>
