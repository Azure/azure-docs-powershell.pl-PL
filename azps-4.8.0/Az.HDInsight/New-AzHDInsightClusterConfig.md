---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 66857c9d12bb23ffdccb893b8fae8bfc7c6e0f4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063545"
---
# <span data-ttu-id="747ab-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="747ab-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="747ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="747ab-102">SYNOPSIS</span></span>
<span data-ttu-id="747ab-103">Tworzy nieutrwalony obiekt konfiguracji klastra opisujący konfigurację klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="747ab-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="747ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="747ab-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>]
 [-OutboundPublicNetworkAccessType <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="747ab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="747ab-105">DESCRIPTION</span></span>
<span data-ttu-id="747ab-106">Polecenie cmdlet **New-AzHDInsightClusterConfig** tworzy nieutrwalony obiekt opisujący konfigurację klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="747ab-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="747ab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="747ab-107">EXAMPLES</span></span>

### <span data-ttu-id="747ab-108">Przykład 1. Tworzenie obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="747ab-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="747ab-109">To polecenie tworzy obiekt konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="747ab-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="747ab-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="747ab-110">PARAMETERS</span></span>

### <span data-ttu-id="747ab-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="747ab-111">-AadTenantId</span></span>
<span data-ttu-id="747ab-112">Określa identyfikator dzierżawy usługi Azure AD, który będzie stosowany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="747ab-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="747ab-113">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="747ab-113">-ApplicationId</span></span>
<span data-ttu-id="747ab-114">Pobiera lub ustawia identyfikator aplikacji głównej usługi w celu uzyskania dostępu do usługi Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="747ab-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="747ab-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="747ab-115">-AssignedIdentity</span></span>
<span data-ttu-id="747ab-116">Pobiera lub ustawia przypisaną tożsamość.</span><span class="sxs-lookup"><span data-stu-id="747ab-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="747ab-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="747ab-117">-CertificateFileContents</span></span>
<span data-ttu-id="747ab-118">Określa zawartość pliku certyfikatu, która będzie używana podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="747ab-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="747ab-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="747ab-119">-CertificateFilePath</span></span>
<span data-ttu-id="747ab-120">Określa ścieżkę do pliku certyfikatu, który zostanie wykorzystany do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="747ab-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="747ab-121">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="747ab-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="747ab-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="747ab-122">-CertificatePassword</span></span>
<span data-ttu-id="747ab-123">Określa hasło certyfikatu, które zostanie użyte do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="747ab-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="747ab-124">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="747ab-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="747ab-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="747ab-125">-ClusterTier</span></span>
<span data-ttu-id="747ab-126">Określa poziom klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="747ab-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="747ab-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="747ab-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="747ab-128">Standard</span><span class="sxs-lookup"><span data-stu-id="747ab-128">Standard</span></span>
- <span data-ttu-id="747ab-129">Premium wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="747ab-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="747ab-130">Warstwa Premium może być używana tylko w przypadku klastrów z systemem Linux i umożliwia korzystanie z nowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="747ab-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="747ab-131">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="747ab-131">-ClusterType</span></span>
<span data-ttu-id="747ab-132">Określa typ klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="747ab-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="747ab-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="747ab-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="747ab-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="747ab-134">Hadoop</span></span>
- <span data-ttu-id="747ab-135">HBase</span><span class="sxs-lookup"><span data-stu-id="747ab-135">HBase</span></span>
- <span data-ttu-id="747ab-136">Burz</span><span class="sxs-lookup"><span data-stu-id="747ab-136">Storm</span></span>
- <span data-ttu-id="747ab-137">ISKr</span><span class="sxs-lookup"><span data-stu-id="747ab-137">Spark</span></span>
- <span data-ttu-id="747ab-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="747ab-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="747ab-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="747ab-139">Kafka</span></span>
- <span data-ttu-id="747ab-140">RServer</span><span class="sxs-lookup"><span data-stu-id="747ab-140">RServer</span></span>

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

### <span data-ttu-id="747ab-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="747ab-141">-DefaultProfile</span></span>
<span data-ttu-id="747ab-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="747ab-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="747ab-143">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="747ab-143">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="747ab-144">Określa klucz konta dla domyślnego konta usługi Azure Storage, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="747ab-144">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="747ab-145">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="747ab-145">-DefaultStorageAccountName</span></span>
<span data-ttu-id="747ab-146">Określa nazwę domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="747ab-146">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="747ab-147">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="747ab-147">-DefaultStorageAccountType</span></span>
<span data-ttu-id="747ab-148">Określa typ domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="747ab-148">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="747ab-149">Możliwe wartości to AzureStorage i AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="747ab-149">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="747ab-150">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="747ab-150">-EdgeNodeSize</span></span>
<span data-ttu-id="747ab-151">Określa rozmiar maszyny wirtualnej dla węzła Edge.</span><span class="sxs-lookup"><span data-stu-id="747ab-151">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="747ab-152">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="747ab-152">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="747ab-153">Ten parametr jest prawidłowy tylko w przypadku klastrów RServer.</span><span class="sxs-lookup"><span data-stu-id="747ab-153">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="747ab-154">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="747ab-154">-EncryptionAlgorithm</span></span>
<span data-ttu-id="747ab-155">Pobiera lub ustawia algorytm szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="747ab-155">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="747ab-156">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="747ab-156">-EncryptionAtHost</span></span>
<span data-ttu-id="747ab-157">Pobiera lub ustawia flagę wskazującą, czy włączyć szyfrowanie na hoście.</span><span class="sxs-lookup"><span data-stu-id="747ab-157">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="747ab-158">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="747ab-158">-EncryptionInTransit</span></span>
<span data-ttu-id="747ab-159">Pobiera lub ustawia flagę wskazującą, czy włączyć szyfrowanie w tranzycie.</span><span class="sxs-lookup"><span data-stu-id="747ab-159">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="747ab-160">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="747ab-160">-EncryptionKeyName</span></span>
<span data-ttu-id="747ab-161">Pobiera lub ustawia nazwę klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="747ab-161">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="747ab-162">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="747ab-162">-EncryptionKeyVersion</span></span>
<span data-ttu-id="747ab-163">Pobiera lub ustawia wersję klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="747ab-163">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="747ab-164">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="747ab-164">-EncryptionVaultUri</span></span>
<span data-ttu-id="747ab-165">Pobiera lub ustawia identyfikator URI magazynu szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="747ab-165">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="747ab-166">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="747ab-166">-HeadNodeSize</span></span>
<span data-ttu-id="747ab-167">Określa rozmiar maszyny wirtualnej dla węzła głównego.</span><span class="sxs-lookup"><span data-stu-id="747ab-167">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="747ab-168">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="747ab-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="747ab-169">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="747ab-169">-HiveMetastore</span></span>
<span data-ttu-id="747ab-170">Określa, że metadane gałęzi są przechowywane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="747ab-170">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="747ab-171">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="747ab-171">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="747ab-172">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="747ab-172">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="747ab-173">Pobiera lub ustawia minimalną obsługiwaną wersję protokołu TLS.</span><span class="sxs-lookup"><span data-stu-id="747ab-173">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="747ab-174">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="747ab-174">-ObjectId</span></span>
<span data-ttu-id="747ab-175">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD reprezentujący klaster.</span><span class="sxs-lookup"><span data-stu-id="747ab-175">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="747ab-176">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="747ab-176">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="747ab-177">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="747ab-177">-OozieMetastore</span></span>
<span data-ttu-id="747ab-178">Określa, że w magazynie są przechowywane metadane Oozie.</span><span class="sxs-lookup"><span data-stu-id="747ab-178">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="747ab-179">Możesz również użyć polecenia cmdlet **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="747ab-179">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="747ab-180">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="747ab-180">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="747ab-181">Pobiera lub ustawia typ dostępu wychodzącego dla sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="747ab-181">Gets or sets the outbound access type to the public network.</span></span>

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

### <span data-ttu-id="747ab-182">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="747ab-182">-PublicNetworkAccessType</span></span>
<span data-ttu-id="747ab-183">Pobiera lub ustawia typ dostępu do sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="747ab-183">Gets or sets the public network access type.</span></span>

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

### <span data-ttu-id="747ab-184">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="747ab-184">-WorkerNodeSize</span></span>
<span data-ttu-id="747ab-185">Określa rozmiar maszyny wirtualnej dla węzła roboczego.</span><span class="sxs-lookup"><span data-stu-id="747ab-185">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="747ab-186">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="747ab-186">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="747ab-187">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="747ab-187">-ZookeeperNodeSize</span></span>
<span data-ttu-id="747ab-188">Określa rozmiar maszyny wirtualnej dla węzła Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="747ab-188">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="747ab-189">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="747ab-189">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="747ab-190">Ten parametr jest prawidłowy tylko w przypadku klastrów HBase lub burzy.</span><span class="sxs-lookup"><span data-stu-id="747ab-190">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="747ab-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="747ab-191">CommonParameters</span></span>
<span data-ttu-id="747ab-192">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="747ab-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="747ab-193">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="747ab-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="747ab-194">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="747ab-194">INPUTS</span></span>

### <span data-ttu-id="747ab-195">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="747ab-195">None</span></span>

## <span data-ttu-id="747ab-196">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="747ab-196">OUTPUTS</span></span>

### <span data-ttu-id="747ab-197">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="747ab-197">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="747ab-198">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="747ab-198">NOTES</span></span>

## <span data-ttu-id="747ab-199">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="747ab-199">RELATED LINKS</span></span>

[<span data-ttu-id="747ab-200">Dodaj-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="747ab-200">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


