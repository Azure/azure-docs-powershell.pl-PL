---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: 9008cb1dba2c39a2c552b2395f4115ca50a17fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063550"
---
# <span data-ttu-id="f8da9-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f8da9-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="f8da9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8da9-102">SYNOPSIS</span></span>
<span data-ttu-id="f8da9-103">Tworzy klaster usługi Azure HDInsight w określonej grupie zasobów dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f8da9-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="f8da9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8da9-104">SYNTAX</span></span>

### <span data-ttu-id="f8da9-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f8da9-105">Default (Default)</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>]
 [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8da9-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f8da9-106">CertificateFilePath</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8da9-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f8da9-107">CertificateFileContents</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8da9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f8da9-108">DESCRIPTION</span></span>
<span data-ttu-id="f8da9-109">New-AzHDInsightCluster tworzy klaster usługi Azure HDInsight przy użyciu określonych parametrów lub obiektu konfiguracji utworzonego za pomocą polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="f8da9-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="f8da9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8da9-110">EXAMPLES</span></span>

### <span data-ttu-id="f8da9-111">Przykład 1. Tworzenie klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="f8da9-111">Example 1: Create an Azure HDInsight cluster</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="f8da9-112">To polecenie tworzy klaster w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f8da9-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="f8da9-113">Przykład 2: Tworzenie klastra za pomocą szyfrowania dysków klucza zarządzanego przez klienta</span><span class="sxs-lookup"><span data-stu-id="f8da9-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
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
        $clusterName = "your-cmk-cluster"
        $clusterCreds = Get-Credential

        # Customer-managed Key info
        $assignedIdentity = "your-ami-resource-id"
        $encryptionKeyName = "new-key"
        $encryptionVaultUri = "https://MyKeyVault.vault.azure.net"
        $encryptionKeyVersion = "00000000000000000000000000000000"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Spark `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="f8da9-114">Przykład 3: Tworzenie klastra usługi Azure HDInsight umożliwiającego szyfrowanie w tranzycie</span><span class="sxs-lookup"><span data-stu-id="f8da9-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="f8da9-115">Przykład 4: Tworzenie klastra usługi Azure HDInsight za pomocą funkcji prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="f8da9-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Virtual network info
        $virtualNetworkId="yourvnetresourceid"
        $subnetName="yoursubnetresourceid"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="f8da9-116">Przykład 5: Tworzenie klastra usługi Azure HDInsight umożliwiającego szyfrowanie na hoście</span><span class="sxs-lookup"><span data-stu-id="f8da9-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="f8da9-117">Przykład 6: Tworzenie klastra usługi Azure HDInsight umożliwiającego automatyczne skalowanie.</span><span class="sxs-lookup"><span data-stu-id="f8da9-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create autoscale configuration
        $autoscaleConfiguration=New-AzHDInsightClusterAutoscaleConfiguration `
            -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

## <span data-ttu-id="f8da9-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8da9-118">PARAMETERS</span></span>

### <span data-ttu-id="f8da9-119">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="f8da9-119">-AadTenantId</span></span>
<span data-ttu-id="f8da9-120">Określa identyfikator dzierżawy usługi Azure AD, który będzie stosowany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8da9-120">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f8da9-121">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="f8da9-121">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="f8da9-122">Określa dodatkowe konta magazynu platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="f8da9-122">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="f8da9-123">Możesz również użyć polecenia cmdlet Add-AzHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="f8da9-123">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="f8da9-124">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="f8da9-124">-ApplicationId</span></span>
<span data-ttu-id="f8da9-125">Pobiera lub ustawia identyfikator aplikacji głównej usługi w celu uzyskania dostępu do usługi Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="f8da9-125">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="f8da9-126">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f8da9-126">-AssignedIdentity</span></span>
<span data-ttu-id="f8da9-127">Pobiera lub ustawia przypisaną tożsamość.</span><span class="sxs-lookup"><span data-stu-id="f8da9-127">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="f8da9-128">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8da9-128">-AutoscaleConfiguration</span></span>
<span data-ttu-id="f8da9-129">Pobiera lub ustawia konfigurację skalowania automatycznego</span><span class="sxs-lookup"><span data-stu-id="f8da9-129">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8da9-130">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f8da9-130">-CertificateFileContents</span></span>
<span data-ttu-id="f8da9-131">Określa zawartość pliku certyfikatu, która będzie używana podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8da9-131">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f8da9-132">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f8da9-132">-CertificateFilePath</span></span>
<span data-ttu-id="f8da9-133">Określa ścieżkę do pliku certyfikatu, który zostanie wykorzystany do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f8da9-133">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f8da9-134">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8da9-134">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f8da9-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f8da9-135">-CertificatePassword</span></span>
<span data-ttu-id="f8da9-136">Określa hasło certyfikatu, które zostanie użyte do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f8da9-136">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f8da9-137">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8da9-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f8da9-138">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="f8da9-138">-ClusterName</span></span>
<span data-ttu-id="f8da9-139">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="f8da9-139">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f8da9-140">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="f8da9-140">-ClusterSizeInNodes</span></span>
<span data-ttu-id="f8da9-141">Określa liczbę węzłów procesu roboczego klastra.</span><span class="sxs-lookup"><span data-stu-id="f8da9-141">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="f8da9-142">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="f8da9-142">-ClusterTier</span></span>
<span data-ttu-id="f8da9-143">Określa poziom klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8da9-143">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="f8da9-144">Domyślnie jest to standard.</span><span class="sxs-lookup"><span data-stu-id="f8da9-144">By default, this is Standard.</span></span>
<span data-ttu-id="f8da9-145">Warstwa Premium może być używana tylko w przypadku klastrów z systemem Linux i umożliwia korzystanie z nowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="f8da9-145">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="f8da9-146">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="f8da9-146">-ClusterType</span></span>
<span data-ttu-id="f8da9-147">Określa typ klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="f8da9-147">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="f8da9-148">Dostępne opcje: Hadoop, HBase, burza, Spark, INTERACTIVEHIVE, Kafka i RServer</span><span class="sxs-lookup"><span data-stu-id="f8da9-148">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="f8da9-149">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="f8da9-149">-ComponentVersion</span></span>
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

### <span data-ttu-id="f8da9-150">-Config</span><span class="sxs-lookup"><span data-stu-id="f8da9-150">-Config</span></span>
<span data-ttu-id="f8da9-151">Określa obiekt klastra, który ma zostać wykorzystany do utworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="f8da9-151">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="f8da9-152">Ten obiekt można utworzyć przy użyciu polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="f8da9-152">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="f8da9-153">-Konfiguracje</span><span class="sxs-lookup"><span data-stu-id="f8da9-153">-Configurations</span></span>
<span data-ttu-id="f8da9-154">Określa konfiguracje tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8da9-154">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="f8da9-155">Możesz również użyć polecenia cmdlet Add-AzHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="f8da9-155">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="f8da9-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8da9-156">-DefaultProfile</span></span>
<span data-ttu-id="f8da9-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f8da9-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8da9-158">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f8da9-158">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="f8da9-159">Określa klucz konta dla domyślnego konta usługi Azure Storage, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8da9-159">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="f8da9-160">Możesz również użyć polecenia cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="f8da9-160">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="f8da9-161">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f8da9-161">-DefaultStorageAccountName</span></span>
<span data-ttu-id="f8da9-162">Określa nazwę domyślnego konta magazynu platformy Azure, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8da9-162">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="f8da9-163">Możesz również użyć polecenia cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="f8da9-163">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="f8da9-164">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f8da9-164">-DefaultStorageAccountType</span></span>
<span data-ttu-id="f8da9-165">Określa typ domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8da9-165">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="f8da9-166">Możliwe wartości to AzureStorage i AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="f8da9-166">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="f8da9-167">Wartość domyślna to AzureStorage, jeśli nie określono.</span><span class="sxs-lookup"><span data-stu-id="f8da9-167">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="f8da9-168">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f8da9-168">-DefaultStorageContainer</span></span>
<span data-ttu-id="f8da9-169">Określa nazwę kontenera domyślnego w domyślnym koncie magazynu platformy Azure, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8da9-169">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="f8da9-170">Możesz również użyć polecenia cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="f8da9-170">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="f8da9-171">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="f8da9-171">-DefaultStorageRootPath</span></span>
<span data-ttu-id="f8da9-172">Określa prefiks ścieżki na koncie usługi Data Lake Store, które będzie używane przez klaster usługi HDInsight jako domyślny system plików.</span><span class="sxs-lookup"><span data-stu-id="f8da9-172">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="f8da9-173">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="f8da9-173">-DisksPerWorkerNode</span></span>
<span data-ttu-id="f8da9-174">Określa liczbę dysków dla roli węzła procesu roboczego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="f8da9-174">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="f8da9-175">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="f8da9-175">-EdgeNodeSize</span></span>
<span data-ttu-id="f8da9-176">Określa rozmiar maszyny wirtualnej dla węzła Edge.</span><span class="sxs-lookup"><span data-stu-id="f8da9-176">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="f8da9-177">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8da9-177">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="f8da9-178">Ten parametr jest prawidłowy tylko w przypadku klastrów RServer.</span><span class="sxs-lookup"><span data-stu-id="f8da9-178">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="f8da9-179">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="f8da9-179">-EncryptionAlgorithm</span></span>
<span data-ttu-id="f8da9-180">Pobiera lub ustawia algorytm szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="f8da9-180">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8da9-181">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="f8da9-181">-EncryptionAtHost</span></span>
<span data-ttu-id="f8da9-182">Pobiera lub ustawia flagę wskazującą, czy włączyć szyfrowanie na hoście.</span><span class="sxs-lookup"><span data-stu-id="f8da9-182">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8da9-183">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="f8da9-183">-EncryptionInTransit</span></span>
<span data-ttu-id="f8da9-184">Pobiera lub ustawia flagę wskazującą, czy włączyć szyfrowanie w tranzycie.</span><span class="sxs-lookup"><span data-stu-id="f8da9-184">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8da9-185">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="f8da9-185">-EncryptionKeyName</span></span>
<span data-ttu-id="f8da9-186">Pobiera lub ustawia nazwę klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="f8da9-186">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="f8da9-187">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f8da9-187">-EncryptionKeyVersion</span></span>
<span data-ttu-id="f8da9-188">Pobiera lub ustawia wersję klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="f8da9-188">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="f8da9-189">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="f8da9-189">-EncryptionVaultUri</span></span>
<span data-ttu-id="f8da9-190">Pobiera lub ustawia identyfikator URI magazynu szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="f8da9-190">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="f8da9-191">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="f8da9-191">-HeadNodeSize</span></span>
<span data-ttu-id="f8da9-192">Określa rozmiar maszyny wirtualnej dla węzła głównego.</span><span class="sxs-lookup"><span data-stu-id="f8da9-192">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="f8da9-193">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8da9-193">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="f8da9-194">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="f8da9-194">-HiveMetastore</span></span>
<span data-ttu-id="f8da9-195">Określa bazę danych SQL do przechowywania metadanych gałęzi.</span><span class="sxs-lookup"><span data-stu-id="f8da9-195">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="f8da9-196">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="f8da9-196">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="f8da9-197">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f8da9-197">-HttpCredential</span></span>
<span data-ttu-id="f8da9-198">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="f8da9-198">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="f8da9-199">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f8da9-199">-Location</span></span>
<span data-ttu-id="f8da9-200">Określa lokalizację klastra.</span><span class="sxs-lookup"><span data-stu-id="f8da9-200">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="f8da9-201">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f8da9-201">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="f8da9-202">Pobiera lub ustawia minimalną obsługiwaną wersję protokołu TLS.</span><span class="sxs-lookup"><span data-stu-id="f8da9-202">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="f8da9-203">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f8da9-203">-ObjectId</span></span>
<span data-ttu-id="f8da9-204">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD reprezentujący klaster.</span><span class="sxs-lookup"><span data-stu-id="f8da9-204">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="f8da9-205">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8da9-205">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f8da9-206">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="f8da9-206">-OozieMetastore</span></span>
<span data-ttu-id="f8da9-207">Określa bazę danych SQL do przechowywania metadanych Oozie.</span><span class="sxs-lookup"><span data-stu-id="f8da9-207">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="f8da9-208">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="f8da9-208">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="f8da9-209">-OSType</span><span class="sxs-lookup"><span data-stu-id="f8da9-209">-OSType</span></span>
<span data-ttu-id="f8da9-210">Określa system operacyjny dla klastra.</span><span class="sxs-lookup"><span data-stu-id="f8da9-210">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="f8da9-211">Dostępne opcje: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="f8da9-211">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="f8da9-212">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="f8da9-212">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="f8da9-213">Pobiera lub ustawia typ dostępu wychodzącego dla sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="f8da9-213">Gets or sets the outbound access type to the public network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PublicLoadBalancer, UDR

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8da9-214">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="f8da9-214">-PublicNetworkAccessType</span></span>
<span data-ttu-id="f8da9-215">Pobiera lub ustawia typ dostępu do sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="f8da9-215">Gets or sets the public network access type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InboundAndOutbound, OutboundOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8da9-216">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="f8da9-216">-RdpAccessExpiry</span></span>
<span data-ttu-id="f8da9-217">Określa wygaśnięcie jako obiekt DateTime, aby uzyskać dostęp do klastra za pomocą protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="f8da9-217">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="f8da9-218">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="f8da9-218">-RdpCredential</span></span>
<span data-ttu-id="f8da9-219">Określa poświadczenia pulpitu zdalnego (RDP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="f8da9-219">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="f8da9-220">Dotyczy to tylko klastrów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="f8da9-220">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="f8da9-221">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8da9-221">-ResourceGroupName</span></span>
<span data-ttu-id="f8da9-222">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f8da9-222">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f8da9-223">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="f8da9-223">-ScriptActions</span></span>
<span data-ttu-id="f8da9-224">Określa akcje skryptu, które mają być uruchamiane w klastrze na koniec tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="f8da9-224">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="f8da9-225">Możesz również użyć dodatku Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="f8da9-225">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="f8da9-226">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="f8da9-226">-SecurityProfile</span></span>
<span data-ttu-id="f8da9-227">Określa właściwości związane z zabezpieczeniami używane do tworzenia bezpiecznego klastra.</span><span class="sxs-lookup"><span data-stu-id="f8da9-227">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="f8da9-228">Możesz również użyć polecenia cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="f8da9-228">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="f8da9-229">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="f8da9-229">-SshCredential</span></span>
<span data-ttu-id="f8da9-230">Określa poświadczenie SSH, które ma być używane dla połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="f8da9-230">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="f8da9-231">Dotyczy to tylko klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="f8da9-231">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="f8da9-232">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f8da9-232">-SshPublicKey</span></span>
<span data-ttu-id="f8da9-233">Określa klucz publiczny, który ma być stosowany do połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="f8da9-233">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="f8da9-234">Dotyczy to tylko klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="f8da9-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="f8da9-235">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="f8da9-235">-SubnetName</span></span>
<span data-ttu-id="f8da9-236">Określa nazwę podsieci w wybranej sieci wirtualnej klastra.</span><span class="sxs-lookup"><span data-stu-id="f8da9-236">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="f8da9-237">-Version</span><span class="sxs-lookup"><span data-stu-id="f8da9-237">-Version</span></span>
<span data-ttu-id="f8da9-238">Określa wersję HDI klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8da9-238">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="f8da9-239">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f8da9-239">-VirtualNetworkId</span></span>
<span data-ttu-id="f8da9-240">Określa identyfikator sieci wirtualnej, do której ma być zastrzec klaster.</span><span class="sxs-lookup"><span data-stu-id="f8da9-240">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="f8da9-241">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="f8da9-241">-WorkerNodeSize</span></span>
<span data-ttu-id="f8da9-242">Określa rozmiar maszyny wirtualnej dla węzła roboczego.</span><span class="sxs-lookup"><span data-stu-id="f8da9-242">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="f8da9-243">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8da9-243">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="f8da9-244">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="f8da9-244">-ZookeeperNodeSize</span></span>
<span data-ttu-id="f8da9-245">Określa rozmiar maszyny wirtualnej dla węzła Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="f8da9-245">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="f8da9-246">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f8da9-246">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="f8da9-247">Ten parametr jest prawidłowy tylko w przypadku klastrów HBase lub burzy.</span><span class="sxs-lookup"><span data-stu-id="f8da9-247">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="f8da9-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8da9-248">CommonParameters</span></span>
<span data-ttu-id="f8da9-249">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8da9-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8da9-250">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8da9-250">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8da9-251">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8da9-251">INPUTS</span></span>

### <span data-ttu-id="f8da9-252">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f8da9-252">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f8da9-253">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8da9-253">OUTPUTS</span></span>

### <span data-ttu-id="f8da9-254">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f8da9-254">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="f8da9-255">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8da9-255">NOTES</span></span>
<span data-ttu-id="f8da9-256">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, HDInsight, HD, Insights</span><span class="sxs-lookup"><span data-stu-id="f8da9-256">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="f8da9-257">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8da9-257">RELATED LINKS</span></span>

[<span data-ttu-id="f8da9-258">Nowe — AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f8da9-258">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

