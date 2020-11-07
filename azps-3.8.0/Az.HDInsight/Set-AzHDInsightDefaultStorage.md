---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: e4ecdb86d3c8b055f76303af5c3b86fc9813e167
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895209"
---
# <span data-ttu-id="630e6-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="630e6-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="630e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="630e6-102">SYNOPSIS</span></span>
<span data-ttu-id="630e6-103">Ustawia domyślne ustawienie konta magazynu w obiekcie konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="630e6-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="630e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="630e6-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="630e6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="630e6-105">DESCRIPTION</span></span>
<span data-ttu-id="630e6-106">Polecenie cmdlet **Set-AzHDInsightDefaultStorage** umożliwia ustawienie domyślnego konta magazynu w obiekcie konfiguracji klastra usługi Azure HDInsight utworzonego za pomocą polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="630e6-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="630e6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="630e6-107">EXAMPLES</span></span>

### <span data-ttu-id="630e6-108">Przykład 1: Ustawianie domyślnego konta magazynu dla obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="630e6-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Set-AzHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="630e6-109">To polecenie ustawia domyślne konto magazynu dla obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="630e6-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="630e6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="630e6-110">PARAMETERS</span></span>

### <span data-ttu-id="630e6-111">-Config</span><span class="sxs-lookup"><span data-stu-id="630e6-111">-Config</span></span>
<span data-ttu-id="630e6-112">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="630e6-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="630e6-113">Ten obiekt jest tworzony przez polecenie cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="630e6-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="630e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="630e6-114">-DefaultProfile</span></span>
<span data-ttu-id="630e6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="630e6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="630e6-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="630e6-116">-StorageAccountKey</span></span>
<span data-ttu-id="630e6-117">Określa klucz konta dla domyślnego konta usługi Azure Storage, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="630e6-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="630e6-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="630e6-118">-StorageAccountName</span></span>
<span data-ttu-id="630e6-119">Określa nazwę domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="630e6-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="630e6-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="630e6-120">-StorageAccountType</span></span>
<span data-ttu-id="630e6-121">Pobiera lub ustawia typ domyślnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="630e6-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="630e6-122">Domyślnie AzureStorage</span><span class="sxs-lookup"><span data-stu-id="630e6-122">Defaults to AzureStorage</span></span>

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

### <span data-ttu-id="630e6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="630e6-123">CommonParameters</span></span>
<span data-ttu-id="630e6-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="630e6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="630e6-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="630e6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="630e6-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="630e6-126">INPUTS</span></span>

### <span data-ttu-id="630e6-127">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="630e6-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="630e6-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="630e6-128">OUTPUTS</span></span>

### <span data-ttu-id="630e6-129">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="630e6-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="630e6-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="630e6-130">NOTES</span></span>

## <span data-ttu-id="630e6-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="630e6-131">RELATED LINKS</span></span>
