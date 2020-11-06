---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 64ebe431333914a907c515744501f4624a7977ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542131"
---
# <span data-ttu-id="01415-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="01415-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="01415-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01415-102">SYNOPSIS</span></span>
<span data-ttu-id="01415-103">Umożliwia usunięcie zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="01415-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01415-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01415-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01415-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01415-105">DESCRIPTION</span></span>
<span data-ttu-id="01415-106">Polecenie cmdlet **Remove-AzureRmStreamAnalyticsJob** asynchronicznie usuwa określone zadanie analizy strumienia na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="01415-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="01415-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01415-107">EXAMPLES</span></span>

### <span data-ttu-id="01415-108">PRZYKŁAD 1: usuwanie zadania</span><span class="sxs-lookup"><span data-stu-id="01415-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="01415-109">To polecenie usuwa zadanie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="01415-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="01415-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01415-110">PARAMETERS</span></span>

### <span data-ttu-id="01415-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01415-111">-DefaultProfile</span></span>
<span data-ttu-id="01415-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01415-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01415-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="01415-113">-Name</span></span>
<span data-ttu-id="01415-114">Określa nazwę zadania usługi Azure Stream Analytics, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="01415-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="01415-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01415-115">-ResourceGroupName</span></span>
<span data-ttu-id="01415-116">Określa nazwę grupy zasobów, do której należy zadanie usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="01415-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="01415-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="01415-117">-Confirm</span></span>
<span data-ttu-id="01415-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01415-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01415-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01415-119">-WhatIf</span></span>
<span data-ttu-id="01415-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01415-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01415-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="01415-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01415-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01415-122">CommonParameters</span></span>
<span data-ttu-id="01415-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01415-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01415-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01415-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01415-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01415-125">INPUTS</span></span>

### <span data-ttu-id="01415-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="01415-126">None</span></span>
<span data-ttu-id="01415-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="01415-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01415-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01415-128">OUTPUTS</span></span>

### <span data-ttu-id="01415-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="01415-129">System.Object</span></span>

## <span data-ttu-id="01415-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01415-130">NOTES</span></span>

## <span data-ttu-id="01415-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01415-131">RELATED LINKS</span></span>

[<span data-ttu-id="01415-132">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="01415-132">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="01415-133">Nowe — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="01415-133">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="01415-134">Start — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="01415-134">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="01415-135">Zatrzymaj — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="01415-135">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


