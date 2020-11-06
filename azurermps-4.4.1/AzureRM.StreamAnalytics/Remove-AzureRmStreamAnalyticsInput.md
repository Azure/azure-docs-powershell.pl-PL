---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: f801a7c8dd83927e8aceebdc98138aa6ad39d31c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552300"
---
# <span data-ttu-id="ffc4a-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ffc4a-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="ffc4a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ffc4a-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc4a-103">Usuwa dane wejściowe z zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffc4a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ffc4a-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc4a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ffc4a-105">DESCRIPTION</span></span>
<span data-ttu-id="ffc4a-106">Polecenie cmdlet **Remove-AzureRmStreamAnalyticsInput** asynchronicznie usuwa dane wejściowe z zadania Stream Analytics na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="ffc4a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ffc4a-107">EXAMPLES</span></span>

### <span data-ttu-id="ffc4a-108">PRZYKŁAD 1. Usuń strumień wejściowy z zadania</span><span class="sxs-lookup"><span data-stu-id="ffc4a-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="ffc4a-109">To polecenie usuwa EventStream wejściowy z StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="ffc4a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffc4a-110">PARAMETERS</span></span>

### <span data-ttu-id="ffc4a-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="ffc4a-111">-JobName</span></span>
<span data-ttu-id="ffc4a-112">Określa nazwę zadania usługi Azure Stream Analytics, do którego należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="ffc4a-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ffc4a-113">-Name</span></span>
<span data-ttu-id="ffc4a-114">Określa nazwę danych wejściowych funkcji Analiza strumienia Azure do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-114">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="ffc4a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc4a-115">-ResourceGroupName</span></span>
<span data-ttu-id="ffc4a-116">Określa nazwę grupy zasobów, do której należy dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="ffc4a-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ffc4a-117">-Confirm</span></span>
<span data-ttu-id="ffc4a-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffc4a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffc4a-119">-WhatIf</span></span>
<span data-ttu-id="ffc4a-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffc4a-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffc4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc4a-122">-DefaultProfile</span></span>
<span data-ttu-id="ffc4a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffc4a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc4a-124">CommonParameters</span></span>
<span data-ttu-id="ffc4a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffc4a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc4a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffc4a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc4a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffc4a-127">INPUTS</span></span>

## <span data-ttu-id="ffc4a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ffc4a-128">OUTPUTS</span></span>

### <span data-ttu-id="ffc4a-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="ffc4a-129">System.Object</span></span>

## <span data-ttu-id="ffc4a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ffc4a-130">NOTES</span></span>

## <span data-ttu-id="ffc4a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffc4a-131">RELATED LINKS</span></span>

[<span data-ttu-id="ffc4a-132">Nowe — AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ffc4a-132">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="ffc4a-133">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ffc4a-133">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="ffc4a-134">Test — AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ffc4a-134">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


