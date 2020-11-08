---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: d3c5e578e6921297d7d5edc467e10b9a2b4e9e53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232927"
---
# <span data-ttu-id="a5364-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a5364-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="a5364-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5364-102">SYNOPSIS</span></span>
<span data-ttu-id="a5364-103">Usuwa dane wejściowe z zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a5364-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="a5364-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5364-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5364-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a5364-105">DESCRIPTION</span></span>
<span data-ttu-id="a5364-106">Polecenie cmdlet **Remove-AzStreamAnalyticsInput** asynchronicznie usuwa dane wejściowe z zadania Stream Analytics na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a5364-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="a5364-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5364-107">EXAMPLES</span></span>

### <span data-ttu-id="a5364-108">PRZYKŁAD 1. Usuń strumień wejściowy z zadania</span><span class="sxs-lookup"><span data-stu-id="a5364-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="a5364-109">To polecenie usuwa EventStream wejściowy z StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="a5364-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="a5364-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5364-110">PARAMETERS</span></span>

### <span data-ttu-id="a5364-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5364-111">-DefaultProfile</span></span>
<span data-ttu-id="a5364-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5364-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5364-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="a5364-113">-JobName</span></span>
<span data-ttu-id="a5364-114">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="a5364-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="a5364-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5364-115">-Name</span></span>
<span data-ttu-id="a5364-116">Określa nazwę danych wejściowych funkcji Analiza strumienia Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a5364-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="a5364-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5364-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5364-118">Określa nazwę grupy zasobów, do której należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="a5364-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="a5364-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5364-119">-Confirm</span></span>
<span data-ttu-id="a5364-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5364-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5364-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5364-121">-WhatIf</span></span>
<span data-ttu-id="a5364-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5364-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5364-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a5364-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5364-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5364-124">CommonParameters</span></span>
<span data-ttu-id="a5364-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5364-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5364-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5364-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5364-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5364-127">INPUTS</span></span>

### <span data-ttu-id="a5364-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a5364-128">System.String</span></span>

## <span data-ttu-id="a5364-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5364-129">OUTPUTS</span></span>

### <span data-ttu-id="a5364-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5364-130">System.Boolean</span></span>

## <span data-ttu-id="a5364-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5364-131">NOTES</span></span>

## <span data-ttu-id="a5364-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5364-132">RELATED LINKS</span></span>

[<span data-ttu-id="a5364-133">Nowe — AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a5364-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="a5364-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a5364-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="a5364-135">Test — AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="a5364-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


