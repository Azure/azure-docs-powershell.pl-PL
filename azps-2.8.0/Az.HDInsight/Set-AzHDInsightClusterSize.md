---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 1616714879a260dea3611809b5f7028b4a203d34
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705294"
---
# <span data-ttu-id="aa57d-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="aa57d-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="aa57d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa57d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa57d-103">Ustawia liczbę węzłów procesu roboczego w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="aa57d-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="aa57d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa57d-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa57d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aa57d-105">DESCRIPTION</span></span>
<span data-ttu-id="aa57d-106">Polecenie cmdlet **Set-AzHDInsightClusterSize** określa liczbę węzłów procesu roboczego w określonym klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="aa57d-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="aa57d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa57d-107">EXAMPLES</span></span>

### <span data-ttu-id="aa57d-108">Przykład 1: Ustawianie rozmiaru określonego klastra</span><span class="sxs-lookup"><span data-stu-id="aa57d-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="aa57d-109">To polecenie ustawia rozmiar klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="aa57d-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="aa57d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa57d-110">PARAMETERS</span></span>

### <span data-ttu-id="aa57d-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="aa57d-111">-ClusterName</span></span>
<span data-ttu-id="aa57d-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="aa57d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="aa57d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa57d-113">-DefaultProfile</span></span>
<span data-ttu-id="aa57d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="aa57d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa57d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa57d-115">-ResourceGroupName</span></span>
<span data-ttu-id="aa57d-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa57d-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="aa57d-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="aa57d-117">-TargetInstanceCount</span></span>
<span data-ttu-id="aa57d-118">Określa żądaną liczbę węzłów procesu roboczego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="aa57d-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa57d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa57d-119">CommonParameters</span></span>
<span data-ttu-id="aa57d-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa57d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa57d-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa57d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa57d-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa57d-122">INPUTS</span></span>

### <span data-ttu-id="aa57d-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="aa57d-123">None</span></span>

## <span data-ttu-id="aa57d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa57d-124">OUTPUTS</span></span>

### <span data-ttu-id="aa57d-125">Microsoft. Azure. Management. HDInsight. modele. Cluster</span><span class="sxs-lookup"><span data-stu-id="aa57d-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="aa57d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa57d-126">NOTES</span></span>

## <span data-ttu-id="aa57d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa57d-127">RELATED LINKS</span></span>
