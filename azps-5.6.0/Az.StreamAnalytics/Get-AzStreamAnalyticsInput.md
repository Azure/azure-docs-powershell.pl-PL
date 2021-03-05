---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: 726d9d9294c4cf6e5789399ec821d4657e6f787e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973873"
---
# <span data-ttu-id="bcbc5-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="bcbc5-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="bcbc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcbc5-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbc5-103">Pobiera informacje o zadaniach analizy strumieniowej.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="bcbc5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bcbc5-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcbc5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bcbc5-105">DESCRIPTION</span></span>
<span data-ttu-id="bcbc5-106">Polecenie **cmdlet Get-AzStreamAnalyticsInput** wyświetla listę wszystkich danych wejściowych zdefiniowanych w zadaniu analizy strumienia lub pobierających informacje o określonych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="bcbc5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bcbc5-107">EXAMPLES</span></span>

### <span data-ttu-id="bcbc5-108">Przykład 1. Uzyskiwanie informacji o danych wejściowych zdefiniowanych w zadaniu</span><span class="sxs-lookup"><span data-stu-id="bcbc5-108">Example 1: Get information about the inputs defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="bcbc5-109">To polecenie zwraca informacje o wszystkich danych wejściowych zdefiniowanych w zadaniu StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="bcbc5-110">Przykład 2. Uzyskiwanie informacji o konkretnym wejściu zdefiniowanym w zadaniu</span><span class="sxs-lookup"><span data-stu-id="bcbc5-110">Example 2: Get information about a specific input defined on a job</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="bcbc5-111">To polecenie zwraca informacje o danych wejściowych o nazwie EntryStream zdefiniowanych w zadaniu StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="bcbc5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcbc5-112">PARAMETERS</span></span>

### <span data-ttu-id="bcbc5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbc5-113">-DefaultProfile</span></span>
<span data-ttu-id="bcbc5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcbc5-115">— JobName</span><span class="sxs-lookup"><span data-stu-id="bcbc5-115">-JobName</span></span>
<span data-ttu-id="bcbc5-116">Określa nazwę zadania Azure Stream Analytics, do którego należy dane wejściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="bcbc5-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bcbc5-117">-Name</span></span>
<span data-ttu-id="bcbc5-118">Określa nazwę danych wejściowych usługi Azure Stream Analytics do pobrania.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="bcbc5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcbc5-119">-ResourceGroupName</span></span>
<span data-ttu-id="bcbc5-120">Określa nazwę grupy zasobów, do której należy dane wejściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="bcbc5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbc5-121">CommonParameters</span></span>
<span data-ttu-id="bcbc5-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcbc5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbc5-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcbc5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbc5-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcbc5-124">INPUTS</span></span>

### <span data-ttu-id="bcbc5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="bcbc5-125">System.String</span></span>

## <span data-ttu-id="bcbc5-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bcbc5-126">OUTPUTS</span></span>

### <span data-ttu-id="bcbc5-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="bcbc5-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="bcbc5-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bcbc5-128">NOTES</span></span>

## <span data-ttu-id="bcbc5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bcbc5-129">RELATED LINKS</span></span>

[<span data-ttu-id="bcbc5-130">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="bcbc5-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="bcbc5-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="bcbc5-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="bcbc5-132">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="bcbc5-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


