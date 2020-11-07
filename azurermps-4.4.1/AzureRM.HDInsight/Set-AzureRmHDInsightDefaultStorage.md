---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightDefaultStorage.md
ms.openlocfilehash: a0c534042df15d4ef999b47a5e468b1e13a8d14f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719310"
---
# <span data-ttu-id="9747b-101">Set-AzureRmHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="9747b-101">Set-AzureRmHDInsightDefaultStorage</span></span>

## <span data-ttu-id="9747b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9747b-102">SYNOPSIS</span></span>
<span data-ttu-id="9747b-103">Ustawia domyślne ustawienie konta magazynu w obiekcie konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="9747b-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9747b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9747b-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9747b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9747b-105">DESCRIPTION</span></span>
<span data-ttu-id="9747b-106">Polecenie cmdlet **Set-AzureRmHDInsightDefaultStorage** umożliwia ustawienie domyślnego konta magazynu w obiekcie konfiguracji klastra usługi Azure HDInsight utworzonego za pomocą polecenia cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="9747b-106">The **Set-AzureRmHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="9747b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9747b-107">EXAMPLES</span></span>

### <span data-ttu-id="9747b-108">Przykład 1: Ustawianie domyślnego konta magazynu dla obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="9747b-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Set-AzureRmHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="9747b-109">To polecenie ustawia domyślne konto magazynu dla obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="9747b-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="9747b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9747b-110">PARAMETERS</span></span>

### <span data-ttu-id="9747b-111">-Config</span><span class="sxs-lookup"><span data-stu-id="9747b-111">-Config</span></span>
<span data-ttu-id="9747b-112">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9747b-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="9747b-113">Ten obiekt jest tworzony przez polecenie cmdlet **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="9747b-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="9747b-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9747b-114">-StorageAccountKey</span></span>
<span data-ttu-id="9747b-115">Określa klucz konta dla domyślnego konta usługi Azure Storage, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9747b-115">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9747b-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9747b-116">-StorageAccountName</span></span>
<span data-ttu-id="9747b-117">Określa nazwę domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9747b-117">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="9747b-118">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9747b-118">-StorageAccountType</span></span>
<span data-ttu-id="9747b-119">Pobiera lub ustawia typ domyślnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="9747b-119">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="9747b-120">Domyślnie AzureStorage</span><span class="sxs-lookup"><span data-stu-id="9747b-120">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9747b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9747b-121">-DefaultProfile</span></span>
<span data-ttu-id="9747b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9747b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9747b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9747b-123">CommonParameters</span></span>
<span data-ttu-id="9747b-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9747b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9747b-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9747b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9747b-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9747b-126">INPUTS</span></span>

### <span data-ttu-id="9747b-127">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="9747b-127">AzureHDInsightConfig</span></span>
<span data-ttu-id="9747b-128">Parametr "config" akceptuje wartość typu "AzureHDInsightConfig" z procesu</span><span class="sxs-lookup"><span data-stu-id="9747b-128">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="9747b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9747b-129">OUTPUTS</span></span>

### <span data-ttu-id="9747b-130">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="9747b-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="9747b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9747b-131">NOTES</span></span>

## <span data-ttu-id="9747b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9747b-132">RELATED LINKS</span></span>

