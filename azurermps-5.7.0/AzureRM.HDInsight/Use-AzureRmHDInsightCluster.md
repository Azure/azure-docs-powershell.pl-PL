---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/use-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: c8a58963e66c8260a0001c144230cabf3a80b295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719185"
---
# <span data-ttu-id="87f35-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="87f35-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="87f35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87f35-102">SYNOPSIS</span></span>
<span data-ttu-id="87f35-103">Umożliwia wybranie klastra do użycia z poleceniem cmdlet Invoke-RmAzureHDInsightHiveJob.</span><span class="sxs-lookup"><span data-stu-id="87f35-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87f35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87f35-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87f35-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87f35-105">DESCRIPTION</span></span>
<span data-ttu-id="87f35-106">Polecenie cmdlet **use-AzureRmHDInsightCluster** umożliwia wybranie klastra usługi Azure HDInsight dla Invoke-AzureRmHDInsightHiveJob polecenia cmdlet służącego do przesyłania zadań w usłudze Hive.</span><span class="sxs-lookup"><span data-stu-id="87f35-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="87f35-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87f35-107">EXAMPLES</span></span>

### <span data-ttu-id="87f35-108">Przykład 1: Wybieranie klastra na potrzeby przesyłania zapytań dotyczących gałęzi</span><span class="sxs-lookup"><span data-stu-id="87f35-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="87f35-109">To polecenie umożliwia wybranie klastra do przesyłania zapytań dotyczących gałęzi.</span><span class="sxs-lookup"><span data-stu-id="87f35-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="87f35-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87f35-110">PARAMETERS</span></span>

### <span data-ttu-id="87f35-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="87f35-111">-ClusterName</span></span>
<span data-ttu-id="87f35-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="87f35-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f35-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f35-113">-DefaultProfile</span></span>
<span data-ttu-id="87f35-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="87f35-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87f35-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="87f35-115">-HttpCredential</span></span>
<span data-ttu-id="87f35-116">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="87f35-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f35-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87f35-117">-ResourceGroupName</span></span>
<span data-ttu-id="87f35-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87f35-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87f35-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f35-119">CommonParameters</span></span>
<span data-ttu-id="87f35-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87f35-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f35-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87f35-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f35-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87f35-122">INPUTS</span></span>

### <span data-ttu-id="87f35-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="87f35-123">None</span></span>
<span data-ttu-id="87f35-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="87f35-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87f35-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87f35-125">OUTPUTS</span></span>

### <span data-ttu-id="87f35-126">System. String</span><span class="sxs-lookup"><span data-stu-id="87f35-126">System.String</span></span>

## <span data-ttu-id="87f35-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87f35-127">NOTES</span></span>

## <span data-ttu-id="87f35-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87f35-128">RELATED LINKS</span></span>

[<span data-ttu-id="87f35-129">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="87f35-129">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="87f35-130">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="87f35-130">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


