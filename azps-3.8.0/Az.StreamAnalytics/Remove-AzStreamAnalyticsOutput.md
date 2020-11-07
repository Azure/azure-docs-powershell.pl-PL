---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894694"
---
# <span data-ttu-id="29d61-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="29d61-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="29d61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29d61-102">SYNOPSIS</span></span>
<span data-ttu-id="29d61-103">Usuwa dane wyjściowe z zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="29d61-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="29d61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29d61-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29d61-105">Opis</span><span class="sxs-lookup"><span data-stu-id="29d61-105">DESCRIPTION</span></span>
<span data-ttu-id="29d61-106">Polecenie cmdlet **Remove-AzStreamAnalyticsOutput** asynchronicznie usuwa dane wyjściowe z zadania Stream Analytics na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="29d61-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="29d61-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29d61-107">EXAMPLES</span></span>

### <span data-ttu-id="29d61-108">PRZYKŁAD 1. Usuwanie danych wyjściowych z zadania</span><span class="sxs-lookup"><span data-stu-id="29d61-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="29d61-109">To polecenie usuwa dane wyjściowe z StreamingJob zadań.</span><span class="sxs-lookup"><span data-stu-id="29d61-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="29d61-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29d61-110">PARAMETERS</span></span>

### <span data-ttu-id="29d61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d61-111">-DefaultProfile</span></span>
<span data-ttu-id="29d61-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29d61-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29d61-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="29d61-113">-JobName</span></span>
<span data-ttu-id="29d61-114">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="29d61-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="29d61-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29d61-115">-Name</span></span>
<span data-ttu-id="29d61-116">Określa nazwę danych wyjściowych funkcji Analiza strumienia Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="29d61-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="29d61-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d61-117">-ResourceGroupName</span></span>
<span data-ttu-id="29d61-118">Określa nazwę grupy zasobów, do której należy dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="29d61-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="29d61-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29d61-119">-Confirm</span></span>
<span data-ttu-id="29d61-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29d61-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29d61-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29d61-121">-WhatIf</span></span>
<span data-ttu-id="29d61-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29d61-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29d61-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29d61-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29d61-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d61-124">CommonParameters</span></span>
<span data-ttu-id="29d61-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29d61-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d61-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29d61-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d61-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29d61-127">INPUTS</span></span>

### <span data-ttu-id="29d61-128">System. String</span><span class="sxs-lookup"><span data-stu-id="29d61-128">System.String</span></span>

## <span data-ttu-id="29d61-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29d61-129">OUTPUTS</span></span>

### <span data-ttu-id="29d61-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29d61-130">System.Boolean</span></span>

## <span data-ttu-id="29d61-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29d61-131">NOTES</span></span>

## <span data-ttu-id="29d61-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29d61-132">RELATED LINKS</span></span>

[<span data-ttu-id="29d61-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="29d61-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="29d61-134">Nowe — AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="29d61-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="29d61-135">Test — AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="29d61-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


