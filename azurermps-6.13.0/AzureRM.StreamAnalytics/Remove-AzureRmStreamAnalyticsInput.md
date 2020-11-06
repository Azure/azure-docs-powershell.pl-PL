---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 8e80162d5efa6aa274617941df218812ae6901a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546363"
---
# <span data-ttu-id="1af75-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1af75-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="1af75-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1af75-102">SYNOPSIS</span></span>
<span data-ttu-id="1af75-103">Usuwa dane wejściowe z zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="1af75-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1af75-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1af75-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1af75-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1af75-105">DESCRIPTION</span></span>
<span data-ttu-id="1af75-106">Polecenie cmdlet **Remove-AzureRmStreamAnalyticsInput** asynchronicznie usuwa dane wejściowe z zadania Stream Analytics na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1af75-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="1af75-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1af75-107">EXAMPLES</span></span>

### <span data-ttu-id="1af75-108">PRZYKŁAD 1. Usuń strumień wejściowy z zadania</span><span class="sxs-lookup"><span data-stu-id="1af75-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="1af75-109">To polecenie usuwa EventStream wejściowy z StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="1af75-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="1af75-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1af75-110">PARAMETERS</span></span>

### <span data-ttu-id="1af75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af75-111">-DefaultProfile</span></span>
<span data-ttu-id="1af75-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1af75-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1af75-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="1af75-113">-JobName</span></span>
<span data-ttu-id="1af75-114">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="1af75-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="1af75-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1af75-115">-Name</span></span>
<span data-ttu-id="1af75-116">Określa nazwę danych wejściowych funkcji Analiza strumienia Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1af75-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="1af75-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af75-117">-ResourceGroupName</span></span>
<span data-ttu-id="1af75-118">Określa nazwę grupy zasobów, do której należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="1af75-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="1af75-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1af75-119">-Confirm</span></span>
<span data-ttu-id="1af75-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1af75-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1af75-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af75-121">-WhatIf</span></span>
<span data-ttu-id="1af75-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1af75-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1af75-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1af75-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1af75-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af75-124">CommonParameters</span></span>
<span data-ttu-id="1af75-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1af75-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af75-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af75-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af75-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1af75-127">INPUTS</span></span>

### <span data-ttu-id="1af75-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1af75-128">System.String</span></span>

## <span data-ttu-id="1af75-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1af75-129">OUTPUTS</span></span>

### <span data-ttu-id="1af75-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1af75-130">System.Boolean</span></span>

## <span data-ttu-id="1af75-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1af75-131">NOTES</span></span>

## <span data-ttu-id="1af75-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1af75-132">RELATED LINKS</span></span>

[<span data-ttu-id="1af75-133">Nowe — AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1af75-133">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="1af75-134">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1af75-134">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="1af75-135">Test — AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1af75-135">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


