---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232311"
---
# <span data-ttu-id="372ec-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="372ec-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="372ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="372ec-102">SYNOPSIS</span></span>
<span data-ttu-id="372ec-103">Tworzy nieutrwalony obiekt konfiguracji klastra opisujący konfigurację klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="372ec-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="372ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="372ec-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-StorageAccountResourceId <String>] [-StorageAccountKey <String>]
 [-StorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="372ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="372ec-105">DESCRIPTION</span></span>
<span data-ttu-id="372ec-106">Polecenie cmdlet **New-AzHDInsightClusterConfig** tworzy nieutrwalony obiekt opisujący konfigurację klastra usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="372ec-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="372ec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="372ec-107">EXAMPLES</span></span>

### <span data-ttu-id="372ec-108">Przykład 1. Tworzenie obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="372ec-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
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
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="372ec-109">To polecenie tworzy obiekt konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="372ec-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="372ec-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="372ec-110">PARAMETERS</span></span>

### <span data-ttu-id="372ec-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="372ec-111">-AadTenantId</span></span>
<span data-ttu-id="372ec-112">Określa identyfikator dzierżawy usługi Azure AD, który będzie stosowany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="372ec-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="372ec-113">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="372ec-113">-ApplicationId</span></span>
<span data-ttu-id="372ec-114">Pobiera lub ustawia identyfikator aplikacji głównej usługi w celu uzyskania dostępu do usługi Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="372ec-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="372ec-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="372ec-115">-AssignedIdentity</span></span>
<span data-ttu-id="372ec-116">Pobiera lub ustawia przypisaną tożsamość.</span><span class="sxs-lookup"><span data-stu-id="372ec-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="372ec-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="372ec-117">-CertificateFileContents</span></span>
<span data-ttu-id="372ec-118">Określa zawartość pliku certyfikatu, która będzie używana podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="372ec-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="372ec-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="372ec-119">-CertificateFilePath</span></span>
<span data-ttu-id="372ec-120">Określa ścieżkę do pliku certyfikatu, który zostanie wykorzystany do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="372ec-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="372ec-121">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="372ec-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="372ec-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="372ec-122">-CertificatePassword</span></span>
<span data-ttu-id="372ec-123">Określa hasło certyfikatu, które zostanie użyte do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="372ec-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="372ec-124">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="372ec-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="372ec-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="372ec-125">-ClusterTier</span></span>
<span data-ttu-id="372ec-126">Określa poziom klastra usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="372ec-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="372ec-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="372ec-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="372ec-128">Standard</span><span class="sxs-lookup"><span data-stu-id="372ec-128">Standard</span></span>
- <span data-ttu-id="372ec-129">Premium wartość domyślna to standard.</span><span class="sxs-lookup"><span data-stu-id="372ec-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="372ec-130">Warstwa Premium może być używana tylko w przypadku klastrów z systemem Linux i umożliwia korzystanie z nowych funkcji.</span><span class="sxs-lookup"><span data-stu-id="372ec-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="372ec-131">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="372ec-131">-ClusterType</span></span>
<span data-ttu-id="372ec-132">Określa typ klastra do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="372ec-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="372ec-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="372ec-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="372ec-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="372ec-134">Hadoop</span></span>
- <span data-ttu-id="372ec-135">HBase</span><span class="sxs-lookup"><span data-stu-id="372ec-135">HBase</span></span>
- <span data-ttu-id="372ec-136">Burz</span><span class="sxs-lookup"><span data-stu-id="372ec-136">Storm</span></span>
- <span data-ttu-id="372ec-137">ISKr</span><span class="sxs-lookup"><span data-stu-id="372ec-137">Spark</span></span>
- <span data-ttu-id="372ec-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="372ec-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="372ec-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="372ec-139">Kafka</span></span>
- <span data-ttu-id="372ec-140">RServer</span><span class="sxs-lookup"><span data-stu-id="372ec-140">RServer</span></span>

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

### <span data-ttu-id="372ec-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372ec-141">-DefaultProfile</span></span>
<span data-ttu-id="372ec-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="372ec-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="372ec-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="372ec-143">-EdgeNodeSize</span></span>
<span data-ttu-id="372ec-144">Określa rozmiar maszyny wirtualnej dla węzła Edge.</span><span class="sxs-lookup"><span data-stu-id="372ec-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="372ec-145">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="372ec-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="372ec-146">Ten parametr jest prawidłowy tylko w przypadku klastrów RServer.</span><span class="sxs-lookup"><span data-stu-id="372ec-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="372ec-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="372ec-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="372ec-148">Pobiera lub ustawia algorytm szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="372ec-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="372ec-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="372ec-149">-EncryptionAtHost</span></span>
<span data-ttu-id="372ec-150">Pobiera lub ustawia flagę wskazującą, czy włączyć szyfrowanie na hoście.</span><span class="sxs-lookup"><span data-stu-id="372ec-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="372ec-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="372ec-151">-EncryptionInTransit</span></span>
<span data-ttu-id="372ec-152">Pobiera lub ustawia flagę wskazującą, czy włączyć szyfrowanie w tranzycie.</span><span class="sxs-lookup"><span data-stu-id="372ec-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="372ec-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="372ec-153">-EncryptionKeyName</span></span>
<span data-ttu-id="372ec-154">Pobiera lub ustawia nazwę klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="372ec-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="372ec-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="372ec-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="372ec-156">Pobiera lub ustawia wersję klucza szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="372ec-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="372ec-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="372ec-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="372ec-158">Pobiera lub ustawia identyfikator URI magazynu szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="372ec-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="372ec-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="372ec-159">-HeadNodeSize</span></span>
<span data-ttu-id="372ec-160">Określa rozmiar maszyny wirtualnej dla węzła głównego.</span><span class="sxs-lookup"><span data-stu-id="372ec-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="372ec-161">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="372ec-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="372ec-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="372ec-162">-HiveMetastore</span></span>
<span data-ttu-id="372ec-163">Określa, że metadane gałęzi są przechowywane w magazynie.</span><span class="sxs-lookup"><span data-stu-id="372ec-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="372ec-164">Możesz również użyć polecenia cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="372ec-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="372ec-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="372ec-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="372ec-166">Pobiera lub ustawia minimalną obsługiwaną wersję protokołu TLS.</span><span class="sxs-lookup"><span data-stu-id="372ec-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="372ec-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="372ec-167">-ObjectId</span></span>
<span data-ttu-id="372ec-168">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD reprezentujący klaster.</span><span class="sxs-lookup"><span data-stu-id="372ec-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="372ec-169">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="372ec-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="372ec-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="372ec-170">-OozieMetastore</span></span>
<span data-ttu-id="372ec-171">Określa, że w magazynie są przechowywane metadane Oozie.</span><span class="sxs-lookup"><span data-stu-id="372ec-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="372ec-172">Możesz również użyć polecenia cmdlet **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="372ec-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="372ec-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="372ec-173">-StorageAccountKey</span></span>
<span data-ttu-id="372ec-174">Pobiera lub ustawia klucz dostępu do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="372ec-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="372ec-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="372ec-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="372ec-176">Pobiera lub ustawia identyfikator zasobu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="372ec-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="372ec-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="372ec-177">-StorageAccountType</span></span>
<span data-ttu-id="372ec-178">Pobiera lub ustawia typ domyślnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="372ec-178">Gets or sets the type of the default storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372ec-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="372ec-179">-WorkerNodeSize</span></span>
<span data-ttu-id="372ec-180">Określa rozmiar maszyny wirtualnej dla węzła roboczego.</span><span class="sxs-lookup"><span data-stu-id="372ec-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="372ec-181">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="372ec-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="372ec-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="372ec-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="372ec-183">Określa rozmiar maszyny wirtualnej dla węzła Zookeeper.</span><span class="sxs-lookup"><span data-stu-id="372ec-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="372ec-184">Użyj Get-AzVMSize w celu uzyskania dopuszczalnych rozmiarów maszyn wirtualnych, a następnie zobacz cennik usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="372ec-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="372ec-185">Ten parametr jest prawidłowy tylko w przypadku klastrów HBase lub burzy.</span><span class="sxs-lookup"><span data-stu-id="372ec-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="372ec-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372ec-186">CommonParameters</span></span>
<span data-ttu-id="372ec-187">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="372ec-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372ec-188">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="372ec-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372ec-189">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="372ec-189">INPUTS</span></span>

### <span data-ttu-id="372ec-190">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="372ec-190">None</span></span>

## <span data-ttu-id="372ec-191">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="372ec-191">OUTPUTS</span></span>

### <span data-ttu-id="372ec-192">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="372ec-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="372ec-193">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="372ec-193">NOTES</span></span>

## <span data-ttu-id="372ec-194">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="372ec-194">RELATED LINKS</span></span>

[<span data-ttu-id="372ec-195">Dodaj-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="372ec-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


