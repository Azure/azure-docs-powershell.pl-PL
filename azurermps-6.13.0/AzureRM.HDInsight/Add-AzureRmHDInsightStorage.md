---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightStorage.md
ms.openlocfilehash: 1d81b5c528739fb012f90e6e112422c4e828c1f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545320"
---
# <span data-ttu-id="0c138-101">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="0c138-101">Add-AzureRmHDInsightStorage</span></span>

## <span data-ttu-id="0c138-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c138-102">SYNOPSIS</span></span>
<span data-ttu-id="0c138-103">Dodaje klucz usługi Azure Storage do obiektu konfiguracji klastra.</span><span class="sxs-lookup"><span data-stu-id="0c138-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c138-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c138-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c138-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0c138-105">DESCRIPTION</span></span>
<span data-ttu-id="0c138-106">Polecenie cmdlet **Add-AzureRmHDInsightStorage** dodaje wpis konta usługi Azure Storage do obiektu konfiguracji usługi Azure HDInsight utworzonego za pomocą polecenia cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="0c138-106">The **Add-AzureRmHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="0c138-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c138-107">EXAMPLES</span></span>

### <span data-ttu-id="0c138-108">Przykład 1: Dodawanie klucza magazynu platformy Azure do obiektu konfiguracji klastra</span><span class="sxs-lookup"><span data-stu-id="0c138-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
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

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzureRmStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="0c138-109">To polecenie dodaje wpis konta magazynu obiektów BLOB do konfiguracji usługi HDInsight o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="0c138-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="0c138-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c138-110">PARAMETERS</span></span>

### <span data-ttu-id="0c138-111">-Config</span><span class="sxs-lookup"><span data-stu-id="0c138-111">-Config</span></span>
<span data-ttu-id="0c138-112">Określa obiekt konfiguracji klastra usługi HDInsight, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c138-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="0c138-113">Ten obiekt jest tworzony przez polecenie cmdlet **New-AzureRmHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="0c138-113">This object is created by the **New-AzureRmHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="0c138-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c138-114">-DefaultProfile</span></span>
<span data-ttu-id="0c138-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0c138-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c138-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0c138-116">-StorageAccountKey</span></span>
<span data-ttu-id="0c138-117">Określa klucz konta magazynu dla konta magazynu, który ma zostać dodany do nowego klastra.</span><span class="sxs-lookup"><span data-stu-id="0c138-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c138-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0c138-118">-StorageAccountName</span></span>
<span data-ttu-id="0c138-119">Określa nazwę konta magazynu dla konta magazynu, które ma zostać dodane do klastra.</span><span class="sxs-lookup"><span data-stu-id="0c138-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="0c138-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c138-120">CommonParameters</span></span>
<span data-ttu-id="0c138-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c138-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c138-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c138-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c138-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c138-123">INPUTS</span></span>

### <span data-ttu-id="0c138-124">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0c138-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="0c138-125">Parametry: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c138-125">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="0c138-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c138-126">OUTPUTS</span></span>

### <span data-ttu-id="0c138-127">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0c138-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="0c138-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c138-128">NOTES</span></span>

## <span data-ttu-id="0c138-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c138-129">RELATED LINKS</span></span>

[<span data-ttu-id="0c138-130">Nowe — AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="0c138-130">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)


