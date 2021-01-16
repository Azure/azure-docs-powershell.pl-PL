---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: e13b90da8e1901faf0b18eb6ebf3cc78ce1bbcda
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338230"
---
# <span data-ttu-id="1c033-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="1c033-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="1c033-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c033-102">SYNOPSIS</span></span>
<span data-ttu-id="1c033-103">Pobiera właściwości usługi HDInsight, takie jak dostępne lokalizacje i pojemność.</span><span class="sxs-lookup"><span data-stu-id="1c033-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="1c033-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c033-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c033-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1c033-105">DESCRIPTION</span></span>
<span data-ttu-id="1c033-106">Polecenie cmdlet **Get-AzHDInsightProperty** pobiera właściwości specyficzne dla usługi Azure HDInsight, takie jak lista dostępnych lokalizacji, wersje klastra usługi HDInsight i dostępne zdolności obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="1c033-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="1c033-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c033-107">EXAMPLES</span></span>

### <span data-ttu-id="1c033-108">Przykład 1: uzyskiwanie właściwości klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="1c033-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="1c033-109">To polecenie pobiera właściwości z usługi HDInsight z lokalizacji wschód US 2.</span><span class="sxs-lookup"><span data-stu-id="1c033-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="1c033-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c033-110">PARAMETERS</span></span>

### <span data-ttu-id="1c033-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c033-111">-DefaultProfile</span></span>
<span data-ttu-id="1c033-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1c033-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c033-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1c033-113">-Location</span></span>
<span data-ttu-id="1c033-114">Określa lokalizację, w której mają zostać pobrane właściwości usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1c033-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="1c033-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c033-115">CommonParameters</span></span>
<span data-ttu-id="1c033-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c033-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c033-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c033-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c033-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c033-118">INPUTS</span></span>

### <span data-ttu-id="1c033-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1c033-119">None</span></span>
## <span data-ttu-id="1c033-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c033-120">OUTPUTS</span></span>

### <span data-ttu-id="1c033-121">Microsoft. Azure. Management. HDInsight. MODELES. AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="1c033-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="1c033-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c033-122">NOTES</span></span>

## <span data-ttu-id="1c033-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c033-123">RELATED LINKS</span></span>
