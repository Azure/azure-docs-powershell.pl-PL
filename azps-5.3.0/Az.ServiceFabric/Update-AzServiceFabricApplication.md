---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: e53ed405c9a03e7a9ec7a7c3694a44d513a1a1ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502775"
---
# <span data-ttu-id="d5074-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d5074-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="d5074-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5074-102">SYNOPSIS</span></span>
<span data-ttu-id="d5074-103">Aktualizowanie aplikacji sieci szkieletowej usługi.</span><span class="sxs-lookup"><span data-stu-id="d5074-103">Update a service fabric application.</span></span> <span data-ttu-id="d5074-104">Umożliwia to zaktualizowanie parametrów aplikacji i/lub uaktualnienie wersji typu aplikacji, która wyzwoli uaktualnienie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d5074-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="d5074-105">Obsługuje tylko aplikacje rozmieszczone w ARM.</span><span class="sxs-lookup"><span data-stu-id="d5074-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="d5074-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5074-106">SYNTAX</span></span>

### <span data-ttu-id="d5074-107">ByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d5074-107">ByResourceGroup (Default)</span></span>
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

### <span data-ttu-id="d5074-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d5074-108">ByResourceId</span></span>
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

### <span data-ttu-id="d5074-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d5074-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5074-110">Opis</span><span class="sxs-lookup"><span data-stu-id="d5074-110">DESCRIPTION</span></span>
<span data-ttu-id="d5074-111">Tego polecenia cmdlet można użyć w celu zaktualizowania parametrów aplikacji i uaktualnienia wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d5074-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="d5074-112">Aktualizacja parametru spowoduje zmianę modelu tylko po stronie ARM, tylko wtedy, gdy używana jest nowa wersja typu, polecenie wyzwoli uaktualnienie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d5074-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="d5074-113">Określona wersja typu powinna być już utworzona w klastrze przy użyciu polecenia **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="d5074-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="d5074-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5074-114">EXAMPLES</span></span>

### <span data-ttu-id="d5074-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d5074-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="d5074-116">W tym przykładzie rozpocznie się Uaktualnianie aplikacji w celu zaktualizowania wersji typu na wartość "v2", która została utworzona przy użyciu **nowego-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="d5074-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="d5074-117">Używane parametry aplikacji powinny być zdefiniowane w manifeście aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d5074-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="d5074-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d5074-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="d5074-119">W tym przykładzie zostanie zaktualizowana minimalna i Maksymalna liczba węzłów dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d5074-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="d5074-120">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d5074-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="d5074-121">W tym przykładzie rozpocznie się Uaktualnianie aplikacji w celu zaktualizowania wersji typu "v2", a także ustawienie kilku parametrów zasad uaktualniania, które zaczną obowiązywać od bieżącego uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="d5074-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="d5074-122">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="d5074-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="d5074-123">W tym przykładzie są aktualizowane parametry aplikacji, ale te zmiany zostaną wprowadzone tylko wtedy, gdy Następna wersja zostanie uaktualniona do aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d5074-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="d5074-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5074-124">PARAMETERS</span></span>

### <span data-ttu-id="d5074-125">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="d5074-125">-ApplicationParameter</span></span>
<span data-ttu-id="d5074-126">Określ parametry aplikacji jako pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="d5074-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="d5074-127">Te parametry muszą istnieć w manifeście aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d5074-127">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="d5074-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d5074-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="d5074-129">Określanie wersji typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="d5074-129">Specify the application type version</span></span>

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

### <span data-ttu-id="d5074-130">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="d5074-130">-ClusterName</span></span>
<span data-ttu-id="d5074-131">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d5074-131">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d5074-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="d5074-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="d5074-133">Wskazuje, czy zdarzenie dotyczące kondycji ma być traktowane jako zdarzenie błędu podczas oceny kondycji.</span><span class="sxs-lookup"><span data-stu-id="d5074-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

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

### <span data-ttu-id="d5074-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5074-134">-DefaultProfile</span></span>
<span data-ttu-id="d5074-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5074-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5074-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="d5074-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="d5074-137">Określa maksymalny procent partycji unhelthy na usługę, które są dozwolone przez zasady dotyczące kondycji dla domyślnego typu usługi, który ma być używany dla uaktualnienia monitorowanego.</span><span class="sxs-lookup"><span data-stu-id="d5074-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="d5074-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="d5074-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="d5074-139">Określa maksymalny procent replik unhelthy na usługę, które są dozwolone przez zasady dotyczące kondycji dla domyślnego typu usługi, który ma być używany dla uaktualnienia monitorowanego.</span><span class="sxs-lookup"><span data-stu-id="d5074-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="d5074-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="d5074-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="d5074-141">Określa maksymalny procent usług unhelthy dozwolonych przez zasady dotyczące kondycji dla domyślnego typu usługi, który ma być używany do monitorowania uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="d5074-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="d5074-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="d5074-142">-FailureAction</span></span>
<span data-ttu-id="d5074-143">Określa akcję, którą należy podjąć w przypadku niepowodzenia monitorowanego uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="d5074-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="d5074-144">Dopuszczalne wartości tego parametru to wycofywanie lub ręczne.</span><span class="sxs-lookup"><span data-stu-id="d5074-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

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

### <span data-ttu-id="d5074-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="d5074-145">-ForceRestart</span></span>
<span data-ttu-id="d5074-146">Wskazuje, że host usługi zostanie ponownie uruchomiony, nawet jeśli uaktualnienie jest zmieniane tylko w konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="d5074-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

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

### <span data-ttu-id="d5074-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d5074-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="d5074-148">Określa czas trwania w sekundach, po upływie którego usługa Fabric ponowi próbuje sprawdzić kondycję, jeśli poprzednie Sprawdzenie kondycji nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="d5074-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

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

### <span data-ttu-id="d5074-149">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="d5074-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="d5074-150">Określa czas trwania usługi Fabric (w sekundach) w celu sprawdzenia, czy aplikacja jest stabilna przed przejściem do następnej domeny uaktualnienia lub po zakończeniu uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="d5074-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="d5074-151">Ten czas trwania oczekiwania uniemożliwia niewykryte zmiany kondycji bezpośrednio po przeprowadzeniu kontroli kondycji.</span><span class="sxs-lookup"><span data-stu-id="d5074-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

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

### <span data-ttu-id="d5074-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="d5074-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="d5074-153">Określa czas trwania (w sekundach), po upływie którego usługa sieci szkieletowej będzie wykonywała pierwotne Sprawdzenie kondycji po zakończeniu uaktualniania domeny uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="d5074-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

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

### <span data-ttu-id="d5074-154">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d5074-154">-InputObject</span></span>
<span data-ttu-id="d5074-155">Zasób aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d5074-155">The application resource.</span></span>

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

### <span data-ttu-id="d5074-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="d5074-156">-MaximumNodeCount</span></span>
<span data-ttu-id="d5074-157">Określa maksymalną liczbę węzłów, na których ma zostać umieszczona aplikacja.</span><span class="sxs-lookup"><span data-stu-id="d5074-157">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="d5074-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="d5074-158">-MinimumNodeCount</span></span>
<span data-ttu-id="d5074-159">Określa minimalną liczbę węzłów, w których program Service Fabric rezerwuje wydajność dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d5074-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="d5074-160">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d5074-160">-Name</span></span>
<span data-ttu-id="d5074-161">Określanie nazwy aplikacji</span><span class="sxs-lookup"><span data-stu-id="d5074-161">Specify the name of the application</span></span>

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

### <span data-ttu-id="d5074-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5074-162">-ResourceGroupName</span></span>
<span data-ttu-id="d5074-163">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d5074-163">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d5074-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5074-164">-ResourceId</span></span>
<span data-ttu-id="d5074-165">Identyfikator zasobu ARM aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d5074-165">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="d5074-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="d5074-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="d5074-167">Określa mapę zasad dotyczących kondycji, które mają być używane dla różnych typów usług jako tabela skrótów, w następującym formacie: @ {"ServiceTypeName": "MaxPercentUnhealthyPartitionsPerService, MaxPercentUnhealthyReplicasPerPartition, MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="d5074-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="d5074-168">Na przykład: @ {"ServiceTypeName01" = "5; 10; 5"; "ServiceTypeName02" = "5, 5, 5"}</span><span class="sxs-lookup"><span data-stu-id="d5074-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

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

### <span data-ttu-id="d5074-169">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="d5074-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="d5074-170">Określa maksymalną wartość procentową wystąpień aplikacji wdrożonych w węzłach w klastrze, których stan kondycji jest błąd, zanim stan kondycji aplikacji dla klastra to błąd.</span><span class="sxs-lookup"><span data-stu-id="d5074-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

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

### <span data-ttu-id="d5074-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d5074-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="d5074-172">Określa maksymalny czas (w sekundach), po którym usługa sieci szkieletowej przeprowadzi uaktualnienie jednej domeny uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="d5074-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="d5074-173">Po tym okresie uaktualnienie nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="d5074-173">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="d5074-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d5074-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="d5074-175">Określa maksymalny czas oczekiwania usługi sieci szkieletowej na ponowne skonfigurowanie usługi do stanu bezpiecznego, jeśli nie jest jeszcze w stanie bezpiecznym, zanim usługa sieci szkielet będzie kontynuować uaktualnienie.</span><span class="sxs-lookup"><span data-stu-id="d5074-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

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

### <span data-ttu-id="d5074-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="d5074-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="d5074-177">Określa maksymalny czas (w sekundach), po jakim usługa sieci szkieletowej zajmie całe uaktualnienie.</span><span class="sxs-lookup"><span data-stu-id="d5074-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="d5074-178">Po tym okresie uaktualnienie nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="d5074-178">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="d5074-179">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d5074-179">-Confirm</span></span>
<span data-ttu-id="d5074-180">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5074-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5074-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5074-181">-WhatIf</span></span>
<span data-ttu-id="d5074-182">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5074-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5074-183">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d5074-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5074-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5074-184">CommonParameters</span></span>
<span data-ttu-id="d5074-185">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5074-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5074-186">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5074-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5074-187">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5074-187">INPUTS</span></span>

### <span data-ttu-id="d5074-188">System. String</span><span class="sxs-lookup"><span data-stu-id="d5074-188">System.String</span></span>

### <span data-ttu-id="d5074-189">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplication</span><span class="sxs-lookup"><span data-stu-id="d5074-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="d5074-190">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5074-190">OUTPUTS</span></span>

### <span data-ttu-id="d5074-191">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplication</span><span class="sxs-lookup"><span data-stu-id="d5074-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="d5074-192">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5074-192">NOTES</span></span>

## <span data-ttu-id="d5074-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5074-193">RELATED LINKS</span></span>
