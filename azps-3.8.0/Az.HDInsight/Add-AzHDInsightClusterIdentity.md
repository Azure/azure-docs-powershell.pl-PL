---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: fcad97b2316e9db652fe4dc9df70bdc0f5d8b84d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053849"
---
# <span data-ttu-id="c0626-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="c0626-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="c0626-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0626-102">SYNOPSIS</span></span>
<span data-ttu-id="c0626-103">Dodaje tożsamość klastra do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="c0626-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="c0626-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0626-104">SYNTAX</span></span>

### <span data-ttu-id="c0626-105">CertificateFilePath (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c0626-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-ApplicationId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0626-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c0626-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-ApplicationId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0626-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c0626-107">DESCRIPTION</span></span>
<span data-ttu-id="c0626-108">Polecenie cmdlet **Add-AzHDInsightClusterIdentity** dodaje tożsamość klastra do obiektu konfiguracji usługi Azure HDInsight utworzonego za pomocą polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="c0626-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="c0626-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0626-109">EXAMPLES</span></span>

### <span data-ttu-id="c0626-110">Przykład 1: Dodawanie informacji o tożsamości klastra do obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="c0626-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $applicationId = "<Azure AD Service Principal Application ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -Application $applicationId
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="c0626-111">To polecenie dodaje informacje o tożsamości klastra do klastra o nazwie Your-Hadoop-001, co umożliwia klastrowi uzyskiwanie dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c0626-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="c0626-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0626-112">PARAMETERS</span></span>

### <span data-ttu-id="c0626-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="c0626-113">-AadTenantId</span></span>
<span data-ttu-id="c0626-114">Określa identyfikator dzierżawy usługi Azure AD, który będzie stosowany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c0626-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0626-115">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="c0626-115">-ApplicationId</span></span>
<span data-ttu-id="c0626-116">Identyfikator głównej aplikacji usługi w celu uzyskania dostępu do usługi Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="c0626-116">The Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="c0626-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c0626-117">-CertificateFileContents</span></span>
<span data-ttu-id="c0626-118">Określa zawartość pliku certyfikatu, która będzie używana podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c0626-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0626-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c0626-119">-CertificateFilePath</span></span>
<span data-ttu-id="c0626-120">Określa ścieżkę do pliku certyfikatu, który zostanie wykorzystany do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c0626-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c0626-121">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c0626-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0626-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c0626-122">-CertificatePassword</span></span>
<span data-ttu-id="c0626-123">Określa hasło certyfikatu, które zostanie użyte do uwierzytelnienia jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="c0626-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c0626-124">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c0626-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0626-125">-Config</span><span class="sxs-lookup"><span data-stu-id="c0626-125">-Config</span></span>
<span data-ttu-id="c0626-126">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0626-126">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="c0626-127">Ten obiekt jest tworzony za pomocą polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="c0626-127">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0626-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0626-128">-DefaultProfile</span></span>
<span data-ttu-id="c0626-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c0626-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0626-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c0626-130">-ObjectId</span></span>
<span data-ttu-id="c0626-131">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD reprezentujący klaster.</span><span class="sxs-lookup"><span data-stu-id="c0626-131">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="c0626-132">Klaster będzie go używać podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c0626-132">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0626-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0626-133">CommonParameters</span></span>
<span data-ttu-id="c0626-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0626-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0626-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0626-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0626-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0626-136">INPUTS</span></span>

### <span data-ttu-id="c0626-137">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c0626-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="c0626-138">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c0626-138">System.Guid</span></span>

## <span data-ttu-id="c0626-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0626-139">OUTPUTS</span></span>

### <span data-ttu-id="c0626-140">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c0626-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="c0626-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0626-141">NOTES</span></span>

## <span data-ttu-id="c0626-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0626-142">RELATED LINKS</span></span>

[<span data-ttu-id="c0626-143">Nowe — AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c0626-143">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


