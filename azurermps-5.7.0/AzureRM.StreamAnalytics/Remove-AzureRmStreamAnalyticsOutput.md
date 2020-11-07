---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 03cca81794e190a97ce21b7e9ed8c82392db3e36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716471"
---
# <span data-ttu-id="88a6c-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="88a6c-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="88a6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="88a6c-103">Usuwa dane wyjściowe z zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="88a6c-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88a6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88a6c-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88a6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88a6c-105">DESCRIPTION</span></span>
<span data-ttu-id="88a6c-106">Polecenie cmdlet **Remove-AzureRmStreamAnalyticsOutput** asynchronicznie usuwa dane wyjściowe z zadania Stream Analytics na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="88a6c-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="88a6c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88a6c-107">EXAMPLES</span></span>

### <span data-ttu-id="88a6c-108">PRZYKŁAD 1. Usuwanie danych wyjściowych z zadania</span><span class="sxs-lookup"><span data-stu-id="88a6c-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="88a6c-109">To polecenie usuwa dane wyjściowe z StreamingJob zadań.</span><span class="sxs-lookup"><span data-stu-id="88a6c-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="88a6c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88a6c-110">PARAMETERS</span></span>

### <span data-ttu-id="88a6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88a6c-111">-DefaultProfile</span></span>
<span data-ttu-id="88a6c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88a6c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88a6c-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="88a6c-113">-JobName</span></span>
<span data-ttu-id="88a6c-114">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="88a6c-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="88a6c-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88a6c-115">-Name</span></span>
<span data-ttu-id="88a6c-116">Określa nazwę danych wyjściowych funkcji Analiza strumienia Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="88a6c-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88a6c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88a6c-117">-ResourceGroupName</span></span>
<span data-ttu-id="88a6c-118">Określa nazwę grupy zasobów, do której należy dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="88a6c-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="88a6c-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88a6c-119">-Confirm</span></span>
<span data-ttu-id="88a6c-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88a6c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88a6c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88a6c-121">-WhatIf</span></span>
<span data-ttu-id="88a6c-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88a6c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88a6c-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88a6c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88a6c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a6c-124">CommonParameters</span></span>
<span data-ttu-id="88a6c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88a6c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a6c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88a6c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a6c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88a6c-127">INPUTS</span></span>

### <span data-ttu-id="88a6c-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="88a6c-128">None</span></span>
<span data-ttu-id="88a6c-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="88a6c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88a6c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88a6c-130">OUTPUTS</span></span>

### <span data-ttu-id="88a6c-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="88a6c-131">System.Object</span></span>

## <span data-ttu-id="88a6c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88a6c-132">NOTES</span></span>

## <span data-ttu-id="88a6c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88a6c-133">RELATED LINKS</span></span>

[<span data-ttu-id="88a6c-134">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="88a6c-134">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="88a6c-135">Nowe — AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="88a6c-135">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="88a6c-136">Test — AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="88a6c-136">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


