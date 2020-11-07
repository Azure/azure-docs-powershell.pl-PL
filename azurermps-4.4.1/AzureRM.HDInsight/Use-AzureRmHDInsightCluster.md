---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: 01f9a2a9bae03606773c146f44f7e737fb9b613f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719304"
---
# <span data-ttu-id="8400b-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8400b-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="8400b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8400b-102">SYNOPSIS</span></span>
<span data-ttu-id="8400b-103">Umożliwia wybranie klastra do użycia z poleceniem cmdlet Invoke-RmAzureHDInsightHiveJob.</span><span class="sxs-lookup"><span data-stu-id="8400b-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8400b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8400b-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8400b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8400b-105">DESCRIPTION</span></span>
<span data-ttu-id="8400b-106">Polecenie cmdlet **use-AzureRmHDInsightCluster** umożliwia wybranie klastra usługi Azure HDInsight dla Invoke-AzureRmHDInsightHiveJob polecenia cmdlet służącego do przesyłania zadań w usłudze Hive.</span><span class="sxs-lookup"><span data-stu-id="8400b-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="8400b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8400b-107">EXAMPLES</span></span>

### <span data-ttu-id="8400b-108">Przykład 1: Wybieranie klastra na potrzeby przesyłania zapytań dotyczących gałęzi</span><span class="sxs-lookup"><span data-stu-id="8400b-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="8400b-109">To polecenie umożliwia wybranie klastra do przesyłania zapytań dotyczących gałęzi.</span><span class="sxs-lookup"><span data-stu-id="8400b-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="8400b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8400b-110">PARAMETERS</span></span>

### <span data-ttu-id="8400b-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="8400b-111">-ClusterName</span></span>
<span data-ttu-id="8400b-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="8400b-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8400b-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="8400b-113">-HttpCredential</span></span>
<span data-ttu-id="8400b-114">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="8400b-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8400b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8400b-115">-ResourceGroupName</span></span>
<span data-ttu-id="8400b-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8400b-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8400b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8400b-117">-DefaultProfile</span></span>
<span data-ttu-id="8400b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8400b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8400b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8400b-119">CommonParameters</span></span>
<span data-ttu-id="8400b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8400b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8400b-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8400b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8400b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8400b-122">INPUTS</span></span>

## <span data-ttu-id="8400b-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8400b-123">OUTPUTS</span></span>

### <span data-ttu-id="8400b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8400b-124">System.String</span></span>

## <span data-ttu-id="8400b-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8400b-125">NOTES</span></span>

## <span data-ttu-id="8400b-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8400b-126">RELATED LINKS</span></span>

[<span data-ttu-id="8400b-127">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8400b-127">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="8400b-128">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8400b-128">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


