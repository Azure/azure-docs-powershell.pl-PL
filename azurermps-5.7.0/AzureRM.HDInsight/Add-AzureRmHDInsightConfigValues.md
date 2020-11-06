---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightconfigvalues
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightConfigValues.md
ms.openlocfilehash: 75d68b98d93168d69db4d5120dde41ca1a8f8f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544320"
---
# <span data-ttu-id="18eee-101">Add-AzureRmHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="18eee-101">Add-AzureRmHDInsightConfigValues</span></span>

## <span data-ttu-id="18eee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18eee-102">SYNOPSIS</span></span>
<span data-ttu-id="18eee-103">Umożliwia dodanie dostosowania wartości konfiguracji usługi Hadoop i/lub dostosowania biblioteki udostępnionej do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="18eee-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18eee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18eee-104">SYNTAX</span></span>

### <span data-ttu-id="18eee-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="18eee-105">Spark1</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18eee-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="18eee-106">Spark2</span></span>
```
Add-AzureRmHDInsightConfigValues [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18eee-107">Opis</span><span class="sxs-lookup"><span data-stu-id="18eee-107">DESCRIPTION</span></span>
<span data-ttu-id="18eee-108">Polecenie cmdlet **Add-AzureRmHDInsightConfigValues** umożliwia dodanie dostosowania wartości konfiguracji usługi Hadoop, takiego jak core-site.xml lub hive-site.xml, i/lub dostosowania biblioteki udostępnionej w gałęzi do obiektu konfiguracji usługi HDInsight utworzonego za pomocą polecenia cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="18eee-108">The **Add-AzureRmHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="18eee-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18eee-109">EXAMPLES</span></span>

### <span data-ttu-id="18eee-110">Przykład 1. Dodawanie niestandardowej wartości konfiguracji do obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="18eee-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightConfigValues `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="18eee-111">To polecenie dodaje wartość konfiguracji usługi Hadoop do klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="18eee-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="18eee-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18eee-112">PARAMETERS</span></span>

### <span data-ttu-id="18eee-113">-Config</span><span class="sxs-lookup"><span data-stu-id="18eee-113">-Config</span></span>
<span data-ttu-id="18eee-114">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18eee-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="18eee-115">Ten obiekt jest tworzony za pomocą polecenia cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="18eee-115">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18eee-116">-Core</span><span class="sxs-lookup"><span data-stu-id="18eee-116">-Core</span></span>
<span data-ttu-id="18eee-117">Określa podstawowe konfiguracje witryn tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="18eee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18eee-118">-DefaultProfile</span></span>
<span data-ttu-id="18eee-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="18eee-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eee-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="18eee-120">-HBaseEnv</span></span>
<span data-ttu-id="18eee-121">Określa ENV HBase konfigurację tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="18eee-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="18eee-122">-HBaseSite</span></span>
<span data-ttu-id="18eee-123">Określa konfiguracje witryny HBase dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="18eee-124">-HDFS</span><span class="sxs-lookup"><span data-stu-id="18eee-124">-Hdfs</span></span>
<span data-ttu-id="18eee-125">Określa konfiguracje HDFS tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="18eee-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="18eee-126">-HiveEnv</span></span>
<span data-ttu-id="18eee-127">Określa konfigurację ENV gałęzi dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="18eee-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="18eee-128">-HiveSite</span></span>
<span data-ttu-id="18eee-129">Określa konfiguracje witryn gałęzi dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="18eee-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="18eee-130">-MapRed</span></span>
<span data-ttu-id="18eee-131">Określa konfiguracje witryny MapRed dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="18eee-132">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="18eee-132">-OozieEnv</span></span>
<span data-ttu-id="18eee-133">Określa ENV Oozie konfigurację tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="18eee-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="18eee-134">-OozieSite</span></span>
<span data-ttu-id="18eee-135">Określa konfiguracje witryny Oozie dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="18eee-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="18eee-136">-RServer</span></span>
<span data-ttu-id="18eee-137">Określa konfiguracje RServer.</span><span class="sxs-lookup"><span data-stu-id="18eee-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="18eee-138">Dotyczy tylko klastrów RServer.</span><span class="sxs-lookup"><span data-stu-id="18eee-138">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="18eee-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="18eee-139">-Spark2Defaults</span></span>
<span data-ttu-id="18eee-140">Określa konfigurację domyślnych Spark2 dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eee-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="18eee-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="18eee-142">Określa konfiguracje Spark2 Thrift SparkConf w tym klastrze usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eee-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="18eee-143">-SparkDefaults</span></span>
<span data-ttu-id="18eee-144">Określa ustawienia domyślne konfiguracji platformy Spark dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eee-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="18eee-145">-SparkThriftConf</span></span>
<span data-ttu-id="18eee-146">Określa konfiguracje SparkConf platformy Thrift dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Spark1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eee-147">— Burza</span><span class="sxs-lookup"><span data-stu-id="18eee-147">-Storm</span></span>
<span data-ttu-id="18eee-148">Określa konfiguracje witryny burzy dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="18eee-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="18eee-149">-Tez</span></span>
<span data-ttu-id="18eee-150">Określa konfiguracje witryny tez dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="18eee-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="18eee-151">-WebHCat</span></span>
<span data-ttu-id="18eee-152">Określa konfiguracje witryny WebHCat dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="18eee-153">-Przędza</span><span class="sxs-lookup"><span data-stu-id="18eee-153">-Yarn</span></span>
<span data-ttu-id="18eee-154">Określa konfiguracje witryny PRZĘDZy dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="18eee-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="18eee-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18eee-155">CommonParameters</span></span>
<span data-ttu-id="18eee-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18eee-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18eee-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18eee-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18eee-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18eee-158">INPUTS</span></span>

### <span data-ttu-id="18eee-159">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="18eee-159">AzureHDInsightConfig</span></span>
<span data-ttu-id="18eee-160">Parametr "config" akceptuje wartość typu "AzureHDInsightConfig" z procesu</span><span class="sxs-lookup"><span data-stu-id="18eee-160">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="18eee-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18eee-161">OUTPUTS</span></span>

### <span data-ttu-id="18eee-162">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="18eee-162">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="18eee-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18eee-163">NOTES</span></span>

## <span data-ttu-id="18eee-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18eee-164">RELATED LINKS</span></span>

[<span data-ttu-id="18eee-165">Nowe — AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="18eee-165">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


