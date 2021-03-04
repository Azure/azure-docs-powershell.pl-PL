---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightClusterIdentity.md
ms.openlocfilehash: b154ab0bbcf10c0fb1d68b7634e5e2d1bf97a45d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990193"
---
# <span data-ttu-id="0d33d-101">Add-AzHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="0d33d-101">Add-AzHDInsightClusterIdentity</span></span>

## <span data-ttu-id="0d33d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d33d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d33d-103">Dodaje tożsamość klastra do obiektu konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="0d33d-103">Adds a cluster identity to a cluster configuration object.</span></span>

## <span data-ttu-id="0d33d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0d33d-104">SYNTAX</span></span>

### <span data-ttu-id="0d33d-105">CertificateFilePath (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0d33d-105">CertificateFilePath (Default)</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d33d-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="0d33d-106">CertificateFileContents</span></span>
```
Add-AzHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [[-ApplicationId] <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d33d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0d33d-107">DESCRIPTION</span></span>
<span data-ttu-id="0d33d-108">Polecenie **cmdlet Add-AzHDInsightClusterIdentity** dodaje tożsamość klastrów do obiektu konfiguracji usługi Azure HDInsight utworzonego za pomocą New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d33d-108">The **Add-AzHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="0d33d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0d33d-109">EXAMPLES</span></span>

### <span data-ttu-id="0d33d-110">Przykład 1. Dodawanie informacji tożsamości klastrów do obiektu konfiguracji klastrów</span><span class="sxs-lookup"><span data-stu-id="0d33d-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
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
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="0d33d-111">To polecenie dodaje informacje tożsamości klastrów do klastra o nazwie Twoja-hadoop-001, umożliwiając klastrowi dostęp do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d33d-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="0d33d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d33d-112">PARAMETERS</span></span>

### <span data-ttu-id="0d33d-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="0d33d-113">-AadTenantId</span></span>
<span data-ttu-id="0d33d-114">Określa identyfikator dzierżawy usługi Azure AD, który będzie używany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d33d-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0d33d-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0d33d-115">-ApplicationId</span></span>
<span data-ttu-id="0d33d-116">The Service Principal Application Id for accessing Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="0d33d-116">The Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d33d-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="0d33d-117">-CertificateFileContents</span></span>
<span data-ttu-id="0d33d-118">Określa zawartość pliku certyfikatu, który będzie używany podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d33d-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0d33d-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="0d33d-119">-CertificateFilePath</span></span>
<span data-ttu-id="0d33d-120">Określa ścieżkę pliku do certyfikatu, który będzie używany do uwierzytelniania jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="0d33d-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="0d33d-121">Klaster będzie korzystać z tej funkcji podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d33d-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0d33d-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="0d33d-122">-CertificatePassword</span></span>
<span data-ttu-id="0d33d-123">Określa hasło certyfikatu, który będzie używany do uwierzytelniania jako podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="0d33d-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="0d33d-124">Klaster będzie korzystać z tej funkcji podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d33d-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0d33d-125">-Config</span><span class="sxs-lookup"><span data-stu-id="0d33d-125">-Config</span></span>
<span data-ttu-id="0d33d-126">Określa obiekt konfiguracji klastrów HDInsight, który modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d33d-126">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="0d33d-127">Ten obiekt jest tworzony przez New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d33d-127">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="0d33d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d33d-128">-DefaultProfile</span></span>
<span data-ttu-id="0d33d-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0d33d-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d33d-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0d33d-130">-ObjectId</span></span>
<span data-ttu-id="0d33d-131">Określa identyfikator obiektu usługi Azure AD (identyfikator GUID) podmiotu zabezpieczeń usługi Azure AD, który reprezentuje klaster.</span><span class="sxs-lookup"><span data-stu-id="0d33d-131">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="0d33d-132">Klaster będzie korzystać z tej funkcji podczas uzyskiwania dostępu do usługi Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d33d-132">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0d33d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d33d-133">CommonParameters</span></span>
<span data-ttu-id="0d33d-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d33d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d33d-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d33d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d33d-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d33d-136">INPUTS</span></span>

### <span data-ttu-id="0d33d-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0d33d-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

### <span data-ttu-id="0d33d-138">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0d33d-138">System.Guid</span></span>

## <span data-ttu-id="0d33d-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d33d-139">OUTPUTS</span></span>

### <span data-ttu-id="0d33d-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0d33d-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="0d33d-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0d33d-141">NOTES</span></span>

## <span data-ttu-id="0d33d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d33d-142">RELATED LINKS</span></span>

[<span data-ttu-id="0d33d-143">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="0d33d-143">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


