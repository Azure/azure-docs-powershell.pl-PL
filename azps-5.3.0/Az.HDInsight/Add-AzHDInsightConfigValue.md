---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 4de1a76d2c9ec2cba7dae67d26f73ef55a5f827f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489641"
---
# <span data-ttu-id="cbd1d-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="cbd1d-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="cbd1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cbd1d-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd1d-103">Umożliwia dodanie dostosowania wartości konfiguracji usługi Hadoop i/lub dostosowania biblioteki udostępnionej do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="cbd1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cbd1d-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbd1d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cbd1d-105">DESCRIPTION</span></span>
<span data-ttu-id="cbd1d-106">Polecenie cmdlet **Add-AzHDInsightConfigValue** umożliwia dodanie dostosowania wartości konfiguracji usługi Hadoop, takiego jak core-site.xml lub hive-site.xml, i/lub dostosowania biblioteki udostępnionej w gałęzi do obiektu konfiguracji usługi HDInsight utworzonego za pomocą polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="cbd1d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cbd1d-107">EXAMPLES</span></span>

### <span data-ttu-id="cbd1d-108">Przykład 1. Dodawanie niestandardowej wartości konfiguracji do obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="cbd1d-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightConfigValue `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="cbd1d-109">To polecenie dodaje wartość konfiguracji usługi Hadoop do klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="cbd1d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cbd1d-110">PARAMETERS</span></span>

### <span data-ttu-id="cbd1d-111">-Config</span><span class="sxs-lookup"><span data-stu-id="cbd1d-111">-Config</span></span>
<span data-ttu-id="cbd1d-112">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="cbd1d-113">Ten obiekt jest tworzony za pomocą polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd1d-114">-Core</span><span class="sxs-lookup"><span data-stu-id="cbd1d-114">-Core</span></span>
<span data-ttu-id="cbd1d-115">Określa podstawowe konfiguracje witryn tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd1d-116">-DefaultProfile</span></span>
<span data-ttu-id="cbd1d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cbd1d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbd1d-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="cbd1d-118">-HBaseEnv</span></span>
<span data-ttu-id="cbd1d-119">Określa ENV HBase konfigurację tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="cbd1d-120">-HBaseSite</span></span>
<span data-ttu-id="cbd1d-121">Określa konfiguracje witryny HBase dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-122">-HDFS</span><span class="sxs-lookup"><span data-stu-id="cbd1d-122">-Hdfs</span></span>
<span data-ttu-id="cbd1d-123">Określa konfiguracje HDFS tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="cbd1d-124">-HiveEnv</span></span>
<span data-ttu-id="cbd1d-125">Określa konfigurację ENV gałęzi dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="cbd1d-126">-HiveSite</span></span>
<span data-ttu-id="cbd1d-127">Określa konfiguracje witryn gałęzi dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="cbd1d-128">-MapRed</span></span>
<span data-ttu-id="cbd1d-129">Określa konfiguracje witryny MapRed dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="cbd1d-130">-OozieEnv</span></span>
<span data-ttu-id="cbd1d-131">Określa ENV Oozie konfigurację tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="cbd1d-132">-OozieSite</span></span>
<span data-ttu-id="cbd1d-133">Określa konfiguracje witryny Oozie dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="cbd1d-134">-RServer</span></span>
<span data-ttu-id="cbd1d-135">Określa konfiguracje RServer.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="cbd1d-136">Dotyczy tylko klastrów RServer.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="cbd1d-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="cbd1d-137">-Spark2Defaults</span></span>
<span data-ttu-id="cbd1d-138">Określa konfigurację domyślnych Spark2 dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="cbd1d-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="cbd1d-140">Określa konfiguracje Spark2 Thrift SparkConf w tym klastrze usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="cbd1d-141">-SparkDefaults</span></span>
<span data-ttu-id="cbd1d-142">Określa ustawienia domyślne konfiguracji platformy Spark dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="cbd1d-143">-SparkThriftConf</span></span>
<span data-ttu-id="cbd1d-144">Określa konfiguracje SparkConf platformy Thrift dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-145">— Burza</span><span class="sxs-lookup"><span data-stu-id="cbd1d-145">-Storm</span></span>
<span data-ttu-id="cbd1d-146">Określa konfiguracje witryny burzy dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="cbd1d-147">-Tez</span></span>
<span data-ttu-id="cbd1d-148">Określa konfiguracje witryny tez dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="cbd1d-149">-WebHCat</span></span>
<span data-ttu-id="cbd1d-150">Określa konfiguracje witryny WebHCat dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-151">-Przędza</span><span class="sxs-lookup"><span data-stu-id="cbd1d-151">-Yarn</span></span>
<span data-ttu-id="cbd1d-152">Określa konfiguracje witryny PRZĘDZy dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="cbd1d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd1d-153">CommonParameters</span></span>
<span data-ttu-id="cbd1d-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd1d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd1d-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbd1d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd1d-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbd1d-156">INPUTS</span></span>

### <span data-ttu-id="cbd1d-157">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="cbd1d-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="cbd1d-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cbd1d-158">OUTPUTS</span></span>

### <span data-ttu-id="cbd1d-159">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="cbd1d-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="cbd1d-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cbd1d-160">NOTES</span></span>

## <span data-ttu-id="cbd1d-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbd1d-161">RELATED LINKS</span></span>

[<span data-ttu-id="cbd1d-162">Nowe — AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="cbd1d-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


