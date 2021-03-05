---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: 9f0ff8ea56110da2fcdc34a973fe8968aa7a701f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009089"
---
# <span data-ttu-id="b73c4-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="b73c4-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="b73c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b73c4-102">SYNOPSIS</span></span>
<span data-ttu-id="b73c4-103">Pobiera właściwości usługi HDInsight, takie jak dostępne lokalizacje i pojemność.</span><span class="sxs-lookup"><span data-stu-id="b73c4-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="b73c4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b73c4-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b73c4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b73c4-105">DESCRIPTION</span></span>
<span data-ttu-id="b73c4-106">Polecenie **cmdlet Get-AzHDInsightProperty** pobiera właściwości specyficzne dla usługi Azure HDInsight, takie jak lista dostępnych lokalizacji, wersje klastrów HDInsight oraz dostępna pojemność obliczeniowa.</span><span class="sxs-lookup"><span data-stu-id="b73c4-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="b73c4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b73c4-107">EXAMPLES</span></span>

### <span data-ttu-id="b73c4-108">Przykład 1. Uzyskiwanie właściwości klastrów HDInsight platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b73c4-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="b73c4-109">To polecenie pobiera właściwości z usługi HDInsight z lokalizacji East US 2.</span><span class="sxs-lookup"><span data-stu-id="b73c4-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="b73c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b73c4-110">PARAMETERS</span></span>

### <span data-ttu-id="b73c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b73c4-111">-DefaultProfile</span></span>
<span data-ttu-id="b73c4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b73c4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b73c4-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b73c4-113">-Location</span></span>
<span data-ttu-id="b73c4-114">Określa lokalizację, dla której mają być pobierane właściwości usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b73c4-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="b73c4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b73c4-115">CommonParameters</span></span>
<span data-ttu-id="b73c4-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b73c4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b73c4-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b73c4-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b73c4-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b73c4-118">INPUTS</span></span>

### <span data-ttu-id="b73c4-119">Brak</span><span class="sxs-lookup"><span data-stu-id="b73c4-119">None</span></span>
## <span data-ttu-id="b73c4-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b73c4-120">OUTPUTS</span></span>

### <span data-ttu-id="b73c4-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="b73c4-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="b73c4-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b73c4-122">NOTES</span></span>

## <span data-ttu-id="b73c4-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b73c4-123">RELATED LINKS</span></span>
