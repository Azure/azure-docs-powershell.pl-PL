---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: e4ecdb86d3c8b055f76303af5c3b86fc9813e167
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064100"
---
# <span data-ttu-id="d58f2-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="d58f2-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="d58f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d58f2-102">SYNOPSIS</span></span>
<span data-ttu-id="d58f2-103">Ustawia domyślne ustawienie konta magazynu w obiekcie konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="d58f2-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="d58f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d58f2-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d58f2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d58f2-105">DESCRIPTION</span></span>
<span data-ttu-id="d58f2-106">Polecenie cmdlet **Set-AzHDInsightDefaultStorage** umożliwia ustawienie domyślnego konta magazynu w obiekcie konfiguracji klastra usługi Azure HDInsight utworzonego za pomocą polecenia cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="d58f2-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="d58f2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d58f2-107">EXAMPLES</span></span>

### <span data-ttu-id="d58f2-108">Przykład 1: Ustawianie domyślnego konta magazynu dla obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="d58f2-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
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

<span data-ttu-id="d58f2-109">To polecenie ustawia domyślne konto magazynu dla obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="d58f2-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="d58f2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d58f2-110">PARAMETERS</span></span>

### <span data-ttu-id="d58f2-111">-Config</span><span class="sxs-lookup"><span data-stu-id="d58f2-111">-Config</span></span>
<span data-ttu-id="d58f2-112">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58f2-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="d58f2-113">Ten obiekt jest tworzony przez polecenie cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="d58f2-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="d58f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58f2-114">-DefaultProfile</span></span>
<span data-ttu-id="d58f2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d58f2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d58f2-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d58f2-116">-StorageAccountKey</span></span>
<span data-ttu-id="d58f2-117">Określa klucz konta dla domyślnego konta usługi Azure Storage, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d58f2-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="d58f2-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d58f2-118">-StorageAccountName</span></span>
<span data-ttu-id="d58f2-119">Określa nazwę domyślnego konta magazynu, które będzie używane przez klaster usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d58f2-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="d58f2-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d58f2-120">-StorageAccountType</span></span>
<span data-ttu-id="d58f2-121">Pobiera lub ustawia typ domyślnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d58f2-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="d58f2-122">Domyślnie AzureStorage</span><span class="sxs-lookup"><span data-stu-id="d58f2-122">Defaults to AzureStorage</span></span>

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

### <span data-ttu-id="d58f2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58f2-123">CommonParameters</span></span>
<span data-ttu-id="d58f2-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58f2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58f2-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d58f2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58f2-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d58f2-126">INPUTS</span></span>

### <span data-ttu-id="d58f2-127">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d58f2-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="d58f2-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d58f2-128">OUTPUTS</span></span>

### <span data-ttu-id="d58f2-129">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d58f2-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="d58f2-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d58f2-130">NOTES</span></span>

## <span data-ttu-id="d58f2-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d58f2-131">RELATED LINKS</span></span>
