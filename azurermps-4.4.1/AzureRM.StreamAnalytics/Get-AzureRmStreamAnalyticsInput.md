---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: e9f4017156a72b1284de8b62d1ae2ebf7d8321ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544632"
---
# <span data-ttu-id="3fb54-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3fb54-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="3fb54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3fb54-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb54-103">Pobiera dane wejściowe zadania analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="3fb54-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fb54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3fb54-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fb54-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3fb54-105">DESCRIPTION</span></span>
<span data-ttu-id="3fb54-106">Polecenie cmdlet **Get-AzureRmStreamAnalyticsInput** wyświetla listę wszystkich składników wejściowych zdefiniowanych w zadaniu Stream Analytics lub pobiera informacje o określonych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3fb54-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="3fb54-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3fb54-107">EXAMPLES</span></span>

### <span data-ttu-id="3fb54-108">PRZYKŁAD 1: uzyskiwanie informacji o danych wejściowych zdefiniowanych w zadaniu</span><span class="sxs-lookup"><span data-stu-id="3fb54-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="3fb54-109">To polecenie zwraca informacje o wszystkich danych wejściowych zdefiniowanych w StreamingJobie zadania.</span><span class="sxs-lookup"><span data-stu-id="3fb54-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="3fb54-110">PRZYKŁAD 2: uzyskiwanie informacji na temat określonych danych wejściowych zdefiniowanych w zadaniu</span><span class="sxs-lookup"><span data-stu-id="3fb54-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="3fb54-111">To polecenie zwraca informacje o wejściu o nazwie EntryStream zdefiniowane w StreamingJobie zadania.</span><span class="sxs-lookup"><span data-stu-id="3fb54-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="3fb54-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3fb54-112">PARAMETERS</span></span>

### <span data-ttu-id="3fb54-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="3fb54-113">-JobName</span></span>
<span data-ttu-id="3fb54-114">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="3fb54-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fb54-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3fb54-115">-Name</span></span>
<span data-ttu-id="3fb54-116">Określa nazwę danych wejściowych funkcji Analiza strumienia Azure do pobrania.</span><span class="sxs-lookup"><span data-stu-id="3fb54-116">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fb54-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fb54-117">-ResourceGroupName</span></span>
<span data-ttu-id="3fb54-118">Określa nazwę grupy zasobów, do której należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="3fb54-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fb54-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fb54-119">-DefaultProfile</span></span>
<span data-ttu-id="3fb54-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3fb54-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fb54-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb54-121">CommonParameters</span></span>
<span data-ttu-id="3fb54-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fb54-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb54-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fb54-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb54-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fb54-124">INPUTS</span></span>

## <span data-ttu-id="3fb54-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3fb54-125">OUTPUTS</span></span>

### <span data-ttu-id="3fb54-126">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. StreamAnalytics. MODELES. PSInput, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. modele. PSInput</span><span class="sxs-lookup"><span data-stu-id="3fb54-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="3fb54-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3fb54-127">NOTES</span></span>

## <span data-ttu-id="3fb54-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fb54-128">RELATED LINKS</span></span>

[<span data-ttu-id="3fb54-129">Nowe — AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3fb54-129">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="3fb54-130">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3fb54-130">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="3fb54-131">Test — AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3fb54-131">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


