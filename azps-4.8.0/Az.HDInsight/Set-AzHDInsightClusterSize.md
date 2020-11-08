---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 8f34e9233da61bb2381c99c33922fa4332b588fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062722"
---
# <span data-ttu-id="f5a86-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="f5a86-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="f5a86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5a86-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a86-103">Ustawia liczbę węzłów procesu roboczego w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="f5a86-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="f5a86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5a86-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5a86-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f5a86-105">DESCRIPTION</span></span>
<span data-ttu-id="f5a86-106">Polecenie cmdlet **Set-AzHDInsightClusterSize** określa liczbę węzłów procesu roboczego w określonym klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f5a86-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f5a86-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5a86-107">EXAMPLES</span></span>

### <span data-ttu-id="f5a86-108">Przykład 1: Ustawianie rozmiaru określonego klastra</span><span class="sxs-lookup"><span data-stu-id="f5a86-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="f5a86-109">To polecenie ustawia rozmiar klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="f5a86-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f5a86-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5a86-110">PARAMETERS</span></span>

### <span data-ttu-id="f5a86-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="f5a86-111">-ClusterName</span></span>
<span data-ttu-id="f5a86-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="f5a86-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f5a86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a86-113">-DefaultProfile</span></span>
<span data-ttu-id="f5a86-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f5a86-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5a86-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5a86-115">-ResourceGroupName</span></span>
<span data-ttu-id="f5a86-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f5a86-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f5a86-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="f5a86-117">-TargetInstanceCount</span></span>
<span data-ttu-id="f5a86-118">Określa żądaną liczbę węzłów procesu roboczego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="f5a86-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="f5a86-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a86-119">CommonParameters</span></span>
<span data-ttu-id="f5a86-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5a86-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a86-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5a86-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a86-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5a86-122">INPUTS</span></span>

### <span data-ttu-id="f5a86-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f5a86-123">None</span></span>

## <span data-ttu-id="f5a86-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5a86-124">OUTPUTS</span></span>

### <span data-ttu-id="f5a86-125">Microsoft. Azure. Management. HDInsight. modele. Cluster</span><span class="sxs-lookup"><span data-stu-id="f5a86-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="f5a86-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5a86-126">NOTES</span></span>

## <span data-ttu-id="f5a86-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5a86-127">RELATED LINKS</span></span>
