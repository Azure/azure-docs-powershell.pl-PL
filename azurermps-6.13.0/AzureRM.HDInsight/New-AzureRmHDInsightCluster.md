---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: b10fe80fb0a58267212912f554d044b2715fd1d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545279"
---
# <span data-ttu-id="ef98a-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ef98a-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="ef98a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef98a-102">SYNOPSIS</span></span>
<span data-ttu-id="ef98a-103">Tworzy klaster usługi Azure HDInsight w określonej grupie zasobów dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ef98a-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef98a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef98a-104">SYNTAX</span></span>

### <span data-ttu-id="ef98a-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ef98a-105">Default (Default)</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificatePassword <String>] [-AadTenantId <Guid>]
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef98a-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="ef98a-106">CertificateFilePath</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef98a-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="ef98a-107">CertificateFileContents</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef98a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ef98a-108">DESCRIPTION</span></span>
<span data-ttu-id="ef98a-109">New-AzureHDInsightCluster tworzy klaster usługi Azure HDInsight przy użyciu określonych parametrów lub obiektu konfiguracji utworzonego za pomocą polecenia cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="ef98a-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="ef98a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef98a-110">EXAMPLES</span></span>

### <span data-ttu-id="ef98a-111">Przykład 1. Tworzenie klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="ef98a-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightCluster `
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

<span data-ttu-id="ef98a-112">To polecenie tworzy klaster w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ef98a-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="ef98a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef98a-113">PARAMETERS</span></span>

### <span data-ttu-id="ef98a-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="ef98a-114">-AadTenantId</span></span>
<span data-ttu-id="ef98a-115">Określa identyfikator dzierżawy usługi Azure AD, który będzie stosowany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ef98a-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ef98a-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="ef98a-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="ef98a-117">Określa dodatkowe konta magazynu platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="ef98a-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="ef98a-118">Możesz również użyć polecenia cmdlet Add-AzureRmHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="ef98a-118">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="ef98a-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="ef98a-119">-CertificateFileContents</span></span>
<span data-ttu-id="ef98a-120">Określa zawartość pliku certyfikatu, która będzie używana podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ef98a-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ef98a-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="ef98a-121">-CertificateFilePath</span></span>
<span data-ttu-id="ef98a-122">Określa ścieżkę do pliku certyfikatu, który zostanie wykorzystany do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="ef98a-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="ef98a-123">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ef98a-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ef98a-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ef98a-124">-CertificatePassword</span></span>
<span data-ttu-id="ef98a-125">Określa hasło certyfikatu, które zostanie użyte do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="ef98a-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="ef98a-126">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ef98a-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ef98a-127">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="ef98a-127">-ClusterName</span></span>
<span data-ttu-id="ef98a-128">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="ef98a-128">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ef98a-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="ef98a-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="ef98a-130">Określa liczbę węzłów procesu roboczego klastra.</span><span class="sxs-lookup"><span data-stu-id="ef98a-130">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="ef98a-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="ef98a-131">-ClusterTier</span></span>
<span data-ttu-id="ef98a-132">Określa poziom klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ef98a-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="ef98a-133">Domyślnie jest to standard.</span><span class="sxs-lookup"><span data-stu-id="ef98a-133">By default, this is Standard.</span></span>
<span data-ttu-id="ef98a-134">Warstwa Premium może być używana tylko w przypadku klastrów z systemem Linux i umożliwia korzystanie z nowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="ef98a-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="ef98a-135">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="ef98a-135">-ClusterType</span></span>
<span data-ttu-id="ef98a-136">Określa typ klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="ef98a-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="ef98a-137">Dostępne opcje: Hadoop, HBase, burza, Spark</span><span class="sxs-lookup"><span data-stu-id="ef98a-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="ef98a-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="ef98a-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="ef98a-139">-Config</span><span class="sxs-lookup"><span data-stu-id="ef98a-139">-Config</span></span>
<span data-ttu-id="ef98a-140">Określa obiekt klastra, który ma zostać wykorzystany do utworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="ef98a-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="ef98a-141">Ten obiekt można utworzyć przy użyciu polecenia cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="ef98a-141">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="ef98a-142">-Konfiguracje</span><span class="sxs-lookup"><span data-stu-id="ef98a-142">-Configurations</span></span>
<span data-ttu-id="ef98a-143">Określa konfiguracje tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ef98a-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="ef98a-144">Możesz również użyć polecenia cmdlet Add-AzureRmHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="ef98a-144">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="ef98a-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef98a-145">-DefaultProfile</span></span>
<span data-ttu-id="ef98a-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ef98a-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef98a-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ef98a-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="ef98a-148">Określa klucz konta dla domyślnego konta usługi Azure Storage, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ef98a-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="ef98a-149">Możesz również użyć polecenia cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="ef98a-149">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="ef98a-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ef98a-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="ef98a-151">Określa nazwę domyślnego konta magazynu platformy Azure, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ef98a-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="ef98a-152">Możesz również użyć polecenia cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="ef98a-152">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="ef98a-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ef98a-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="ef98a-154">Określa typ domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ef98a-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="ef98a-155">Możliwe wartości to AzureStorage i AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="ef98a-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="ef98a-156">Wartość domyślna to AzureStorage, jeśli nie określono.</span><span class="sxs-lookup"><span data-stu-id="ef98a-156">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="ef98a-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ef98a-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="ef98a-158">Określa nazwę kontenera domyślnego w domyślnym koncie magazynu platformy Azure, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ef98a-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="ef98a-159">Możesz również użyć polecenia cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="ef98a-159">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="ef98a-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="ef98a-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="ef98a-161">Określa prefiks ścieżki na koncie usługi Data Lake Store, które będzie używane przez klaster usługi HDInsight jako domyślny system plików.</span><span class="sxs-lookup"><span data-stu-id="ef98a-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="ef98a-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="ef98a-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="ef98a-163">Określa liczbę dysków dla roli węzła procesu roboczego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="ef98a-163">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="ef98a-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="ef98a-164">-EdgeNodeSize</span></span>
<span data-ttu-id="ef98a-165">Określa rozmiar maszyny wirtualnej dla węzła Edge.</span><span class="sxs-lookup"><span data-stu-id="ef98a-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="ef98a-166">Użyj Get-AzureRmVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ef98a-166">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="ef98a-167">Ten parametr jest prawidłowy tylko w przypadku klastrów RServer.</span><span class="sxs-lookup"><span data-stu-id="ef98a-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="ef98a-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="ef98a-168">-HeadNodeSize</span></span>
<span data-ttu-id="ef98a-169">Określa rozmiar maszyny wirtualnej dla węzła głównego.</span><span class="sxs-lookup"><span data-stu-id="ef98a-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="ef98a-170">Użyj Get-AzureRmVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ef98a-170">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="ef98a-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="ef98a-171">-HiveMetastore</span></span>
<span data-ttu-id="ef98a-172">Określa bazę danych SQL do przechowywania metadanych gałęzi.</span><span class="sxs-lookup"><span data-stu-id="ef98a-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="ef98a-173">Możesz również użyć polecenia cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="ef98a-173">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="ef98a-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="ef98a-174">-HttpCredential</span></span>
<span data-ttu-id="ef98a-175">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="ef98a-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="ef98a-176">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ef98a-176">-Location</span></span>
<span data-ttu-id="ef98a-177">Określa lokalizację klastra.</span><span class="sxs-lookup"><span data-stu-id="ef98a-177">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="ef98a-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ef98a-178">-ObjectId</span></span>
<span data-ttu-id="ef98a-179">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD reprezentujący klaster.</span><span class="sxs-lookup"><span data-stu-id="ef98a-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="ef98a-180">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ef98a-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ef98a-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="ef98a-181">-OozieMetastore</span></span>
<span data-ttu-id="ef98a-182">Określa bazę danych SQL do przechowywania metadanych Oozie.</span><span class="sxs-lookup"><span data-stu-id="ef98a-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="ef98a-183">Możesz również użyć polecenia cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="ef98a-183">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="ef98a-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="ef98a-184">-OSType</span></span>
<span data-ttu-id="ef98a-185">Określa system operacyjny dla klastra.</span><span class="sxs-lookup"><span data-stu-id="ef98a-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="ef98a-186">Dostępne opcje: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="ef98a-186">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="ef98a-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="ef98a-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="ef98a-188">Określa wygaśnięcie jako obiekt DateTime, aby uzyskać dostęp do klastra za pomocą protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="ef98a-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="ef98a-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="ef98a-189">-RdpCredential</span></span>
<span data-ttu-id="ef98a-190">Określa poświadczenia pulpitu zdalnego (RDP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="ef98a-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="ef98a-191">Dotyczy to tylko klastrów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="ef98a-191">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="ef98a-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef98a-192">-ResourceGroupName</span></span>
<span data-ttu-id="ef98a-193">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef98a-193">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ef98a-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="ef98a-194">-ScriptActions</span></span>
<span data-ttu-id="ef98a-195">Określa akcje skryptu, które mają być uruchamiane w klastrze na koniec tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="ef98a-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="ef98a-196">Możesz również użyć dodatku Add-AzureRmHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="ef98a-196">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="ef98a-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="ef98a-197">-SecurityProfile</span></span>
<span data-ttu-id="ef98a-198">Określa właściwości związane z zabezpieczeniami używane do tworzenia bezpiecznego klastra.</span><span class="sxs-lookup"><span data-stu-id="ef98a-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="ef98a-199">Możesz również użyć polecenia cmdlet Add-AzureRmHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="ef98a-199">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="ef98a-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="ef98a-200">-SshCredential</span></span>
<span data-ttu-id="ef98a-201">Określa poświadczenie SSH, które ma być używane dla połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="ef98a-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="ef98a-202">Dotyczy to tylko klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="ef98a-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="ef98a-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ef98a-203">-SshPublicKey</span></span>
<span data-ttu-id="ef98a-204">Określa klucz publiczny, który ma być stosowany do połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="ef98a-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="ef98a-205">Dotyczy to tylko klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="ef98a-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="ef98a-206">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="ef98a-206">-SubnetName</span></span>
<span data-ttu-id="ef98a-207">Określa nazwę podsieci w wybranej sieci wirtualnej klastra.</span><span class="sxs-lookup"><span data-stu-id="ef98a-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="ef98a-208">-Version</span><span class="sxs-lookup"><span data-stu-id="ef98a-208">-Version</span></span>
<span data-ttu-id="ef98a-209">Określa wersję HDI klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ef98a-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="ef98a-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ef98a-210">-VirtualNetworkId</span></span>
<span data-ttu-id="ef98a-211">Określa identyfikator sieci wirtualnej, do której ma być zastrzec klaster.</span><span class="sxs-lookup"><span data-stu-id="ef98a-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="ef98a-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="ef98a-212">-WorkerNodeSize</span></span>
<span data-ttu-id="ef98a-213">Określa rozmiar maszyny wirtualnej dla węzła roboczego.</span><span class="sxs-lookup"><span data-stu-id="ef98a-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="ef98a-214">Użyj Get-AzureRmVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ef98a-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="ef98a-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="ef98a-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="ef98a-216">Określa rozmiar maszyny wirtualnej dla węzła Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="ef98a-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="ef98a-217">Użyj Get-AzureRmVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ef98a-217">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="ef98a-218">Ten parametr jest prawidłowy tylko w przypadku klastrów HBase lub burzy.</span><span class="sxs-lookup"><span data-stu-id="ef98a-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="ef98a-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef98a-219">CommonParameters</span></span>
<span data-ttu-id="ef98a-220">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef98a-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef98a-221">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef98a-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef98a-222">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef98a-222">INPUTS</span></span>

### <span data-ttu-id="ef98a-223">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ef98a-223">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="ef98a-224">Parametry: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef98a-224">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="ef98a-225">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef98a-225">OUTPUTS</span></span>

### <span data-ttu-id="ef98a-226">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ef98a-226">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="ef98a-227">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef98a-227">NOTES</span></span>
<span data-ttu-id="ef98a-228">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, HDInsight, HD, Insights</span><span class="sxs-lookup"><span data-stu-id="ef98a-228">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="ef98a-229">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef98a-229">RELATED LINKS</span></span>

[<span data-ttu-id="ef98a-230">Nowe — AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ef98a-230">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

