---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: fad988977cf5fe24e440d654206e0f1a212be6b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868248"
---
# <span data-ttu-id="c2e1e-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c2e1e-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="c2e1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e1e-103">Tworzy nieutrwalony obiekt konfiguracji klastra opisujący konfigurację klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="c2e1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2e1e-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2e1e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2e1e-105">DESCRIPTION</span></span>
<span data-ttu-id="c2e1e-106">Polecenie cmdlet **New-AzHDInsightClusterConfig** tworzy nieutrwalony obiekt opisujący konfigurację klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="c2e1e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2e1e-107">EXAMPLES</span></span>

### <span data-ttu-id="c2e1e-108">Przykład 1. Tworzenie obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="c2e1e-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
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

<span data-ttu-id="c2e1e-109">To polecenie tworzy obiekt konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="c2e1e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2e1e-110">PARAMETERS</span></span>

### <span data-ttu-id="c2e1e-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="c2e1e-111">-AadTenantId</span></span>
<span data-ttu-id="c2e1e-112">Określa identyfikator dzierżawy usługi Azure AD, który będzie stosowany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c2e1e-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c2e1e-113">-CertificateFileContents</span></span>
<span data-ttu-id="c2e1e-114">Określa zawartość pliku certyfikatu, która będzie używana podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c2e1e-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c2e1e-115">-CertificateFilePath</span></span>
<span data-ttu-id="c2e1e-116">Określa ścieżkę do pliku certyfikatu, który zostanie wykorzystany do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c2e1e-117">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c2e1e-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c2e1e-118">-CertificatePassword</span></span>
<span data-ttu-id="c2e1e-119">Określa hasło certyfikatu, które zostanie użyte do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c2e1e-120">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c2e1e-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="c2e1e-121">-ClusterTier</span></span>
<span data-ttu-id="c2e1e-122">Określa poziom klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="c2e1e-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c2e1e-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2e1e-124">Standard</span><span class="sxs-lookup"><span data-stu-id="c2e1e-124">Standard</span></span>
- <span data-ttu-id="c2e1e-125">Premium wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-125">Premium The default value is Standard.</span></span>
<span data-ttu-id="c2e1e-126">Warstwa Premium może być używana tylko w przypadku klastrów z systemem Linux i umożliwia korzystanie z nowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-126">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="c2e1e-127">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="c2e1e-127">-ClusterType</span></span>
<span data-ttu-id="c2e1e-128">Określa typ klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-128">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="c2e1e-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c2e1e-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2e1e-130">Hadoop</span><span class="sxs-lookup"><span data-stu-id="c2e1e-130">Hadoop</span></span>
- <span data-ttu-id="c2e1e-131">HBase</span><span class="sxs-lookup"><span data-stu-id="c2e1e-131">HBase</span></span>
- <span data-ttu-id="c2e1e-132">Burz</span><span class="sxs-lookup"><span data-stu-id="c2e1e-132">Storm</span></span>
- <span data-ttu-id="c2e1e-133">ISKr</span><span class="sxs-lookup"><span data-stu-id="c2e1e-133">Spark</span></span>

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

### <span data-ttu-id="c2e1e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e1e-134">-DefaultProfile</span></span>
<span data-ttu-id="c2e1e-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c2e1e-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2e1e-136">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c2e1e-136">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="c2e1e-137">Określa klucz konta dla domyślnego konta usługi Azure Storage, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-137">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="c2e1e-138">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c2e1e-138">-DefaultStorageAccountName</span></span>
<span data-ttu-id="c2e1e-139">Określa nazwę domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-139">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="c2e1e-140">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c2e1e-140">-DefaultStorageAccountType</span></span>
<span data-ttu-id="c2e1e-141">Określa typ domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-141">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="c2e1e-142">Możliwe wartości to AzureStorage i AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-142">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="c2e1e-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="c2e1e-143">-EdgeNodeSize</span></span>
<span data-ttu-id="c2e1e-144">Określa rozmiar maszyny wirtualnej dla węzła Edge.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="c2e1e-145">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="c2e1e-146">Ten parametr jest prawidłowy tylko w przypadku klastrów RServer.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="c2e1e-147">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="c2e1e-147">-HeadNodeSize</span></span>
<span data-ttu-id="c2e1e-148">Określa rozmiar maszyny wirtualnej dla węzła głównego.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-148">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="c2e1e-149">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-149">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c2e1e-150">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="c2e1e-150">-HiveMetastore</span></span>
<span data-ttu-id="c2e1e-151">Określa, że metadane gałęzi są przechowywane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-151">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="c2e1e-152">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-152">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="c2e1e-153">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c2e1e-153">-ObjectId</span></span>
<span data-ttu-id="c2e1e-154">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD reprezentujący klaster.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-154">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="c2e1e-155">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-155">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c2e1e-156">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="c2e1e-156">-OozieMetastore</span></span>
<span data-ttu-id="c2e1e-157">Określa, że w magazynie są przechowywane metadane Oozie.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-157">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="c2e1e-158">Możesz również użyć polecenia cmdlet **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="c2e1e-158">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="c2e1e-159">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="c2e1e-159">-WorkerNodeSize</span></span>
<span data-ttu-id="c2e1e-160">Określa rozmiar maszyny wirtualnej dla węzła roboczego.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-160">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="c2e1e-161">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c2e1e-162">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="c2e1e-162">-ZookeeperNodeSize</span></span>
<span data-ttu-id="c2e1e-163">Określa rozmiar maszyny wirtualnej dla węzła Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-163">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="c2e1e-164">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-164">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="c2e1e-165">Ten parametr jest prawidłowy tylko w przypadku klastrów HBase lub burzy.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-165">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="c2e1e-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e1e-166">CommonParameters</span></span>
<span data-ttu-id="c2e1e-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2e1e-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e1e-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2e1e-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e1e-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2e1e-169">INPUTS</span></span>

### <span data-ttu-id="c2e1e-170">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c2e1e-170">None</span></span>

## <span data-ttu-id="c2e1e-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2e1e-171">OUTPUTS</span></span>

### <span data-ttu-id="c2e1e-172">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c2e1e-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c2e1e-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2e1e-173">NOTES</span></span>

## <span data-ttu-id="c2e1e-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2e1e-174">RELATED LINKS</span></span>

[<span data-ttu-id="c2e1e-175">Dodaj-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="c2e1e-175">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


