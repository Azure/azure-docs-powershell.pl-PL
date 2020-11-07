---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsInput.md
ms.openlocfilehash: cd6e7e4bf9ba9a99b9b3a9a5f58acb9578236037
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707430"
---
# <span data-ttu-id="64f5e-101">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="64f5e-101">Get-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="64f5e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="64f5e-103">Pobiera dane wejściowe zadania analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="64f5e-103">Gets Stream Analytics job inputs.</span></span>

## <span data-ttu-id="64f5e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64f5e-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64f5e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="64f5e-105">DESCRIPTION</span></span>
<span data-ttu-id="64f5e-106">Polecenie cmdlet **Get-AzStreamAnalyticsInput** wyświetla listę wszystkich składników wejściowych zdefiniowanych w zadaniu Stream Analytics lub pobiera informacje o określonych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="64f5e-106">The **Get-AzStreamAnalyticsInput** cmdlet lists all of the inputs that are defined in a Stream Analytics job or gets information about a specific input.</span></span>

## <span data-ttu-id="64f5e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64f5e-107">EXAMPLES</span></span>

### <span data-ttu-id="64f5e-108">PRZYKŁAD 1: uzyskiwanie informacji o danych wejściowych zdefiniowanych w zadaniu</span><span class="sxs-lookup"><span data-stu-id="64f5e-108">EXAMPLE 1: Get information about the inputs defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="64f5e-109">To polecenie zwraca informacje o wszystkich danych wejściowych zdefiniowanych w StreamingJobie zadania.</span><span class="sxs-lookup"><span data-stu-id="64f5e-109">This command returns information about all the inputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="64f5e-110">PRZYKŁAD 2: uzyskiwanie informacji na temat określonych danych wejściowych zdefiniowanych w zadaniu</span><span class="sxs-lookup"><span data-stu-id="64f5e-110">EXAMPLE 2: Get information about a specific input defined on a job</span></span>
```
PS C:\>Get-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="64f5e-111">To polecenie zwraca informacje o wejściu o nazwie EntryStream zdefiniowane w StreamingJobie zadania.</span><span class="sxs-lookup"><span data-stu-id="64f5e-111">This command returns information about the input named EntryStream defined on the job StreamingJob.</span></span>

## <span data-ttu-id="64f5e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64f5e-112">PARAMETERS</span></span>

### <span data-ttu-id="64f5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f5e-113">-DefaultProfile</span></span>
<span data-ttu-id="64f5e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64f5e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64f5e-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="64f5e-115">-JobName</span></span>
<span data-ttu-id="64f5e-116">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="64f5e-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="64f5e-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="64f5e-117">-Name</span></span>
<span data-ttu-id="64f5e-118">Określa nazwę danych wejściowych funkcji Analiza strumienia Azure do pobrania.</span><span class="sxs-lookup"><span data-stu-id="64f5e-118">Specifies the name of the Azure Stream Analytics input to retrieve.</span></span>

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

### <span data-ttu-id="64f5e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64f5e-119">-ResourceGroupName</span></span>
<span data-ttu-id="64f5e-120">Określa nazwę grupy zasobów, do której należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="64f5e-120">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="64f5e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f5e-121">CommonParameters</span></span>
<span data-ttu-id="64f5e-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64f5e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f5e-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64f5e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f5e-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64f5e-124">INPUTS</span></span>

### <span data-ttu-id="64f5e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="64f5e-125">System.String</span></span>

## <span data-ttu-id="64f5e-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64f5e-126">OUTPUTS</span></span>

### <span data-ttu-id="64f5e-127">Microsoft. Azure. Commands. StreamAnalytics. models. PSInput</span><span class="sxs-lookup"><span data-stu-id="64f5e-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="64f5e-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64f5e-128">NOTES</span></span>

## <span data-ttu-id="64f5e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64f5e-129">RELATED LINKS</span></span>

[<span data-ttu-id="64f5e-130">Nowe — AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="64f5e-130">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="64f5e-131">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="64f5e-131">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="64f5e-132">Test — AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="64f5e-132">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)

