---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 950d761324f0750f2433b0b88edb5d37859945e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984017"
---
# <span data-ttu-id="9b56b-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9b56b-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="9b56b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b56b-102">SYNOPSIS</span></span>
<span data-ttu-id="9b56b-103">Usuwa dane wyjściowe z zadania analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="9b56b-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="9b56b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9b56b-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b56b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9b56b-105">DESCRIPTION</span></span>
<span data-ttu-id="9b56b-106">Polecenie **cmdlet Remove-AzStreamAnalyticsOutput** asynchronicznie usuwa dane wyjściowe z zadania analizy strumienia na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="9b56b-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="9b56b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9b56b-107">EXAMPLES</span></span>

### <span data-ttu-id="9b56b-108">PRZYKŁAD 1. Usuwanie danych wyjściowych z zadania</span><span class="sxs-lookup"><span data-stu-id="9b56b-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="9b56b-109">To polecenie usuwa dane wyjściowe zadania StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="9b56b-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="9b56b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b56b-110">PARAMETERS</span></span>

### <span data-ttu-id="9b56b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b56b-111">-DefaultProfile</span></span>
<span data-ttu-id="9b56b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b56b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b56b-113">— JobName</span><span class="sxs-lookup"><span data-stu-id="9b56b-113">-JobName</span></span>
<span data-ttu-id="9b56b-114">Określa nazwę zadania Azure Stream Analytics, do którego należy dane wyjściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="9b56b-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="9b56b-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9b56b-115">-Name</span></span>
<span data-ttu-id="9b56b-116">Określa nazwę danych wyjściowych usługi Azure Stream Analytics do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9b56b-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="9b56b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b56b-117">-ResourceGroupName</span></span>
<span data-ttu-id="9b56b-118">Określa nazwę grupy zasobów, do której należy dane wyjściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="9b56b-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="9b56b-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b56b-119">-Confirm</span></span>
<span data-ttu-id="9b56b-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9b56b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b56b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b56b-121">-WhatIf</span></span>
<span data-ttu-id="9b56b-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b56b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b56b-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9b56b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b56b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b56b-124">CommonParameters</span></span>
<span data-ttu-id="9b56b-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b56b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b56b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b56b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b56b-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b56b-127">INPUTS</span></span>

### <span data-ttu-id="9b56b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9b56b-128">System.String</span></span>

## <span data-ttu-id="9b56b-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b56b-129">OUTPUTS</span></span>

### <span data-ttu-id="9b56b-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9b56b-130">System.Boolean</span></span>

## <span data-ttu-id="9b56b-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9b56b-131">NOTES</span></span>

## <span data-ttu-id="9b56b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b56b-132">RELATED LINKS</span></span>

[<span data-ttu-id="9b56b-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9b56b-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="9b56b-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9b56b-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="9b56b-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9b56b-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


