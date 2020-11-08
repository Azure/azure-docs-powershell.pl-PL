---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: e438b4f22bbd3d574788efd93d29aad0b2586767
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052687"
---
# <span data-ttu-id="a174b-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a174b-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="a174b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a174b-102">SYNOPSIS</span></span>
<span data-ttu-id="a174b-103">Aktualizowanie aplikacji sieci szkieletowej usługi.</span><span class="sxs-lookup"><span data-stu-id="a174b-103">Update a service fabric application.</span></span> <span data-ttu-id="a174b-104">Umożliwia to zaktualizowanie parametrów aplikacji i/lub uaktualnienie wersji typu aplikacji, która wyzwoli uaktualnienie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a174b-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

## <span data-ttu-id="a174b-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a174b-105">SYNTAX</span></span>

### <span data-ttu-id="a174b-106">ByResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a174b-106">ByResourceGroup (Default)</span></span>
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

### <span data-ttu-id="a174b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a174b-107">ByResourceId</span></span>
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

### <span data-ttu-id="a174b-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a174b-108">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a174b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a174b-109">DESCRIPTION</span></span>
<span data-ttu-id="a174b-110">Tego polecenia cmdlet można użyć w celu zaktualizowania parametrów aplikacji i uaktualnienia wersji typu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a174b-110">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="a174b-111">Aktualizacja parametru spowoduje zmianę modelu tylko po stronie ARM, tylko wtedy, gdy używana jest nowa wersja typu, polecenie wyzwoli uaktualnienie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a174b-111">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="a174b-112">Określona wersja typu powinna być już utworzona w klastrze przy użyciu polecenia **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="a174b-112">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="a174b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a174b-113">EXAMPLES</span></span>

### <span data-ttu-id="a174b-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a174b-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="a174b-115">W tym przykładzie rozpocznie się Uaktualnianie aplikacji w celu zaktualizowania wersji typu na wartość "v2", która została utworzona przy użyciu **nowego-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="a174b-115">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="a174b-116">Używane parametry aplikacji powinny być zdefiniowane w manifeście aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a174b-116">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="a174b-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a174b-117">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="a174b-118">W tym przykładzie zostanie zaktualizowana minimalna i Maksymalna liczba węzłów dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a174b-118">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="a174b-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a174b-119">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="a174b-120">W tym przykładzie rozpocznie się Uaktualnianie aplikacji w celu zaktualizowania wersji typu "v2", a także ustawienie kilku parametrów zasad uaktualniania, które zaczną obowiązywać od bieżącego uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="a174b-120">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="a174b-121">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="a174b-121">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="a174b-122">W tym przykładzie są aktualizowane parametry aplikacji, ale te zmiany zostaną wprowadzone tylko wtedy, gdy Następna wersja zostanie uaktualniona do aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a174b-122">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="a174b-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a174b-123">PARAMETERS</span></span>

### <span data-ttu-id="a174b-124">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="a174b-124">-ApplicationParameter</span></span>
<span data-ttu-id="a174b-125">Określ parametry aplikacji jako pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="a174b-125">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="a174b-126">Te parametry muszą istnieć w manifeście aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a174b-126">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="a174b-127">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a174b-127">-ApplicationTypeVersion</span></span>
<span data-ttu-id="a174b-128">Określanie wersji typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="a174b-128">Specify the application type version</span></span>

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

### <span data-ttu-id="a174b-129">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="a174b-129">-ClusterName</span></span>
<span data-ttu-id="a174b-130">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="a174b-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a174b-131">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="a174b-131">-ConsiderWarningAsError</span></span>
<span data-ttu-id="a174b-132">Wskazuje, czy zdarzenie dotyczące kondycji ma być traktowane jako zdarzenie błędu podczas oceny kondycji.</span><span class="sxs-lookup"><span data-stu-id="a174b-132">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

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

### <span data-ttu-id="a174b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a174b-133">-DefaultProfile</span></span>
<span data-ttu-id="a174b-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a174b-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a174b-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="a174b-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="a174b-136">Określa maksymalny procent partycji unhelthy na usługę, które są dozwolone przez zasady dotyczące kondycji dla domyślnego typu usługi, który ma być używany dla uaktualnienia monitorowanego.</span><span class="sxs-lookup"><span data-stu-id="a174b-136">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="a174b-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="a174b-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="a174b-138">Określa maksymalny procent replik unhelthy na usługę, które są dozwolone przez zasady dotyczące kondycji dla domyślnego typu usługi, który ma być używany dla uaktualnienia monitorowanego.</span><span class="sxs-lookup"><span data-stu-id="a174b-138">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="a174b-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="a174b-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="a174b-140">Określa maksymalny procent usług unhelthy dozwolonych przez zasady dotyczące kondycji dla domyślnego typu usługi, który ma być używany do monitorowania uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="a174b-140">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="a174b-141">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="a174b-141">-FailureAction</span></span>
<span data-ttu-id="a174b-142">Określa akcję, którą należy podjąć w przypadku niepowodzenia monitorowanego uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="a174b-142">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="a174b-143">Dopuszczalne wartości tego parametru to wycofywanie lub ręczne.</span><span class="sxs-lookup"><span data-stu-id="a174b-143">The acceptable values for this parameter are Rollback or Manual.</span></span>

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

### <span data-ttu-id="a174b-144">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="a174b-144">-ForceRestart</span></span>
<span data-ttu-id="a174b-145">Wskazuje, że host usługi zostanie ponownie uruchomiony, nawet jeśli uaktualnienie jest zmieniane tylko w konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="a174b-145">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

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

### <span data-ttu-id="a174b-146">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="a174b-146">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="a174b-147">Określa czas trwania w sekundach, po upływie którego usługa Fabric ponowi próbuje sprawdzić kondycję, jeśli poprzednie Sprawdzenie kondycji nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="a174b-147">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

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

### <span data-ttu-id="a174b-148">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="a174b-148">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="a174b-149">Określa czas trwania usługi Fabric (w sekundach) w celu sprawdzenia, czy aplikacja jest stabilna przed przejściem do następnej domeny uaktualnienia lub po zakończeniu uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="a174b-149">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="a174b-150">Ten czas trwania oczekiwania uniemożliwia niewykryte zmiany kondycji bezpośrednio po przeprowadzeniu kontroli kondycji.</span><span class="sxs-lookup"><span data-stu-id="a174b-150">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

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

### <span data-ttu-id="a174b-151">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="a174b-151">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="a174b-152">Określa czas trwania (w sekundach), po upływie którego usługa sieci szkieletowej będzie wykonywała pierwotne Sprawdzenie kondycji po zakończeniu uaktualniania domeny uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="a174b-152">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

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

### <span data-ttu-id="a174b-153">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a174b-153">-InputObject</span></span>
<span data-ttu-id="a174b-154">Zasób aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a174b-154">The application resource.</span></span>

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

### <span data-ttu-id="a174b-155">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="a174b-155">-MaximumNodeCount</span></span>
<span data-ttu-id="a174b-156">Określa maksymalną liczbę węzłów, na których ma zostać umieszczona aplikacja.</span><span class="sxs-lookup"><span data-stu-id="a174b-156">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="a174b-157">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="a174b-157">-MinimumNodeCount</span></span>
<span data-ttu-id="a174b-158">Określa minimalną liczbę węzłów, w których program Service Fabric rezerwuje wydajność dla tej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a174b-158">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="a174b-159">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a174b-159">-Name</span></span>
<span data-ttu-id="a174b-160">Określanie nazwy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a174b-160">Specify the name of the application</span></span>

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

### <span data-ttu-id="a174b-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a174b-161">-ResourceGroupName</span></span>
<span data-ttu-id="a174b-162">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a174b-162">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a174b-163">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a174b-163">-ResourceId</span></span>
<span data-ttu-id="a174b-164">Identyfikator zasobu ARM aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a174b-164">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="a174b-165">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="a174b-165">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="a174b-166">Określa mapę zasad dotyczących kondycji, które mają być używane dla różnych typów usług jako tabela skrótów, w następującym formacie: @ {"ServiceTypeName": "MaxPercentUnhealthyPartitionsPerService, MaxPercentUnhealthyReplicasPerPartition, MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="a174b-166">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="a174b-167">Na przykład: @ {"ServiceTypeName01" = "5; 10; 5"; "ServiceTypeName02" = "5, 5, 5"}</span><span class="sxs-lookup"><span data-stu-id="a174b-167">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

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

### <span data-ttu-id="a174b-168">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="a174b-168">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="a174b-169">Określa maksymalną wartość procentową wystąpień aplikacji wdrożonych w węzłach w klastrze, których stan kondycji jest błąd, zanim stan kondycji aplikacji dla klastra to błąd.</span><span class="sxs-lookup"><span data-stu-id="a174b-169">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

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

### <span data-ttu-id="a174b-170">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="a174b-170">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="a174b-171">Określa maksymalny czas (w sekundach), po którym usługa sieci szkieletowej przeprowadzi uaktualnienie jednej domeny uaktualnienia.</span><span class="sxs-lookup"><span data-stu-id="a174b-171">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="a174b-172">Po tym okresie uaktualnienie nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="a174b-172">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="a174b-173">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="a174b-173">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="a174b-174">Określa maksymalny czas oczekiwania usługi sieci szkieletowej na ponowne skonfigurowanie usługi do stanu bezpiecznego, jeśli nie jest jeszcze w stanie bezpiecznym, zanim usługa sieci szkielet będzie kontynuować uaktualnienie.</span><span class="sxs-lookup"><span data-stu-id="a174b-174">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

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

### <span data-ttu-id="a174b-175">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="a174b-175">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="a174b-176">Określa maksymalny czas (w sekundach), po jakim usługa sieci szkieletowej zajmie całe uaktualnienie.</span><span class="sxs-lookup"><span data-stu-id="a174b-176">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="a174b-177">Po tym okresie uaktualnienie nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="a174b-177">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="a174b-178">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a174b-178">-Confirm</span></span>
<span data-ttu-id="a174b-179">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a174b-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a174b-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a174b-180">-WhatIf</span></span>
<span data-ttu-id="a174b-181">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a174b-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a174b-182">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a174b-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a174b-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a174b-183">CommonParameters</span></span>
<span data-ttu-id="a174b-184">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a174b-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a174b-185">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a174b-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a174b-186">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a174b-186">INPUTS</span></span>

### <span data-ttu-id="a174b-187">System. String</span><span class="sxs-lookup"><span data-stu-id="a174b-187">System.String</span></span>

### <span data-ttu-id="a174b-188">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplication</span><span class="sxs-lookup"><span data-stu-id="a174b-188">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="a174b-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a174b-189">OUTPUTS</span></span>

### <span data-ttu-id="a174b-190">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplication</span><span class="sxs-lookup"><span data-stu-id="a174b-190">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="a174b-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a174b-191">NOTES</span></span>

## <span data-ttu-id="a174b-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a174b-192">RELATED LINKS</span></span>
