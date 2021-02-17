---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 65d0e40fd522d223eed2d0462e5c66beb9e9709a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182931"
---
# <span data-ttu-id="b71b2-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b71b2-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="b71b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b71b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b71b2-103">Usuwa zadanie analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="b71b2-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="b71b2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b71b2-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b71b2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b71b2-105">DESCRIPTION</span></span>
<span data-ttu-id="b71b2-106">Polecenie **cmdlet Remove-AzStreamAnalyticsJob** asynchronicznie usuwa określone zadanie analizy strumienia na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="b71b2-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="b71b2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b71b2-107">EXAMPLES</span></span>

### <span data-ttu-id="b71b2-108">PRZYKŁAD 1. Usuwanie zadania</span><span class="sxs-lookup"><span data-stu-id="b71b2-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="b71b2-109">To polecenie usuwa zadanie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="b71b2-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="b71b2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b71b2-110">PARAMETERS</span></span>

### <span data-ttu-id="b71b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b71b2-111">-DefaultProfile</span></span>
<span data-ttu-id="b71b2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b71b2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b71b2-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b71b2-113">-Name</span></span>
<span data-ttu-id="b71b2-114">Określa nazwę zadania Azure Stream Analytics do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b71b2-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="b71b2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b71b2-115">-ResourceGroupName</span></span>
<span data-ttu-id="b71b2-116">Określa nazwę grupy zasobów, do której należy zadanie Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b71b2-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="b71b2-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b71b2-117">-Confirm</span></span>
<span data-ttu-id="b71b2-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b71b2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b71b2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b71b2-119">-WhatIf</span></span>
<span data-ttu-id="b71b2-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b71b2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b71b2-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b71b2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b71b2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b71b2-122">CommonParameters</span></span>
<span data-ttu-id="b71b2-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b71b2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b71b2-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b71b2-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b71b2-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b71b2-125">INPUTS</span></span>

### <span data-ttu-id="b71b2-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b71b2-126">System.String</span></span>

## <span data-ttu-id="b71b2-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b71b2-127">OUTPUTS</span></span>

### <span data-ttu-id="b71b2-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b71b2-128">System.Boolean</span></span>

## <span data-ttu-id="b71b2-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b71b2-129">NOTES</span></span>

## <span data-ttu-id="b71b2-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b71b2-130">RELATED LINKS</span></span>

[<span data-ttu-id="b71b2-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b71b2-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b71b2-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b71b2-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b71b2-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b71b2-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="b71b2-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b71b2-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


