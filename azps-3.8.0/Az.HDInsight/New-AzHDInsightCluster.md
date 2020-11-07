---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: c0d3d6518025aab22add0859bde69cb1ad279138
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896702"
---
# <span data-ttu-id="3fd74-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3fd74-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="3fd74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3fd74-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd74-103">Tworzy klaster usługi Azure HDInsight w określonej grupie zasobów dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3fd74-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="3fd74-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3fd74-104">SYNTAX</span></span>

### <span data-ttu-id="3fd74-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3fd74-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>] [[-SecurityProfile] <AzureHDInsightSecurityProfile>]
 [[-DisksPerWorkerNode] <Int32>] [[-MinSupportedTlsVersion] <String>]
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fd74-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3fd74-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-SecurityProfile] <AzureHDInsightSecurityProfile>] [[-DisksPerWorkerNode] <Int32>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fd74-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="3fd74-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificateFileContents] <Byte[]>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-SecurityProfile] <AzureHDInsightSecurityProfile>] [[-DisksPerWorkerNode] <Int32>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fd74-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3fd74-108">DESCRIPTION</span></span>
<span data-ttu-id="3fd74-109">New-AzHDInsightCluster tworzy klaster usługi Azure HDInsight przy użyciu określonych parametrów lub obiektu konfiguracji utworzonego za pomocą polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="3fd74-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="3fd74-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3fd74-110">EXAMPLES</span></span>

### <span data-ttu-id="3fd74-111">Przykład 1. Tworzenie klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="3fd74-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -OSType Windows `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="3fd74-112">To polecenie tworzy klaster w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3fd74-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="3fd74-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3fd74-113">PARAMETERS</span></span>

### <span data-ttu-id="3fd74-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="3fd74-114">-AadTenantId</span></span>
<span data-ttu-id="3fd74-115">Określa identyfikator dzierżawy usługi Azure AD, który będzie stosowany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3fd74-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="3fd74-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="3fd74-117">Określa dodatkowe konta magazynu platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="3fd74-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="3fd74-118">Możesz również użyć polecenia cmdlet Add-AzHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="3fd74-118">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-119">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="3fd74-119">-ApplicationId</span></span>
<span data-ttu-id="3fd74-120">Pobiera lub ustawia identyfikator aplikacji głównej usługi w celu uzyskania dostępu do usługi Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="3fd74-120">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-121">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="3fd74-121">-CertificateFileContents</span></span>
<span data-ttu-id="3fd74-122">Określa zawartość pliku certyfikatu, która będzie używana podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3fd74-122">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-123">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3fd74-123">-CertificateFilePath</span></span>
<span data-ttu-id="3fd74-124">Określa ścieżkę do pliku certyfikatu, który zostanie wykorzystany do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="3fd74-124">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3fd74-125">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3fd74-125">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-126">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3fd74-126">-CertificatePassword</span></span>
<span data-ttu-id="3fd74-127">Określa hasło certyfikatu, które zostanie użyte do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="3fd74-127">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3fd74-128">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3fd74-128">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-129">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="3fd74-129">-ClusterName</span></span>
<span data-ttu-id="3fd74-130">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="3fd74-130">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3fd74-131">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="3fd74-131">-ClusterSizeInNodes</span></span>
<span data-ttu-id="3fd74-132">Określa liczbę węzłów procesu roboczego klastra.</span><span class="sxs-lookup"><span data-stu-id="3fd74-132">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-133">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="3fd74-133">-ClusterTier</span></span>
<span data-ttu-id="3fd74-134">Określa poziom klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3fd74-134">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="3fd74-135">Domyślnie jest to standard.</span><span class="sxs-lookup"><span data-stu-id="3fd74-135">By default, this is Standard.</span></span>
<span data-ttu-id="3fd74-136">Warstwa Premium może być używana tylko w przypadku klastrów z systemem Linux i umożliwia korzystanie z nowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="3fd74-136">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-137">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="3fd74-137">-ClusterType</span></span>
<span data-ttu-id="3fd74-138">Określa typ klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="3fd74-138">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="3fd74-139">Dostępne opcje: Hadoop, HBase, burza, Spark, INTERACTIVEHIVE, Kafka i RServer</span><span class="sxs-lookup"><span data-stu-id="3fd74-139">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-140">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="3fd74-140">-ComponentVersion</span></span>
```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-141">-Config</span><span class="sxs-lookup"><span data-stu-id="3fd74-141">-Config</span></span>
<span data-ttu-id="3fd74-142">Określa obiekt klastra, który ma zostać wykorzystany do utworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="3fd74-142">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="3fd74-143">Ten obiekt można utworzyć przy użyciu polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="3fd74-143">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-144">-Konfiguracje</span><span class="sxs-lookup"><span data-stu-id="3fd74-144">-Configurations</span></span>
<span data-ttu-id="3fd74-145">Określa konfiguracje tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3fd74-145">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="3fd74-146">Możesz również użyć polecenia cmdlet Add-AzHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="3fd74-146">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd74-147">-DefaultProfile</span></span>
<span data-ttu-id="3fd74-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3fd74-148">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fd74-149">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3fd74-149">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="3fd74-150">Określa klucz konta dla domyślnego konta usługi Azure Storage, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3fd74-150">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="3fd74-151">Możesz również użyć polecenia cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="3fd74-151">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-152">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3fd74-152">-DefaultStorageAccountName</span></span>
<span data-ttu-id="3fd74-153">Określa nazwę domyślnego konta magazynu platformy Azure, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3fd74-153">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="3fd74-154">Możesz również użyć polecenia cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="3fd74-154">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-155">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3fd74-155">-DefaultStorageAccountType</span></span>
<span data-ttu-id="3fd74-156">Określa typ domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3fd74-156">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="3fd74-157">Możliwe wartości to AzureStorage i AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="3fd74-157">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="3fd74-158">Wartość domyślna to AzureStorage, jeśli nie określono.</span><span class="sxs-lookup"><span data-stu-id="3fd74-158">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-159">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3fd74-159">-DefaultStorageContainer</span></span>
<span data-ttu-id="3fd74-160">Określa nazwę kontenera domyślnego w domyślnym koncie magazynu platformy Azure, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3fd74-160">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="3fd74-161">Możesz również użyć polecenia cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="3fd74-161">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-162">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="3fd74-162">-DefaultStorageRootPath</span></span>
<span data-ttu-id="3fd74-163">Określa prefiks ścieżki na koncie usługi Data Lake Store, które będzie używane przez klaster usługi HDInsight jako domyślny system plików.</span><span class="sxs-lookup"><span data-stu-id="3fd74-163">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-164">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="3fd74-164">-DisksPerWorkerNode</span></span>
<span data-ttu-id="3fd74-165">Określa liczbę dysków dla roli węzła procesu roboczego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="3fd74-165">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-166">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="3fd74-166">-EdgeNodeSize</span></span>
<span data-ttu-id="3fd74-167">Określa rozmiar maszyny wirtualnej dla węzła Edge.</span><span class="sxs-lookup"><span data-stu-id="3fd74-167">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="3fd74-168">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3fd74-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="3fd74-169">Ten parametr jest prawidłowy tylko w przypadku klastrów RServer.</span><span class="sxs-lookup"><span data-stu-id="3fd74-169">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-170">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="3fd74-170">-HeadNodeSize</span></span>
<span data-ttu-id="3fd74-171">Określa rozmiar maszyny wirtualnej dla węzła głównego.</span><span class="sxs-lookup"><span data-stu-id="3fd74-171">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="3fd74-172">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3fd74-172">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-173">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="3fd74-173">-HiveMetastore</span></span>
<span data-ttu-id="3fd74-174">Określa bazę danych SQL do przechowywania metadanych gałęzi.</span><span class="sxs-lookup"><span data-stu-id="3fd74-174">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="3fd74-175">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="3fd74-175">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-176">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="3fd74-176">-HttpCredential</span></span>
<span data-ttu-id="3fd74-177">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="3fd74-177">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-178">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3fd74-178">-Location</span></span>
<span data-ttu-id="3fd74-179">Określa lokalizację klastra.</span><span class="sxs-lookup"><span data-stu-id="3fd74-179">Specifies the location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-180">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3fd74-180">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="3fd74-181">Pobiera lub ustawia minimalną obsługiwaną wersję protokołu TLS.</span><span class="sxs-lookup"><span data-stu-id="3fd74-181">Gets or sets the minimal supported TLS version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-182">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3fd74-182">-ObjectId</span></span>
<span data-ttu-id="3fd74-183">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD reprezentujący klaster.</span><span class="sxs-lookup"><span data-stu-id="3fd74-183">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="3fd74-184">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3fd74-184">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-185">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="3fd74-185">-OozieMetastore</span></span>
<span data-ttu-id="3fd74-186">Określa bazę danych SQL do przechowywania metadanych Oozie.</span><span class="sxs-lookup"><span data-stu-id="3fd74-186">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="3fd74-187">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="3fd74-187">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-188">-OSType</span><span class="sxs-lookup"><span data-stu-id="3fd74-188">-OSType</span></span>
<span data-ttu-id="3fd74-189">Określa system operacyjny dla klastra.</span><span class="sxs-lookup"><span data-stu-id="3fd74-189">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="3fd74-190">Dostępne opcje: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="3fd74-190">Options are: Windows, Linux</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.OSType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-191">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="3fd74-191">-RdpAccessExpiry</span></span>
<span data-ttu-id="3fd74-192">Określa wygaśnięcie jako obiekt DateTime, aby uzyskać dostęp do klastra za pomocą protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="3fd74-192">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-193">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="3fd74-193">-RdpCredential</span></span>
<span data-ttu-id="3fd74-194">Określa poświadczenia pulpitu zdalnego (RDP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="3fd74-194">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="3fd74-195">Dotyczy to tylko klastrów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="3fd74-195">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fd74-196">-ResourceGroupName</span></span>
<span data-ttu-id="3fd74-197">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3fd74-197">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-198">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="3fd74-198">-ScriptActions</span></span>
<span data-ttu-id="3fd74-199">Określa akcje skryptu, które mają być uruchamiane w klastrze na koniec tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="3fd74-199">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="3fd74-200">Możesz również użyć dodatku Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="3fd74-200">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-201">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="3fd74-201">-SecurityProfile</span></span>
<span data-ttu-id="3fd74-202">Określa właściwości związane z zabezpieczeniami używane do tworzenia bezpiecznego klastra.</span><span class="sxs-lookup"><span data-stu-id="3fd74-202">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="3fd74-203">Możesz również użyć polecenia cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="3fd74-203">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-204">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="3fd74-204">-SshCredential</span></span>
<span data-ttu-id="3fd74-205">Określa poświadczenie SSH, które ma być używane dla połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="3fd74-205">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="3fd74-206">Dotyczy to tylko klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="3fd74-206">This is only for Linux clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-207">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="3fd74-207">-SshPublicKey</span></span>
<span data-ttu-id="3fd74-208">Określa klucz publiczny, który ma być stosowany do połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="3fd74-208">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="3fd74-209">Dotyczy to tylko klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="3fd74-209">This is only for Linux clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-210">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="3fd74-210">-SubnetName</span></span>
<span data-ttu-id="3fd74-211">Określa nazwę podsieci w wybranej sieci wirtualnej klastra.</span><span class="sxs-lookup"><span data-stu-id="3fd74-211">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-212">-Version</span><span class="sxs-lookup"><span data-stu-id="3fd74-212">-Version</span></span>
<span data-ttu-id="3fd74-213">Określa wersję HDI klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3fd74-213">Specifies the HDI version of the HDInsight cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-214">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3fd74-214">-VirtualNetworkId</span></span>
<span data-ttu-id="3fd74-215">Określa identyfikator sieci wirtualnej, do której ma być zastrzec klaster.</span><span class="sxs-lookup"><span data-stu-id="3fd74-215">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-216">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="3fd74-216">-WorkerNodeSize</span></span>
<span data-ttu-id="3fd74-217">Określa rozmiar maszyny wirtualnej dla węzła roboczego.</span><span class="sxs-lookup"><span data-stu-id="3fd74-217">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="3fd74-218">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3fd74-218">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-219">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="3fd74-219">-ZookeeperNodeSize</span></span>
<span data-ttu-id="3fd74-220">Określa rozmiar maszyny wirtualnej dla węzła Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="3fd74-220">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="3fd74-221">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3fd74-221">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="3fd74-222">Ten parametr jest prawidłowy tylko w przypadku klastrów HBase lub burzy.</span><span class="sxs-lookup"><span data-stu-id="3fd74-222">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd74-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd74-223">CommonParameters</span></span>
<span data-ttu-id="3fd74-224">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd74-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd74-225">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fd74-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd74-226">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fd74-226">INPUTS</span></span>

### <span data-ttu-id="3fd74-227">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3fd74-227">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3fd74-228">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3fd74-228">OUTPUTS</span></span>

### <span data-ttu-id="3fd74-229">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3fd74-229">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="3fd74-230">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3fd74-230">NOTES</span></span>
<span data-ttu-id="3fd74-231">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, HDInsight, HD, Insights</span><span class="sxs-lookup"><span data-stu-id="3fd74-231">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="3fd74-232">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fd74-232">RELATED LINKS</span></span>

[<span data-ttu-id="3fd74-233">Nowe — AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3fd74-233">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

