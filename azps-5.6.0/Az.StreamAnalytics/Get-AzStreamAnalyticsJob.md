---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsJob.md
ms.openlocfilehash: 26808bd3db72f8618505045b2b20f6d0b56806da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973866"
---
# <span data-ttu-id="53a6c-101">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="53a6c-101">Get-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="53a6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="53a6c-103">Otrzymuje informacje o zadaniach usługi Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="53a6c-103">Gets Stream Analytics jobs information.</span></span>

## <span data-ttu-id="53a6c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="53a6c-104">SYNTAX</span></span>

### <span data-ttu-id="53a6c-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53a6c-105">ByResourceGroup</span></span>
```
Get-AzStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53a6c-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="53a6c-106">BySubscription</span></span>
```
Get-AzStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53a6c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="53a6c-107">DESCRIPTION</span></span>
<span data-ttu-id="53a6c-108">Polecenie **cmdlet Get-AzStreamAnalyticsJob** wyświetla listę wszystkich zadań usługi Stream Analytics zdefiniowanych w subskrypcji platformy Azure lub określonej grupie zasobów albo otrzymuje informacje o zadaniu określonym w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="53a6c-108">The **Get-AzStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="53a6c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="53a6c-109">EXAMPLES</span></span>

### <span data-ttu-id="53a6c-110">PRZYKŁAD 1. Uzyskiwanie informacji o wszystkich zadaniach w subskrypcji</span><span class="sxs-lookup"><span data-stu-id="53a6c-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob
```

<span data-ttu-id="53a6c-111">To polecenie zwraca informacje o wszystkich zadaniach usługi Stream Analytics w subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="53a6c-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="53a6c-112">PRZYKŁAD 2. Uzyskiwanie informacji o wszystkich zadaniach w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="53a6c-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="53a6c-113">To polecenie zwraca informacje o wszystkich zadaniach usługi Stream Analytics w grupie zasobów StreamAnalytics-Default-West-US.</span><span class="sxs-lookup"><span data-stu-id="53a6c-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="53a6c-114">PRZYKŁAD 3. Uzyskiwanie informacji o określonym zadaniu w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="53a6c-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="53a6c-115">To polecenie zwraca informacje o zadaniu Stream Analytics StreamingJob w grupie zasobów StreamAnalytics-Default-West-US.</span><span class="sxs-lookup"><span data-stu-id="53a6c-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="53a6c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53a6c-116">PARAMETERS</span></span>

### <span data-ttu-id="53a6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a6c-117">-DefaultProfile</span></span>
<span data-ttu-id="53a6c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="53a6c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53a6c-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="53a6c-119">-Name</span></span>
<span data-ttu-id="53a6c-120">Określa nazwę zadania Azure Stream Analytics do pobrania.</span><span class="sxs-lookup"><span data-stu-id="53a6c-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53a6c-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="53a6c-121">-NoExpand</span></span>
<span data-ttu-id="53a6c-122">Wskazuje, że polecenie cmdlet pobierze zadanie Azure Stream Analytics, ale nie zwróci informacji o jego danych wejściowych, wynikach i przekształceniach.</span><span class="sxs-lookup"><span data-stu-id="53a6c-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

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

### <span data-ttu-id="53a6c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a6c-123">-ResourceGroupName</span></span>
<span data-ttu-id="53a6c-124">Określa nazwę grupy zasobów, do której należy zadanie Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="53a6c-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53a6c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a6c-125">CommonParameters</span></span>
<span data-ttu-id="53a6c-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53a6c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a6c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53a6c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a6c-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53a6c-128">INPUTS</span></span>

### <span data-ttu-id="53a6c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="53a6c-129">System.String</span></span>

### <span data-ttu-id="53a6c-130">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="53a6c-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="53a6c-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53a6c-131">OUTPUTS</span></span>

### <span data-ttu-id="53a6c-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="53a6c-132">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="53a6c-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="53a6c-133">NOTES</span></span>

## <span data-ttu-id="53a6c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53a6c-134">RELATED LINKS</span></span>

[<span data-ttu-id="53a6c-135">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="53a6c-135">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="53a6c-136">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="53a6c-136">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="53a6c-137">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="53a6c-137">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="53a6c-138">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="53a6c-138">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


