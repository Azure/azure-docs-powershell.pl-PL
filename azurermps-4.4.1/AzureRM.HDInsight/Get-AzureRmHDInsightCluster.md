---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: 81f25eeb8d0e6b704c4ee6ef71cd2aebcf3624ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549187"
---
# <span data-ttu-id="21587-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="21587-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="21587-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21587-102">SYNOPSIS</span></span>
<span data-ttu-id="21587-103">Pobiera i wyświetla listę wszystkich klastrów usługi Azure HDInsight skojarzonych z bieżącą subskrypcją lub określoną grupą zasobów albo pobiera określony klaster.</span><span class="sxs-lookup"><span data-stu-id="21587-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21587-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21587-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21587-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21587-105">DESCRIPTION</span></span>
<span data-ttu-id="21587-106">Polecenie cmdlet **Get-AzureRmHDInsightCluster** zawiera listę klastrów usługi Azure HDInsight dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="21587-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="21587-107">Użyj parametru *ClusterName* , aby uzyskać szczegółowe informacje dotyczące określonego klastra.</span><span class="sxs-lookup"><span data-stu-id="21587-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="21587-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21587-108">EXAMPLES</span></span>

### <span data-ttu-id="21587-109">Przykład 1: Lista wszystkich klastrów usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="21587-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="21587-110">To polecenie wyświetla listę wszystkich klastrów usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="21587-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="21587-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21587-111">PARAMETERS</span></span>

### <span data-ttu-id="21587-112">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="21587-112">-ClusterName</span></span>
<span data-ttu-id="21587-113">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="21587-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="21587-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21587-114">-ResourceGroupName</span></span>
<span data-ttu-id="21587-115">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21587-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="21587-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21587-116">-DefaultProfile</span></span>
<span data-ttu-id="21587-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21587-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21587-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21587-118">CommonParameters</span></span>
<span data-ttu-id="21587-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21587-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21587-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21587-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21587-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21587-121">INPUTS</span></span>

## <span data-ttu-id="21587-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21587-122">OUTPUTS</span></span>

### <span data-ttu-id="21587-123">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. HDInsight. modele. AzureHDInsightCluster]</span><span class="sxs-lookup"><span data-stu-id="21587-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster]</span></span>

## <span data-ttu-id="21587-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21587-124">NOTES</span></span>

## <span data-ttu-id="21587-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21587-125">RELATED LINKS</span></span>

[<span data-ttu-id="21587-126">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="21587-126">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="21587-127">Użyj — AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="21587-127">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


