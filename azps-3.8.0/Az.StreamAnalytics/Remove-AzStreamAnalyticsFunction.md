---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d481cf5ba28a87e098691d4b3fa5c179670d881d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895534"
---
# <span data-ttu-id="1d54c-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1d54c-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="1d54c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d54c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d54c-103">Umożliwia usunięcie funkcji z zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="1d54c-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="1d54c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d54c-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d54c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d54c-105">DESCRIPTION</span></span>
<span data-ttu-id="1d54c-106">Polecenie cmdlet **Remove-AzStreamAnalyticsFunction** usuwa działanie funkcji asynchronicznie z zadania usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="1d54c-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="1d54c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d54c-107">EXAMPLES</span></span>

### <span data-ttu-id="1d54c-108">Przykład 1: usuwanie funkcji Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="1d54c-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="1d54c-109">To polecenie umożliwia usunięcie funkcji o nazwie ScoreTweet z zadania o nazwie StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="1d54c-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="1d54c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d54c-110">PARAMETERS</span></span>

### <span data-ttu-id="1d54c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d54c-111">-DefaultProfile</span></span>
<span data-ttu-id="1d54c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d54c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d54c-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="1d54c-113">-JobName</span></span>
<span data-ttu-id="1d54c-114">Określa nazwę zadania Stream Analytics, do którego należy funkcja.</span><span class="sxs-lookup"><span data-stu-id="1d54c-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="1d54c-115">To polecenie cmdlet umożliwia usunięcie funkcji z zadania, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1d54c-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d54c-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1d54c-116">-Name</span></span>
<span data-ttu-id="1d54c-117">Określa nazwę funkcji Stream Analytics, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d54c-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1d54c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d54c-118">-ResourceGroupName</span></span>
<span data-ttu-id="1d54c-119">Określa nazwę grupy zasobów, do której należy funkcja Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="1d54c-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="1d54c-120">To polecenie cmdlet umożliwia usunięcie funkcji w grupie zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1d54c-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d54c-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d54c-121">-Confirm</span></span>
<span data-ttu-id="1d54c-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d54c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d54c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d54c-123">-WhatIf</span></span>
<span data-ttu-id="1d54c-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d54c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d54c-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1d54c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d54c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d54c-126">CommonParameters</span></span>
<span data-ttu-id="1d54c-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d54c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d54c-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d54c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d54c-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d54c-129">INPUTS</span></span>

### <span data-ttu-id="1d54c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1d54c-130">System.String</span></span>

## <span data-ttu-id="1d54c-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d54c-131">OUTPUTS</span></span>

### <span data-ttu-id="1d54c-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d54c-132">System.Boolean</span></span>

## <span data-ttu-id="1d54c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d54c-133">NOTES</span></span>

## <span data-ttu-id="1d54c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d54c-134">RELATED LINKS</span></span>

[<span data-ttu-id="1d54c-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1d54c-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="1d54c-136">Nowe — AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1d54c-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="1d54c-137">Test — AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="1d54c-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


