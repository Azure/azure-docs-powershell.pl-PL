---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1a500f883b6896e91767f0f7d560ee28e4bfc9f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973809"
---
# <span data-ttu-id="78384-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="78384-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="78384-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78384-102">SYNOPSIS</span></span>
<span data-ttu-id="78384-103">Usuwa funkcję z zadania analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="78384-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="78384-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="78384-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78384-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="78384-105">DESCRIPTION</span></span>
<span data-ttu-id="78384-106">Polecenie **cmdlet Remove-AzStreamAnalyticsFunction** usuwa funkcję asynchronicznie z zadania usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="78384-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="78384-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="78384-107">EXAMPLES</span></span>

### <span data-ttu-id="78384-108">Przykład 1. Usuwanie funkcji Analiza strumienia</span><span class="sxs-lookup"><span data-stu-id="78384-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="78384-109">To polecenie usuwa funkcję o nazwie ScoreTweet z zadania o nazwie StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="78384-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="78384-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78384-110">PARAMETERS</span></span>

### <span data-ttu-id="78384-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78384-111">-DefaultProfile</span></span>
<span data-ttu-id="78384-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="78384-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78384-113">— JobName</span><span class="sxs-lookup"><span data-stu-id="78384-113">-JobName</span></span>
<span data-ttu-id="78384-114">Określa nazwę zadania analizy strumienia, do którego należy funkcja.</span><span class="sxs-lookup"><span data-stu-id="78384-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="78384-115">To polecenie cmdlet usuwa funkcję z zadania, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="78384-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="78384-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="78384-116">-Name</span></span>
<span data-ttu-id="78384-117">Określa nazwę funkcji Analiza strumienia, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78384-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="78384-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78384-118">-ResourceGroupName</span></span>
<span data-ttu-id="78384-119">Określa nazwę grupy zasobów, do której należy funkcja Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="78384-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="78384-120">To polecenie cmdlet usuwa funkcję z grupy zasobów, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="78384-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="78384-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78384-121">-Confirm</span></span>
<span data-ttu-id="78384-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="78384-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78384-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78384-123">-WhatIf</span></span>
<span data-ttu-id="78384-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78384-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78384-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="78384-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78384-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78384-126">CommonParameters</span></span>
<span data-ttu-id="78384-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78384-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78384-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78384-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78384-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78384-129">INPUTS</span></span>

### <span data-ttu-id="78384-130">System.String</span><span class="sxs-lookup"><span data-stu-id="78384-130">System.String</span></span>

## <span data-ttu-id="78384-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78384-131">OUTPUTS</span></span>

### <span data-ttu-id="78384-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="78384-132">System.Boolean</span></span>

## <span data-ttu-id="78384-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="78384-133">NOTES</span></span>

## <span data-ttu-id="78384-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78384-134">RELATED LINKS</span></span>

[<span data-ttu-id="78384-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="78384-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="78384-136">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="78384-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="78384-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="78384-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


