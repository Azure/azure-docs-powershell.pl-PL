---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: bc89dff9fa6feecf38f0d9f81efb3bdc18c70641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719315"
---
# <span data-ttu-id="d9699-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d9699-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="d9699-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9699-102">SYNOPSIS</span></span>
<span data-ttu-id="d9699-103">Tworzy klaster usługi Azure HDInsight w określonej grupie zasobów dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d9699-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9699-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9699-104">SYNTAX</span></span>

### <span data-ttu-id="d9699-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d9699-105">Default (Default)</span></span>
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
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9699-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="d9699-106">CertificateFilePath</span></span>
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
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9699-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="d9699-107">CertificateFileContents</span></span>
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
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9699-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d9699-108">DESCRIPTION</span></span>
<span data-ttu-id="d9699-109">New-AzureHDInsightCluster tworzy klaster usługi Azure HDInsight przy użyciu określonych parametrów lub obiektu konfiguracji utworzonego za pomocą polecenia cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="d9699-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="d9699-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9699-110">EXAMPLES</span></span>

### <span data-ttu-id="d9699-111">--------------------------Przykład 1: Tworzenie klastra usługi Azure HDInsight--------------------------</span><span class="sxs-lookup"><span data-stu-id="d9699-111">--------------------------  Example 1: Create an Azure HDInsight cluster  --------------------------</span></span>
<span data-ttu-id="d9699-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="d9699-112">@{paragraph=PS C:\\\>}</span></span>









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

<span data-ttu-id="d9699-113">To polecenie tworzy klaster w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d9699-113">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="d9699-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9699-114">PARAMETERS</span></span>

### <span data-ttu-id="d9699-115">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="d9699-115">-AadTenantId</span></span>
<span data-ttu-id="d9699-116">Określa identyfikator dzierżawy usługi Azure AD, który będzie stosowany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d9699-116">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d9699-117">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="d9699-117">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="d9699-118">Określa dodatkowe konta magazynu platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="d9699-118">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="d9699-119">Możesz również użyć polecenia cmdlet Add-AzureRmHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="d9699-119">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="d9699-120">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="d9699-120">-CertificateFileContents</span></span>
<span data-ttu-id="d9699-121">Określa zawartość pliku certyfikatu, która będzie używana podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d9699-121">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d9699-122">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="d9699-122">-CertificateFilePath</span></span>
<span data-ttu-id="d9699-123">Określa ścieżkę do pliku certyfikatu, który zostanie wykorzystany do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="d9699-123">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="d9699-124">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d9699-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d9699-125">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="d9699-125">-CertificatePassword</span></span>
<span data-ttu-id="d9699-126">Określa hasło certyfikatu, które zostanie użyte do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="d9699-126">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="d9699-127">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d9699-127">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d9699-128">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="d9699-128">-ClusterName</span></span>
<span data-ttu-id="d9699-129">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="d9699-129">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d9699-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="d9699-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="d9699-131">Określa liczbę węzłów procesu roboczego klastra.</span><span class="sxs-lookup"><span data-stu-id="d9699-131">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="d9699-132">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="d9699-132">-ClusterTier</span></span>
<span data-ttu-id="d9699-133">Określa poziom klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d9699-133">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="d9699-134">Domyślnie jest to standard.</span><span class="sxs-lookup"><span data-stu-id="d9699-134">By default, this is Standard.</span></span>
<span data-ttu-id="d9699-135">Warstwa Premium może być używana tylko w przypadku klastrów z systemem Linux i umożliwia korzystanie z nowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="d9699-135">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="d9699-136">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="d9699-136">-ClusterType</span></span>
<span data-ttu-id="d9699-137">Określa typ klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="d9699-137">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="d9699-138">Dostępne opcje: Hadoop, HBase, burza, Spark</span><span class="sxs-lookup"><span data-stu-id="d9699-138">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="d9699-139">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="d9699-139">-ComponentVersion</span></span>
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

### <span data-ttu-id="d9699-140">-Config</span><span class="sxs-lookup"><span data-stu-id="d9699-140">-Config</span></span>
<span data-ttu-id="d9699-141">Określa obiekt klastra, który ma zostać wykorzystany do utworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="d9699-141">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="d9699-142">Ten obiekt można utworzyć przy użyciu polecenia cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="d9699-142">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="d9699-143">-Konfiguracje</span><span class="sxs-lookup"><span data-stu-id="d9699-143">-Configurations</span></span>
<span data-ttu-id="d9699-144">Określa konfiguracje tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d9699-144">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="d9699-145">Możesz również użyć polecenia cmdlet Add-AzureRmHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="d9699-145">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="d9699-146">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d9699-146">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="d9699-147">Określa klucz konta dla domyślnego konta usługi Azure Storage, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d9699-147">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="d9699-148">Możesz również użyć polecenia cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="d9699-148">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="d9699-149">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d9699-149">-DefaultStorageAccountName</span></span>
<span data-ttu-id="d9699-150">Określa nazwę domyślnego konta magazynu platformy Azure, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d9699-150">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="d9699-151">Możesz również użyć polecenia cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="d9699-151">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="d9699-152">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d9699-152">-DefaultStorageAccountType</span></span>
<span data-ttu-id="d9699-153">Określa typ domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d9699-153">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="d9699-154">Możliwe wartości to AzureStorage i AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="d9699-154">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="d9699-155">Wartość domyślna to AzureStorage, jeśli nie określono.</span><span class="sxs-lookup"><span data-stu-id="d9699-155">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="d9699-156">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d9699-156">-DefaultStorageContainer</span></span>
<span data-ttu-id="d9699-157">Określa nazwę kontenera domyślnego w domyślnym koncie magazynu platformy Azure, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d9699-157">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="d9699-158">Możesz również użyć polecenia cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="d9699-158">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="d9699-159">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="d9699-159">-DefaultStorageRootPath</span></span>
<span data-ttu-id="d9699-160">Określa prefiks ścieżki na koncie usługi Data Lake Store, które będzie używane przez klaster usługi HDInsight jako domyślny system plików.</span><span class="sxs-lookup"><span data-stu-id="d9699-160">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="d9699-161">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="d9699-161">-EdgeNodeSize</span></span>
<span data-ttu-id="d9699-162">Określa rozmiar maszyny wirtualnej dla węzła Edge.</span><span class="sxs-lookup"><span data-stu-id="d9699-162">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="d9699-163">Użyj Get-AzureRmVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d9699-163">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="d9699-164">Ten parametr jest prawidłowy tylko w przypadku klastrów RServer.</span><span class="sxs-lookup"><span data-stu-id="d9699-164">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="d9699-165">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="d9699-165">-HeadNodeSize</span></span>
<span data-ttu-id="d9699-166">Określa rozmiar maszyny wirtualnej dla węzła głównego.</span><span class="sxs-lookup"><span data-stu-id="d9699-166">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="d9699-167">Użyj Get-AzureRmVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d9699-167">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="d9699-168">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="d9699-168">-HiveMetastore</span></span>
<span data-ttu-id="d9699-169">Określa bazę danych SQL do przechowywania metadanych gałęzi.</span><span class="sxs-lookup"><span data-stu-id="d9699-169">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="d9699-170">Możesz również użyć polecenia cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="d9699-170">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="d9699-171">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d9699-171">-HttpCredential</span></span>
<span data-ttu-id="d9699-172">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="d9699-172">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="d9699-173">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d9699-173">-Location</span></span>
<span data-ttu-id="d9699-174">Określa lokalizację klastra.</span><span class="sxs-lookup"><span data-stu-id="d9699-174">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="d9699-175">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d9699-175">-ObjectId</span></span>
<span data-ttu-id="d9699-176">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD reprezentujący klaster.</span><span class="sxs-lookup"><span data-stu-id="d9699-176">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="d9699-177">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d9699-177">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="d9699-178">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="d9699-178">-OozieMetastore</span></span>
<span data-ttu-id="d9699-179">Określa bazę danych SQL do przechowywania metadanych Oozie.</span><span class="sxs-lookup"><span data-stu-id="d9699-179">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="d9699-180">Możesz również użyć polecenia cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="d9699-180">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="d9699-181">-OSType</span><span class="sxs-lookup"><span data-stu-id="d9699-181">-OSType</span></span>
<span data-ttu-id="d9699-182">Określa system operacyjny dla klastra.</span><span class="sxs-lookup"><span data-stu-id="d9699-182">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="d9699-183">Dostępne opcje: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="d9699-183">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="d9699-184">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="d9699-184">-RdpAccessExpiry</span></span>
<span data-ttu-id="d9699-185">Określa wygaśnięcie jako obiekt DateTime, aby uzyskać dostęp do klastra za pomocą protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="d9699-185">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="d9699-186">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="d9699-186">-RdpCredential</span></span>
<span data-ttu-id="d9699-187">Określa poświadczenia pulpitu zdalnego (RDP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="d9699-187">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="d9699-188">Dotyczy to tylko klastrów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="d9699-188">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="d9699-189">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9699-189">-ResourceGroupName</span></span>
<span data-ttu-id="d9699-190">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9699-190">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d9699-191">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="d9699-191">-ScriptActions</span></span>
<span data-ttu-id="d9699-192">Określa akcje skryptu, które mają być uruchamiane w klastrze na koniec tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="d9699-192">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="d9699-193">Możesz również użyć dodatku Add-AzureRmHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="d9699-193">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="d9699-194">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="d9699-194">-SecurityProfile</span></span>
<span data-ttu-id="d9699-195">Określa właściwości związane z zabezpieczeniami używane do tworzenia bezpiecznego klastra.</span><span class="sxs-lookup"><span data-stu-id="d9699-195">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="d9699-196">Możesz również użyć polecenia cmdlet Add-AzureRmHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="d9699-196">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="d9699-197">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="d9699-197">-SshCredential</span></span>
<span data-ttu-id="d9699-198">Określa poświadczenie SSH, które ma być używane dla połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="d9699-198">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="d9699-199">Dotyczy to tylko klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="d9699-199">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="d9699-200">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d9699-200">-SshPublicKey</span></span>
<span data-ttu-id="d9699-201">Określa klucz publiczny, który ma być stosowany do połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="d9699-201">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="d9699-202">Dotyczy to tylko klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="d9699-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="d9699-203">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="d9699-203">-SubnetName</span></span>
<span data-ttu-id="d9699-204">Określa nazwę podsieci w wybranej sieci wirtualnej klastra.</span><span class="sxs-lookup"><span data-stu-id="d9699-204">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="d9699-205">-Version</span><span class="sxs-lookup"><span data-stu-id="d9699-205">-Version</span></span>
<span data-ttu-id="d9699-206">Określa wersję HDI klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d9699-206">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="d9699-207">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d9699-207">-VirtualNetworkId</span></span>
<span data-ttu-id="d9699-208">Określa identyfikator sieci wirtualnej, do której ma być zastrzec klaster.</span><span class="sxs-lookup"><span data-stu-id="d9699-208">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="d9699-209">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="d9699-209">-WorkerNodeSize</span></span>
<span data-ttu-id="d9699-210">Określa rozmiar maszyny wirtualnej dla węzła roboczego.</span><span class="sxs-lookup"><span data-stu-id="d9699-210">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="d9699-211">Użyj Get-AzureRmVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d9699-211">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="d9699-212">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="d9699-212">-ZookeeperNodeSize</span></span>
<span data-ttu-id="d9699-213">Określa rozmiar maszyny wirtualnej dla węzła Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="d9699-213">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="d9699-214">Użyj Get-AzureRmVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d9699-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="d9699-215">Ten parametr jest prawidłowy tylko w przypadku klastrów HBase lub burzy.</span><span class="sxs-lookup"><span data-stu-id="d9699-215">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="d9699-216">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9699-216">-DefaultProfile</span></span>
<span data-ttu-id="d9699-217">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9699-217">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9699-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9699-218">CommonParameters</span></span>
<span data-ttu-id="d9699-219">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9699-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9699-220">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9699-220">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9699-221">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9699-221">INPUTS</span></span>

### <span data-ttu-id="d9699-222">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d9699-222">AzureHDInsightConfig</span></span>
<span data-ttu-id="d9699-223">Parametr "config" akceptuje wartość typu "AzureHDInsightConfig" z procesu</span><span class="sxs-lookup"><span data-stu-id="d9699-223">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="d9699-224">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9699-224">OUTPUTS</span></span>

### <span data-ttu-id="d9699-225">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d9699-225">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="d9699-226">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9699-226">NOTES</span></span>
<span data-ttu-id="d9699-227">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, HDInsight, HD, Insights</span><span class="sxs-lookup"><span data-stu-id="d9699-227">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="d9699-228">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9699-228">RELATED LINKS</span></span>

[<span data-ttu-id="d9699-229">Nowe — AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="d9699-229">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

