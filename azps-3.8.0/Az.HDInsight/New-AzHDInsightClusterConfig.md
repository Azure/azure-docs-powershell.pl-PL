---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 38dc23c2bebe3c608833e55bcb4ffb2d687f9041
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896698"
---
# <span data-ttu-id="7f150-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="7f150-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="7f150-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f150-102">SYNOPSIS</span></span>
<span data-ttu-id="7f150-103">Tworzy nieutrwalony obiekt konfiguracji klastra opisujący konfigurację klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7f150-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="7f150-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f150-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [[-DefaultStorageAccountType] <StorageType>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>] [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>]
 [[-EdgeNodeSize] <String>] [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>] [[-ClusterTier] <Tier>]
 [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>] [[-CertificateFileContents] <Byte[]>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f150-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7f150-105">DESCRIPTION</span></span>
<span data-ttu-id="7f150-106">Polecenie cmdlet **New-AzHDInsightClusterConfig** tworzy nieutrwalony obiekt opisujący konfigurację klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7f150-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="7f150-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f150-107">EXAMPLES</span></span>

### <span data-ttu-id="7f150-108">Przykład 1. Tworzenie obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="7f150-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="7f150-109">To polecenie tworzy obiekt konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="7f150-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="7f150-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f150-110">PARAMETERS</span></span>

### <span data-ttu-id="7f150-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="7f150-111">-AadTenantId</span></span>
<span data-ttu-id="7f150-112">Określa identyfikator dzierżawy usługi Azure AD, który będzie stosowany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f150-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7f150-113">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="7f150-113">-ApplicationId</span></span>
<span data-ttu-id="7f150-114">Pobiera lub ustawia identyfikator aplikacji głównej usługi w celu uzyskania dostępu do usługi Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="7f150-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="7f150-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="7f150-115">-CertificateFileContents</span></span>
<span data-ttu-id="7f150-116">Określa zawartość pliku certyfikatu, która będzie używana podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f150-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7f150-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="7f150-117">-CertificateFilePath</span></span>
<span data-ttu-id="7f150-118">Określa ścieżkę do pliku certyfikatu, który zostanie wykorzystany do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="7f150-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="7f150-119">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f150-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7f150-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="7f150-120">-CertificatePassword</span></span>
<span data-ttu-id="7f150-121">Określa hasło certyfikatu, które zostanie użyte do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="7f150-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="7f150-122">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f150-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7f150-123">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="7f150-123">-ClusterTier</span></span>
<span data-ttu-id="7f150-124">Określa poziom klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7f150-124">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="7f150-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7f150-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f150-126">Standard</span><span class="sxs-lookup"><span data-stu-id="7f150-126">Standard</span></span>
- <span data-ttu-id="7f150-127">Premium wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="7f150-127">Premium The default value is Standard.</span></span>
<span data-ttu-id="7f150-128">Warstwa Premium może być używana tylko w przypadku klastrów z systemem Linux i umożliwia korzystanie z nowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="7f150-128">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="7f150-129">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="7f150-129">-ClusterType</span></span>
<span data-ttu-id="7f150-130">Określa typ klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="7f150-130">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="7f150-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7f150-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f150-132">Hadoop</span><span class="sxs-lookup"><span data-stu-id="7f150-132">Hadoop</span></span>
- <span data-ttu-id="7f150-133">HBase</span><span class="sxs-lookup"><span data-stu-id="7f150-133">HBase</span></span>
- <span data-ttu-id="7f150-134">Burz</span><span class="sxs-lookup"><span data-stu-id="7f150-134">Storm</span></span>
- <span data-ttu-id="7f150-135">ISKr</span><span class="sxs-lookup"><span data-stu-id="7f150-135">Spark</span></span>
- <span data-ttu-id="7f150-136">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="7f150-136">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="7f150-137">Kafka</span><span class="sxs-lookup"><span data-stu-id="7f150-137">Kafka</span></span>
- <span data-ttu-id="7f150-138">RServer</span><span class="sxs-lookup"><span data-stu-id="7f150-138">RServer</span></span>

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

### <span data-ttu-id="7f150-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f150-139">-DefaultProfile</span></span>
<span data-ttu-id="7f150-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7f150-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f150-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7f150-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="7f150-142">Określa klucz konta dla domyślnego konta usługi Azure Storage, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7f150-142">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="7f150-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7f150-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="7f150-144">Określa nazwę domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7f150-144">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="7f150-145">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7f150-145">-DefaultStorageAccountType</span></span>
<span data-ttu-id="7f150-146">Określa typ domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7f150-146">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="7f150-147">Możliwe wartości to AzureStorage i AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="7f150-147">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="7f150-148">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="7f150-148">-EdgeNodeSize</span></span>
<span data-ttu-id="7f150-149">Określa rozmiar maszyny wirtualnej dla węzła Edge.</span><span class="sxs-lookup"><span data-stu-id="7f150-149">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="7f150-150">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7f150-150">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="7f150-151">Ten parametr jest prawidłowy tylko w przypadku klastrów RServer.</span><span class="sxs-lookup"><span data-stu-id="7f150-151">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="7f150-152">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="7f150-152">-HeadNodeSize</span></span>
<span data-ttu-id="7f150-153">Określa rozmiar maszyny wirtualnej dla węzła głównego.</span><span class="sxs-lookup"><span data-stu-id="7f150-153">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="7f150-154">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7f150-154">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="7f150-155">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="7f150-155">-HiveMetastore</span></span>
<span data-ttu-id="7f150-156">Określa, że metadane gałęzi są przechowywane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="7f150-156">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="7f150-157">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="7f150-157">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="7f150-158">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="7f150-158">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="7f150-159">Pobiera lub ustawia minimalną obsługiwaną wersję protokołu TLS.</span><span class="sxs-lookup"><span data-stu-id="7f150-159">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="7f150-160">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7f150-160">-ObjectId</span></span>
<span data-ttu-id="7f150-161">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD reprezentujący klaster.</span><span class="sxs-lookup"><span data-stu-id="7f150-161">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="7f150-162">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f150-162">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="7f150-163">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="7f150-163">-OozieMetastore</span></span>
<span data-ttu-id="7f150-164">Określa, że w magazynie są przechowywane metadane Oozie.</span><span class="sxs-lookup"><span data-stu-id="7f150-164">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="7f150-165">Możesz również użyć polecenia cmdlet **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="7f150-165">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="7f150-166">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="7f150-166">-WorkerNodeSize</span></span>
<span data-ttu-id="7f150-167">Określa rozmiar maszyny wirtualnej dla węzła roboczego.</span><span class="sxs-lookup"><span data-stu-id="7f150-167">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="7f150-168">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7f150-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="7f150-169">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="7f150-169">-ZookeeperNodeSize</span></span>
<span data-ttu-id="7f150-170">Określa rozmiar maszyny wirtualnej dla węzła Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="7f150-170">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="7f150-171">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7f150-171">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="7f150-172">Ten parametr jest prawidłowy tylko w przypadku klastrów HBase lub burzy.</span><span class="sxs-lookup"><span data-stu-id="7f150-172">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="7f150-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f150-173">CommonParameters</span></span>
<span data-ttu-id="7f150-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f150-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f150-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f150-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f150-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f150-176">INPUTS</span></span>

### <span data-ttu-id="7f150-177">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7f150-177">None</span></span>

## <span data-ttu-id="7f150-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f150-178">OUTPUTS</span></span>

### <span data-ttu-id="7f150-179">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="7f150-179">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="7f150-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f150-180">NOTES</span></span>

## <span data-ttu-id="7f150-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f150-181">RELATED LINKS</span></span>

[<span data-ttu-id="7f150-182">Dodaj-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="7f150-182">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


