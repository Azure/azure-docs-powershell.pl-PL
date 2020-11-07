---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: a372654faa9c3f157c44e5f60ff2f4244cd16d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868252"
---
# <span data-ttu-id="23548-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="23548-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="23548-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23548-102">SYNOPSIS</span></span>
<span data-ttu-id="23548-103">Tworzy klaster usługi Azure HDInsight w określonej grupie zasobów dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="23548-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="23548-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23548-104">SYNTAX</span></span>

### <span data-ttu-id="23548-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="23548-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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

### <span data-ttu-id="23548-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="23548-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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

### <span data-ttu-id="23548-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="23548-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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

## <span data-ttu-id="23548-108">Opis</span><span class="sxs-lookup"><span data-stu-id="23548-108">DESCRIPTION</span></span>
<span data-ttu-id="23548-109">New-AzHDInsightCluster tworzy klaster usługi Azure HDInsight przy użyciu określonych parametrów lub obiektu konfiguracji utworzonego za pomocą polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="23548-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="23548-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23548-110">EXAMPLES</span></span>

### <span data-ttu-id="23548-111">Przykład 1. Tworzenie klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="23548-111">Example 1: Create an Azure HDInsight cluster</span></span>
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

<span data-ttu-id="23548-112">To polecenie tworzy klaster w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="23548-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="23548-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23548-113">PARAMETERS</span></span>

### <span data-ttu-id="23548-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="23548-114">-AadTenantId</span></span>
<span data-ttu-id="23548-115">Określa identyfikator dzierżawy usługi Azure AD, który będzie stosowany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="23548-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="23548-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="23548-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="23548-117">Określa dodatkowe konta magazynu platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="23548-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="23548-118">Możesz również użyć polecenia cmdlet Add-AzHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="23548-118">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="23548-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="23548-119">-CertificateFileContents</span></span>
<span data-ttu-id="23548-120">Określa zawartość pliku certyfikatu, która będzie używana podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="23548-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="23548-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="23548-121">-CertificateFilePath</span></span>
<span data-ttu-id="23548-122">Określa ścieżkę do pliku certyfikatu, który zostanie wykorzystany do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="23548-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="23548-123">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="23548-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="23548-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="23548-124">-CertificatePassword</span></span>
<span data-ttu-id="23548-125">Określa hasło certyfikatu, które zostanie użyte do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="23548-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="23548-126">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="23548-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="23548-127">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="23548-127">-ClusterName</span></span>
<span data-ttu-id="23548-128">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="23548-128">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="23548-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="23548-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="23548-130">Określa liczbę węzłów procesu roboczego klastra.</span><span class="sxs-lookup"><span data-stu-id="23548-130">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="23548-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="23548-131">-ClusterTier</span></span>
<span data-ttu-id="23548-132">Określa poziom klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23548-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="23548-133">Domyślnie jest to standard.</span><span class="sxs-lookup"><span data-stu-id="23548-133">By default, this is Standard.</span></span>
<span data-ttu-id="23548-134">Warstwa Premium może być używana tylko w przypadku klastrów z systemem Linux i umożliwia korzystanie z nowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="23548-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="23548-135">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="23548-135">-ClusterType</span></span>
<span data-ttu-id="23548-136">Określa typ klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="23548-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="23548-137">Dostępne opcje: Hadoop, HBase, burza, Spark</span><span class="sxs-lookup"><span data-stu-id="23548-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="23548-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="23548-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="23548-139">-Config</span><span class="sxs-lookup"><span data-stu-id="23548-139">-Config</span></span>
<span data-ttu-id="23548-140">Określa obiekt klastra, który ma zostać wykorzystany do utworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="23548-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="23548-141">Ten obiekt można utworzyć przy użyciu polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="23548-141">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="23548-142">-Konfiguracje</span><span class="sxs-lookup"><span data-stu-id="23548-142">-Configurations</span></span>
<span data-ttu-id="23548-143">Określa konfiguracje tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23548-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="23548-144">Możesz również użyć polecenia cmdlet Add-AzHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="23548-144">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="23548-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23548-145">-DefaultProfile</span></span>
<span data-ttu-id="23548-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="23548-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23548-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="23548-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="23548-148">Określa klucz konta dla domyślnego konta usługi Azure Storage, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23548-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="23548-149">Możesz również użyć polecenia cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="23548-149">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="23548-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="23548-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="23548-151">Określa nazwę domyślnego konta magazynu platformy Azure, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23548-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="23548-152">Możesz również użyć polecenia cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="23548-152">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="23548-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="23548-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="23548-154">Określa typ domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23548-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="23548-155">Możliwe wartości to AzureStorage i AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="23548-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="23548-156">Wartość domyślna to AzureStorage, jeśli nie określono.</span><span class="sxs-lookup"><span data-stu-id="23548-156">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="23548-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="23548-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="23548-158">Określa nazwę kontenera domyślnego w domyślnym koncie magazynu platformy Azure, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23548-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="23548-159">Możesz również użyć polecenia cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="23548-159">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="23548-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="23548-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="23548-161">Określa prefiks ścieżki na koncie usługi Data Lake Store, które będzie używane przez klaster usługi HDInsight jako domyślny system plików.</span><span class="sxs-lookup"><span data-stu-id="23548-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="23548-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="23548-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="23548-163">Określa liczbę dysków dla roli węzła procesu roboczego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="23548-163">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="23548-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="23548-164">-EdgeNodeSize</span></span>
<span data-ttu-id="23548-165">Określa rozmiar maszyny wirtualnej dla węzła Edge.</span><span class="sxs-lookup"><span data-stu-id="23548-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="23548-166">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23548-166">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="23548-167">Ten parametr jest prawidłowy tylko w przypadku klastrów RServer.</span><span class="sxs-lookup"><span data-stu-id="23548-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="23548-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="23548-168">-HeadNodeSize</span></span>
<span data-ttu-id="23548-169">Określa rozmiar maszyny wirtualnej dla węzła głównego.</span><span class="sxs-lookup"><span data-stu-id="23548-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="23548-170">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23548-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="23548-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="23548-171">-HiveMetastore</span></span>
<span data-ttu-id="23548-172">Określa bazę danych SQL do przechowywania metadanych gałęzi.</span><span class="sxs-lookup"><span data-stu-id="23548-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="23548-173">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="23548-173">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="23548-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="23548-174">-HttpCredential</span></span>
<span data-ttu-id="23548-175">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="23548-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="23548-176">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="23548-176">-Location</span></span>
<span data-ttu-id="23548-177">Określa lokalizację klastra.</span><span class="sxs-lookup"><span data-stu-id="23548-177">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="23548-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="23548-178">-ObjectId</span></span>
<span data-ttu-id="23548-179">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD reprezentujący klaster.</span><span class="sxs-lookup"><span data-stu-id="23548-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="23548-180">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="23548-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="23548-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="23548-181">-OozieMetastore</span></span>
<span data-ttu-id="23548-182">Określa bazę danych SQL do przechowywania metadanych Oozie.</span><span class="sxs-lookup"><span data-stu-id="23548-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="23548-183">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="23548-183">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="23548-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="23548-184">-OSType</span></span>
<span data-ttu-id="23548-185">Określa system operacyjny dla klastra.</span><span class="sxs-lookup"><span data-stu-id="23548-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="23548-186">Dostępne opcje: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="23548-186">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="23548-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="23548-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="23548-188">Określa wygaśnięcie jako obiekt DateTime, aby uzyskać dostęp do klastra za pomocą protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="23548-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="23548-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="23548-189">-RdpCredential</span></span>
<span data-ttu-id="23548-190">Określa poświadczenia pulpitu zdalnego (RDP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="23548-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="23548-191">Dotyczy to tylko klastrów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="23548-191">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="23548-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23548-192">-ResourceGroupName</span></span>
<span data-ttu-id="23548-193">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23548-193">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="23548-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="23548-194">-ScriptActions</span></span>
<span data-ttu-id="23548-195">Określa akcje skryptu, które mają być uruchamiane w klastrze na koniec tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="23548-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="23548-196">Możesz również użyć dodatku Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="23548-196">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="23548-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="23548-197">-SecurityProfile</span></span>
<span data-ttu-id="23548-198">Określa właściwości związane z zabezpieczeniami używane do tworzenia bezpiecznego klastra.</span><span class="sxs-lookup"><span data-stu-id="23548-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="23548-199">Możesz również użyć polecenia cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="23548-199">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="23548-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="23548-200">-SshCredential</span></span>
<span data-ttu-id="23548-201">Określa poświadczenie SSH, które ma być używane dla połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="23548-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="23548-202">Dotyczy to tylko klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="23548-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="23548-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="23548-203">-SshPublicKey</span></span>
<span data-ttu-id="23548-204">Określa klucz publiczny, który ma być stosowany do połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="23548-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="23548-205">Dotyczy to tylko klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="23548-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="23548-206">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="23548-206">-SubnetName</span></span>
<span data-ttu-id="23548-207">Określa nazwę podsieci w wybranej sieci wirtualnej klastra.</span><span class="sxs-lookup"><span data-stu-id="23548-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="23548-208">-Version</span><span class="sxs-lookup"><span data-stu-id="23548-208">-Version</span></span>
<span data-ttu-id="23548-209">Określa wersję HDI klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23548-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="23548-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="23548-210">-VirtualNetworkId</span></span>
<span data-ttu-id="23548-211">Określa identyfikator sieci wirtualnej, do której ma być zastrzec klaster.</span><span class="sxs-lookup"><span data-stu-id="23548-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="23548-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="23548-212">-WorkerNodeSize</span></span>
<span data-ttu-id="23548-213">Określa rozmiar maszyny wirtualnej dla węzła roboczego.</span><span class="sxs-lookup"><span data-stu-id="23548-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="23548-214">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23548-214">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="23548-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="23548-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="23548-216">Określa rozmiar maszyny wirtualnej dla węzła Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="23548-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="23548-217">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="23548-217">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="23548-218">Ten parametr jest prawidłowy tylko w przypadku klastrów HBase lub burzy.</span><span class="sxs-lookup"><span data-stu-id="23548-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="23548-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23548-219">CommonParameters</span></span>
<span data-ttu-id="23548-220">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23548-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23548-221">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23548-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23548-222">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23548-222">INPUTS</span></span>

### <span data-ttu-id="23548-223">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="23548-223">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="23548-224">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23548-224">OUTPUTS</span></span>

### <span data-ttu-id="23548-225">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="23548-225">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="23548-226">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23548-226">NOTES</span></span>
<span data-ttu-id="23548-227">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, HDInsight, HD, Insights</span><span class="sxs-lookup"><span data-stu-id="23548-227">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="23548-228">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23548-228">RELATED LINKS</span></span>

[<span data-ttu-id="23548-229">Nowe — AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="23548-229">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

