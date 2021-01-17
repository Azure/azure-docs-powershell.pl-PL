---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 289f7b4bf397384b1420af02a5517e57bf51675d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489634"
---
# <span data-ttu-id="29d35-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="29d35-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="29d35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29d35-102">SYNOPSIS</span></span>
<span data-ttu-id="29d35-103">Pobiera i wyświetla listę wszystkich klastrów usługi Azure HDInsight skojarzonych z bieżącą subskrypcją lub określoną grupą zasobów albo pobiera określony klaster.</span><span class="sxs-lookup"><span data-stu-id="29d35-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="29d35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29d35-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29d35-105">Opis</span><span class="sxs-lookup"><span data-stu-id="29d35-105">DESCRIPTION</span></span>
<span data-ttu-id="29d35-106">Polecenie cmdlet **Get-AzHDInsightCluster** zawiera listę klastrów usługi Azure HDInsight dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="29d35-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="29d35-107">Użyj parametru *ClusterName* , aby uzyskać szczegółowe informacje dotyczące określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="29d35-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="29d35-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29d35-108">EXAMPLES</span></span>

### <span data-ttu-id="29d35-109">Przykład 1: Lista wszystkich klastrów usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="29d35-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="29d35-110">To polecenie wyświetla listę wszystkich klastrów usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="29d35-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="29d35-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29d35-111">PARAMETERS</span></span>

### <span data-ttu-id="29d35-112">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="29d35-112">-ClusterName</span></span>
<span data-ttu-id="29d35-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="29d35-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d35-114">-DefaultProfile</span></span>
<span data-ttu-id="29d35-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="29d35-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29d35-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d35-116">-ResourceGroupName</span></span>
<span data-ttu-id="29d35-117">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="29d35-117">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d35-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d35-118">CommonParameters</span></span>
<span data-ttu-id="29d35-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29d35-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d35-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29d35-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d35-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29d35-121">INPUTS</span></span>

### <span data-ttu-id="29d35-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="29d35-122">None</span></span>

## <span data-ttu-id="29d35-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29d35-123">OUTPUTS</span></span>

### <span data-ttu-id="29d35-124">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="29d35-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="29d35-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29d35-125">NOTES</span></span>

## <span data-ttu-id="29d35-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29d35-126">RELATED LINKS</span></span>

[<span data-ttu-id="29d35-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="29d35-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="29d35-128">Użyj — AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="29d35-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


