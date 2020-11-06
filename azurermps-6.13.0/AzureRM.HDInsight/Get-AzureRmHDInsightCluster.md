---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: f232d1df7bef3800fc54b2469a51f3f69c8d4fa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545303"
---
# <span data-ttu-id="e2880-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e2880-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="e2880-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2880-102">SYNOPSIS</span></span>
<span data-ttu-id="e2880-103">Pobiera i wyświetla listę wszystkich klastrów usługi Azure HDInsight skojarzonych z bieżącą subskrypcją lub określoną grupą zasobów albo pobiera określony klaster.</span><span class="sxs-lookup"><span data-stu-id="e2880-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2880-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2880-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2880-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e2880-105">DESCRIPTION</span></span>
<span data-ttu-id="e2880-106">Polecenie cmdlet **Get-AzureRmHDInsightCluster** zawiera listę klastrów usługi Azure HDInsight dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e2880-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="e2880-107">Użyj parametru *ClusterName* , aby uzyskać szczegółowe informacje dotyczące określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="e2880-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="e2880-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2880-108">EXAMPLES</span></span>

### <span data-ttu-id="e2880-109">Przykład 1: Lista wszystkich klastrów usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="e2880-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="e2880-110">To polecenie wyświetla listę wszystkich klastrów usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e2880-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="e2880-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2880-111">PARAMETERS</span></span>

### <span data-ttu-id="e2880-112">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="e2880-112">-ClusterName</span></span>
<span data-ttu-id="e2880-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="e2880-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e2880-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2880-114">-DefaultProfile</span></span>
<span data-ttu-id="e2880-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e2880-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2880-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2880-116">-ResourceGroupName</span></span>
<span data-ttu-id="e2880-117">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2880-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e2880-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2880-118">CommonParameters</span></span>
<span data-ttu-id="e2880-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2880-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2880-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2880-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2880-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2880-121">INPUTS</span></span>

### <span data-ttu-id="e2880-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e2880-122">None</span></span>

## <span data-ttu-id="e2880-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2880-123">OUTPUTS</span></span>

### <span data-ttu-id="e2880-124">Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e2880-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="e2880-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2880-125">NOTES</span></span>

## <span data-ttu-id="e2880-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2880-126">RELATED LINKS</span></span>

[<span data-ttu-id="e2880-127">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e2880-127">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="e2880-128">Użyj — AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e2880-128">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


