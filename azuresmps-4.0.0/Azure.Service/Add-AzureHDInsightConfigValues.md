---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054694"
---
# <span data-ttu-id="043fc-101">Add-AzureHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="043fc-101">Add-AzureHDInsightConfigValues</span></span>

## <span data-ttu-id="043fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="043fc-102">SYNOPSIS</span></span>
<span data-ttu-id="043fc-103">Umożliwia dodanie dostosowania wartości konfiguracji usługi Hadoop lub dostosowania udostępnionej biblioteki gałęzi do konfiguracji klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="043fc-103">Adds a Hadoop configuration value customization or a Hive shared library customization to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="043fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="043fc-104">SYNTAX</span></span>

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="043fc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="043fc-105">DESCRIPTION</span></span>
<span data-ttu-id="043fc-106">Ta wersja usługi Azure PowerShell HDInsight jest przestarzała.</span><span class="sxs-lookup"><span data-stu-id="043fc-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="043fc-107">Te polecenia cmdlet zostaną usunięte z 1 stycznia 2017 r.</span><span class="sxs-lookup"><span data-stu-id="043fc-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="043fc-108">Użyj nowszej wersji usługi HDInsight Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="043fc-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="043fc-109">Aby uzyskać informacje na temat tworzenia klastra przy użyciu nowego HDInsight, zobacz [Tworzenie klastrów opartych na systemie Linux w usłudze HDInsight przy użyciu środowiska Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span><span class="sxs-lookup"><span data-stu-id="043fc-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="043fc-110">Aby uzyskać informacje na temat przesyłania zadań przy użyciu środowiska Azure PowerShell i innych metod, zobacz [przesyłanie zadań usługi Hadoop w usłudze HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span><span class="sxs-lookup"><span data-stu-id="043fc-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="043fc-111">Aby uzyskać informacje referencyjne dotyczące usługi Azure PowerShell HDInsight, zobacz [polecenia cmdlet usługi Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span><span class="sxs-lookup"><span data-stu-id="043fc-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="043fc-112">Polecenie cmdlet **Add-AzureHDInsightConfigValues** umożliwia dodanie dostosowania wartości konfiguracji usługi Hadoop, takiego jak Core-site.xml lub Hive-site.xml, lub dostosowania biblioteki udostępnionej w usłudze Azure do konfiguracji klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="043fc-112">The **Add-AzureHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as Core-site.xml or Hive-site.xml, or a Hive shared library customization to an Azure HDInsight cluster configuration.</span></span>

<span data-ttu-id="043fc-113">Polecenie cmdlet umożliwia dodanie niestandardowych wartości konfiguracji do określonego obiektu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="043fc-113">The cmdlet adds custom configuration values to a specified configuration object.</span></span>
<span data-ttu-id="043fc-114">Ustawienia niestandardowe są dodawane do plików konfiguracji odpowiednich usług Hadoop po wdrożeniu klastra.</span><span class="sxs-lookup"><span data-stu-id="043fc-114">The custom settings are added to the configuration files of the relevant Hadoop services when the cluster is deployed.</span></span>

## <span data-ttu-id="043fc-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="043fc-115">EXAMPLES</span></span>

### <span data-ttu-id="043fc-116">Przykład 1: Konfigurowanie klastra</span><span class="sxs-lookup"><span data-stu-id="043fc-116">Example 1: Configure a cluster</span></span>
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

<span data-ttu-id="043fc-117">Pierwsze polecenie tworzy nowy obiekt **AzureHDInsightHiveConfiguration** , a następnie zapisuje go w zmiennej $HiveConfigValues.</span><span class="sxs-lookup"><span data-stu-id="043fc-117">The first command creates a new **AzureHDInsightHiveConfiguration** object, and then stores it in the $HiveConfigValues variable.</span></span>

<span data-ttu-id="043fc-118">Kolejne pięć poleceń umożliwia utworzenie wartości konfiguracji gałęzi i zapisanie tych wartości jako członków $HiveConfigValues.</span><span class="sxs-lookup"><span data-stu-id="043fc-118">The next five commands create configuration values for Hive and store those values as members of $HiveConfigValues.</span></span>

<span data-ttu-id="043fc-119">Polecenie siódme powoduje utworzenie obiektu **AzureHDInsightOozieConfiguration** , a następnie zapisanie go w zmiennej $OozieConfigValues.</span><span class="sxs-lookup"><span data-stu-id="043fc-119">The seventh command creates an **AzureHDInsightOozieConfiguration** object, and then stores it in the $OozieConfigValues variable.</span></span>
<span data-ttu-id="043fc-120">Ósmej polecenie tworzy wartość konfiguracji dla Oozie, a następnie przechowuje te wartości jako członka $OozieConfigValues.</span><span class="sxs-lookup"><span data-stu-id="043fc-120">The eighth command creates a configuration value for Oozie, and then stores that values as a member of $OozieConfigValues.</span></span>

<span data-ttu-id="043fc-121">Dziewiąte polecenie tworzy obiekt **AzureHDInsightMapReduceConfiguration** , a następnie zapisuje go w zmiennej $MapredConfigValues.</span><span class="sxs-lookup"><span data-stu-id="043fc-121">The ninth command creates an **AzureHDInsightMapReduceConfiguration** object, and then stores it in the $MapredConfigValues variable.</span></span>
<span data-ttu-id="043fc-122">Następne dwa polecenia tworzą wartości konfiguracji dla MapReduce i przechowuj te wartości jako członkowie $MapredConfigValues.</span><span class="sxs-lookup"><span data-stu-id="043fc-122">The next two commands create configuration values for MapReduce and store those values as members of $MapredConfigValues.</span></span>

<span data-ttu-id="043fc-123">W poleceniu dwunaste użyto polecenia cmdlet **New-AzureHDInsightClusterConfig** w celu utworzenia konfiguracji klastra usługi HDInsight, a następnie zapisu w zmiennej $config.</span><span class="sxs-lookup"><span data-stu-id="043fc-123">The twelfth command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>
<span data-ttu-id="043fc-124">W poleceniu użyto operatora potoku w celu przekazania $Config do polecenia cmdlet **Set-AzureHDInsightDefaultStorage** w celu zaktualizowania domyślnego ustawienia przechowywania i polecenia cmdlet **Add-AzureHDInsightConfigValues** w celu dodania nowych wartości konfiguracji do konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="043fc-124">The command uses the pipeline operator to pass $Config to the **Set-AzureHDInsightDefaultStorage** cmdlet to update the default storage setting and to the **Add-AzureHDInsightConfigValues** cmdlet to add the new configuration values to the cluster configuration.</span></span>

<span data-ttu-id="043fc-125">W poleceniu ostatnim jest używany operator potoku umożliwiający przekazanie $Config do polecenia cmdlet **New-AzureHDInsightCluster** w celu utworzenia nowego klastra usługi HDInsight z dostosowanymi ustawieniami.</span><span class="sxs-lookup"><span data-stu-id="043fc-125">The final command uses the pipeline operator to pass $Config to the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster with the customized settings.</span></span>

## <span data-ttu-id="043fc-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="043fc-126">PARAMETERS</span></span>

### <span data-ttu-id="043fc-127">-Config</span><span class="sxs-lookup"><span data-stu-id="043fc-127">-Config</span></span>
<span data-ttu-id="043fc-128">Określa obiekt konfiguracji, do którego ma zostać dodana konfiguracja usługi Hadoop.</span><span class="sxs-lookup"><span data-stu-id="043fc-128">Specifies the configuration object to which to add a Hadoop configuration.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="043fc-129">-Core</span><span class="sxs-lookup"><span data-stu-id="043fc-129">-Core</span></span>
<span data-ttu-id="043fc-130">Określa zestaw wartości konfiguracji usługi Hadoop dla Core-site.xml.</span><span class="sxs-lookup"><span data-stu-id="043fc-130">Specifies a set of Hadoop configuration values for Core-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043fc-131">-HBase</span><span class="sxs-lookup"><span data-stu-id="043fc-131">-HBase</span></span>
<span data-ttu-id="043fc-132">Określa zestaw HBaseych wartości konfiguracji dla Hbase-site.xml.</span><span class="sxs-lookup"><span data-stu-id="043fc-132">Specifies a set of HBase configuration values for Hbase-site.xml.</span></span>

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043fc-133">-HDFS</span><span class="sxs-lookup"><span data-stu-id="043fc-133">-Hdfs</span></span>
<span data-ttu-id="043fc-134">Określa zestaw wartości konfiguracji usługi Hadoop dla Hdfs-site.xml.</span><span class="sxs-lookup"><span data-stu-id="043fc-134">Specifies a set of Hadoop configuration values for Hdfs-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043fc-135">-Gałąź rejestru</span><span class="sxs-lookup"><span data-stu-id="043fc-135">-Hive</span></span>
<span data-ttu-id="043fc-136">Określa obiekt Customization dla usługi uli usługi Hadoop, w tym zestaw wartości konfiguracji usługi Hadoop dla Hive-site.xml i udostępnionych bibliotek gałęzi.</span><span class="sxs-lookup"><span data-stu-id="043fc-136">Specifies a customization object for Hadoop Hive service, including a set of Hadoop configuration values for Hive-site.xml and Hive shared libraries.</span></span>

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043fc-137">-MapReduce</span><span class="sxs-lookup"><span data-stu-id="043fc-137">-MapReduce</span></span>
<span data-ttu-id="043fc-138">Określa obiekt dostosowania dla MapReduce i harmonogramu pojemności.</span><span class="sxs-lookup"><span data-stu-id="043fc-138">Specifies a customization object for MapReduce and the capacity scheduler.</span></span>

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043fc-139">-Oozie</span><span class="sxs-lookup"><span data-stu-id="043fc-139">-Oozie</span></span>
<span data-ttu-id="043fc-140">Określa obiekt dostosowywania dla usługi Oozie usługi Hadoop, w tym zestaw wartości konfiguracji usługi Hadoop dla Oozie-site.xml.</span><span class="sxs-lookup"><span data-stu-id="043fc-140">Specifies a customization object for Hadoop Oozie service, including a set of Hadoop configuration values for Oozie-site.xml.</span></span>

```yaml
Type: AzureHDInsightOozieConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043fc-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="043fc-141">-Profile</span></span>
<span data-ttu-id="043fc-142">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="043fc-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="043fc-143">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="043fc-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043fc-144">-Spark</span><span class="sxs-lookup"><span data-stu-id="043fc-144">-Spark</span></span>
<span data-ttu-id="043fc-145">Określa obiekt dostosowania dla programu Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="043fc-145">Specifies a customization object for Apache Spark.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043fc-146">— Burza</span><span class="sxs-lookup"><span data-stu-id="043fc-146">-Storm</span></span>
<span data-ttu-id="043fc-147">Określa obiekt Customization (Dostosowywanie) dla programu Apache.</span><span class="sxs-lookup"><span data-stu-id="043fc-147">Specifies a customization object for Apache Storm.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043fc-148">-Przędza</span><span class="sxs-lookup"><span data-stu-id="043fc-148">-Yarn</span></span>
<span data-ttu-id="043fc-149">Określa obiekt dostosowania dla PRZĘDZy usługi Hadoop, określając zestaw dostosowanych wartości konfiguracji PRZĘDZy dla Yarn-site.xml.</span><span class="sxs-lookup"><span data-stu-id="043fc-149">Specifies a customization object for Hadoop YARN, specifying a set of customized YARN configuration values for Yarn-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="043fc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="043fc-150">CommonParameters</span></span>
<span data-ttu-id="043fc-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="043fc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="043fc-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="043fc-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="043fc-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="043fc-153">INPUTS</span></span>

## <span data-ttu-id="043fc-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="043fc-154">OUTPUTS</span></span>

## <span data-ttu-id="043fc-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="043fc-155">NOTES</span></span>

## <span data-ttu-id="043fc-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="043fc-156">RELATED LINKS</span></span>

[<span data-ttu-id="043fc-157">Nowe — AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="043fc-157">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="043fc-158">Nowe — AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="043fc-158">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="043fc-159">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="043fc-159">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
