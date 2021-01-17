---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: f4592a371e528c7779e07251bf79677dac47e6df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323363"
---
# <span data-ttu-id="70ccc-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="70ccc-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="70ccc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="70ccc-103">Tworzy klaster usługi Azure HDInsight w określonej grupie zasobów dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="70ccc-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="70ccc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70ccc-104">SYNTAX</span></span>

### <span data-ttu-id="70ccc-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="70ccc-105">Default (Default)</span></span>
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
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70ccc-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="70ccc-106">CertificateFilePath</span></span>
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
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70ccc-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="70ccc-107">CertificateFileContents</span></span>
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
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70ccc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="70ccc-108">DESCRIPTION</span></span>
<span data-ttu-id="70ccc-109">New-AzHDInsightCluster tworzy klaster usługi Azure HDInsight przy użyciu określonych parametrów lub obiektu konfiguracji utworzonego za pomocą polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="70ccc-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="70ccc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70ccc-110">EXAMPLES</span></span>

### <span data-ttu-id="70ccc-111">Przykład 1. Tworzenie klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="70ccc-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="70ccc-112">To polecenie tworzy klaster w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="70ccc-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="70ccc-113">Przykład 2: Tworzenie klastra za pomocą szyfrowania dysków klucza zarządzanego przez klienta</span><span class="sxs-lookup"><span data-stu-id="70ccc-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="70ccc-114">Przykład 3: Tworzenie klastra usługi Azure HDInsight umożliwiającego szyfrowanie w tranzycie</span><span class="sxs-lookup"><span data-stu-id="70ccc-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="70ccc-115">Przykład 4: Tworzenie klastra usługi Azure HDInsight za pomocą funkcji przekazywania połączeń wychodzących i prywatnych</span><span class="sxs-lookup"><span data-stu-id="70ccc-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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

### <span data-ttu-id="70ccc-116">Przykład 5: Tworzenie klastra usługi Azure HDInsight umożliwiającego szyfrowanie na hoście</span><span class="sxs-lookup"><span data-stu-id="70ccc-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="70ccc-117">Przykład 6: Tworzenie klastra usługi Azure HDInsight umożliwiającego automatyczne skalowanie.</span><span class="sxs-lookup"><span data-stu-id="70ccc-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

### <span data-ttu-id="70ccc-118">Przykład 7: Tworzenie klastra usługi Azure HDInsight za pomocą serwera proxy usługi Kafka.</span><span class="sxs-lookup"><span data-stu-id="70ccc-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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

### <span data-ttu-id="70ccc-119">Przykład 8: Tworzenie klastra usługi Azure HDInsight za pomocą magazynu usługi Azure Data Lake Gen2 Storage.</span><span class="sxs-lookup"><span data-stu-id="70ccc-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
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

### <span data-ttu-id="70ccc-120">Przykład 9: Tworzenie klastra Azure HDInsight z pakietem zabezpieczeń przedsiębiorstwa (ESP) i włączanie brokera identyfikatorów usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70ccc-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
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

## <span data-ttu-id="70ccc-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70ccc-121">PARAMETERS</span></span>

### <span data-ttu-id="70ccc-122">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="70ccc-122">-AadTenantId</span></span>
<span data-ttu-id="70ccc-123">Określa identyfikator dzierżawy usługi Azure AD, który będzie stosowany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="70ccc-123">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="70ccc-124">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="70ccc-124">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="70ccc-125">Określa dodatkowe konta magazynu platformy Azure dla klastra.</span><span class="sxs-lookup"><span data-stu-id="70ccc-125">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="70ccc-126">Możesz również użyć polecenia cmdlet Add-AzHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="70ccc-126">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="70ccc-127">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="70ccc-127">-AmbariDatabase</span></span>
<span data-ttu-id="70ccc-128">Pobiera lub ustawia bazę danych dla Ambari.</span><span class="sxs-lookup"><span data-stu-id="70ccc-128">Gets or sets the database for ambari.</span></span>

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

### <span data-ttu-id="70ccc-129">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="70ccc-129">-ApplicationId</span></span>
<span data-ttu-id="70ccc-130">Pobiera lub ustawia identyfikator aplikacji głównej usługi w celu uzyskania dostępu do usługi Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="70ccc-130">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="70ccc-131">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="70ccc-131">-AssignedIdentity</span></span>
<span data-ttu-id="70ccc-132">Pobiera lub ustawia przypisaną tożsamość.</span><span class="sxs-lookup"><span data-stu-id="70ccc-132">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="70ccc-133">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="70ccc-133">-AutoscaleConfiguration</span></span>
<span data-ttu-id="70ccc-134">Pobiera lub ustawia konfigurację skalowania automatycznego</span><span class="sxs-lookup"><span data-stu-id="70ccc-134">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="70ccc-135">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="70ccc-135">-CertificateFileContents</span></span>
<span data-ttu-id="70ccc-136">Określa zawartość pliku certyfikatu, która będzie używana podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="70ccc-136">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="70ccc-137">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="70ccc-137">-CertificateFilePath</span></span>
<span data-ttu-id="70ccc-138">Określa ścieżkę do pliku certyfikatu, który zostanie wykorzystany do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="70ccc-138">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="70ccc-139">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="70ccc-139">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="70ccc-140">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="70ccc-140">-CertificatePassword</span></span>
<span data-ttu-id="70ccc-141">Określa hasło certyfikatu, które zostanie użyte do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="70ccc-141">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="70ccc-142">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="70ccc-142">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="70ccc-143">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="70ccc-143">-ClusterName</span></span>
<span data-ttu-id="70ccc-144">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="70ccc-144">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="70ccc-145">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="70ccc-145">-ClusterSizeInNodes</span></span>
<span data-ttu-id="70ccc-146">Określa liczbę węzłów procesu roboczego klastra.</span><span class="sxs-lookup"><span data-stu-id="70ccc-146">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="70ccc-147">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="70ccc-147">-ClusterTier</span></span>
<span data-ttu-id="70ccc-148">Określa poziom klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70ccc-148">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="70ccc-149">Domyślnie jest to standard.</span><span class="sxs-lookup"><span data-stu-id="70ccc-149">By default, this is Standard.</span></span>
<span data-ttu-id="70ccc-150">Warstwa Premium może być używana tylko w przypadku klastrów z systemem Linux i umożliwia korzystanie z nowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="70ccc-150">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="70ccc-151">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="70ccc-151">-ClusterType</span></span>
<span data-ttu-id="70ccc-152">Określa typ klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="70ccc-152">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="70ccc-153">Dostępne opcje: Hadoop, HBase, burza, Spark, INTERACTIVEHIVE, Kafka i RServer</span><span class="sxs-lookup"><span data-stu-id="70ccc-153">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="70ccc-154">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="70ccc-154">-ComponentVersion</span></span>
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

### <span data-ttu-id="70ccc-155">-Config</span><span class="sxs-lookup"><span data-stu-id="70ccc-155">-Config</span></span>
<span data-ttu-id="70ccc-156">Określa obiekt klastra, który ma zostać wykorzystany do utworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="70ccc-156">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="70ccc-157">Ten obiekt można utworzyć przy użyciu polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="70ccc-157">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="70ccc-158">-Konfiguracje</span><span class="sxs-lookup"><span data-stu-id="70ccc-158">-Configurations</span></span>
<span data-ttu-id="70ccc-159">Określa konfiguracje tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70ccc-159">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="70ccc-160">Możesz również użyć polecenia cmdlet Add-AzHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="70ccc-160">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="70ccc-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ccc-161">-DefaultProfile</span></span>
<span data-ttu-id="70ccc-162">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="70ccc-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70ccc-163">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="70ccc-163">-DisksPerWorkerNode</span></span>
<span data-ttu-id="70ccc-164">Określa liczbę dysków dla roli węzła procesu roboczego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="70ccc-164">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="70ccc-165">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="70ccc-165">-EdgeNodeSize</span></span>
<span data-ttu-id="70ccc-166">Określa rozmiar maszyny wirtualnej dla węzła Edge.</span><span class="sxs-lookup"><span data-stu-id="70ccc-166">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="70ccc-167">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70ccc-167">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="70ccc-168">Ten parametr jest prawidłowy tylko w przypadku klastrów RServer.</span><span class="sxs-lookup"><span data-stu-id="70ccc-168">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="70ccc-169">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="70ccc-169">-EnableIDBroker</span></span>
<span data-ttu-id="70ccc-170">Włącza funkcję brokera tożsamości usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70ccc-170">Enables HDInsight Identity Broker feature.</span></span>

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

### <span data-ttu-id="70ccc-171">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="70ccc-171">-EncryptionAlgorithm</span></span>
<span data-ttu-id="70ccc-172">Pobiera lub ustawia algorytm szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="70ccc-172">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="70ccc-173">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="70ccc-173">-EncryptionAtHost</span></span>
<span data-ttu-id="70ccc-174">Pobiera lub ustawia flagę wskazującą, czy włączyć szyfrowanie na hoście.</span><span class="sxs-lookup"><span data-stu-id="70ccc-174">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="70ccc-175">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="70ccc-175">-EncryptionInTransit</span></span>
<span data-ttu-id="70ccc-176">Pobiera lub ustawia flagę wskazującą, czy włączyć szyfrowanie w tranzycie.</span><span class="sxs-lookup"><span data-stu-id="70ccc-176">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="70ccc-177">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="70ccc-177">-EncryptionKeyName</span></span>
<span data-ttu-id="70ccc-178">Pobiera lub ustawia nazwę klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="70ccc-178">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="70ccc-179">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="70ccc-179">-EncryptionKeyVersion</span></span>
<span data-ttu-id="70ccc-180">Pobiera lub ustawia wersję klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="70ccc-180">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="70ccc-181">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="70ccc-181">-EncryptionVaultUri</span></span>
<span data-ttu-id="70ccc-182">Pobiera lub ustawia identyfikator URI magazynu szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="70ccc-182">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="70ccc-183">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="70ccc-183">-HeadNodeSize</span></span>
<span data-ttu-id="70ccc-184">Określa rozmiar maszyny wirtualnej dla węzła głównego.</span><span class="sxs-lookup"><span data-stu-id="70ccc-184">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="70ccc-185">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70ccc-185">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="70ccc-186">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="70ccc-186">-HiveMetastore</span></span>
<span data-ttu-id="70ccc-187">Określa bazę danych SQL do przechowywania metadanych gałęzi.</span><span class="sxs-lookup"><span data-stu-id="70ccc-187">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="70ccc-188">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="70ccc-188">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="70ccc-189">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="70ccc-189">-HttpCredential</span></span>
<span data-ttu-id="70ccc-190">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="70ccc-190">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="70ccc-191">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="70ccc-191">-KafkaClientGroupId</span></span>
<span data-ttu-id="70ccc-192">Pobiera lub ustawia identyfikator grupy klientów na potrzeby dostępu do serwera proxy usługi Kafka.</span><span class="sxs-lookup"><span data-stu-id="70ccc-192">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="70ccc-193">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="70ccc-193">-KafkaClientGroupName</span></span>
<span data-ttu-id="70ccc-194">Pobiera lub ustawia nazwę grupy klientów na potrzeby dostępu do serwera proxy usługi Kafka.</span><span class="sxs-lookup"><span data-stu-id="70ccc-194">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="70ccc-195">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="70ccc-195">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="70ccc-196">Pobiera lub ustawia rozmiar węzła zarządzania Kafka.</span><span class="sxs-lookup"><span data-stu-id="70ccc-196">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="70ccc-197">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="70ccc-197">-Location</span></span>
<span data-ttu-id="70ccc-198">Określa lokalizację klastra.</span><span class="sxs-lookup"><span data-stu-id="70ccc-198">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="70ccc-199">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="70ccc-199">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="70ccc-200">Pobiera lub ustawia minimalną obsługiwaną wersję protokołu TLS.</span><span class="sxs-lookup"><span data-stu-id="70ccc-200">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="70ccc-201">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="70ccc-201">-ObjectId</span></span>
<span data-ttu-id="70ccc-202">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD reprezentujący klaster.</span><span class="sxs-lookup"><span data-stu-id="70ccc-202">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="70ccc-203">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="70ccc-203">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="70ccc-204">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="70ccc-204">-OozieMetastore</span></span>
<span data-ttu-id="70ccc-205">Określa bazę danych SQL do przechowywania metadanych Oozie.</span><span class="sxs-lookup"><span data-stu-id="70ccc-205">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="70ccc-206">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="70ccc-206">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="70ccc-207">-OSType</span><span class="sxs-lookup"><span data-stu-id="70ccc-207">-OSType</span></span>
<span data-ttu-id="70ccc-208">Określa system operacyjny dla klastra.</span><span class="sxs-lookup"><span data-stu-id="70ccc-208">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="70ccc-209">Dostępne opcje: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="70ccc-209">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="70ccc-210">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="70ccc-210">-PrivateLink</span></span>
<span data-ttu-id="70ccc-211">Pobiera lub ustawia typ linku prywatnego.</span><span class="sxs-lookup"><span data-stu-id="70ccc-211">Gets or sets the private link type.</span></span>

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

### <span data-ttu-id="70ccc-212">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="70ccc-212">-RdpAccessExpiry</span></span>
<span data-ttu-id="70ccc-213">Określa wygaśnięcie jako obiekt DateTime, aby uzyskać dostęp do klastra za pomocą protokołu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="70ccc-213">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="70ccc-214">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="70ccc-214">-RdpCredential</span></span>
<span data-ttu-id="70ccc-215">Określa poświadczenia pulpitu zdalnego (RDP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="70ccc-215">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="70ccc-216">Dotyczy to tylko klastrów systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="70ccc-216">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="70ccc-217">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70ccc-217">-ResourceGroupName</span></span>
<span data-ttu-id="70ccc-218">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70ccc-218">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="70ccc-219">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="70ccc-219">-ResourceProviderConnection</span></span>
<span data-ttu-id="70ccc-220">Pobiera lub ustawia typ połączenia dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70ccc-220">Gets or sets the resource provider connection type.</span></span>

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

### <span data-ttu-id="70ccc-221">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="70ccc-221">-ScriptActions</span></span>
<span data-ttu-id="70ccc-222">Określa akcje skryptu, które mają być uruchamiane w klastrze na koniec tworzenia klastra.</span><span class="sxs-lookup"><span data-stu-id="70ccc-222">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="70ccc-223">Możesz również użyć dodatku Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="70ccc-223">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="70ccc-224">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="70ccc-224">-SecurityProfile</span></span>
<span data-ttu-id="70ccc-225">Określa właściwości związane z zabezpieczeniami używane do tworzenia bezpiecznego klastra.</span><span class="sxs-lookup"><span data-stu-id="70ccc-225">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="70ccc-226">Możesz również użyć polecenia cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="70ccc-226">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="70ccc-227">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="70ccc-227">-SshCredential</span></span>
<span data-ttu-id="70ccc-228">Określa poświadczenie SSH, które ma być używane dla połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="70ccc-228">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="70ccc-229">Dotyczy to tylko klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="70ccc-229">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="70ccc-230">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="70ccc-230">-SshPublicKey</span></span>
<span data-ttu-id="70ccc-231">Określa klucz publiczny, który ma być stosowany do połączeń SSH.</span><span class="sxs-lookup"><span data-stu-id="70ccc-231">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="70ccc-232">Dotyczy to tylko klastrów w systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="70ccc-232">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="70ccc-233">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="70ccc-233">-StorageAccountKey</span></span>
<span data-ttu-id="70ccc-234">Pobiera lub ustawia klucz dostępu konta magazynu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="70ccc-234">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="70ccc-235">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="70ccc-235">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="70ccc-236">Pobiera lub ustawia tożsamość zarządzaną konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="70ccc-236">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="70ccc-237">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="70ccc-237">-StorageAccountResourceId</span></span>
<span data-ttu-id="70ccc-238">Pobiera lub ustawia identyfikator zasobu magazynu dla konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="70ccc-238">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="70ccc-239">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="70ccc-239">-StorageAccountType</span></span>
<span data-ttu-id="70ccc-240">Pobiera lub ustawia typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="70ccc-240">Gets or sets the type of the storage account.</span></span>

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

### <span data-ttu-id="70ccc-241">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="70ccc-241">-StorageContainer</span></span>
<span data-ttu-id="70ccc-242">Pobiera lub ustawia nazwę StorageContainer dla domyślnego konta magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="70ccc-242">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="70ccc-243">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="70ccc-243">-StorageFileSystem</span></span>
<span data-ttu-id="70ccc-244">Pobiera lub ustawia system plików dla domyślnego konta usługi Azure Data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="70ccc-244">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="70ccc-245">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="70ccc-245">-StorageRootPath</span></span>
<span data-ttu-id="70ccc-246">Pobiera lub ustawia ścieżkę do katalogu głównego klastra na domyślnym koncie usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="70ccc-246">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="70ccc-247">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="70ccc-247">-SubnetName</span></span>
<span data-ttu-id="70ccc-248">Pobiera lub ustawia nazwę podsieci dla tego klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70ccc-248">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="70ccc-249">-Version</span><span class="sxs-lookup"><span data-stu-id="70ccc-249">-Version</span></span>
<span data-ttu-id="70ccc-250">Określa wersję HDI klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70ccc-250">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="70ccc-251">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="70ccc-251">-VirtualNetworkId</span></span>
<span data-ttu-id="70ccc-252">Określa identyfikator sieci wirtualnej, do której ma być zastrzec klaster.</span><span class="sxs-lookup"><span data-stu-id="70ccc-252">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="70ccc-253">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="70ccc-253">-WorkerNodeSize</span></span>
<span data-ttu-id="70ccc-254">Określa rozmiar maszyny wirtualnej dla węzła roboczego.</span><span class="sxs-lookup"><span data-stu-id="70ccc-254">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="70ccc-255">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70ccc-255">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="70ccc-256">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="70ccc-256">-ZookeeperNodeSize</span></span>
<span data-ttu-id="70ccc-257">Określa rozmiar maszyny wirtualnej dla węzła Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="70ccc-257">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="70ccc-258">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="70ccc-258">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="70ccc-259">Ten parametr jest prawidłowy tylko w przypadku klastrów HBase lub burzy.</span><span class="sxs-lookup"><span data-stu-id="70ccc-259">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="70ccc-260">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ccc-260">CommonParameters</span></span>
<span data-ttu-id="70ccc-261">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ccc-261">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ccc-262">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70ccc-262">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ccc-263">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70ccc-263">INPUTS</span></span>

### <span data-ttu-id="70ccc-264">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="70ccc-264">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="70ccc-265">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70ccc-265">OUTPUTS</span></span>

### <span data-ttu-id="70ccc-266">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="70ccc-266">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="70ccc-267">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70ccc-267">NOTES</span></span>
<span data-ttu-id="70ccc-268">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, HDInsight, HD, Insights</span><span class="sxs-lookup"><span data-stu-id="70ccc-268">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="70ccc-269">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70ccc-269">RELATED LINKS</span></span>

[<span data-ttu-id="70ccc-270">Nowe — AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="70ccc-270">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

