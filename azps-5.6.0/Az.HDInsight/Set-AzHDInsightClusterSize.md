---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: eba552917b17b9bb1337a2b62c83d3d1adebc1cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001521"
---
# <span data-ttu-id="74b82-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="74b82-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="74b82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74b82-102">SYNOPSIS</span></span>
<span data-ttu-id="74b82-103">Ustawia liczbę węzłów pracownik w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="74b82-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="74b82-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74b82-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74b82-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="74b82-105">DESCRIPTION</span></span>
<span data-ttu-id="74b82-106">Polecenie **cmdlet Set-AzHDInsightClusterSize** ustawia liczbę węzłów Worker w określonym klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="74b82-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="74b82-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74b82-107">EXAMPLES</span></span>

### <span data-ttu-id="74b82-108">Przykład 1. Ustawianie rozmiaru określonego klastra</span><span class="sxs-lookup"><span data-stu-id="74b82-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="74b82-109">To polecenie ustawia rozmiar klastra o nazwie Twoja-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="74b82-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="74b82-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74b82-110">PARAMETERS</span></span>

### <span data-ttu-id="74b82-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="74b82-111">-ClusterName</span></span>
<span data-ttu-id="74b82-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="74b82-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="74b82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b82-113">-DefaultProfile</span></span>
<span data-ttu-id="74b82-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="74b82-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74b82-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b82-115">-ResourceGroupName</span></span>
<span data-ttu-id="74b82-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74b82-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="74b82-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="74b82-117">-TargetInstanceCount</span></span>
<span data-ttu-id="74b82-118">Określa żądaną liczbę węzłów Pracownik w klastrze.</span><span class="sxs-lookup"><span data-stu-id="74b82-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="74b82-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b82-119">CommonParameters</span></span>
<span data-ttu-id="74b82-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74b82-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b82-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74b82-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b82-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74b82-122">INPUTS</span></span>

### <span data-ttu-id="74b82-123">Brak</span><span class="sxs-lookup"><span data-stu-id="74b82-123">None</span></span>

## <span data-ttu-id="74b82-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74b82-124">OUTPUTS</span></span>

### <span data-ttu-id="74b82-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="74b82-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="74b82-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74b82-126">NOTES</span></span>

## <span data-ttu-id="74b82-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74b82-127">RELATED LINKS</span></span>
