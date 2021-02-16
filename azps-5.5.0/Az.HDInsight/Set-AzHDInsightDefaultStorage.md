---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: 06a783d0faf32dc2a3a35b448b1316ef50ba3326
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200187"
---
# <span data-ttu-id="50385-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="50385-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="50385-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50385-102">SYNOPSIS</span></span>
<span data-ttu-id="50385-103">Ustawia domyślne ustawienie konta magazynu w obiekcie konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="50385-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="50385-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="50385-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountResourceId] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50385-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="50385-105">DESCRIPTION</span></span>
<span data-ttu-id="50385-106">Polecenie cmdlet **Set-AzHDInsightDefaultStorage** ustawia domyślne ustawienie konta magazynu w obiekcie konfiguracji grup usługi Azure HDInsight utworzonym za pomocą polecenia cmdlet New-AzHDInsightClusterConfig magazynu.</span><span class="sxs-lookup"><span data-stu-id="50385-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="50385-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="50385-107">EXAMPLES</span></span>

### <span data-ttu-id="50385-108">Przykład 1. Ustawianie domyślnego konta magazynu dla obiektu konfiguracji klastrów</span><span class="sxs-lookup"><span data-stu-id="50385-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
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
                -StorageAccountResourceId $storageAccountResourceId `
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

<span data-ttu-id="50385-109">To polecenie ustawia domyślne konto magazynu dla obiektu konfiguracji klastrów.</span><span class="sxs-lookup"><span data-stu-id="50385-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="50385-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50385-110">PARAMETERS</span></span>

### <span data-ttu-id="50385-111">-Config</span><span class="sxs-lookup"><span data-stu-id="50385-111">-Config</span></span>
<span data-ttu-id="50385-112">Określa obiekt konfiguracji klastrów HDInsight, który zostanie zmodyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50385-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="50385-113">Ten obiekt jest tworzony przez polecenie cmdlet **New-AzHDInsightClusterConfig.**</span><span class="sxs-lookup"><span data-stu-id="50385-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="50385-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50385-114">-DefaultProfile</span></span>
<span data-ttu-id="50385-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="50385-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50385-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="50385-116">-StorageAccountKey</span></span>
<span data-ttu-id="50385-117">Określa klucz konta dla domyślnego konta usługi Azure Storage, które będzie używać klastra HDInsight.</span><span class="sxs-lookup"><span data-stu-id="50385-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="50385-118">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="50385-118">-StorageAccountResourceId</span></span>
<span data-ttu-id="50385-119">Nazwa konta magazynu, które ma zostać dodane do nowego klastra.</span><span class="sxs-lookup"><span data-stu-id="50385-119">The storage account name for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="50385-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="50385-120">-StorageAccountType</span></span>
<span data-ttu-id="50385-121">Pobiera lub ustawia typ domyślnego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="50385-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="50385-122">Wartość domyślna to AzureStorage</span><span class="sxs-lookup"><span data-stu-id="50385-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50385-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50385-123">CommonParameters</span></span>
<span data-ttu-id="50385-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50385-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50385-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50385-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50385-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50385-126">INPUTS</span></span>

### <span data-ttu-id="50385-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="50385-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="50385-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50385-128">OUTPUTS</span></span>

### <span data-ttu-id="50385-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="50385-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="50385-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="50385-130">NOTES</span></span>

## <span data-ttu-id="50385-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50385-131">RELATED LINKS</span></span>
