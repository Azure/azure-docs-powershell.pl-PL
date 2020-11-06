---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 98074a9893525882ce63ab86e31c677281f34ca3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525957"
---
# <span data-ttu-id="17fb2-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="17fb2-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="17fb2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="17fb2-103">Usuwa dane wyjściowe z zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="17fb2-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17fb2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17fb2-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17fb2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="17fb2-105">DESCRIPTION</span></span>
<span data-ttu-id="17fb2-106">Polecenie cmdlet **Remove-AzureRmStreamAnalyticsOutput** asynchronicznie usuwa dane wyjściowe z zadania Stream Analytics na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="17fb2-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="17fb2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17fb2-107">EXAMPLES</span></span>

### <span data-ttu-id="17fb2-108">PRZYKŁAD 1. Usuwanie danych wyjściowych z zadania</span><span class="sxs-lookup"><span data-stu-id="17fb2-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="17fb2-109">To polecenie usuwa dane wyjściowe z StreamingJob zadań.</span><span class="sxs-lookup"><span data-stu-id="17fb2-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="17fb2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17fb2-110">PARAMETERS</span></span>

### <span data-ttu-id="17fb2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17fb2-111">-DefaultProfile</span></span>
<span data-ttu-id="17fb2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17fb2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17fb2-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="17fb2-113">-JobName</span></span>
<span data-ttu-id="17fb2-114">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="17fb2-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="17fb2-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="17fb2-115">-Name</span></span>
<span data-ttu-id="17fb2-116">Określa nazwę danych wyjściowych funkcji Analiza strumienia Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="17fb2-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="17fb2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17fb2-117">-ResourceGroupName</span></span>
<span data-ttu-id="17fb2-118">Określa nazwę grupy zasobów, do której należy dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="17fb2-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="17fb2-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="17fb2-119">-Confirm</span></span>
<span data-ttu-id="17fb2-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17fb2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17fb2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17fb2-121">-WhatIf</span></span>
<span data-ttu-id="17fb2-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17fb2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17fb2-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="17fb2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17fb2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fb2-124">CommonParameters</span></span>
<span data-ttu-id="17fb2-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17fb2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fb2-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17fb2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fb2-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17fb2-127">INPUTS</span></span>

### <span data-ttu-id="17fb2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="17fb2-128">System.String</span></span>

## <span data-ttu-id="17fb2-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17fb2-129">OUTPUTS</span></span>

### <span data-ttu-id="17fb2-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="17fb2-130">System.Boolean</span></span>

## <span data-ttu-id="17fb2-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17fb2-131">NOTES</span></span>

## <span data-ttu-id="17fb2-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17fb2-132">RELATED LINKS</span></span>

[<span data-ttu-id="17fb2-133">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="17fb2-133">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="17fb2-134">Nowe — AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="17fb2-134">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="17fb2-135">Test — AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="17fb2-135">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


