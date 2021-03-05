---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: 94b982eb2add8341b861732bef5e63d88e67a937
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009057"
---
# <span data-ttu-id="f2df1-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f2df1-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="f2df1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2df1-102">SYNOPSIS</span></span>
<span data-ttu-id="f2df1-103">Tworzy klaster usługi Azure HDInsight w określonej grupie zasobów dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f2df1-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="f2df1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f2df1-104">SYNTAX</span></span>

### <span data-ttu-id="f2df1-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f2df1-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-StorageAccountManagedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker] [-KafkaClientGroupId <String>]
 [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>] [-PrivateLink <String>]
 [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2df1-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f2df1-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2df1-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f2df1-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2df1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f2df1-108">DESCRIPTION</span></span>
<span data-ttu-id="f2df1-109">Ten New-AzHDInsightCluster tworzy klaster usługi Azure HDInsight przy użyciu określonych parametrów lub obiektu konfiguracji utworzonego za pomocą New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2df1-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="f2df1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f2df1-110">EXAMPLES</span></span>

### <span data-ttu-id="f2df1-111">Przykład 1. Tworzenie klastrów usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="f2df1-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="f2df1-112">To polecenie tworzy klaster w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f2df1-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="f2df1-113">Przykład 2. Tworzenie klastrów przy użyciu szyfrowania dysków zarządzanych przez klienta</span><span class="sxs-lookup"><span data-stu-id="f2df1-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="f2df1-114">Przykład 3. Tworzenie klastrów usługi Azure HDInsight, które umożliwia szyfrowanie podczas przesyłania</span><span class="sxs-lookup"><span data-stu-id="f2df1-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}}
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="f2df1-115">Przykład 4. Tworzenie klastrów usługi Azure HDInsight z funkcją przekazywania wychodzącego i prywatnego linku</span><span class="sxs-lookup"><span data-stu-id="f2df1-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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
        $subnetName="yoursubnetname"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -ResourceProviderConnection Outbound -PrivateLink Enabled `
```

### <span data-ttu-id="f2df1-116">Przykład 5. Tworzenie klastrów usługi Azure HDInsight, które umożliwia szyfrowanie na hoście</span><span class="sxs-lookup"><span data-stu-id="f2df1-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="f2df1-117">Przykład 6. Tworzenie klastrów usługi Azure HDInsight, które umożliwia automatyczne skalowanie.</span><span class="sxs-lookup"><span data-stu-id="f2df1-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

### <span data-ttu-id="f2df1-118">Przykład 7. Tworzenie klastrów usługi Azure HDInsight z serwerem proxy usługi Kafka Rest.</span><span class="sxs-lookup"><span data-stu-id="f2df1-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Kafka Rest Proxy configuration info
        $kafkaClientGroupName = "yourclientgroupname"
        $kafkaClientGroupId = "yourclientgroupid"
        $kafkaManagementNodeSize = "Standard_D4_v2"
        $disksPerWorkerNode = 2

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Kafka `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -KafkaClientGroupId  $kafkaClientGroupId -KafkaClientGroupName $kafkaClientGroupName `
            -KafkaManagementNodeSize $kafkaManagementNodeSize -DisksPerWorkerNode $disksPerWorkerNode
```

### <span data-ttu-id="f2df1-119">Przykład 8. Tworzenie klastrów usługi Azure HDInsight przy użyciu magazynu usługi Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="f2df1-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageManagedIdentity = "yourstorageusermanagedidentity"
        $storageFileSystem = "filesystem01"
        $storageAccountType=AzureDataLakeStorageGen2

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
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountManagedIdentity $storageManagedIdentity `
            -StorageFileSystem $storageFileSystem `
            -StorageAccountType $storageAccountType `
            -SshCredential $clusterCreds
```

### <span data-ttu-id="f2df1-120">Przykład 9. Tworzenie klastrów usługi Azure HDInsight przy użyciu pakietu zabezpieczeń przedsiębiorstwa (ESP) i włączanie pośrednictwa identyfikatorów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f2df1-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountKey = "yourstorageaccountaccesskey"
        $storageContainer = "yourcontainer01"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # ESP configuration
        $domainResourceId = "your Azure AD Domin Service resource id"
        $domainUser = "yourdomainuser"
        $domainPassword = "yourdoaminpasswd"
        $domainPassword = ConvertTo-SecureString $domainPassword -AsPlainText -Force
        $domainCredential = New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
        $clusterUserGroupDns = "dominusergroup"
        $ldapUrls = "ldaps://{your domain name}:636"

        $clusterTier = Premium
        $vnetId = "yourvnetid"
        $subnetName = "yoursubnetname"
        $assignedIdentity = "your user managed assigned identity resourcee id"

        #Create security profile
        $config= New-AzHDInsightClusterConfig|Add-AzHDInsightSecurityProfile -DomainResourceId $domainResourceId -DomainUserCredential $domainCredential -LdapsUrls $ldapUrls -ClusterUsersGroupDNs $clusterUserGroupDns

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusteTier $clusterTier `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $vnetId -SubnetName $subnetName `
            -AssignedIdentity $assignedIdentity `
            -SecurityProfile $config.SecurityProfile -EnableIDBroker
```

### <span data-ttu-id="f2df1-121">Przykład 10. Utwórz klaster usługi Azure HDInsight, który umożliwia izolacji obliczeniowej.</span><span class="sxs-lookup"><span data-stu-id="f2df1-121">Example 10: Create an Azure HDInsight cluster which enables compute isolation.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential
        $workerNodeSize="Standard_E16S_V3" # here is just an example
        $headNodeSize="Standard_E8S_V3"
        $zookeeperNodeSize="Standard_E2S_V3"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -WorkerNodeSize $workerNodeSize `
            -HeadNodeSize $headNodeSize `
            -ZookeeperNodeSize $zookeeperNodeSize `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EnableComputeIsolation `
```

## <span data-ttu-id="f2df1-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2df1-122">PARAMETERS</span></span>

### <span data-ttu-id="f2df1-123">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="f2df1-123">-AadTenantId</span></span>
<span data-ttu-id="f2df1-124">Określa identyfikator dzierżawy usługi Azure AD, który będzie używany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f2df1-124">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f2df1-125">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="f2df1-125">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="f2df1-126">Określa dodatkowe konta magazynu platformy Azure dla klastrów.</span><span class="sxs-lookup"><span data-stu-id="f2df1-126">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="f2df1-127">Możesz również użyć polecenia cmdlet Add-AzHDInsightStorage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2df1-127">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="f2df1-128">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="f2df1-128">-AmbariDatabase</span></span>
<span data-ttu-id="f2df1-129">Pobiera lub ustawia bazę danych dla ambari.</span><span class="sxs-lookup"><span data-stu-id="f2df1-129">Gets or sets the database for ambari.</span></span>

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

### <span data-ttu-id="f2df1-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f2df1-130">-ApplicationId</span></span>
<span data-ttu-id="f2df1-131">Pobiera lub ustawia główny identyfikator aplikacji usługi na celu uzyskanie dostępu do usługi Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="f2df1-131">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="f2df1-132">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f2df1-132">-AssignedIdentity</span></span>
<span data-ttu-id="f2df1-133">Pobiera lub ustawia przypisaną tożsamość.</span><span class="sxs-lookup"><span data-stu-id="f2df1-133">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="f2df1-134">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2df1-134">-AutoscaleConfiguration</span></span>
<span data-ttu-id="f2df1-135">Pobiera lub ustawia konfigurację automatycznego skalowania</span><span class="sxs-lookup"><span data-stu-id="f2df1-135">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="f2df1-136">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="f2df1-136">-CertificateFileContents</span></span>
<span data-ttu-id="f2df1-137">Określa zawartość pliku certyfikatu, który będzie używany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f2df1-137">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f2df1-138">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f2df1-138">-CertificateFilePath</span></span>
<span data-ttu-id="f2df1-139">Określa ścieżkę pliku do certyfikatu, który będzie używany do uwierzytelniania jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f2df1-139">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f2df1-140">Klaster będzie korzystać z tej funkcji podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f2df1-140">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f2df1-141">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f2df1-141">-CertificatePassword</span></span>
<span data-ttu-id="f2df1-142">Określa hasło certyfikatu, który będzie używany do uwierzytelniania jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="f2df1-142">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="f2df1-143">Klaster będzie korzystać z tej funkcji podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f2df1-143">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f2df1-144">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f2df1-144">-ClusterName</span></span>
<span data-ttu-id="f2df1-145">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="f2df1-145">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f2df1-146">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="f2df1-146">-ClusterSizeInNodes</span></span>
<span data-ttu-id="f2df1-147">Określa liczbę węzłów pracownik w klastrze.</span><span class="sxs-lookup"><span data-stu-id="f2df1-147">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="f2df1-148">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="f2df1-148">-ClusterTier</span></span>
<span data-ttu-id="f2df1-149">Określa warstwę klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f2df1-149">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="f2df1-150">Domyślnie jest to ustawienie Standardowe.</span><span class="sxs-lookup"><span data-stu-id="f2df1-150">By default, this is Standard.</span></span>
<span data-ttu-id="f2df1-151">Warstwa Premium może być używana tylko z klastrami systemu Linux i umożliwia korzystanie z niektórych nowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="f2df1-151">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="f2df1-152">- ClusterType</span><span class="sxs-lookup"><span data-stu-id="f2df1-152">-ClusterType</span></span>
<span data-ttu-id="f2df1-153">Określa typ klastrów do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="f2df1-153">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="f2df1-154">Dostępne opcje: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka i RServer</span><span class="sxs-lookup"><span data-stu-id="f2df1-154">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="f2df1-155">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="f2df1-155">-ComponentVersion</span></span>
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

### <span data-ttu-id="f2df1-156">-ComputeIsolationHostSku</span><span class="sxs-lookup"><span data-stu-id="f2df1-156">-ComputeIsolationHostSku</span></span>
<span data-ttu-id="f2df1-157">Pobiera lub ustawia dedykowaną jednostkę SKU hosta dla izolacji obliczeniowej.</span><span class="sxs-lookup"><span data-stu-id="f2df1-157">Gets or sets the dedicated host sku for compute isolation.</span></span>

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

### <span data-ttu-id="f2df1-158">-Config</span><span class="sxs-lookup"><span data-stu-id="f2df1-158">-Config</span></span>
<span data-ttu-id="f2df1-159">Określa obiekt klastrów, który ma być używany do tworzenia klastrów.</span><span class="sxs-lookup"><span data-stu-id="f2df1-159">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="f2df1-160">Ten obiekt można utworzyć za pomocą New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2df1-160">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="f2df1-161">— Konfiguracje</span><span class="sxs-lookup"><span data-stu-id="f2df1-161">-Configurations</span></span>
<span data-ttu-id="f2df1-162">Określa konfiguracje tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f2df1-162">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="f2df1-163">Możesz również użyć polecenia cmdlet Add-AzHDInsightConfigValues cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2df1-163">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="f2df1-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2df1-164">-DefaultProfile</span></span>
<span data-ttu-id="f2df1-165">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f2df1-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2df1-166">-WąsyPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="f2df1-166">-DisksPerWorkerNode</span></span>
<span data-ttu-id="f2df1-167">Określa liczbę dysków dla roli węzła pracownika w klastrze.</span><span class="sxs-lookup"><span data-stu-id="f2df1-167">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="f2df1-168">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="f2df1-168">-EdgeNodeSize</span></span>
<span data-ttu-id="f2df1-169">Określa rozmiar maszyny wirtualnej dla węzła brzegowego.</span><span class="sxs-lookup"><span data-stu-id="f2df1-169">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="f2df1-170">Użyj Get-AzVMSize dla akceptowalnych rozmiarów maszyn wirtualnych i zobacz stronę cenową usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f2df1-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="f2df1-171">Ten parametr jest prawidłowy tylko dla klastrów serwera RServer.</span><span class="sxs-lookup"><span data-stu-id="f2df1-171">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="f2df1-172">-EnableComputeIsolation</span><span class="sxs-lookup"><span data-stu-id="f2df1-172">-EnableComputeIsolation</span></span>
<span data-ttu-id="f2df1-173">Włącza funkcję izolacji obliczeniowej HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f2df1-173">Enables HDInsight compute isolation feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2df1-174">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="f2df1-174">-EnableIDBroker</span></span>
<span data-ttu-id="f2df1-175">Umożliwia korzystanie z funkcji doradców tożsamości usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f2df1-175">Enables HDInsight Identity Broker feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2df1-176">— EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="f2df1-176">-EncryptionAlgorithm</span></span>
<span data-ttu-id="f2df1-177">Pobiera lub ustawia algorytm szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="f2df1-177">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="f2df1-178">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="f2df1-178">-EncryptionAtHost</span></span>
<span data-ttu-id="f2df1-179">Pobiera lub ustawia flagę wskazującą, czy włączyć szyfrowanie u hosta, czy nie.</span><span class="sxs-lookup"><span data-stu-id="f2df1-179">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="f2df1-180">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="f2df1-180">-EncryptionInTransit</span></span>
<span data-ttu-id="f2df1-181">Pobiera lub ustawia flagę wskazującą, czy włączyć szyfrowanie podczas przesyłania.</span><span class="sxs-lookup"><span data-stu-id="f2df1-181">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="f2df1-182">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="f2df1-182">-EncryptionKeyName</span></span>
<span data-ttu-id="f2df1-183">Pobiera lub ustawia nazwę klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="f2df1-183">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="f2df1-184">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="f2df1-184">-EncryptionKeyVersion</span></span>
<span data-ttu-id="f2df1-185">Pobiera lub ustawia wersję klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="f2df1-185">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="f2df1-186">- EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="f2df1-186">-EncryptionVaultUri</span></span>
<span data-ttu-id="f2df1-187">Pobiera lub ustawia uri magazynu szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="f2df1-187">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="f2df1-188">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="f2df1-188">-HeadNodeSize</span></span>
<span data-ttu-id="f2df1-189">Określa rozmiar maszyny wirtualnej dla węzła Head.</span><span class="sxs-lookup"><span data-stu-id="f2df1-189">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="f2df1-190">Użyj Get-AzVMSize dla akceptowalnych rozmiarów maszyn wirtualnych i zobacz stronę cenową usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f2df1-190">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="f2df1-191">- GałąźMetastore</span><span class="sxs-lookup"><span data-stu-id="f2df1-191">-HiveMetastore</span></span>
<span data-ttu-id="f2df1-192">Określa bazę danych SQL do przechowywania metadanych Programu Sql.</span><span class="sxs-lookup"><span data-stu-id="f2df1-192">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="f2df1-193">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2df1-193">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="f2df1-194">- HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f2df1-194">-HttpCredential</span></span>
<span data-ttu-id="f2df1-195">Określa poświadczenia logowania klastrów (HTTP) dla tego klastra.</span><span class="sxs-lookup"><span data-stu-id="f2df1-195">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="f2df1-196">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="f2df1-196">-KafkaClientGroupId</span></span>
<span data-ttu-id="f2df1-197">Pobiera lub ustawia identyfikator grupy klienta dla dostępu serwera proxy Rest usługi Kafka.</span><span class="sxs-lookup"><span data-stu-id="f2df1-197">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="f2df1-198">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="f2df1-198">-KafkaClientGroupName</span></span>
<span data-ttu-id="f2df1-199">Pobiera lub ustawia nazwę grupy klienta dla dostępu serwera proxy Rest platformy Kafka.</span><span class="sxs-lookup"><span data-stu-id="f2df1-199">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="f2df1-200">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="f2df1-200">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="f2df1-201">Pobiera lub ustawia rozmiar węzła zarządzania kafką.</span><span class="sxs-lookup"><span data-stu-id="f2df1-201">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="f2df1-202">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f2df1-202">-Location</span></span>
<span data-ttu-id="f2df1-203">Określa lokalizację klastrów.</span><span class="sxs-lookup"><span data-stu-id="f2df1-203">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="f2df1-204">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="f2df1-204">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="f2df1-205">Pobiera lub ustawia minimalną obsługiwaną wersję TLS.</span><span class="sxs-lookup"><span data-stu-id="f2df1-205">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="f2df1-206">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f2df1-206">-ObjectId</span></span>
<span data-ttu-id="f2df1-207">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD, który reprezentuje klaster.</span><span class="sxs-lookup"><span data-stu-id="f2df1-207">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="f2df1-208">Klaster będzie korzystać z tej funkcji podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f2df1-208">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="f2df1-209">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="f2df1-209">-OozieMetastore</span></span>
<span data-ttu-id="f2df1-210">Określa bazę danych SQL do przechowywania metadanych Oozie.</span><span class="sxs-lookup"><span data-stu-id="f2df1-210">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="f2df1-211">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2df1-211">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="f2df1-212">- OSType</span><span class="sxs-lookup"><span data-stu-id="f2df1-212">-OSType</span></span>
<span data-ttu-id="f2df1-213">Określa system operacyjny dla klastra.</span><span class="sxs-lookup"><span data-stu-id="f2df1-213">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="f2df1-214">Dostępne opcje: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="f2df1-214">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="f2df1-215">- PrivateLink</span><span class="sxs-lookup"><span data-stu-id="f2df1-215">-PrivateLink</span></span>
<span data-ttu-id="f2df1-216">Pobiera lub ustawia prywatny typ linku.</span><span class="sxs-lookup"><span data-stu-id="f2df1-216">Gets or sets the private link type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2df1-217">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="f2df1-217">-RdpAccessExpiry</span></span>
<span data-ttu-id="f2df1-218">Określa wygasanie dostępu do klastrów za pomocą protokołu RDP (Remote Desktop Protocol) jako obiektu DateTime.</span><span class="sxs-lookup"><span data-stu-id="f2df1-218">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="f2df1-219">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="f2df1-219">-RdpCredential</span></span>
<span data-ttu-id="f2df1-220">Określa poświadczenia pulpitu zdalnego (RDP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="f2df1-220">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="f2df1-221">Dotyczy to tylko klastrów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="f2df1-221">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="f2df1-222">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2df1-222">-ResourceGroupName</span></span>
<span data-ttu-id="f2df1-223">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2df1-223">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f2df1-224">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="f2df1-224">-ResourceProviderConnection</span></span>
<span data-ttu-id="f2df1-225">Pobiera lub ustawia typ połączenia dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f2df1-225">Gets or sets the resource provider connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2df1-226">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="f2df1-226">-ScriptActions</span></span>
<span data-ttu-id="f2df1-227">Określa akcje skryptu, które mają być uruchamiane w klastrze pod koniec tworzenia klastrów.</span><span class="sxs-lookup"><span data-stu-id="f2df1-227">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="f2df1-228">Możesz również użyć funkcji Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="f2df1-228">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="f2df1-229">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="f2df1-229">-SecurityProfile</span></span>
<span data-ttu-id="f2df1-230">Określa właściwości związane z zabezpieczeniami używane do tworzenia bezpiecznego klastru.</span><span class="sxs-lookup"><span data-stu-id="f2df1-230">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="f2df1-231">Możesz również użyć polecenia cmdlet Add-AzHDInsightSecurityProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2df1-231">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="f2df1-232">- SshCredential</span><span class="sxs-lookup"><span data-stu-id="f2df1-232">-SshCredential</span></span>
<span data-ttu-id="f2df1-233">Określa poświadczenia SSH, które mają być używane dla połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="f2df1-233">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="f2df1-234">Dotyczy to tylko klastrów systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="f2df1-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="f2df1-235">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f2df1-235">-SshPublicKey</span></span>
<span data-ttu-id="f2df1-236">Określa klucz publiczny, który ma być używany dla połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="f2df1-236">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="f2df1-237">Dotyczy to tylko klastrów systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="f2df1-237">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="f2df1-238">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f2df1-238">-StorageAccountKey</span></span>
<span data-ttu-id="f2df1-239">Pobiera lub ustawia klucz dostępu konta magazynu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f2df1-239">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="f2df1-240">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="f2df1-240">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="f2df1-241">Pobiera lub ustawia tożsamość zarządzaną konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f2df1-241">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="f2df1-242">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f2df1-242">-StorageAccountResourceId</span></span>
<span data-ttu-id="f2df1-243">Pobiera lub ustawia identyfikator zasobu magazynu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f2df1-243">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="f2df1-244">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f2df1-244">-StorageAccountType</span></span>
<span data-ttu-id="f2df1-245">Pobiera lub ustawia typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f2df1-245">Gets or sets the type of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2df1-246">— StorageContainer</span><span class="sxs-lookup"><span data-stu-id="f2df1-246">-StorageContainer</span></span>
<span data-ttu-id="f2df1-247">Pobiera lub ustawia nazwę magazynuContainer domyślnego konta magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f2df1-247">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="f2df1-248">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="f2df1-248">-StorageFileSystem</span></span>
<span data-ttu-id="f2df1-249">Pobiera lub ustawia system plików dla domyślnego konta usługi Azure Data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="f2df1-249">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="f2df1-250">- StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="f2df1-250">-StorageRootPath</span></span>
<span data-ttu-id="f2df1-251">Pobiera lub ustawia ścieżkę do katalogu głównego klastra w domyślnym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f2df1-251">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="f2df1-252">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f2df1-252">-SubnetName</span></span>
<span data-ttu-id="f2df1-253">Pobiera lub ustawia nazwę podsieci dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f2df1-253">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="f2df1-254">— Wersja</span><span class="sxs-lookup"><span data-stu-id="f2df1-254">-Version</span></span>
<span data-ttu-id="f2df1-255">Określa wersję HDI klastrów HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f2df1-255">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="f2df1-256">- VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f2df1-256">-VirtualNetworkId</span></span>
<span data-ttu-id="f2df1-257">Określa identyfikator sieci wirtualnej, w której ma być aprowizowanie klastrów.</span><span class="sxs-lookup"><span data-stu-id="f2df1-257">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="f2df1-258">- WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="f2df1-258">-WorkerNodeSize</span></span>
<span data-ttu-id="f2df1-259">Określa rozmiar maszyny wirtualnej dla węzła Pracownik.</span><span class="sxs-lookup"><span data-stu-id="f2df1-259">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="f2df1-260">Użyj Get-AzVMSize dla akceptowalnych rozmiarów maszyn wirtualnych i zobacz stronę cenową usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f2df1-260">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="f2df1-261">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="f2df1-261">-ZookeeperNodeSize</span></span>
<span data-ttu-id="f2df1-262">Określa rozmiar maszyny wirtualnej węzła Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="f2df1-262">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="f2df1-263">Użyj Get-AzVMSize dla akceptowalnych rozmiarów maszyn wirtualnych i zobacz stronę cenową usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f2df1-263">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="f2df1-264">Ten parametr jest prawidłowy tylko dla klastrów HBase lub Storm.</span><span class="sxs-lookup"><span data-stu-id="f2df1-264">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="f2df1-265">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2df1-265">CommonParameters</span></span>
<span data-ttu-id="f2df1-266">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2df1-266">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2df1-267">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2df1-267">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2df1-268">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2df1-268">INPUTS</span></span>

### <span data-ttu-id="f2df1-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f2df1-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="f2df1-270">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2df1-270">OUTPUTS</span></span>

### <span data-ttu-id="f2df1-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f2df1-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="f2df1-272">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f2df1-272">NOTES</span></span>
<span data-ttu-id="f2df1-273">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span><span class="sxs-lookup"><span data-stu-id="f2df1-273">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="f2df1-274">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2df1-274">RELATED LINKS</span></span>

[<span data-ttu-id="f2df1-275">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f2df1-275">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

