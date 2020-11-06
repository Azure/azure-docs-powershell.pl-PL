---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 724441a09ec2714048ec43b781f5792903bce73a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526509"
---
# <span data-ttu-id="fbabd-101">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="fbabd-101">Get-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="fbabd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbabd-102">SYNOPSIS</span></span>
<span data-ttu-id="fbabd-103">Pobiera dane wejściowe zadania analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="fbabd-103">Gets Stream Analytics job inputs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbabd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbabd-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbabd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fbabd-105">DESCRIPTION</span></span>
<span data-ttu-id="fbabd-106">Polecenie cmdlet **Get-AzureRmStreamAnalyticsInput** wyświetla listę wszystkich składników wejściowych zdefiniowanych w zadaniu Stream Analytics lub pobiera informacje o określonych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="fbabd-106">The **Get-AzureRmStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="fbabd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbabd-107">EXAMPLES</span></span>

### <span data-ttu-id="fbabd-108">PRZYKŁAD 1: uzyskiwanie informacji o danych wejściowych zdefiniowanych w zadaniu</span><span class="sxs-lookup"><span data-stu-id="fbabd-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="fbabd-109">To polecenie zwraca informacje o wszystkich danych wejściowych zdefiniowanych w StreamingJobie zadania.</span><span class="sxs-lookup"><span data-stu-id="fbabd-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="fbabd-110">PRZYKŁAD 2: uzyskiwanie informacji na temat określonych danych wejściowych zdefiniowanych w zadaniu</span><span class="sxs-lookup"><span data-stu-id="fbabd-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="fbabd-111">To polecenie zwraca informacje o wejściu o nazwie EntryStream zdefiniowane w StreamingJobie zadania.</span><span class="sxs-lookup"><span data-stu-id="fbabd-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="fbabd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbabd-112">PARAMETERS</span></span>

### <span data-ttu-id="fbabd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbabd-113">-DefaultProfile</span></span>
<span data-ttu-id="fbabd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbabd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbabd-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="fbabd-115">-JobName</span></span>
<span data-ttu-id="fbabd-116">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="fbabd-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbabd-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fbabd-117">-Name</span></span>
<span data-ttu-id="fbabd-118">Określa nazwę danych wejściowych funkcji Analiza strumienia Azure do pobrania.</span><span class="sxs-lookup"><span data-stu-id="fbabd-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbabd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbabd-119">-ResourceGroupName</span></span>
<span data-ttu-id="fbabd-120">Określa nazwę grupy zasobów, do której należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="fbabd-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbabd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbabd-121">CommonParameters</span></span>
<span data-ttu-id="fbabd-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbabd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbabd-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbabd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbabd-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbabd-124">INPUTS</span></span>

### <span data-ttu-id="fbabd-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fbabd-125">None</span></span>
<span data-ttu-id="fbabd-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="fbabd-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fbabd-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbabd-127">OUTPUTS</span></span>

### <span data-ttu-id="fbabd-128">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. StreamAnalytics. MODELES. PSInput, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. modele. PSInput</span><span class="sxs-lookup"><span data-stu-id="fbabd-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="fbabd-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbabd-129">NOTES</span></span>

## <span data-ttu-id="fbabd-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbabd-130">RELATED LINKS</span></span>

[<span data-ttu-id="fbabd-131">Nowe — AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="fbabd-131">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="fbabd-132">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="fbabd-132">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="fbabd-133">Test — AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="fbabd-133">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


