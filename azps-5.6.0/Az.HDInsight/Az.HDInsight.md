---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: ec924f7424d2b522e6bbd9ce1db51e8c920ec663
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990130"
---
# <span data-ttu-id="1b1f5-101">Moduł Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="1b1f5-101">Az.HDInsight Module</span></span>
## <span data-ttu-id="1b1f5-102">Opis</span><span class="sxs-lookup"><span data-stu-id="1b1f5-102">Description</span></span>
<span data-ttu-id="1b1f5-103">Tematy w tej sekcji dokumentu zawierają polecenia cmdlet programu Azure PowerShell dla usługi HdInsight platformy Microsoft Azure w ramach usługi Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="1b1f5-103">The topics in this section document the Azure PowerShell cmdlets for Microsoft Azure HDInsight in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="1b1f5-104">Te polecenia cmdlet są używane do zarządzania klastrami HDInsight i uruchomionymi na nich zadaniami.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-104">These cmdlets are used to manage HDInsight clusters and the jobs that run on them.</span></span> <span data-ttu-id="1b1f5-105">Polecenia cmdlet istnieją w przestrzeni nazw Microsoft.Azure.Commands.HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-105">The cmdlets exist in the Microsoft.Azure.Commands.HDInsight namespace.</span></span>

## <span data-ttu-id="1b1f5-106">Az.HDInsight Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1b1f5-106">Az.HDInsight Cmdlets</span></span>
### [<span data-ttu-id="1b1f5-107">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="1b1f5-107">Add-AzHDInsightClusterIdentity</span></span>](Add-AzHDInsightClusterIdentity.md)
<span data-ttu-id="1b1f5-108">Dodaje tożsamość klastra do obiektu konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-108">Adds a cluster identity to a cluster configuration object.</span></span>

### [<span data-ttu-id="1b1f5-109">Add-AzHDInsightComponentVersion</span><span class="sxs-lookup"><span data-stu-id="1b1f5-109">Add-AzHDInsightComponentVersion</span></span>](Add-AzHDInsightComponentVersion.md)
<span data-ttu-id="1b1f5-110">Dodaje wersję dla usługi uruchomionej w klastrze do obiektu konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-110">Adds a version for a service running in a cluster to a cluster configuration object.</span></span>

### [<span data-ttu-id="1b1f5-111">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="1b1f5-111">Add-AzHDInsightConfigValue</span></span>](Add-AzHDInsightConfigValue.md)
<span data-ttu-id="1b1f5-112">Powoduje dodanie dostosowania wartości konfiguracji usługi Hadoop i/lub dostosowania biblioteki udostępnionej w użytku w obiekcie konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-112">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

### [<span data-ttu-id="1b1f5-113">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="1b1f5-113">Add-AzHDInsightMetastore</span></span>](Add-AzHDInsightMetastore.md)
<span data-ttu-id="1b1f5-114">Dodaje bazę danych SQL, która będzie pełnić funkcję metastore Oozie lub Gałąź do obiektu konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-114">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

### [<span data-ttu-id="1b1f5-115">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="1b1f5-115">Add-AzHDInsightScriptAction</span></span>](Add-AzHDInsightScriptAction.md)
<span data-ttu-id="1b1f5-116">Dodaje akcję skryptu do obiektu konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-116">Adds a script action to a cluster configuration object.</span></span>

### [<span data-ttu-id="1b1f5-117">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="1b1f5-117">Add-AzHDInsightSecurityProfile</span></span>](Add-AzHDInsightSecurityProfile.md)
<span data-ttu-id="1b1f5-118">Dodaje profil zabezpieczeń do obiektu konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-118">Adds a security profile to a cluster configuration object.</span></span>

### [<span data-ttu-id="1b1f5-119">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="1b1f5-119">Add-AzHDInsightStorage</span></span>](Add-AzHDInsightStorage.md)
<span data-ttu-id="1b1f5-120">Dodaje klucz magazynu platformy Azure do obiektu konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-120">Adds an Azure Storage key to a cluster configuration object.</span></span>

### [<span data-ttu-id="1b1f5-121">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="1b1f5-121">Disable-AzHDInsightMonitoring</span></span>](Disable-AzHDInsightMonitoring.md)
<span data-ttu-id="1b1f5-122">Wyłącza monitorowanie w klastrze HDInsight i odpowiednie dzienniki przestaną przepływać do obszaru roboczego monitorowania określonego podczas włączania.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-122">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="1b1f5-123">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="1b1f5-123">Enable-AzHDInsightMonitoring</span></span>](Enable-AzHDInsightMonitoring.md)
<span data-ttu-id="1b1f5-124">Umożliwia monitorowanie w klastrze HDInsight, a odpowiednie dzienniki będą wysyłane do obszaru roboczego monitorowania określonego podczas włączania.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-124">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

### [<span data-ttu-id="1b1f5-125">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1b1f5-125">Get-AzHDInsightCluster</span></span>](Get-AzHDInsightCluster.md)
<span data-ttu-id="1b1f5-126">Pobiera i wyświetla wszystkie klastry usługi Azure HDInsight skojarzone z bieżącą subskrypcją lub określoną grupą zasobów albo pobiera określony klaster.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-126">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

### [<span data-ttu-id="1b1f5-127">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b1f5-127">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>](Get-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="1b1f5-128">Pobiera konfigurację automatycznego skalowania klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-128">Gets the autoscale configuration of HDInsight cluster.</span></span>

### [<span data-ttu-id="1b1f5-129">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="1b1f5-129">Get-AzHDInsightHost</span></span>](Get-AzHDInsightHost.md)
<span data-ttu-id="1b1f5-130">Wyświetla listę hostów klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-130">Lists the hosts of the HDInsight cluster.</span></span>

### [<span data-ttu-id="1b1f5-131">Get-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1b1f5-131">Get-AzHDInsightJob</span></span>](Get-AzHDInsightJob.md)
<span data-ttu-id="1b1f5-132">Pobiera listę zadań z klastra i wyświetla je w odwrotnej kolejności chronologicznej lub pobiera określone zadanie.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-132">Gets the list of jobs from a cluster and lists them in reverse chronological order, or retrieves a specific job.</span></span>

### [<span data-ttu-id="1b1f5-133">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="1b1f5-133">Get-AzHDInsightJobOutput</span></span>](Get-AzHDInsightJobOutput.md)
<span data-ttu-id="1b1f5-134">Pobiera dane wyjściowe dziennika dla zadania z konta magazynu skojarzonego z określonym klastrem.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-134">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

### [<span data-ttu-id="1b1f5-135">Get-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="1b1f5-135">Get-AzHDInsightMonitoring</span></span>](Get-AzHDInsightMonitoring.md)
<span data-ttu-id="1b1f5-136">Pobiera stan instalacji monitorowania w klastrze.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-136">Gets the status of monitoring installation on the cluster.</span></span>

### [<span data-ttu-id="1b1f5-137">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="1b1f5-137">Get-AzHDInsightPersistedScriptAction</span></span>](Get-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="1b1f5-138">Pobiera utrwalone akcje skryptu dla klastra i wyświetla je w porządku chronologicznym lub pobiera szczegółowe informacje dotyczące określonej, utrwalonej akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-138">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

### [<span data-ttu-id="1b1f5-139">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="1b1f5-139">Get-AzHDInsightProperty</span></span>](Get-AzHDInsightProperty.md)
<span data-ttu-id="1b1f5-140">Pobiera właściwości usługi HDInsight, takie jak dostępne lokalizacje i pojemność.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-140">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

### [<span data-ttu-id="1b1f5-141">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="1b1f5-141">Get-AzHDInsightScriptActionHistory</span></span>](Get-AzHDInsightScriptActionHistory.md)
<span data-ttu-id="1b1f5-142">Pobiera historię akcji skryptu dla klastra i wyświetla ją w odwrotnej kolejności chronologicznej lub zawiera szczegóły wcześniej wykonanej akcji skryptu.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-142">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

### [<span data-ttu-id="1b1f5-143">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="1b1f5-143">Invoke-AzHDInsightHiveJob</span></span>](Invoke-AzHDInsightHiveJob.md)
<span data-ttu-id="1b1f5-144">Przesyła zapytanie Do klastra HDInsight i pobiera wyniki zapytania w jednej operacji.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-144">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

### [<span data-ttu-id="1b1f5-145">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1b1f5-145">New-AzHDInsightCluster</span></span>](New-AzHDInsightCluster.md)
<span data-ttu-id="1b1f5-146">Tworzy klaster usługi Azure HDInsight w określonej grupie zasobów dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-146">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

### [<span data-ttu-id="1b1f5-147">New-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b1f5-147">New-AzHDInsightClusterAutoscaleConfiguration</span></span>](New-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="1b1f5-148">Tworzy nietrwale obiekt opisujący konfigurację automatycznego skalowania klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-148">Creates a non-persisted object that describes the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="1b1f5-149">New-AzHDInsightClusterAutoscaleScheduleCondition</span><span class="sxs-lookup"><span data-stu-id="1b1f5-149">New-AzHDInsightClusterAutoscaleScheduleCondition</span></span>](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
<span data-ttu-id="1b1f5-150">Tworzy warunek autoskalowania oparty na harmonogramie.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-150">Creates Schedule-based autoscale condition.</span></span>

### [<span data-ttu-id="1b1f5-151">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="1b1f5-151">New-AzHDInsightClusterConfig</span></span>](New-AzHDInsightClusterConfig.md)
<span data-ttu-id="1b1f5-152">Tworzy nietrwale obiekt konfiguracji klastrów opisujący konfigurację klastrów HDInsight platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-152">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

### [<span data-ttu-id="1b1f5-153">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1b1f5-153">New-AzHDInsightHiveJobDefinition</span></span>](New-AzHDInsightHiveJobDefinition.md)
<span data-ttu-id="1b1f5-154">Tworzy obiekt zadania Gałąź.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-154">Creates a Hive job object.</span></span>

### [<span data-ttu-id="1b1f5-155">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1b1f5-155">New-AzHDInsightMapReduceJobDefinition</span></span>](New-AzHDInsightMapReduceJobDefinition.md)
<span data-ttu-id="1b1f5-156">Tworzy obiekt zadania MapReduce.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-156">Creates a MapReduce job object.</span></span>

### [<span data-ttu-id="1b1f5-157">New-AzHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1b1f5-157">New-AzHDInsightPigJobDefinition</span></span>](New-AzHDInsightPigJobDefinition.md)
<span data-ttu-id="1b1f5-158">Tworzy obiekt zadania Świnka.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-158">Creates a Pig job object.</span></span>

### [<span data-ttu-id="1b1f5-159">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1b1f5-159">New-AzHDInsightSqoopJobDefinition</span></span>](New-AzHDInsightSqoopJobDefinition.md)
<span data-ttu-id="1b1f5-160">Tworzy obiekt zadania Sqoop.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-160">Creates a Sqoop job object.</span></span>

### [<span data-ttu-id="1b1f5-161">New-AzHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1b1f5-161">New-AzHDInsightStreamingMapReduceJobDefinition</span></span>](New-AzHDInsightStreamingMapReduceJobDefinition.md)
<span data-ttu-id="1b1f5-162">Tworzy obiekt zadania MapReduce przesyłania strumieniowego.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-162">Creates a Streaming MapReduce job object.</span></span>

### [<span data-ttu-id="1b1f5-163">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1b1f5-163">Remove-AzHDInsightCluster</span></span>](Remove-AzHDInsightCluster.md)
<span data-ttu-id="1b1f5-164">Usuwa określony klaster USŁUGI HDInsight z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-164">Removes the specified HDInsight cluster from the current subscription.</span></span>

### [<span data-ttu-id="1b1f5-165">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b1f5-165">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="1b1f5-166">Usuwa konfigurację automatycznego skalowania klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-166">Removes the autoscale configuration of the HDInsight cluster.</span></span>

### [<span data-ttu-id="1b1f5-167">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="1b1f5-167">Remove-AzHDInsightPersistedScriptAction</span></span>](Remove-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="1b1f5-168">Usuwa trwałą akcję skryptu z klastra HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-168">Removes an persisted script action from an HDInsight cluster.</span></span>

### [<span data-ttu-id="1b1f5-169">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="1b1f5-169">Restart-AzHDInsightHost</span></span>](Restart-AzHDInsightHost.md)
<span data-ttu-id="1b1f5-170">Powoduje ponowne uruchomienie określonych hostów klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-170">Restarts the specific hosts of HDInsight cluster.</span></span>

### [<span data-ttu-id="1b1f5-171">Set-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b1f5-171">Set-AzHDInsightClusterAutoscaleConfiguration</span></span>](Set-AzHDInsightClusterAutoscaleConfiguration.md)
<span data-ttu-id="1b1f5-172">Ustawia konfigurację automatycznego skalowania klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-172">Sets the autoscale configuration of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="1b1f5-173">Set-AzHDInsightClusterCryptEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1b1f5-173">Set-AzHDInsightClusterDiskEncryptionKey</span></span>](Set-AzHDInsightClusterDiskEncryptionKey.md)
<span data-ttu-id="1b1f5-174">Obraca klucz szyfrowania dysku określonego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-174">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

### [<span data-ttu-id="1b1f5-175">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="1b1f5-175">Set-AzHDInsightClusterSize</span></span>](Set-AzHDInsightClusterSize.md)
<span data-ttu-id="1b1f5-176">Ustawia liczbę węzłów pracownik w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-176">Sets the number of Worker nodes in a specified cluster.</span></span>

### [<span data-ttu-id="1b1f5-177">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="1b1f5-177">Set-AzHDInsightDefaultStorage</span></span>](Set-AzHDInsightDefaultStorage.md)
<span data-ttu-id="1b1f5-178">Ustawia domyślne ustawienie konta magazynu w obiekcie konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-178">Sets the default Storage account setting in a cluster configuration object.</span></span>

### [<span data-ttu-id="1b1f5-179">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="1b1f5-179">Set-AzHDInsightGatewayCredential</span></span>](Set-AzHDInsightGatewayCredential.md)
<span data-ttu-id="1b1f5-180">Ustawia poświadczenia HTTP bramy dla klastru usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-180">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="1b1f5-181">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="1b1f5-181">Set-AzHDInsightPersistedScriptAction</span></span>](Set-AzHDInsightPersistedScriptAction.md)
<span data-ttu-id="1b1f5-182">Ustawia wcześniej wykonaną akcję skryptu jako trwałą akcję skryptu.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-182">Sets a previously executed script action to be a persisted script action.</span></span>

### [<span data-ttu-id="1b1f5-183">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1b1f5-183">Start-AzHDInsightJob</span></span>](Start-AzHDInsightJob.md)
<span data-ttu-id="1b1f5-184">Uruchamia zdefiniowane zadanie usługi Azure HDInsight w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-184">Starts a defined Azure HDInsight job on a specified cluster.</span></span>

### [<span data-ttu-id="1b1f5-185">Stop-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1b1f5-185">Stop-AzHDInsightJob</span></span>](Stop-AzHDInsightJob.md)
<span data-ttu-id="1b1f5-186">Zatrzymuje określone zadanie uruchomione w klastrze.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-186">Stops a specified running job on a cluster.</span></span>

### [<span data-ttu-id="1b1f5-187">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="1b1f5-187">Submit-AzHDInsightScriptAction</span></span>](Submit-AzHDInsightScriptAction.md)
<span data-ttu-id="1b1f5-188">Przesyła nową akcję skryptu do klastrów usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-188">Submits a new script action to an Azure HDInsight cluster.</span></span>

### [<span data-ttu-id="1b1f5-189">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1b1f5-189">Use-AzHDInsightCluster</span></span>](Use-AzHDInsightCluster.md)
<span data-ttu-id="1b1f5-190">Wybiera klaster, który ma być używany z Invoke-RmAzureHDInsightHiveJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-190">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

### [<span data-ttu-id="1b1f5-191">Wait-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1b1f5-191">Wait-AzHDInsightJob</span></span>](Wait-AzHDInsightJob.md)
<span data-ttu-id="1b1f5-192">Czeka na ukończenie lub niepowodzenie określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="1b1f5-192">Waits for the completion or failure of a specified job.</span></span>

