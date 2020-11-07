---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 4429142b19e64939b9fcc90d56c80f67c5296c15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717182"
---
# <span data-ttu-id="7ba51-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7ba51-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="7ba51-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ba51-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba51-103">Umożliwia usunięcie funkcji z zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7ba51-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ba51-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ba51-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ba51-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ba51-105">DESCRIPTION</span></span>
<span data-ttu-id="7ba51-106">Polecenie cmdlet **Remove-AzureRmStreamAnalyticsFunction** usuwa działanie funkcji asynchronicznie z zadania usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7ba51-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="7ba51-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ba51-107">EXAMPLES</span></span>

### <span data-ttu-id="7ba51-108">Przykład 1: usuwanie funkcji Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="7ba51-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="7ba51-109">To polecenie umożliwia usunięcie funkcji o nazwie ScoreTweet z zadania o nazwie StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="7ba51-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="7ba51-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ba51-110">PARAMETERS</span></span>

### <span data-ttu-id="7ba51-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba51-111">-DefaultProfile</span></span>
<span data-ttu-id="7ba51-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba51-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ba51-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="7ba51-113">-JobName</span></span>
<span data-ttu-id="7ba51-114">Określa nazwę zadania Stream Analytics, do którego należy funkcja.</span><span class="sxs-lookup"><span data-stu-id="7ba51-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="7ba51-115">To polecenie cmdlet umożliwia usunięcie funkcji z zadania, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7ba51-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="7ba51-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7ba51-116">-Name</span></span>
<span data-ttu-id="7ba51-117">Określa nazwę funkcji Stream Analytics, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ba51-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ba51-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ba51-118">-ResourceGroupName</span></span>
<span data-ttu-id="7ba51-119">Określa nazwę grupy zasobów, do której należy funkcja Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="7ba51-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="7ba51-120">To polecenie cmdlet umożliwia usunięcie funkcji w grupie zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7ba51-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7ba51-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7ba51-121">-Confirm</span></span>
<span data-ttu-id="7ba51-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ba51-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba51-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ba51-123">-WhatIf</span></span>
<span data-ttu-id="7ba51-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ba51-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ba51-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7ba51-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba51-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba51-126">CommonParameters</span></span>
<span data-ttu-id="7ba51-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba51-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba51-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ba51-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba51-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ba51-129">INPUTS</span></span>

### <span data-ttu-id="7ba51-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7ba51-130">System.String</span></span>

## <span data-ttu-id="7ba51-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ba51-131">OUTPUTS</span></span>

### <span data-ttu-id="7ba51-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ba51-132">System.Boolean</span></span>

## <span data-ttu-id="7ba51-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ba51-133">NOTES</span></span>

## <span data-ttu-id="7ba51-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ba51-134">RELATED LINKS</span></span>

[<span data-ttu-id="7ba51-135">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7ba51-135">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="7ba51-136">Nowe — AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7ba51-136">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="7ba51-137">Test — AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="7ba51-137">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


