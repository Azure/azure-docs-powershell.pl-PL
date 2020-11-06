---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 7b1130d222e36d53fbef1dcbb60f6d74615c5b11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545943"
---
# <span data-ttu-id="eaf6a-101">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="eaf6a-101">Get-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="eaf6a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eaf6a-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf6a-103">Pobiera informacje o zadaniach analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="eaf6a-103">Gets Stream Analytics jobs information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaf6a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eaf6a-104">SYNTAX</span></span>

### <span data-ttu-id="eaf6a-105">W przypadku obiektów Stream Analytics w danej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="eaf6a-105">For stream analytics objects in the given resource group</span></span>
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaf6a-106">W przypadku obiektów analizy strumienia w danym abonamentzie</span><span class="sxs-lookup"><span data-stu-id="eaf6a-106">For stream analytics objects in the given subscription</span></span>
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaf6a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="eaf6a-107">DESCRIPTION</span></span>
<span data-ttu-id="eaf6a-108">Polecenie cmdlet **Get-AzureRmStreamAnalyticsJob** wyświetla wszystkie zadania analizy strumienia zdefiniowane w subskrypcji platformy Azure lub określonej grupie zasobów albo pobiera informacje o zadaniach dotyczących określonego zadania w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="eaf6a-108">The **Get-AzureRmStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="eaf6a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eaf6a-109">EXAMPLES</span></span>

### <span data-ttu-id="eaf6a-110">PRZYKŁAD 1: uzyskiwanie informacji o wszystkich zadaniach w ramach abonamentu</span><span class="sxs-lookup"><span data-stu-id="eaf6a-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

<span data-ttu-id="eaf6a-111">To polecenie zwraca informacje na temat wszystkich zadań analizy strumienia w ramach subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf6a-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="eaf6a-112">PRZYKŁAD 2: uzyskiwanie informacji o wszystkich zadaniach w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="eaf6a-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="eaf6a-113">To polecenie zwraca informacje na temat wszystkich zadań analizy strumienia w grupie zasób StreamAnalytics-default-zachód-my.</span><span class="sxs-lookup"><span data-stu-id="eaf6a-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="eaf6a-114">PRZYKŁAD 3: uzyskiwanie informacji o konkretnym zadaniu w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="eaf6a-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="eaf6a-115">To polecenie zwraca informacje o zadaniu Stream Analytics StreamingJob w grupie zasób StreamAnalytics-default-zachód-USA.</span><span class="sxs-lookup"><span data-stu-id="eaf6a-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="eaf6a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eaf6a-116">PARAMETERS</span></span>

### <span data-ttu-id="eaf6a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eaf6a-117">-Name</span></span>
<span data-ttu-id="eaf6a-118">Określa nazwę zadania usługi Azure Stream Analytics, które ma zostać pobrane.</span><span class="sxs-lookup"><span data-stu-id="eaf6a-118">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf6a-119">-NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="eaf6a-119">-NoExpand</span></span>
<span data-ttu-id="eaf6a-120">Wskazuje, że polecenie cmdlet będzie pobierać zadanie usługi Azure Stream Analytics, ale nie zwraca informacji na temat danych wejściowych, wyjść i transformacji.</span><span class="sxs-lookup"><span data-stu-id="eaf6a-120">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf6a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaf6a-121">-ResourceGroupName</span></span>
<span data-ttu-id="eaf6a-122">Określa nazwę grupy zasobów, do której należy zadanie usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="eaf6a-122">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf6a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf6a-123">-DefaultProfile</span></span>
<span data-ttu-id="eaf6a-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eaf6a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaf6a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf6a-125">CommonParameters</span></span>
<span data-ttu-id="eaf6a-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaf6a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf6a-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaf6a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf6a-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eaf6a-128">INPUTS</span></span>

## <span data-ttu-id="eaf6a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eaf6a-129">OUTPUTS</span></span>

### <span data-ttu-id="eaf6a-130">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. StreamAnalytics. MODELES. PSJob, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. modele. PSJob</span><span class="sxs-lookup"><span data-stu-id="eaf6a-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="eaf6a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eaf6a-131">NOTES</span></span>

## <span data-ttu-id="eaf6a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eaf6a-132">RELATED LINKS</span></span>

[<span data-ttu-id="eaf6a-133">Nowe — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="eaf6a-133">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="eaf6a-134">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="eaf6a-134">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="eaf6a-135">Start — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="eaf6a-135">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="eaf6a-136">Zatrzymaj — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="eaf6a-136">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


