---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
ms.openlocfilehash: 180cf2082b17e16fe5efcf1ee3009256b7c4703c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719030"
---
# <span data-ttu-id="2d000-101">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="2d000-101">Set-AzureRmHDInsightClusterSize</span></span>

## <span data-ttu-id="2d000-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d000-102">SYNOPSIS</span></span>
<span data-ttu-id="2d000-103">Ustawia liczbę węzłów procesu roboczego w określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="2d000-103">Sets the number of Worker nodes in a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d000-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d000-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d000-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2d000-105">DESCRIPTION</span></span>
<span data-ttu-id="2d000-106">Polecenie cmdlet **Set-AzureRmHDInsightClusterSize** określa liczbę węzłów procesu roboczego w określonym klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d000-106">The **Set-AzureRmHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2d000-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d000-107">EXAMPLES</span></span>

### <span data-ttu-id="2d000-108">Przykład 1: Ustawianie rozmiaru określonego klastra</span><span class="sxs-lookup"><span data-stu-id="2d000-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzureRmHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="2d000-109">To polecenie ustawia rozmiar klastra o nazwie Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="2d000-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2d000-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d000-110">PARAMETERS</span></span>

### <span data-ttu-id="2d000-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="2d000-111">-ClusterName</span></span>
<span data-ttu-id="2d000-112">Określa nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="2d000-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2d000-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d000-113">-ResourceGroupName</span></span>
<span data-ttu-id="2d000-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2d000-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2d000-115">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="2d000-115">-TargetInstanceCount</span></span>
<span data-ttu-id="2d000-116">Określa żądaną liczbę węzłów procesu roboczego w klastrze.</span><span class="sxs-lookup"><span data-stu-id="2d000-116">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="2d000-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d000-117">-DefaultProfile</span></span>
<span data-ttu-id="2d000-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d000-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d000-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d000-119">CommonParameters</span></span>
<span data-ttu-id="2d000-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d000-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d000-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d000-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d000-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d000-122">INPUTS</span></span>

## <span data-ttu-id="2d000-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d000-123">OUTPUTS</span></span>

### <span data-ttu-id="2d000-124">Microsoft. Azure. Management. HDInsight. modele. Cluster</span><span class="sxs-lookup"><span data-stu-id="2d000-124">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="2d000-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d000-125">NOTES</span></span>

## <span data-ttu-id="2d000-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d000-126">RELATED LINKS</span></span>

