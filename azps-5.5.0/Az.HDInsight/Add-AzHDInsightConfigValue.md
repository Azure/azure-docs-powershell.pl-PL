---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 4de1a76d2c9ec2cba7dae67d26f73ef55a5f827f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180603"
---
# <span data-ttu-id="fed23-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="fed23-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="fed23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fed23-102">SYNOPSIS</span></span>
<span data-ttu-id="fed23-103">Powoduje dodanie dostosowania wartości konfiguracji usługi Hadoop i/lub dostosowania biblioteki udostępnionej w użytku w obiekcie konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="fed23-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="fed23-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fed23-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fed23-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fed23-105">DESCRIPTION</span></span>
<span data-ttu-id="fed23-106">Polecenie cmdlet **Add-AzHDInsightConfigValue** powoduje dodanie dostosowania wartości konfiguracji usługi Hadoop, takiego jak core-site.xml lub hive-site.xml, i/lub dostosowania biblioteki udostępnionej Wajdy do obiektu konfiguracyjnego HDInsight utworzonego za pomocą polecenia cmdlet programu New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="fed23-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="fed23-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fed23-107">EXAMPLES</span></span>

### <span data-ttu-id="fed23-108">Przykład 1. Dodawanie niestandardowej wartości konfiguracji do obiektu konfiguracji klastrów</span><span class="sxs-lookup"><span data-stu-id="fed23-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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

<span data-ttu-id="fed23-109">To polecenie dodaje wartość konfiguracji usługi Hadoop do klastra o nazwie Twoja-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="fed23-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="fed23-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fed23-110">PARAMETERS</span></span>

### <span data-ttu-id="fed23-111">-Config</span><span class="sxs-lookup"><span data-stu-id="fed23-111">-Config</span></span>
<span data-ttu-id="fed23-112">Określa obiekt konfiguracji klastrów HDInsight, który zostanie zmodyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fed23-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="fed23-113">Ten obiekt jest tworzony przez New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fed23-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="fed23-114">— Core</span><span class="sxs-lookup"><span data-stu-id="fed23-114">-Core</span></span>
<span data-ttu-id="fed23-115">Określa konfiguracje witryny podstawowej tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed23-116">-DefaultProfile</span></span>
<span data-ttu-id="fed23-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fed23-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fed23-118">- HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="fed23-118">-HBaseEnv</span></span>
<span data-ttu-id="fed23-119">Określa konfiguracje env bazy danych HBase tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="fed23-120">-HBaseSite</span></span>
<span data-ttu-id="fed23-121">Określa konfiguracje witryny programu HBase tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-122">- Hdfs</span><span class="sxs-lookup"><span data-stu-id="fed23-122">-Hdfs</span></span>
<span data-ttu-id="fed23-123">Określa konfiguracje usługi HDFS tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-124">- GałąźEnv</span><span class="sxs-lookup"><span data-stu-id="fed23-124">-HiveEnv</span></span>
<span data-ttu-id="fed23-125">Określa konfiguracje aplikacji Gałąź Env tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-126">- GałąźSite</span><span class="sxs-lookup"><span data-stu-id="fed23-126">-HiveSite</span></span>
<span data-ttu-id="fed23-127">Określa konfiguracje witryny Gałąź tego klastru HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="fed23-128">-MapRed</span></span>
<span data-ttu-id="fed23-129">Określa konfiguracje witryny MapRed tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="fed23-130">-OozieEnv</span></span>
<span data-ttu-id="fed23-131">Określa konfiguracje aplikacji Oozie Env tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="fed23-132">-OozieSite</span></span>
<span data-ttu-id="fed23-133">Określa konfiguracje witryny Oozie tego klastru HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="fed23-134">-RServer</span></span>
<span data-ttu-id="fed23-135">Określa konfiguracje serwera RServer.</span><span class="sxs-lookup"><span data-stu-id="fed23-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="fed23-136">Prawidłowy tylko dla klastrów serwera RServer.</span><span class="sxs-lookup"><span data-stu-id="fed23-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="fed23-137">- Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="fed23-137">-Spark2Defaults</span></span>
<span data-ttu-id="fed23-138">Określa konfiguracje domyślne wykresu przebiegu w sieci (Spark2 Defaults) tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="fed23-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="fed23-140">Określa konfiguracje wykresu Spark2 Thrift SparkConf tego klastru HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-141">- SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="fed23-141">-SparkDefaults</span></span>
<span data-ttu-id="fed23-142">Określa konfiguracje domyślne wykresu przebiegu w sieci w tym klastrze HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="fed23-143">-SparkThriftConf</span></span>
<span data-ttu-id="fed23-144">Określa konfiguracje spark thrift sparkconf tego klastru HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-145">— Burza</span><span class="sxs-lookup"><span data-stu-id="fed23-145">-Storm</span></span>
<span data-ttu-id="fed23-146">Określa konfiguracje witryny burzy tego klastra HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-147">— Tez</span><span class="sxs-lookup"><span data-stu-id="fed23-147">-Tez</span></span>
<span data-ttu-id="fed23-148">Określa konfiguracje witryny programu Tez dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-149">- WebHCat</span><span class="sxs-lookup"><span data-stu-id="fed23-149">-WebHCat</span></span>
<span data-ttu-id="fed23-150">Określa konfiguracje witryny sieci WebHCat tego klastra USŁUGI HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-151">— Pochłoń</span><span class="sxs-lookup"><span data-stu-id="fed23-151">-Yarn</span></span>
<span data-ttu-id="fed23-152">Określa konfiguracje witryny JNW tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fed23-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="fed23-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed23-153">CommonParameters</span></span>
<span data-ttu-id="fed23-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fed23-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed23-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fed23-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed23-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fed23-156">INPUTS</span></span>

### <span data-ttu-id="fed23-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="fed23-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="fed23-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fed23-158">OUTPUTS</span></span>

### <span data-ttu-id="fed23-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="fed23-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="fed23-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fed23-160">NOTES</span></span>

## <span data-ttu-id="fed23-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fed23-161">RELATED LINKS</span></span>

[<span data-ttu-id="fed23-162">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="fed23-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


