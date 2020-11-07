---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: 7e9df747becd5e2bd49b865b61f963d1db585e17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705288"
---
# <span data-ttu-id="3a545-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3a545-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="3a545-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a545-102">SYNOPSIS</span></span>
<span data-ttu-id="3a545-103">Umożliwia wybranie klastra do użycia z poleceniem cmdlet Invoke-RmAzureHDInsightHiveJob.</span><span class="sxs-lookup"><span data-stu-id="3a545-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="3a545-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a545-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a545-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a545-105">DESCRIPTION</span></span>
<span data-ttu-id="3a545-106">Polecenie cmdlet **use-AzHDInsightCluster** umożliwia wybranie klastra usługi Azure HDInsight dla Invoke-AzHDInsightHiveJob polecenia cmdlet służącego do przesyłania zadań w usłudze Hive.</span><span class="sxs-lookup"><span data-stu-id="3a545-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="3a545-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a545-107">EXAMPLES</span></span>

### <span data-ttu-id="3a545-108">Przykład 1: Wybieranie klastra na potrzeby przesyłania zapytań dotyczących gałęzi</span><span class="sxs-lookup"><span data-stu-id="3a545-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="3a545-109">To polecenie umożliwia wybranie klastra do przesyłania zapytań dotyczących gałęzi.</span><span class="sxs-lookup"><span data-stu-id="3a545-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="3a545-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a545-110">PARAMETERS</span></span>

### <span data-ttu-id="3a545-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="3a545-111">-ClusterName</span></span>
<span data-ttu-id="3a545-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="3a545-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3a545-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a545-113">-DefaultProfile</span></span>
<span data-ttu-id="3a545-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3a545-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a545-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="3a545-115">-HttpCredential</span></span>
<span data-ttu-id="3a545-116">Określa poświadczenia logowania klastra (HTTP) dla klastra.</span><span class="sxs-lookup"><span data-stu-id="3a545-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="3a545-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a545-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a545-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a545-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3a545-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a545-119">CommonParameters</span></span>
<span data-ttu-id="3a545-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a545-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a545-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a545-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a545-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a545-122">INPUTS</span></span>

### <span data-ttu-id="3a545-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3a545-123">None</span></span>

## <span data-ttu-id="3a545-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a545-124">OUTPUTS</span></span>

### <span data-ttu-id="3a545-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3a545-125">System.String</span></span>

## <span data-ttu-id="3a545-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a545-126">NOTES</span></span>

## <span data-ttu-id="3a545-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a545-127">RELATED LINKS</span></span>

[<span data-ttu-id="3a545-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3a545-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="3a545-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3a545-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


