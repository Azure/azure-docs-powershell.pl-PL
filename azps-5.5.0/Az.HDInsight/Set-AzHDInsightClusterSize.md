---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 7dae5bd29877097b7d0df60feff8bf44977e61f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241386"
---
# <span data-ttu-id="0cf06-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="0cf06-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="0cf06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cf06-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf06-103">Ustawia liczbę węzłów pracownicy w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="0cf06-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="0cf06-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0cf06-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cf06-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0cf06-105">DESCRIPTION</span></span>
<span data-ttu-id="0cf06-106">Polecenie **cmdlet Set-AzHDInsightClusterSize** ustawia liczbę węzłów Worker w określonym klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0cf06-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="0cf06-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0cf06-107">EXAMPLES</span></span>

### <span data-ttu-id="0cf06-108">Przykład 1. Ustawianie rozmiaru określonego klastra</span><span class="sxs-lookup"><span data-stu-id="0cf06-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="0cf06-109">To polecenie ustawia rozmiar klastra o nazwie Twoja-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="0cf06-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0cf06-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cf06-110">PARAMETERS</span></span>

### <span data-ttu-id="0cf06-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0cf06-111">-ClusterName</span></span>
<span data-ttu-id="0cf06-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="0cf06-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0cf06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf06-113">-DefaultProfile</span></span>
<span data-ttu-id="0cf06-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0cf06-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cf06-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cf06-115">-ResourceGroupName</span></span>
<span data-ttu-id="0cf06-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0cf06-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0cf06-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="0cf06-117">-TargetInstanceCount</span></span>
<span data-ttu-id="0cf06-118">Określa żądaną liczbę węzłów Pracownik w klastrze.</span><span class="sxs-lookup"><span data-stu-id="0cf06-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="0cf06-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf06-119">CommonParameters</span></span>
<span data-ttu-id="0cf06-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf06-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf06-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cf06-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf06-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cf06-122">INPUTS</span></span>

### <span data-ttu-id="0cf06-123">Brak</span><span class="sxs-lookup"><span data-stu-id="0cf06-123">None</span></span>

## <span data-ttu-id="0cf06-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cf06-124">OUTPUTS</span></span>

### <span data-ttu-id="0cf06-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="0cf06-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="0cf06-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0cf06-126">NOTES</span></span>

## <span data-ttu-id="0cf06-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0cf06-127">RELATED LINKS</span></span>
