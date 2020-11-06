---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: 381143b356202a7b6b76e173b233f2fffe87f6a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553884"
---
# <span data-ttu-id="3e3d4-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3e3d4-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="3e3d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="3e3d4-103">Tworzy nieutrwalony obiekt konfiguracji klastra opisujący konfigurację klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e3d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e3d4-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e3d4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3e3d4-105">DESCRIPTION</span></span>
<span data-ttu-id="3e3d4-106">Polecenie cmdlet **New-AzureRmHDInsightClusterConfig** tworzy nieutrwalony obiekt opisujący konfigurację klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="3e3d4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e3d4-107">EXAMPLES</span></span>

### <span data-ttu-id="3e3d4-108">Przykład 1. Tworzenie obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="3e3d4-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="3e3d4-109">To polecenie tworzy obiekt konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="3e3d4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e3d4-110">PARAMETERS</span></span>

### <span data-ttu-id="3e3d4-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="3e3d4-111">-AadTenantId</span></span>
<span data-ttu-id="3e3d4-112">Określa identyfikator dzierżawy usługi Azure AD, który będzie stosowany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3e3d4-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="3e3d4-113">-CertificateFileContents</span></span>
<span data-ttu-id="3e3d4-114">Określa zawartość pliku certyfikatu, która będzie używana podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e3d4-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3e3d4-115">-CertificateFilePath</span></span>
<span data-ttu-id="3e3d4-116">Określa ścieżkę do pliku certyfikatu, który zostanie wykorzystany do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3e3d4-117">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3e3d4-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3e3d4-118">-CertificatePassword</span></span>
<span data-ttu-id="3e3d4-119">Określa hasło certyfikatu, które zostanie użyte do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3e3d4-120">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3e3d4-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="3e3d4-121">-ClusterTier</span></span>
<span data-ttu-id="3e3d4-122">Określa poziom klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="3e3d4-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3e3d4-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3e3d4-124">Standard</span><span class="sxs-lookup"><span data-stu-id="3e3d4-124">Standard</span></span>
- <span data-ttu-id="3e3d4-125">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="3e3d4-125">Premium</span></span>

<span data-ttu-id="3e3d4-126">Wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-126">The default value is Standard.</span></span>
<span data-ttu-id="3e3d4-127">Warstwa Premium może być używana tylko w przypadku klastrów z systemem Linux i umożliwia korzystanie z nowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-127">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="3e3d4-128">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="3e3d4-128">-ClusterType</span></span>
<span data-ttu-id="3e3d4-129">Określa typ klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-129">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="3e3d4-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3e3d4-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3e3d4-131">Hadoop</span><span class="sxs-lookup"><span data-stu-id="3e3d4-131">Hadoop</span></span>
- <span data-ttu-id="3e3d4-132">HBase</span><span class="sxs-lookup"><span data-stu-id="3e3d4-132">HBase</span></span>
- <span data-ttu-id="3e3d4-133">Burz</span><span class="sxs-lookup"><span data-stu-id="3e3d4-133">Storm</span></span>
- <span data-ttu-id="3e3d4-134">ISKr</span><span class="sxs-lookup"><span data-stu-id="3e3d4-134">Spark</span></span>

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

### <span data-ttu-id="3e3d4-135">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3e3d4-135">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="3e3d4-136">Określa klucz konta dla domyślnego konta usługi Azure Storage, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-136">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="3e3d4-137">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3e3d4-137">-DefaultStorageAccountName</span></span>
<span data-ttu-id="3e3d4-138">Określa nazwę domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-138">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="3e3d4-139">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3e3d4-139">-DefaultStorageAccountType</span></span>
<span data-ttu-id="3e3d4-140">Określa typ domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-140">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="3e3d4-141">Możliwe wartości to AzureStorage i AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-141">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e3d4-142">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="3e3d4-142">-EdgeNodeSize</span></span>
<span data-ttu-id="3e3d4-143">Określa rozmiar maszyny wirtualnej dla węzła Edge.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-143">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="3e3d4-144">Użyj Get-AzureRmVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-144">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="3e3d4-145">Ten parametr jest prawidłowy tylko w przypadku klastrów RServer.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-145">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="3e3d4-146">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="3e3d4-146">-HeadNodeSize</span></span>
<span data-ttu-id="3e3d4-147">Określa rozmiar maszyny wirtualnej dla węzła głównego.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-147">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="3e3d4-148">Użyj Get-AzureRMVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-148">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="3e3d4-149">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="3e3d4-149">-HiveMetastore</span></span>
<span data-ttu-id="3e3d4-150">Określa, że metadane gałęzi są przechowywane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-150">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="3e3d4-151">Możesz również użyć polecenia cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-151">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="3e3d4-152">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3e3d4-152">-ObjectId</span></span>
<span data-ttu-id="3e3d4-153">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD reprezentujący klaster.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-153">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="3e3d4-154">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-154">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3e3d4-155">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="3e3d4-155">-OozieMetastore</span></span>
<span data-ttu-id="3e3d4-156">Określa, że w magazynie są przechowywane metadane Oozie.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-156">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="3e3d4-157">Możesz również użyć polecenia cmdlet **Add-AzureRmHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="3e3d4-157">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="3e3d4-158">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="3e3d4-158">-WorkerNodeSize</span></span>
<span data-ttu-id="3e3d4-159">Określa rozmiar maszyny wirtualnej dla węzła roboczego.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-159">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="3e3d4-160">Użyj Get-AzureRMVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-160">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="3e3d4-161">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="3e3d4-161">-ZookeeperNodeSize</span></span>
<span data-ttu-id="3e3d4-162">Określa rozmiar maszyny wirtualnej dla węzła Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-162">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="3e3d4-163">Użyj Get-AzureRMVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-163">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="3e3d4-164">Ten parametr jest prawidłowy tylko w przypadku klastrów HBase lub burzy.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-164">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="3e3d4-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e3d4-165">-DefaultProfile</span></span>
<span data-ttu-id="3e3d4-166">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e3d4-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e3d4-167">CommonParameters</span></span>
<span data-ttu-id="3e3d4-168">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e3d4-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e3d4-169">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e3d4-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e3d4-170">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e3d4-170">INPUTS</span></span>

## <span data-ttu-id="3e3d4-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e3d4-171">OUTPUTS</span></span>

### <span data-ttu-id="3e3d4-172">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3e3d4-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3e3d4-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e3d4-173">NOTES</span></span>

## <span data-ttu-id="3e3d4-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e3d4-174">RELATED LINKS</span></span>

[<span data-ttu-id="3e3d4-175">Dodaj-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="3e3d4-175">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


