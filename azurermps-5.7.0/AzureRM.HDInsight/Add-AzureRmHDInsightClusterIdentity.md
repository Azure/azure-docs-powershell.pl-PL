---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
ms.openlocfilehash: e4e481a7ee26be966abda3d996575ab1bbd03b42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544327"
---
# <span data-ttu-id="66fb9-101">Add-AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="66fb9-101">Add-AzureRmHDInsightClusterIdentity</span></span>

## <span data-ttu-id="66fb9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="66fb9-103">Dodaje tożsamość klastra do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="66fb9-103">Adds a cluster identity to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66fb9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66fb9-104">SYNTAX</span></span>

### <span data-ttu-id="66fb9-105">CertificateFilePath (domyślny)</span><span class="sxs-lookup"><span data-stu-id="66fb9-105">CertificateFilePath (Default)</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66fb9-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="66fb9-106">CertificateFileContents</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66fb9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="66fb9-107">DESCRIPTION</span></span>
<span data-ttu-id="66fb9-108">Polecenie cmdlet **Add-AzureRmHDInsightClusterIdentity** dodaje tożsamość klastra do obiektu konfiguracji usługi Azure HDInsight utworzonego za pomocą polecenia cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="66fb9-108">The **Add-AzureRmHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="66fb9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66fb9-109">EXAMPLES</span></span>

### <span data-ttu-id="66fb9-110">Przykład 1: Dodawanie informacji o tożsamości klastra do obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="66fb9-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzureRmContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="66fb9-111">To polecenie dodaje informacje o tożsamości klastra do klastra o nazwie Your-Hadoop-001, co umożliwia klastrowi uzyskiwanie dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="66fb9-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="66fb9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66fb9-112">PARAMETERS</span></span>

### <span data-ttu-id="66fb9-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="66fb9-113">-AadTenantId</span></span>
<span data-ttu-id="66fb9-114">Określa identyfikator dzierżawy usługi Azure AD, który będzie stosowany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="66fb9-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fb9-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="66fb9-115">-CertificateFileContents</span></span>
<span data-ttu-id="66fb9-116">Określa zawartość pliku certyfikatu, która będzie używana podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="66fb9-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Byte[]
Parameter Sets: CertificateFileContents
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fb9-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="66fb9-117">-CertificateFilePath</span></span>
<span data-ttu-id="66fb9-118">Określa ścieżkę do pliku certyfikatu, który zostanie wykorzystany do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="66fb9-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="66fb9-119">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="66fb9-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: CertificateFilePath
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fb9-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="66fb9-120">-CertificatePassword</span></span>
<span data-ttu-id="66fb9-121">Określa hasło certyfikatu, które zostanie użyte do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="66fb9-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="66fb9-122">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="66fb9-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fb9-123">-Config</span><span class="sxs-lookup"><span data-stu-id="66fb9-123">-Config</span></span>
<span data-ttu-id="66fb9-124">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66fb9-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="66fb9-125">Ten obiekt jest tworzony za pomocą polecenia cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="66fb9-125">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66fb9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fb9-126">-DefaultProfile</span></span>
<span data-ttu-id="66fb9-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="66fb9-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66fb9-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="66fb9-128">-ObjectId</span></span>
<span data-ttu-id="66fb9-129">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD reprezentujący klaster.</span><span class="sxs-lookup"><span data-stu-id="66fb9-129">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="66fb9-130">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="66fb9-130">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66fb9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fb9-131">CommonParameters</span></span>
<span data-ttu-id="66fb9-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66fb9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fb9-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66fb9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fb9-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66fb9-134">INPUTS</span></span>

### <span data-ttu-id="66fb9-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="66fb9-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="66fb9-136">Parametr "config" akceptuje wartość typu "AzureHDInsightConfig" z procesu</span><span class="sxs-lookup"><span data-stu-id="66fb9-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

### <span data-ttu-id="66fb9-137">Wiodąc</span><span class="sxs-lookup"><span data-stu-id="66fb9-137">Guid</span></span>
<span data-ttu-id="66fb9-138">Parametr "ObjectId" przyjmuje wartość typu "GUID" z procesu</span><span class="sxs-lookup"><span data-stu-id="66fb9-138">Parameter 'ObjectId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="66fb9-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66fb9-139">OUTPUTS</span></span>

### <span data-ttu-id="66fb9-140">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="66fb9-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="66fb9-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66fb9-141">NOTES</span></span>

## <span data-ttu-id="66fb9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66fb9-142">RELATED LINKS</span></span>

[<span data-ttu-id="66fb9-143">Nowe — AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="66fb9-143">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

